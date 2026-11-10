# cssbun

CSS bun(dle) is a opinionated codebase for CSS usage inside web projects.

AI agents usually have dificulty in keeping CSS organized and consistent across large web projects. This project aims to provide a structured and opinionated approach to managing CSS, making it easier for AI agents and developers alike to maintain clean and consistent styles.

The project offers a library with a default codebase and a set of rules, patterns, naming conventions and best practices for this CSS library.

The project uses [Bun](https://bun.com) to run javascript code.

## Structure and Tools

Fundamental project folders:

- `src` : Library code and documentation.
- `demo` : Demonstration pages that doubledown as test cases.
- `dist` : Distribution library.

## Specification

The backbone of the css in this library builts around the following **layers**:

1. **Base**: This layer includes all the primitive definitions.
   - **src/base/reset.css**, includes minimal reset rules for `box-sizing`, `margin` and `padding`, remove `list-style` from lists, ensure font inheritance for form elements, block display for all image-based elements and a default style for `code` elements.
   - **src/base/theme.css**, A fixed set of CSS _primitives_ defined inside the `:root` selector with custom properties, including fonts, colors and sizing attributes with default values. It also provides a default variation for `light`and `dark` themes.
   - **src/base/base.css**, imports the `reset`and `theme` styles and then provides classes that expose the the _primitives_ defined in the `theme`.

2. **Utility**: Provides utility classes for common styling patterns, and group styles for specific css libraries like FLEX and GRID.

3. **Layout**: Provides layout-related classes and structures, such as grid systems, flexbox containers, and other layout utilities to organize content within the web project.

4. **Component**: This layer contains complex components that are built using elements from the previous layers, and may include javascript.

The source folder structure is as follows:

```
src/
├── base/
│   ├── reset.css
│   ├── theme.css
│   └── base.css
├── utility/
│   └── utilities.css
├── layout/
│   ├── layouts.css
│   └── ...
└── component/
    ├── form
    │   ├── form.css
    │   ├── form.js
    │   └── ...
    ├── calendar
    │   ├── calendar.css
    │   └── ...
    └── other-component
        └── ...
```

## Layers

TODO - Provide detailed strategy for each layer.
