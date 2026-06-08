---
name: layout-5-agenda-blau
description: Blue background agenda slide
---



> **Category**: agenda
> **Index**: 5
> **Layout name in .pptx master**: `Agenda Blau`

## Purpose
Agenda slide on a dark blue (#003781) background. Lists agenda items in white text. Used as a section-opener or meeting overview.

## Visual Structure

```
+--------------------------------------------------+
|  [Full blue background]                          |
|                                                  |
|  AGENDA                  1. Topic One            |
|  (white, large, left)    2. Topic Two            |
|                          3. Topic Three          |
|                          4. Topic Four           |
|                          (white, right col)      |
|                                                  |
+--------------------------------------------------+
```

## Placeholder Inventory

| # | Name | Type | Position (EMU) | Size (EMU) | Notes |
|---|------|------|----------------|------------|-------|
| 0 | Title ("Agenda") | `PP_TITLE` | L:457200 T:685800 | W:4572000 H:1371600 | Bold, 44pt, white |
| 1 | Agenda Items | `BODY` | L:5486400 T:685800 | W:6248400 H:5486400 | Regular, 18pt, white, numbered list |

## Color Usage

| Element | Color | Hex |
|---------|-------|-----|
| Slide background | Primary Blue | #003781 |
| Title text | White | #FFFFFF |
| List text | White | #FFFFFF |
| Active item highlight | Accent Blue | #0055BC |

## Typography

| Placeholder | Font | Weight | Size |
|-------------|------|--------|------|
| Title | Calibri | Bold | 44pt |
| Agenda items | Calibri | Regular | 18pt |

## python-pptx Implementation Notes

```python
# Use layout index 5 (Agenda Blau)
slide_layout = prs.slide_layouts[5]
slide = prs.slides.add_slide(slide_layout)

title_ph = slide.placeholders[0]
content_ph = slide.placeholders[1]

title_ph.text = "Agenda"

tf = content_ph.text_frame
tf.text = "Topic One"
for item in ["Topic Two", "Topic Three", "Topic Four"]:
    p = tf.add_paragraph()
    p.text = item
    p.level = 0
```

## Content Guidelines

- List 3–7 agenda items.
- Use numbered list format.
- Keep each item to 3–5 words.
