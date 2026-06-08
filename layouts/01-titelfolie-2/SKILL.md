---
name: layout-1-titelfolie-2
description: Centered title slide with full background image
---



> **Category**: title
> **Index**: 1
> **Layout name in .pptx master**: `Titelfolie 2`

## Purpose
Full-bleed background-image title slide. The entire slide is covered by a photo with an overlay; title and subtitle are centered on top.

## Visual Structure

```
+--------------------------------------------------+
|  [Full bleed background image + dark overlay]    |
|                                                  |
|            PRESENTATION TITLE                    |
|              (centered, white)                   |
|                                                  |
|            Subtitle / Claim line                 |
|              (centered, light gray)              |
|                                                  |
|  [LOGO bottom-right]                             |
+--------------------------------------------------+
```

## Placeholder Inventory

| # | Name | Type | Position (EMU) | Size (EMU) | Notes |
|---|------|------|----------------|------------|-------|
| 0 | Title | `PP_TITLE` | L:457200 T:2400000 | W:11277600 H:1371600 | Bold, 40pt, white, centered |
| 1 | Subtitle | `BODY` | L:457200 T:3771600 | W:11277600 H:685800 | Regular, 22pt, #E0E0E0, centered |
| 2 | Background Image | `PICTURE` | L:0 T:0 | W:12192000 H:6858000 | Full-slide, z-order bottom |

## Color Usage

| Element | Color | Hex |
|---------|-------|-----|
| Background overlay | Primary Blue | #003781 at 50% opacity |
| Title text | White | #FFFFFF |
| Subtitle text | Light Gray | #E0E0E0 |

## Typography

| Placeholder | Font | Weight | Size | Alignment |
|-------------|------|--------|------|-----------|
| Title | Calibri | Bold | 40pt | Center |
| Subtitle | Calibri | Regular | 22pt | Center |

## python-pptx Implementation Notes

```python
# Use layout index 1 (Titelfolie 2)
slide_layout = prs.slide_layouts[1]
slide = prs.slides.add_slide(slide_layout)

title_ph = slide.placeholders[0]
subtitle_ph = slide.placeholders[1]

title_ph.text = "Full-Bleed Title"
subtitle_ph.text = "Supporting subtitle text"

# Add background image (send to back)
from pptx.util import Emu
pic = slide.shapes.add_picture(
    "background.jpg",
    left=Emu(0), top=Emu(0),
    width=Emu(12192000), height=Emu(6858000)
)
# Move picture to back
slide.shapes._spTree.remove(pic._element)
slide.shapes._spTree.insert(2, pic._element)
```

## Content Guidelines

- Use high-contrast background photos (avoid very bright images).
- The #003781 overlay at 50% ensures text readability.
- Keep title to 6 words max for full visual impact.
