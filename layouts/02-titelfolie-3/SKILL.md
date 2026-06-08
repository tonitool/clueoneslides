---
name: layout-2-titelfolie-3
description: Split title slide with left color block and right content
---



> **Category**: title
> **Index**: 2
> **Layout name in .pptx master**: `Titelfolie 3`

## Purpose
Split-screen title slide. Left half: solid #003781 color block with white title. Right half: white background with subtitle and optional image thumbnail.

## Visual Structure

```
+----------------------+---------------------------+
|  [Blue block]        |  [White area]             |
|                      |                           |
|  TITLE               |  Subtitle text            |
|  (white, large)      |  (dark, smaller)          |
|                      |                           |
|                      |  [Optional image]         |
|                      |                           |
+----------------------+---------------------------+
```

## Placeholder Inventory

| # | Name | Type | Position (EMU) | Size (EMU) | Notes |
|---|------|------|----------------|------------|-------|
| 0 | Title | `PP_TITLE` | L:457200 T:2400000 | W:5486400 H:1371600 | Bold, 36pt, white |
| 1 | Subtitle | `BODY` | L:6400800 T:2400000 | W:5334000 H:1828800 | Regular, 20pt, #333333 |
| 2 | Image | `PICTURE` | L:6858000 T:4228800 | W:4876800 H:2400000 | Optional thumbnail |

## Color Usage

| Element | Color | Hex |
|---------|-------|-----|
| Left block background | Primary Blue | #003781 |
| Right background | White | #FFFFFF |
| Title text | White | #FFFFFF |
| Subtitle text | Dark Gray | #333333 |

## python-pptx Implementation Notes

```python
# Use layout index 2 (Titelfolie 3)
slide_layout = prs.slide_layouts[2]
slide = prs.slides.add_slide(slide_layout)

title_ph = slide.placeholders[0]
subtitle_ph = slide.placeholders[1]

title_ph.text = "Split Title"
subtitle_ph.text = "Supporting detail text goes here."
```

## Content Guidelines

- Left panel: title only, max 6 words.
- Right panel: subtitle up to 3 short lines; optional supporting image.
