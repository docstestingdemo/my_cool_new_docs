# root-and-body.scss

## Overview

The `root-and-body.scss` file is a crucial part of the Docusaurus template's styling system. It defines CSS variables and styles that control the overall appearance of the website, including color schemes for both light and dark themes, background gradients, and various layout adjustments.

Key features of this file include:

1. Definition of color variables for primary colors and their variations
2. CSS custom properties for Docusaurus theming
3. Separate styles for light and dark themes
4. Animated background gradients
5. Styling for specific Docusaurus elements and classes
6. Responsive design adjustments
7. Typography settings and font-related styles
8. Accessibility considerations for improved readability
9. Performance optimizations for smoother animations and transitions
10. Integration with Docusaurus' built-in theme system

This file serves as a foundation for the visual identity of your Docusaurus site, allowing for easy customization and maintenance of a consistent look and feel across all pages.

## How can I customize this for my use case

To customize the `root-and-body.scss` file for your specific needs, you can make the following adjustments:

1. **Color Scheme**: 
   - Modify the `$color-1` variable and its variations to change the primary color of your site.
   - Adjust the CSS custom properties in the `:root` and `[data-theme="dark"]` selectors to fine-tune the color palette for both light and dark themes.

   ```scss
   $primary: $color-1;
   // Modify other color variables as needed
   
   :root {
     --ifm-color-primary: #{$color-1};
     // Adjust other custom properties
   }
   ```

2. **Background Gradients**:
   - Customize the radial gradients in the `[data-theme="dark"]` and `[data-theme="light"]` selectors to create unique background effects.
   - Modify the `gradientAnimation` keyframes to change the animation behavior.

   ```scss
   [data-theme="dark"] #__docusaurus::before {
     background: radial-gradient(ellipse 349px 354px at 60% 40%, rgba(#YourColor, var(--ellipis-transparency)) 40%, transparent 90%) no-repeat;
     // Adjust other properties as needed
   }
   ```

3. **Layout Adjustments**:
   - Modify the media queries and their associated styles to adjust the layout for different screen sizes.
   - Customize padding, margins, and other layout properties to fit your design preferences.

   ```scss
   [class^="docRoot"] {
     @media (min-width: 1400px) {
       padding-left: 5em;
       padding-right: 5em;
       padding-top: 2em;
     }
     // Add or modify other styles
   }
   ```

4. **Element-Specific Styling**:
   - Add or modify styles for specific elements or classes to customize their appearance.
   - For example, you can adjust the styling for images within documentation:

   ```scss
   [class^="docRoot"] {
     img {
       margin-top: 1.5em;
       margin-bottom: 1.5em;
       // Add other image-specific styles
     }
   }
   ```

5. **Animation and Effects**:
   - Modify the `backdrop-filter` and `-webkit-backdrop-filter` properties to adjust blur and saturation effects.
   - Customize the `animation` property to change the duration or timing function of gradient animations.

6. **Typography**:
   - Adjust font sizes, line heights, and font families to match your brand guidelines.
   - Customize heading styles for better hierarchy and readability.

   ```scss
   :root {
     --ifm-font-family-base: 'Your-Preferred-Font', sans-serif;
     --ifm-heading-font-family: 'Your-Heading-Font', serif;
   }

   h1, h2, h3, h4, h5, h6 {
     font-weight: 700;
     // Add custom heading styles
   }
   ```

7. **Accessibility**:
   - Ensure sufficient color contrast between text and background colors.
   - Adjust font sizes and line heights for better readability on various devices.

   ```scss
   body {
     line-height: 1.6;
     font-size: 16px;
     // Add other accessibility-focused styles
   }
   ```

Remember to test your changes thoroughly across different themes and screen sizes to ensure a consistent and appealing design throughout your Docusaurus site. Additionally, consider the impact of your customizations on page load times and overall performance.