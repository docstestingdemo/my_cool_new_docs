# Styling System Overview

This document provides an overview of the styling system used in our Docusaurus template, explaining how the various SCSS files work together and how to use them effectively.

## Structure

Our styling system is organized into several key SCSS files:

- `_variables.scss`: Defines global variables for colors, fonts, spacing, etc.
- `_mixins.scss`: Contains reusable SCSS mixins for common styling patterns
- `_base.scss`: Sets up base styles for HTML elements
- `_layout.scss`: Defines overall page layout and grid system
- `_components.scss`: Styles for reusable UI components
- `_utilities.scss`: Utility classes for quick styling adjustments

## Usage

To use the styling system in your Docusaurus pages and components:

1. Import the main `styles.scss` file, which includes all the above partials
2. Use variables, mixins, and utility classes as needed in your custom styles
3. Override or extend existing styles by targeting the appropriate selectors

## Best Practices

- Leverage variables and mixins to maintain consistency
- Use utility classes for minor adjustments rather than writing custom CSS
- Follow the existing naming conventions when adding new styles
- Keep component-specific styles separate from global styles

## Customization

To customize the overall look and feel:

1. Modify variables in `_variables.scss` to change colors, fonts, etc.
2. Add new mixins to `_mixins.scss` for reusable style patterns
3. Extend existing component styles in `_components.scss`

By understanding and properly utilizing this styling system, you can maintain a consistent design language throughout your Docusaurus site while allowing for easy customization and extension.