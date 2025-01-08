# Customizing Docusaurus Styling: A Comprehensive Guide

Docusaurus provides a flexible and powerful theming system that allows you to customize the look and feel of your documentation site. This guide will walk you through common customization scenarios and best practices for styling your Docusaurus site.

## Table of Contents

- [Basic Customization](#basic-customization)
- [Advanced Theming](#advanced-theming)
- [Common Customization Scenarios](#common-customization-scenarios)
- [Best Practices](#best-practices)

## Basic Customization

### Modifying the Default Theme

To start customizing your Docusaurus site, you can modify the default theme by creating a `custom.css` file in the `src/css` directory. This file will be automatically loaded and applied to your site.

```css
/* src/css/custom.css */
:root {
  --ifm-color-primary: #25c2a0;
  --ifm-color-primary-dark: rgb(33, 175, 144);
  --ifm-color-primary-darker: rgb(31, 165, 136);
  --ifm-color-primary-darkest: rgb(26, 136, 112);
  --ifm-color-primary-light: rgb(70, 203, 174);
  --ifm-color-primary-lighter: rgb(102, 212, 189);
  --ifm-color-primary-lightest: rgb(146, 224, 208);
  --ifm-code-font-size: 95%;
}
```

### Customizing the Navbar and Footer

You can customize the navbar and footer in the `docusaurus.config.js` file:

```js
module.exports = {
  // ...
  themeConfig: {
    navbar: {
      title: 'My Site',
      logo: {
        alt: 'My Site Logo',
        src: 'img/logo.svg',
      },
      items: [
        // Add your navigation items here
      ],
    },
    footer: {
      style: 'dark',
      links: [
        // Add your footer links here
      ],
      copyright: `Copyright © ${new Date().getFullYear()} My Project, Inc.`,
    },
  },
};
```

## Advanced Theming

### Creating a Custom Theme

For more advanced customization, you can create a custom theme by extending the default theme:

1. Create a new directory for your theme: `src/theme`
2. Create an `index.js` file in this directory to export your theme components
3. Swizzle components you want to customize using the `docusaurus swizzle` command

Example `src/theme/index.js`:

```js
import Footer from '@theme-original/Footer';
import NavBar from '@theme-original/Navbar';

export default {
  Footer,
  NavBar,
  // Add other components you want to customize
};
```

### Using CSS Modules

Docusaurus supports CSS Modules out of the box. Create a `.module.css` file next to your component to use scoped styles:

```css
/* MyComponent.module.css */
.myCustomClass {
  color: #25c2a0;
  font-weight: bold;
}
```

```jsx
import React from 'react';
import styles from './MyComponent.module.css';

function MyComponent() {
  return <div className={styles.myCustomClass}>Hello, world!</div>;
}
```

## Common Customization Scenarios

### Changing the Color Scheme

To change the color scheme, modify the CSS variables in your `custom.css` file:

```css
:root {
  --ifm-color-primary: #4e89e8;
  --ifm-color-primary-dark: #3375e4;
  --ifm-color-primary-darker: #256be2;
  --ifm-color-primary-darkest: #1857bf;
  --ifm-color-primary-light: #699dec;
  --ifm-color-primary-lighter: #77a7ed;
  --ifm-color-primary-lightest: #a0c0f2;
}
```

### Customizing Typography

To change the default font or typography styles:

```css
:root {
  --ifm-font-family-base: 'Roboto', sans-serif;
  --ifm-heading-font-family: 'Poppins', sans-serif;
  --ifm-font-size-base: 16px;
  --ifm-line-height-base: 1.6;
}
```

### Adding Custom Layouts

Create a new layout component in `src/theme/Layout` to customize the overall page structure:

```jsx
import React from 'react';
import Layout from '@theme/Layout';

function CustomLayout({children}) {
  return (
    <Layout>
      <div className="custom-wrapper">{children}</div>
    </Layout>
  );
}

export default CustomLayout;
```

## Best Practices

1. **Use CSS Variables**: Leverage Docusaurus' CSS variables for consistent theming across your site.
2. **Mobile-First Approach**: Always consider mobile devices when styling your components.
3. **Performance**: Minimize the use of heavy CSS frameworks and opt for lightweight, modular solutions.
4. **Accessibility**: Ensure your custom styles maintain good color contrast and readability.
5. **Version Control**: Keep your custom styles in version control to track changes and collaborate with your team.
6. **Documentation**: Document your custom styles and components for easier maintenance and onboarding of new team members.

By following these guidelines and exploring the various customization options, you can create a unique and visually appealing Docusaurus site that aligns with your project's branding and requirements.