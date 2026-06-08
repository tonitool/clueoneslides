---
name: layout-10-titel-und-inhalt
description: Standard title and content slide
---



> **Category**: content
> **Index**: 10
> **Layout name in .pptx master**: `Titel und Inhalt`

## Purpose
The most common slide layout. A headline at the top with a large content area below for bullet points, text, or other content.

## Visual Structure

```
+--------------------------------------------------+
|  SLIDE TITLE                                     |
|  (blue, bold, top)                               |
+--------------------------------------------------+
|                                                  |
|  • Bullet point one                              |
|  • Bullet point two                              |
|  • Bullet point three                            |
|    – Sub-bullet                                  |
|                                                  |
+--------------------------------------------------+
```

## Placeholder Inventory

| # | Name | Type | Position (EMU) | Size (EMU) | Notes |
|---|------|------|----------------|------------|-------|
| 0 | Title | `PP_TITLE` | L:457200 T:274638 | W:11277600 H:1143000 | Bold, 28pt, #003781 |
| 1 | Content | `BODY` | L:457200 T:1600200 | W:11277600 H:4800600 | Regular, 16pt, #333333 |

## Color Usage

| Element | Color | Hex |
|---------|-------|-----|
| Background | White | #FFFFFF |
| Title | Primary Blue | #003781 |
| Body text | Dark Gray | #333333 |
| Bullet markers | Accent Blue | #0055BC |

## Typography

| Placeholder | Font | Weight | Size |
|-------------|------|--------|------|
| Title | Calibri | Bold | 28pt |
| Body | Calibri | Regular | 16pt |
| Sub-bullet | Calibri | Regular | 14pt |

## python-pptx Implementation Notes

```python
# Use layout index 10 (Titel und Inhalt)
slide_layout = prs.slide_layouts[10]
slide = prs.slides.add_slide(slide_layout)

title_ph = slide.placeholders[0]
content_ph = slide.placeholders[1]

title_ph.text = "Slide Title"

tf = content_ph.text_frame
tf.text = "First bullet point"
for bullet in ["Second point", "Third point"]:
    p = tf.add_paragraph()
    p.text = bullet
    p.level = 0
```

## Content Guidelines

- Max 5–6 bullet points per slide.
- Keep each bullet to 1 line if possible.
- Use sub-bullets sparingly (max 2 levels).
