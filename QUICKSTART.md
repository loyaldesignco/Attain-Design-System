# 🚀 Quick Start Guide

Get started with the Attain Design System in 5 minutes.

## What You Have

The **Attain Design System** is a complete design system extracted from your Webflow site, optimized for Claude-powered applications. It includes:

✅ **Design Tokens** - Colors, typography, spacing, shadows  
✅ **Component Library** - Buttons, cards, forms, navigation, layouts  
✅ **CSS Variables** - Ready-to-use stylesheet  
✅ **Documentation** - Complete usage guides  
✅ **Examples** - Working HTML templates  
✅ **Figma Guide** - For designers  
✅ **Claude Integration** - Optimized prompts and patterns  

## Quick Setup

### Option 1: Copy CSS (Fastest)

1. Copy `/tokens/css-variables.css` to your project
2. Link it in your HTML:
```html
<link rel="stylesheet" href="path/to/css-variables.css">
```

3. Start using design system classes:
```html
<div class="card padding-card">
  <h3 class="heading_tertiary">Card Title</h3>
  <p class="paragraph text-color_secondary">Description</p>
</div>
```

### Option 2: Use with Claude

When prompting Claude, include this:

```markdown
Use the Attain Design System. Available at: [your-github-url]

Key classes to use:
- Layout: section, container, grid_3-col, flex_vertical
- Typography: heading_hero, heading_primary, paragraph_xlarge
- Components: card, button, form
- Spacing: padding_section, margin-bottom_large, gap-medium
- Colors: background_primary, text-color_secondary

Create [describe your need] using these design system classes.
```

### Option 3: GitHub Hosting

1. Create a new GitHub repository
2. Upload all files from the `attain-design-system` folder
3. Enable GitHub Pages (Settings → Pages)
4. Share the documentation URL with your team

## Essential Files

| File | Purpose |
|------|---------|
| `README.md` | Overview and structure |
| `docs/design-tokens.md` | **All available classes and utilities** |
| `docs/components.md` | **Component patterns and examples** |
| `docs/claude-usage.md` | How to use with Claude AI |
| `tokens/css-variables.css` | **CSS file to include in projects** |
| `examples/landing-page.html` | Working example page |

## Most Important Classes

### Layout
```html
<section class="section background_primary padding_section">
  <div class="container">
    <!-- Your content -->
  </div>
</section>
```

### Responsive Grid
```html
<div class="grid_3-col gap-large tablet-1-col">
  <div class="card padding-card">Column 1</div>
  <div class="card padding-card">Column 2</div>
  <div class="card padding-card">Column 3</div>
</div>
```

### Typography
```html
<h1 class="heading_hero margin-bottom_small">Hero Title</h1>
<p class="paragraph_xlarge text-color_secondary">Subtitle text</p>
<p class="paragraph">Body text</p>
```

### Buttons
```html
<a href="#" class="button background_accent-primary text-color_inverse">
  <div class="button_label">Click Me</div>
</a>
```

### Cards
```html
<div class="card padding-card flex_vertical gap-medium">
  <h3 class="heading_tertiary">Card Title</h3>
  <p class="paragraph text-color_secondary">Card description</p>
</div>
```

## Color System

| Class | Usage |
|-------|-------|
| `background_primary` | Main backgrounds (white) |
| `background_secondary` | Alternating sections (light gray) |
| `background_inverse` | Dark sections (black) |
| `background_accent-primary` | CTAs and highlights (blue) |
| `text-color_primary` | Main text (dark) |
| `text-color_secondary` | Supporting text (gray) |
| `text-color_inverse` | Text on dark (white) |

## Spacing Scale

| Class | Size | Use For |
|-------|------|---------|
| `gap-small` | 16px | Tight spacing |
| `gap-medium` | 24px | Standard spacing |
| `gap-large` | 32px | Generous spacing |
| `margin-bottom_small` | 16px | After small elements |
| `margin-bottom_medium` | 24px | After headings |
| `margin-bottom_large` | 32px | After sections |
| `padding_section` | 80px | Section vertical padding |
| `padding-card` | 32px | Card internal padding |

