---
name: layout-0-titelfolie
description: Main presentation title slide
---



> **Category**: title
> **Index**: 0
> **Layout name in .pptx master**: `Titelfolie`

## Purpose
Main entry slide for a presentation. Displays the presentation title, an optional subtitle, a decorative image or color block, and the Clue One logo.

## Visual Structure

```
+--------------------------------------------------+
|  [LOGO top-right]                                |
|                                                  |
|  +-----------+  +----------------------------+   |
|  | BIG TITLE |  |  IMAGE / COLOR BLOCK       |   |
|  |  (left)   |  |  (right, ~40% width)       |   |
|  +-----------+  +----------------------------+   |
|                                                  |
|  Subtitle / Claim line (optional)                |
|                                                  |
+--------------------------------------------------+
```

## Placeholder Inventory

| # | Name | Type | Position (EMU) | Size (EMU) | Notes |
|---|------|------|----------------|------------|-------|
| 0 | Title | `PP_TITLE` | L:457200 T:2286000 | W:5486400 H:1371600 | Bold, 36pt |
| 1 | Subtitle | `BODY` | L:457200 T:3657600 | W:5486400 H:914400 | Regular, 20pt |
| 2 | Image | `PICTURE` | L:6400800 T:0 | W:5791200 H:6858000 | Full-height right panel |

## Color Usage

| Element | Color | Hex |
|---------|-------|-----|
| Background | White | #FFFFFF |
| Title text | Primary Blue | #003781 |
| Subtitle text | Dark Gray | #333333 |
| Right panel default fill | Accent Blue | #0055BC |

## Typography

| Placeholder | Font | Weight | Size |
|-------------|------|--------|------|
| Title | Calibri | Bold | 36pt |
| Subtitle | Calibri | Regular | 20pt |

## python-pptx Implementation Notes

```python
from pptx import Presentation
from pptx.util import Emu, Pt
from pptx.dml.color import RGBColor
from pptx.enum.text import PP_ALIGN

# Slide dimensions (16:9)
prs = Presentation()
prs.slide_width = Emu(12192000)
prs.slide_height = Emu(6858000)

# Use layout index 0 (Titelfolie)
slide_layout = prs.slide_layouts[0]
slide = prs.slides.add_slide(slide_layout)

# Access placeholders
title_ph = slide.placeholders[0]
subtitle_ph = slide.placeholders[1]

# Set content
title_ph.text = "Presentation Title"
subtitle_ph.text = "Subtitle or Claim Line"

# Style title
title_ph.text_frame.paragraphs[0].runs[0].font.color.rgb = RGBColor(0x00, 0x37, 0x81)
title_ph.text_frame.paragraphs[0].runs[0].font.bold = True
title_ph.text_frame.paragraphs[0].runs[0].font.size = Pt(36)
```

## Content Guidelines

- **Title**: Short, impactful — max 8 words.
- **Subtitle**: Optional tagline or project name — max 12 words.
- **Image**: Use a full-bleed photo (1920×1080+) cropped to the right panel dimensions.
- **Logo**: Auto-placed from master; do not reposition manually.

## Variants

| Variant | Description |
|---------|-------------|
| Default (image) | Right panel shows a photo |
| Color block | Right panel is solid #0055BC |
| Dark | Background #003781, white text |
