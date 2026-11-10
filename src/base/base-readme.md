# Base layer

This document decribes the structure, organization, and naming conventions for the base CSS layer used in the project.

## reset.css

Used to reset the default styles provided by the browser.

- Ensure adequate box sizing
- Reset margins and paddings to zero
- Ensure same font inheritance for all input elements
- Remove style from list items
- Ensure images display as block by default
- Set light and dark as color schemes
- Define a propper style for `code` elements

## base.css

The base file defines a set of basic classes that set the root styles of the library.
Actual values are indexed into `theme.css` custom properties.

| Class                 | Objective                                                     | Theme Custom    |
| --------------------- | ------------------------------------------------------------- | --------------- |
| `bg-[050-900]`        | Background color sequence                                     | `--color-XXX`   |
| `bg-transparent`      | Transparent background                                        |                 |
| `text-[050-900]`      | Text color sequence                                           | `--color-XXX`   |
| `text-transparent`    | Transparent text                                              |                 |
| `font-[type]`         | Font types: `sans`(serif), `serif`, `mono`(space) and `theme` | `--font-[type]` |
| `fs-[size]`           | Font size, one of `xs;s;m;l;xl`                               | `--fs-[size]`   |
| `fw-[size]`           | Font weight, one of `xs;s;m;l;xl`                             | `--fw-[size]`   |
| `lh-[size]`           | Line height, one of `xs;s;m;l;xl`                             | `--lh-[size]`   |
| `text-underline`      | Underline text                                                |                 |
| `text-strike`         | Strike through text                                           |                 |
| `m-[size]`            | Margin, one of `s;m;l`                                        | `--mx-[size]`   |
| `mx-[size]`           | Margin inline width, one of `s;m;l`                           | `--mx-[size]`   |
| `my-[size]`           | Margin block width, one of `s;m;l`                            | `--my-[size]`   |
| `bw-[size]`           | Border width, one of `s;m;l`                                  | `--bw-[size]`   |
| `bc-[050-900]`        | Border color sequence                                         | `--color-XXX`   |
| `bc-transparent`      | Transparent border                                            |                 |
| `ow-[size]`           | Outline width, one of `s;m;l`                                 | `--ow-[size]`   |
| `oo-[size]`           | Outline offset, one of `s;m;l`                                | `--oo-[size]`   |
| `oc-[050-900]`        | Outline color sequence                                        | `--color-XXX`   |
| `oc-transparent`      | Transparent outline color                                     |                 |
| `p-[size]`            | Padding, one of `s;m;l`                                       | `--px-[size]`   |
| `px-[size]`           | Padding inline width, one of `s;m;l`                          | `--px-[size]`   |
| `py-[size]`           | Padding block width, one of `s;m;l`                           | `--py-[size]`   |
| `inline`              | Display as a inline element                                   |                 |
| `inline-block`        | Display as a inline block element                             |                 |
| `block`               | Display as a block element                                    |                 |
| `hidden`              | Set Display to none                                           |                 |
| `invisible`           | Set Visibility to invisible (the the space reserved)          |                 |
| `static`              | Element position static on the page (default)                 |                 |
| `absolute`            | Element position absolute (to first relative parent)          |                 |
| `relative`            | Element position relative (may offset from normal flow)       |                 |
| `fixed`               | Element position fixed (in the page)                          |                 |
| `sticky`              | Element position sticky (to a inline or block boundary)       |                 |
| `z-index-[index]`     | Push element up in the redering layer, [`1` to `5`]           |                 |
| `isolate`             | Force creation of a new stacking context                      |                 |
| `aspect-[type]`       | Aspect ratio for img, one of `square;video;golden`            |                 |
| `overflow-[type]`     | Overflow, one of `auto;hidden;scroll;clip`                    |                 |
| `overflow-[a]-[type]` | Overflow distinct for axis, one of `x;y` (and then type)      |                 |
| `gap-[size]`          | Gap for Flex and Grid, one of `s;m;l`                         | `--gap-[size]`  |

## theme.css

Defines a set of custom properties under the `:root` selector to define common values for many of the base CSS rules.
Also defines default color values for the **light** and **dark** modes, based on match of one of the selectors `#theme[data-theme="light"]` and `#theme[data-theme="dark"]` respectivelly.

### Typography

