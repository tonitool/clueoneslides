---
name: layout-36-team-3
description: Team slide with 3 member profiles
---



> **Category**: team
> **Index**: 36
> **Layout name in .pptx master**: `Team 3`

## Purpose
Presents 3 team members in equal columns. Each column contains: a circular photo, name, role, and a short bio or key facts.

## Visual Structure

```
+--------------------------------------------------+
|  SLIDE TITLE ("Our Team" or similar)             |
+------------------+------------------+------------+
|  [Photo circle]  |  [Photo circle]  |  [Photo]   |
|  Name            |  Name            |  Name      |
|  Role            |  Role            |  Role      |
|  Bio text        |  Bio text        |  Bio text  |
+------------------+------------------+------------+
```

## Placeholder Inventory

| # | Name | Type | Position (EMU) | Size (EMU) | Notes |
|---|------|------|----------------|------------|-------|
| 0 | Title | `PP_TITLE` | L:457200 T:274638 | W:11277600 H:1143000 | Bold, 28pt, #003781 |
| 1 | Photo 1 | `PICTURE` | L:457200 T:1600200 | W:3429000 H:3429000 | Circular crop |
| 2 | Photo 2 | `PICTURE` | L:4343400 T:1600200 | W:3429000 H:3429000 | Circular crop |
| 3 | Photo 3 | `PICTURE` | L:8229600 T:1600200 | W:3429000 H:3429000 | Circular crop |
| 4 | Name 1 | `BODY` | L:457200 T:5029200 | W:3429000 H:457200 | Bold, 16pt |
| 5 | Name 2 | `BODY` | L:4343400 T:5029200 | W:3429000 H:457200 | Bold, 16pt |
| 6 | Name 3 | `BODY` | L:8229600 T:5029200 | W:3429000 H:457200 | Bold, 16pt |
| 7 | Role 1 | `BODY` | L:457200 T:5486400 | W:3429000 H:457200 | Regular, 14pt, #0055BC |
| 8 | Role 2 | `BODY` | L:4343400 T:5486400 | W:3429000 H:457200 | Regular, 14pt, #0055BC |
| 9 | Role 3 | `BODY` | L:8229600 T:5486400 | W:3429000 H:457200 | Regular, 14pt, #0055BC |

## Content Guidelines

- Photos: square input, auto-cropped to circle by master.
- Names: First Last format.
- Roles: Job title, max 4 words.
- Bio: 1–2 sentences or 3 key facts.
