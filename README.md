# Attain Design System

A comprehensive design system for Claude-powered applications, extracted from the Attain AI Webflow implementation. This design system provides a consistent foundation for building AI-focused interfaces with professional styling, responsive layouts, and accessibility in mind.

## Overview

The Attain Design System is inspired by and extracted from the Webflow-based Attain AI website. It provides design tokens, component patterns, and guidelines optimized for AI/tech products and Claude-based applications.

## Table of Contents

- [Design Principles](#design-principles)
- [Getting Started](#getting-started)
- [Design Tokens](#design-tokens)
- [Components](#components)
- [Layout System](#layout-system)
- [Typography](#typography)
- [Colors](#colors)
- [Spacing](#spacing)
- [Usage with Claude](#usage-with-claude)

## Design Principles

1. **Clarity** - Clear hierarchy and scannable content
2. **Consistency** - Unified patterns across all interfaces
3. **Accessibility** - WCAG compliant and keyboard navigable
4. **Responsiveness** - Mobile-first, adapts to all screen sizes
5. **Professional** - Enterprise-ready aesthetic for B2B applications

## Getting Started

### For Designers

1. Review the [Design Tokens](./docs/design-tokens.md) documentation
2. Explore [Component Patterns](./docs/components.md)
3. Use the [Figma Recreation Guide](./docs/figma-guide.md) to implement in Figma

### For Developers

1. Reference [CSS Variables](./tokens/css-variables.css)
2. Use [Component Classes](./docs/component-classes.md)
3. Follow [Responsive Breakpoints](./docs/responsive.md)

### For Claude Prompts

Include this in your Claude prompts:
```
Use the Attain Design System from [GitHub URL]. Follow the component patterns in /docs/components.md and use the design tokens from /tokens/.
```

## Design Tokens

Design tokens are organized into:

- **Colors** - Primary, secondary, accent palettes with semantic naming
- **Typography** - Font families, sizes, weights, and line heights
- **Spacing** - Consistent spacing scale (xxsmall to xxlarge)
- **Shadows** - Elevation levels for depth
- **Borders** - Radius values for consistent rounding
- **Breakpoints** - Responsive design breakpoints

See [Design Tokens Documentation](./docs/design-tokens.md) for complete reference.

## Components

### Core Components

- **Buttons** - Primary, secondary, inverse variants
- **Cards** - Content containers with padding and shadows
- **Navigation** - Headers, menus, and mobile navigation
- **Forms** - Inputs, textareas, selects, and validation states
- **Typography** - Headings (Hero, Primary, Secondary, Tertiary), Paragraphs
- **Layouts** - Sections, containers, and grid systems

See [Components Documentation](./docs/components.md) for detailed specs.

## Layout System

### Grid System
- 3-column grid on desktop
- 1-column on tablet/mobile
- Automatic responsive stacking

### Breakpoints
- Desktop (Main): 991px+
- Tablet: 767-991px
- Mobile (L): 478-767px
- Mobile: <478px

## Typography

### Heading Scale
- **Hero**: Display-level headings for landing pages
- **Primary (H2)**: Section headings
- **Secondary (H3)**: Subsection headings
- **Tertiary (H4-H6)**: Component-level headings

### Paragraph Styles
- **XLarge**: Hero subheadings
- **Large**: Section introductions
- **Regular**: Body copy
- **Small**: Captions and metadata

## Colors

### Primary Palette
- Primary: Used for main backgrounds and key UI elements
- Secondary: Supporting background colors
- Inverse: Dark mode / contrast elements

### Accent Colors
- Accent Primary: Call-to-action elements
- Accent Secondary: Highlights and interactive states
- Accent Tertiary: Subtle accents

### Semantic Colors
- `text-color_primary`: Default text
- `text-color_secondary`: Muted text
- `text-color_muted`: Disabled/placeholder text
- `text-color_inverse`: Text on dark backgrounds

## Spacing

Consistent spacing scale based on multiples:
- **xxxsmall**: 4px
- **xxsmall**: 8px
- **xsmall**: 12px
- **small**: 16px
- **medium**: 24px
- **large**: 32px
- **xlarge**: 48px
- **xxlarge**: 64px

Applied via utility classes:
- `padding_[size]`
- `margin_[size]`
- `gap-[size]`
- `margin-bottom_[size]`
- `margin-top_[size]`

## Usage with Claude

### Example Prompt

```markdown
Create a landing page using the Attain Design System. Use:
- heading_hero for the main headline
- paragraph_xlarge for the subtitle
- card components with padding-card for feature sections
- grid_3-col layout that stacks on tablet
- Primary button style for CTAs
- background_primary and background_secondary for section alternation
```

### Claude Artifacts

When creating React artifacts with this design system:

```jsx
<section className="section background_primary">
  <div className="container padding_section">
    <h1 className="heading_hero margin-bottom_small">Your Headline</h1>
    <p className="paragraph_xlarge text-color_secondary">Your subtitle</p>
  </div>
</section>
```

## Repository Structure

```
attain-design-system/
├── README.md                          # This file
├── docs/
│   ├── design-tokens.md              # Complete token reference
│   ├── components.md                 # Component specifications
│   ├── typography.md                 # Typography system
│   ├── colors.md                     # Color palette
│   ├── spacing.md                    # Spacing system
│   ├── responsive.md                 # Breakpoints and grid
│   ├── figma-guide.md               # Recreating in Figma
│   └── claude-usage.md              # Using with Claude
├── tokens/
│   ├── colors.json                   # Color tokens
│   ├── typography.json               # Typography tokens
│   ├── spacing.json                  # Spacing tokens
│   └── css-variables.css            # All tokens as CSS vars
└── examples/
    ├── landing-page.html            # Example page
    └── component-library.html       # All components

```

## Contributing

This is a living design system. To contribute:

1. Document new patterns discovered in Attain AI implementations
2. Submit issues for inconsistencies or missing components
3. Propose enhancements following the design principles

## License

This design system is derived from the Attain AI Webflow implementation and is provided for use with Claude-based applications.

## Support

For questions or issues:
- Create an issue in this repository
- Reference the Webflow Flowkit Framework documentation
- Consult the [Webflow University](https://university.webflow.com/)

---

**Version**: 1.0.0  
**Last Updated**: February 2026  
**Based on**: Attain AI Webflow Site (attain-concepts-ai.webflow.io)
