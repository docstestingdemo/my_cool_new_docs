# custom.css vs custom.scss

## Overview

This documentation covers two important styling files in the Docusaurus template: `custom.css` and `custom.scss`. While both files contribute to the project's styling, they serve different purposes and are processed differently.

### custom.css

The `custom.css` file is a crucial part of the Docusaurus template's styling system. It imports the core Tailwind CSS modules, which provide a utility-first CSS framework. This approach allows for rapid UI development with pre-defined classes.

The file consists of three main imports:

1. `@import 'tailwindcss/base';`
2. `@import 'tailwindcss/components';`
3. `@import 'tailwindcss/utilities';`

These imports bring in the base styles, component styles, and utility classes from Tailwind CSS, respectively.

### custom.scss

The `custom.scss` file, on the other hand, is used for writing custom SCSS (Sass) styles. SCSS is a preprocessor scripting language that is interpreted or compiled into CSS. It allows for more advanced features like variables, nested rules, mixins, and functions, which are not available in plain CSS.

## How to use each file

### Using custom.css

To customize the `custom.css` file for your specific needs, you can:

1. **Add custom CSS rules**: You can add your own CSS rules below the Tailwind imports. These will override or complement the Tailwind styles.

2. **Extend Tailwind's configuration**: In your `tailwind.config.js` file, you can extend or override Tailwind's default theme, add new utility classes, or configure plugins.

3. **Use Tailwind's @apply directive**: You can use Tailwind's utility classes within your custom CSS using the `@apply` directive.

4. **Import additional CSS files**: If you have other CSS files for specific components or pages, you can import them in this file.

### Using custom.scss

To utilize the `custom.scss` file:

1. **Write SCSS styles**: You can write your custom styles using SCSS syntax, taking advantage of features like variables, nesting, and mixins.

2. **Import other SCSS files**: You can import other SCSS files to organize your styles more effectively.

3. **Use SCSS features**: Leverage SCSS-specific features like functions and control directives to create more dynamic and maintainable styles.

4. **Compile to CSS**: Ensure your build process includes a step to compile the SCSS file into CSS that can be used by the browser.

Remember to rebuild your project after making changes to either file to see the effects of your customizations.