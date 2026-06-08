# Slide Builder Design System

> Shared design constants inherited by all layout SKILL.md files.

## Slide Dimensions

| Property | EMUs | Inches | Notes |
|----------|------|--------|-------|
| Width | 12192000 | 13.3333 | 16:9 widescreen |
| Height | 6858000 | 7.5000 | Standard HD ratio |
| Aspect Ratio | 1.7778 | 16:9 | Widescreen format |

## Color Palette

### Primary Colors

| Name | Hex | Usage |
|------|-----|-------|
| Primary Blue | #003781 | Headlines, key UI elements, primary backgrounds |
| Accent Blue | #0055BC | Secondary UI, highlights, icons |
| White | #FFFFFF | Text on dark backgrounds, card fills |
| Light Gray | #F5F5F5 | Slide backgrounds, section fills |
| Medium Gray | #E0E0E0 | Borders, dividers, subtle backgrounds |
| Dark Gray | #333333 | Body text, secondary text |
| Black | #000000 | High-contrast text |

### Secondary / Accent Colors

| Name | Hex | Usage |
|------|-----|-------|
| Warm Orange | #F5A623 | Call-to-action, highlights, warnings |
| Success Green | #27AE60 | Positive indicators, checkmarks |
| Alert Red | #E74C3C | Errors, critical info, warnings |
| Neutral Beige | #F2EFE9 | Soft backgrounds, warm neutrals |

## Typography

| Role | Font Family | Weight | Size (pt) | Notes |
|------|-------------|--------|-----------|-------|
| Slide Title | Calibri | Bold (700) | 28–36 | Main slide heading |
| Subtitle | Calibri | Regular (400) | 20–24 | Supporting line under title |
| Body Text | Calibri | Regular (400) | 14–18 | Bullet lists, paragraphs |
| Caption | Calibri | Light (300) | 10–12 | Image captions, footnotes |
| Emphasis | Calibri | Italic (400) | 14–18 | Inline emphasis |
| Quote | Calibri | Italic Bold | 18–22 | Pull quotes, callouts |

## Spacing & Margins

| Property | EMUs | Inches | Notes |
|----------|------|--------|-------|
| Slide Left Margin | 457200 | 0.5 | Content safe zone |
| Slide Right Margin | 457200 | 0.5 | Content safe zone |
| Slide Top Margin | 274638 | 0.3 | Header clearance |
| Slide Bottom Margin | 274638 | 0.3 | Footer clearance |
| Inner Padding (cards) | 91440 | 0.1 | Card/box internal padding |
| Column Gutter | 182880 | 0.2 | Between multi-column layouts |

## Shape & Border Styles

| Style | Corner Radius | Border Width | Border Color | Fill |
|-------|---------------|--------------|--------------|------|
| Card Default | 91440 EMU | 1pt | #E0E0E0 | #FFFFFF |
| Card Highlighted | 91440 EMU | 2pt | #0055BC | #F5F5F5 |
| Card Dark | 91440 EMU | None | — | #003781 |
| Icon Circle | 50% (circle) | None | — | #0055BC |
| Divider Line | 0 | 1pt | #E0E0E0 | None |

## Layout Grid

| Layout Type | Columns | Gutter | Left Offset | Right Offset |
|-------------|---------|--------|-------------|---------------|
| Single Column | 1 | — | 457200 | 457200 |
| Two Column (equal) | 2 | 182880 | 457200 | 457200 |
| Two Column (60/40) | 2 | 182880 | 457200 | 457200 |
| Three Column | 3 | 182880 | 457200 | 457200 |
| Four Column | 4 | 91440 | 457200 | 457200 |

## Reusable Placeholder Positions

### Title Area

| Property | EMUs | Inches |
|----------|------|--------|
| Left | 457200 | 0.5 |
| Top | 274638 | 0.3 |
| Width | 11277600 | 12.33 |
| Height | 685800 | 0.75 |

### Subtitle / Eyebrow

| Property | EMUs | Inches |
|----------|------|--------|
| Left | 457200 | 0.5 |
| Top | 960438 | 1.05 |
| Width | 11277600 | 12.33 |
| Height | 457200 | 0.5 |

### Full Content Area

| Property | EMUs | Inches |
|----------|------|--------|
| Left | 457200 | 0.5 |
| Top | 1371600 | 1.5 |
| Width | 11277600 | 12.33 |
| Height | 5029200 | 5.5 |

### Footer Area

| Property | EMUs | Inches |
|----------|------|--------|
| Left | 457200 | 0.5 |
| Top | 6400800 | 6.99 |
| Width | 11277600 | 12.33 |
| Height | 274638 | 0.3 |

## Icon & Image Guidelines

- **Icons**: Use Microsoft Fluent UI icons or simple geometric SVG shapes. Preferred size: 48×48pt to 64×64pt.
- **Photos**: Always use high-res images (min. 1920×1080px). Apply a subtle overlay (#003781 at 10–20% opacity) on photo backgrounds for text legibility.
- **Logos**: Place in top-right or bottom-right corner. Maintain clear space of at least 1× the logo height on all sides.
- **Aspect Ratio**: Maintain original image aspect ratios; never stretch or skew.

## Animation & Transition Defaults

| Property | Default |
|----------|---------|
| Slide Transition | None (static) |
| Object Animation | None (static) |
| Morph Transition | Allowed for section breaks |

## Naming Conventions

| Element | Convention | Example |
|---------|------------|---------|
| Slide layout | kebab-case | `titel-und-inhalt` |
| Placeholder ID | snake_case | `content_left` |
| Color reference | UPPERCASE hex | `#003781` |
| Font reference | Title case | `Calibri Bold` |

## Accessibility Notes

- Minimum contrast ratio: **4.5:1** for body text, **3:1** for large headings.
- Do not rely on color alone to convey meaning.
- All images should have alt text defined in the `notes` field of the slide.
- Font sizes must never go below **10pt** for any visible text.
