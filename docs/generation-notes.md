# Generation Notes

## Intent

Create a Codex-compatible animated pet inspired by Luban No.7's Time Journey skin from Honor of Kings.

## Source Links

- Official skin design page: https://pvp.qq.com/coming/v2/skins/1013-sjqllbqh.shtml
- Reference image: https://game.gtimg.cn/images/yxzj/coming/v2/skins//image/20231012/16971181211268.jpg
- Reference image: https://x0.ifengimg.com/ucms/2023_41/10528F7A7F57CB53F144B82D5FADC4D93C3F7001_size493_w600_h314.png

## Visual Constraints

- Manga-proofreader/editor Luban No.7-inspired fan pet.
- Corrected hair identity: front bangs are split two-color, viewer-left white or pale cream and viewer-right vivid red; the hair must not collapse into orange or a single red-orange color.
- Pixel-art-adjacent Codex digital pet style: compact chibi proportions, dark outline, limited palette, flat cel shading, readable at 192x208 cells.
- Preserve black suit, red tie, cat-ear hat, red bird, glasses, stamp cannon, and helper robot as compact identity cues.
- No scenery, text, speech bubbles, detached effects, guide marks, shadows, glows, or motion trails.

## Generation Summary

- Base pet was regenerated after color review to lock the corrected split red-and-white front bangs.
- Row jobs delegated to subagents for grounded animation generation.
- `running-left` was generated separately instead of mirrored because the pet has asymmetric hair and props.
- A `running` candidate with detached yellow marks was rejected and regenerated before final ingestion.
- Parent workflow recorded all selected imagegen outputs, composed the final atlas, generated QA media, and packaged the Codex pet.

## QA Summary

- Final spritesheet: `spritesheet.webp`
- Atlas geometry: 1536x1872, 8 columns by 9 rows, 192x208 cells
- Format: RGBA WebP
- Frame extraction: passed
- Atlas validation: passed
- QA reports: `qa/review.json`, `qa/validation.json`
- Visual review: contact sheet checked for identity consistency, corrected red-and-white bangs across all rows, row completeness, transparent unused cells, and forbidden effects.
- README previews: animated WebP files in `qa/previews/` generated from the validated 192x208 frame PNGs with `img2webp`.

