# New UI Foundations

#### What is New UI?
New UI is a modern, semantic UI framework for building beautiful, accessible websites and apps. It gives you all the core design foundations you need—colors, typography, spacing and sizing, reset, grid and layouts, and layering and elevations. It's designed to grow with you, from your first launch to millions of users. Thoughtfully made for makers, small teams, and anyone who cares about great design.

#### Install
To set up the project, open your terminal and run the following command:

```
npm i -D @new-ui/foundations
```

<strong>Note:</strong> This command installs all New UI foundation packages, which include reset, colors, effects, spacings, and typography. If you need to install only specific packages, refer to the foundations documentation for instructions.

#### Import
Import the New UI foundations by adding the following line at the top of your SCSS file:

```scss
@use '@new-ui/foundations';     // Use `@import` for CSS
```

#### Set the theme
Set the theme by adding the `data-new-ui-theme` attribute to your HTML wrapper element, for example:

```html
<html data-new-ui-theme="light">
```

Available themes  | Value
:--- |:---
Light (Default) | `light`
Light warm | `light--warm`
Light cold | `light--cold`
Dark  (Default) | `dark`
Dark warm | `dark--warm`
Dark cold | `dark--cold`


#### Usage guide
- All classes associated with the New UI are prefixed with a global namespace followed by a hyphen: `nu-`
- In addition to a global namespace, we added prefixes to each class to make it more apparent what job that class is doing using BEM syntax.
    - `c-` for UI components.
    - `l-` for layout-related styles.
    - `u-` for utilities.
    - `is-` and `has-` for state-based classes.
    - `js-` for targeting JavaScript-specific functionality.

---

### Design Tokens & Primitives

#### Colors

Background | Role
:--- | :---
**`--background`** | Default app background
**`--background-secondary`** | Secondary app background
**`--background-hover`** | Background hover
**`--background-selected`** | UI element background
**`--background-selected-hover`** | UI element background hovered
**`--background-high-contrast`** | High contrast background

Border | Role
:--- | :---
**`--border-muted`** | Muted strokes and separators
**`--border`** | Default strokes and separators
**`--border-strong`** | Strong strokes and separators
**`--border-inked`** | Inked strokes and separators
**`--border-inverse`** | Inverse strokes and separators
**`--border-focus`** | Focus outline

Button | Role
:--- | :---
**`--button`** | Primary button background
**`--button-hover`** | Primary button hover
**`--button-active`** | Primary button active
**`--button-disabled`** | Disabled button background

Link | Role
:--- | :---
**`--link`** | Primary link
**`--link-hover`** | Hover state for primary link
**`--link-subtle`** | Secondary link
**`--link-visited`** | Link visited

Support | Role
:--- | :---
**`--support-error`** | Error
**`--support-warning`** | Warning
**`--support-success`** | Success
**`--support-info`** | Information

Content | Role
:--- | :---
**`--content-primary`** | Primary body copy
**`--content-secondary`** | Secondary text color
**`--content-secondary-alt`** | Secondary text color alt
**`--content-placeholder`** | Placeholder text color
**`--content-on-color`** | Text on interactive color
**`--content-error`** | Error message
**`--content-success`** | Success message
**`--content-inked`** | Inked text

#### Effects

Shadows | Role
:--- | :---
**`--dialog-strong`** | Modals, sidebar overlays, toasts
**`--dialog`** | Dropdown, tooltip, popover
**`--content`** | Content area, buttons, controls, cards, pills
**`--canvas`** | Background
**`--keyboard-key`** | Keyboard key component

Focus | Role
:--- | :---
**`--focus-default`** | Default focus
**`--focus-accent`** | Accent focus
**`--focus-inverse`** | Focus inverse

Borders | Role
:--- | :---
**`--border-width-01`** | Default border width
**`--border-width-02`** | Used for the selection and focus order

#### Spacings

Token | Size (px/rem)
:--- | :---
**`--spacing-00`** | 0 / 0
**`--spacing-01`** | 2 / 0.125
**`--spacing-02`** | 4 / 0.25
**`--spacing-03`** | 6 / 0.375
**`--spacing-04`** | 8 / 0.5
**`--spacing-05`** | 12 / 0.75
**`--spacing-06`** | 16 / 1
**`--spacing-07`** | 20 / 1.25
**`--spacing-08`** | 24 / 1.5
**`--spacing-09`** | 32 / 2
**`--spacing-10`** | 40 / 2.5
**`--spacing-11`** | 48 / 3
**`--spacing-12`** | 56 / 3.5
**`--spacing-13`** | 64 / 4
**`--spacing-14`** | 72 / 4.5
**`--spacing-15`** | 80 / 5
**`--spacing-16`** | 96 / 6
**`--spacing-17`** | 120 / 7.5
**`--spacing-18`** | 160 / 10

#### Typography

Heading (Desktop) | Heading (Mobile) | Role
:--- | :--- | :---
**`--desktop-heading-01`** | **`--mobile-heading-01`** | Heading 01
**`--desktop-heading-02`** | **`--mobile-heading-02`** | Heading 02
**`--desktop-heading-03`** | **`--mobile-heading-03`** | Heading 03
**`--desktop-heading-04`** | **`--mobile-heading-04`** | Heading 04
**`--desktop-heading-05`** | **`--mobile-heading-05`** | Heading 05
**`--desktop-heading-06`** | **`--mobile-heading-06`** | Heading 06

Body (Desktop) | Body (Mobile) | Role
:--- | :--- | :---
**`--desktop-body-xl`** | **`--mobile-body-xl`** | Body large
**`--desktop-body`** | **`--mobile-body`** | Body copy
**`--desktop-body-sm`** | **`--mobile-body-sm`** | Body small

Utility (Desktop) | Utility (Mobile) | Role
:--- | :--- | :---
**`--desktop-caption`** | **`--mobile-caption`** | Caption
**`--desktop-helper-text`** | **`--mobile-helper-text`** | Helper text
**`--desktop-code`** | **`--mobile-code`** | Code

> Note: To set line height, simply add the prefix `--lh` to the font size variables. For instance, `--desktop-body-xl` becomes `--lh-desktop-body-xl`.

---

### The new reset

A thoughtful SCSS, CSS reset that preserves browser defaults while giving you complete design control. New UI reset eliminates cross-browser inconsistencies without being overly opinionated, allowing you to build upon a clean foundation.

```scss
// https://cdn.jsdelivr.net/npm/@new-ui/reset@latest/dist/index.css

*, *::before, *::after {
  box-sizing: border-box;
}

html {
  -moz-text-size-adjust: none;
  -webkit-text-size-adjust: none;
  text-size-adjust: none;
  vertical-align: baseline;
}

body, h1, h2, h3, h4, p,
figure, blockquote, dl, dd {
  margin: 0;
  padding: 0;
  margin-block-end: 0;
}

ul[role='list'],
ol[role='list'] {
  list-style: none;
}

body {
  min-height: 100vh;
  line-height: 1.5;
}

h1, h2,
h3, h4 {
  text-wrap: balance;
}

a:not([class]) {
  text-decoration-skip-ink: auto;
}

img,
picture {
  max-width: 100%;
  display: block;
}

input, textarea, button, select {
  font-family: inherit;
  font-size: inherit;
  margin: 0;
}

table {
  border-collapse: collapse;
  border-spacing: 0;
}

:target {
  scroll-margin-block: 5ex;
}
```