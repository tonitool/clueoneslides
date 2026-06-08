---
name: layout-3-titelfolie-4
description: Minimalist title slide with top accent bar
---



> **Category**: title
> **Index**: 3
> **Layout name in .pptx master**: `Titelfolie 4`

## Purpose
Minimalist title slide featuring a thin horizontal accent bar at the top and large centered title text on a white background.

## Visual Structure

```
+--------------------------------------------------+
|  [#003781 accent bar, full width, ~60px tall]    |
|                                                  |
|                                                  |
|            PRESENTATION TITLE                    |
|              (centered, dark blue)               |
|                                                  |
|            Subtitle line (optional)              |
|                                                  |
|  [Logo bottom-right]                             |
+--------------------------------------------------+
```

## Placeholder Inventory

| # | Name | Type | Position (EMU) | Size (EMU) | Notes |
|---|------|------|----------------|------------|-------|
| 0 | Title | `PP_TITLE` | L:457200 T:2742000 | W:11277600 H:1371600 | Bold, 40pt, #003781, centered |
| 1 | Subtitle | `BODY` | L:457200 T:4113600 | W:11277600 H:685800 | Regular, 20pt, #333333, centered |

## Color Usage

| Element | Color | Hex |
|---------|-------|-----|
| Background | White | #FFFFFF |
| Top accent bar | Primary Blue | #003781 |
| Title text | Primary Blue | #003781 |
| Subtitle text | Dark Gray | #333333 |

## python-pptx Implementation Notes

```python
# Use layout index 3 (Titelfolie 4)
slide_layout = prs.slide_layouts[3]
slide = prs.slides.add_slide(slide_layout)

title_ph = slide.placeholders[0]
subtitle_ph = slide.placeholders[1]

title_ph.text = "Minimalist Title"
subtitle_ph.text = "Optional subtitle"
```

## Content Guidelines

- Keep title concise — 4–7 words ideal.
- Subtitle is optional; omit if not needed.
