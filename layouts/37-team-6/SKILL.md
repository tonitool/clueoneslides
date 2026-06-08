---
name: layout-37-team-6
description: Team slide with 6 member profiles
---



> **Category**: team
> **Index**: 37
> **Layout name in .pptx master**: `Team 6`

## Purpose
Presents 6 team members in a 3×2 grid. Compact profiles with photo, name, and role only.

## Visual Structure

```
+--------------------------------------------------+
|  SLIDE TITLE                                     |
+------------+------------+------------------------+
|  [Photo]   |  [Photo]   |  [Photo]               |
|  Name/Role |  Name/Role |  Name/Role             |
+------------+------------+------------------------+
|  [Photo]   |  [Photo]   |  [Photo]               |
|  Name/Role |  Name/Role |  Name/Role             |
+------------+------------+------------------------+
```

## Placeholder Inventory

| # | Name | Type | Position (EMU) | Size (EMU) | Notes |
|---|------|------|----------------|------------|-------|
| 0 | Title | `PP_TITLE` | L:457200 T:274638 | W:11277600 H:1143000 | Bold, 28pt |
| 1–6 | Photos 1–6 | `PICTURE` | Grid positions | W:3200400 H:3200400 | Circular crop |
| 7–12 | Names 1–6 | `BODY` | Below each photo | W:3200400 H:457200 | Bold, 14pt |
| 13–18 | Roles 1–6 | `BODY` | Below each name | W:3200400 H:342900 | Regular, 12pt, #0055BC |

## Content Guidelines

- Compact layout — no bio text, just name and role.
- Photos must be square, auto-cropped to circle.
- Consistent photo style (same background or professional headshots).