## Responsive Breakpoints

| Breakpoint | Width | Classes |
|------------|-------|---------|
| Desktop | 991px+ | Default |
| Tablet | 767-991px | `tablet-1-col` |
| Mobile (L) | 478-767px | `mobile-l-1-col` |
| Mobile | <478px | `mobile-1-col` |

## 5-Minute Landing Page

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Page</title>
  <link rel="stylesheet" href="css-variables.css">
</head>
<body>

  <!-- Hero -->
  <section class="section min-height_100dvh flex_vertical is-y-center">
    <div class="container text-align_center">
      <h1 class="heading_hero margin-bottom_small">Welcome</h1>
      <p class="paragraph_xlarge text-color_secondary margin-bottom_large">
        Your subtitle here
      </p>
      <a href="#" class="button background_accent-primary text-color_inverse">
        Get Started
      </a>
    </div>
  </section>

  <!-- Features -->
  <section class="section background_secondary padding_section">
    <div class="container">
      <h2 class="heading_primary text-align_center margin-bottom_xlarge">
        Features
      </h2>
      <div class="grid_3-col gap-large tablet-1-col">
        <div class="card padding-card">
          <h3 class="heading_tertiary margin-bottom_small">Feature 1</h3>
          <p class="text-color_secondary">Description</p>
        </div>
        <div class="card padding-card">
          <h3 class="heading_tertiary margin-bottom_small">Feature 2</h3>
          <p class="text-color_secondary">Description</p>
        </div>
        <div class="card padding-card">
          <h3 class="heading_tertiary margin-bottom_small">Feature 3</h3>
          <p class="text-color_secondary">Description</p>
        </div>
      </div>
    </div>
  </section>

</body>
</html>
```

## Claude Prompting Examples

### Example 1: Create a Feature Section
```
Create a feature section using Attain Design System:
- section with background_secondary and padding_section
- container wrapper
- Centered heading_primary with margin-bottom_xlarge
- grid_3-col gap-large tablet-1-col layout
- 3 cards with padding-card, heading_tertiary, and text-color_secondary description
```

### Example 2: Create a Form
```
Create a contact form using Attain Design System:
- form wrapper with form class
- form_block with flex_vertical gap-medium
- 3 form_item elements (Name, Email, Message)
- Use input_field and input_text-area classes
- Submit button with background_accent-primary
```

## Next Steps

1. **Browse Examples**: Check `examples/landing-page.html` for a complete working example
2. **Read Documentation**: 
   - `/docs/design-tokens.md` - See all available classes
   - `/docs/components.md` - Learn component patterns
   - `/docs/claude-usage.md` - Optimize Claude prompts
3. **For Designers**: Follow `/docs/figma-guide.md` to recreate in Figma
4. **Host on GitHub**: Upload to GitHub and enable Pages for team access

## Getting Help

**Find a Class**: Search `docs/design-tokens.md` for any utility you need

**Component Patterns**: Check `docs/components.md` for common layouts

**Examples**: Look at `examples/landing-page.html` for implementation

**Responsive**: Read `docs/responsive.md` for mobile/tablet behavior

## Pro Tips

✨ **Combine utilities**: `card padding-card flex_vertical gap-medium`

✨ **Use semantic colors**: `text-color_secondary` instead of specific hex values

✨ **Follow spacing scale**: Use predefined spacing (small/medium/large) for consistency

✨ **Mobile-first**: Use `tablet-1-col` and `mobile-l-1-col` for responsive grids

✨ **With Claude**: Be specific about classes to use, Claude will follow the system

---

**You're ready to build!** Start with the example HTML, customize it, and use Claude to generate more components following the design system patterns.