| Type        | Property   | Values                      | Notes                        |
| ----------- | ---------- | --------------------------- | ---------------------------- |
| font family | font-sans  | font-family names           |                              |
| "           | font-serif | "                           |                              |
| "           | font-mono  | "                           |                              |
| "           | font-base  | "                           | The application default font |
| "           | font-brand | "                           | The brand or theme font      |
| font size   | fs-{size}  | font-size: size:[xs...xl]   | Use medium as default        |
| "           | fw-{size}  | font-weight: size:[xs...xl] | Use medium as default        |
| line height | lh-{size}  | line-height: size:[xs...xl] |                              |

### Box Model

| Type              | Property   | Values                       | Notes |
| ----------------- | ---------- | ---------------------------- | ----- |
| margin            | mx-{size}  | margin-inline: size:[s...l]  |       |
| "                 | my-{size}  | margin-block: size:[s...l]   |       |
| border width      | bw-{size}  | border-width: size:[s...l]   |       |
| outline width     | ow-{size}  | outline-width: size:[s...l]  |       |
| outline offset    | oo-{size}  | outline-offset: size:[s...l] |       |
| padding           | px-{size}  | padding-inline: size:[s...l] |       |
| "                 | py-{size}  | padding-block: size:[s...l]  |       |
| gap (flex & grid) | gap-{size} | gap: size:[s...l]            |       |

### Color

| Property        | Values            | Notes |
| --------------- | ----------------- | ----- |
| pallete-{index} | index:[050...950] |       |

## base.css

Contains the **base classes** for color, sizing, typography, layout, etc.
Imports the `reset.css` and `theme.css` files, and is imported by the application as the foundational CSS layer.

# Background and Foreground colors

| Type             | Class name       | CSS                                  | Notes |
| ---------------- | ---------------- | ------------------------------------ | ----- |
| Background color | bg-{color}       | background-color: color:[050 to 950] |       |
| "                | bg-transparent   | background-color: transparent        |       |
| Text color       | text-{color}     | color: size:[050 to 950]             |       |
| "                | text-transparent | color: transparent                   |       |

# Font

| Type        | Class name | Notes                        |
| ----------- | ---------- | ---------------------------- |
| Font family | font-sans  | Sans serif                   |
| "           | font-serif | Serif                        |
| "           | font-mono  | Monospace                    |
| "           | font-base  | The application default font |
| "           | font-brand | The brand or theme font      |

### Layout

### FLEX

| Type                       | Class Name      | CSS                            | Nested CSS              |
| -------------------------- | --------------- | ------------------------------ | ----------------------- |
| flex                       | flex            | display: flex                  |                         |
| direction                  | column          | flex-direction: column         | .flex &.column          |
| wrap (dft)                 | wrap            | flex-wrap: wrap                | .flex &.wrap            |
| "                          | nowrap (dft)    | flex-wrap: nowrap              | .flex &.nowrap          |
| justify (<-->)             | justify-start   | justify-content: flex-start    | .flex &.justify-start   |
| "                          | justify-end     | justify-content: flex-end      | .flex &.justify-end     |
| "                          | justify-center  | justify-content: center        | .flex &.justify-center  |
| "                          | justify-between | justify-content: space-between | .flex &.justify-between |
| "                          | justify-around  | justify-content: space-around  | .flex &.justify-around  |
| "                          | justify-evenly  | justify-content: space-evenly  | .flex &.justify-evenly  |
| align items (y, 1 line)    | items-start     | align-items: flex-start        | .flex &.items-start     |
| "                          | items-end       | align-items: flex-end          | .flex &.items-end       |
| "                          | items-center    | align-items: center            | .flex &.items-center    |
| "                          | items-baseline  | align-items: baseline          | .flex &.items-baseline  |
| "                          | items-stretch   | align-items: stretch           | .flex &.items-stretch   |
| align content (y, n lines) | content-start   | align-content: flex-start      | .flex &.content-start   |
| "                          | content-end     | align-content: flex-end        | .flex &.content-end     |
| "                          | content-center  | align-content: center          | .flex &.content-center  |
| "                          | content-between | align-content: space-between   | .flex &.content-between |
| "                          | content-around  | align-content: space-around    | .flex &.content-around  |
| "                          | content-stretch | align-content: stretch         | .flex &.content-stretch |

### GRID

| Type             | Class Name | CSS                       | Nested CSS        |
| ---------------- | ---------- | ------------------------- | ----------------- |
| grid             | grid       | display: grid             |                   |
| "                | x          | x: v                      |                   |
| (copy from flex) | x          | x: v                      |                   |
| "                | x          | x: v                      |                   |
| "                | x          | x: v                      |                   |
| "                | x          | x: v                      |                   |
| auto columns     | auto-cols  | grid-template-columns:... | .grid &.auto-cols |
