---
name: layout-9-trennseite-mit-vollbild
description: Section divider with full-bleed background image
---



> **Category**: divider
> **Index**: 9
> **Layout name in .pptx master**: `Trennseite mit Vollbild`

## Purpose
Full-bleed image section divider. The entire slide is a photo with a color overlay; the section title is overlaid on top.

## Visual Structure

```
+--------------------------------------------------+
|  [Full bleed image + #003781 overlay 50%]        |
|                                                  |
|         SECTION TITLE                            |
|         (white, large, centered)                 |
|                                                  |
|         Subtitle (optional)                      |
|                                                  |
+--------------------------------------------------+
```

## Placeholder Inventory

| # | Name | Type | Position (EMU) | Size (EMU) | Notes |
|---|------|------|----------------|------------|-------|
| 0 | Section Title | `PP_TITLE` | L:457200 T:2400000 | W:11277600 H:1371600 | Bold, 44pt, white, centered |
| 1 | Subtitle | `BODY` | L:457200 T:3771600 | W:11277600 H:685800 | Regular, 20pt, #E0E0E0, centered |
| 2 | Background Image | `PICTURE` | L:0 T:0 | W:12192000 H:6858000 | Full-slide |

## Color Usage

| Element | Color | Hex |
|---------|-------|-----|
| Background overlay | Primary Blue | #003781 at 50% |
| Title | White | #FFFFFF |
| Subtitle | Light Gray | #E0E0E0 |

## Content Guidelines

- Use dramatic, high-contrast photos.
- Overlay ensures legibility.
