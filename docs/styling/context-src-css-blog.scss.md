# blog.scss

## Overview

The `blog.scss` file is a crucial part of the Docusaurus template's styling system, specifically tailored for the blog section. It contains SCSS (Sassy CSS) code that defines the layout, appearance, and responsive behavior of various blog-related components.

Key features of this file include:

1. Responsive design adjustments for different screen sizes
2. Custom styling for blog post headers and content
3. Layout modifications for both blog list and individual post pages
4. Conditional styling based on theme (light/dark mode)
5. Customizations for typography, spacing, and element visibility

## How can I customize this for my usecase

To customize the `blog.scss` file for your specific needs, consider the following approaches:

1. **Modify existing styles:**
   - Adjust color schemes, fonts, or spacing by changing values in the existing CSS rules.
   - Example: To change the font size of blog post content, locate the `.dev-docs-blog p` selector and modify the `font-size` property.

2. **Add new style rules:**
   - Create new CSS selectors to target specific elements in your blog layout.
   - Example: To add a custom background to your blog sidebar, you could add:
     ```scss
     .blog-sidebar {
       background-color: #f0f0f0;
       padding: 1rem;
     }
     ```

3. **Responsive design adjustments:**
   - Modify or add media queries to fine-tune the layout for different screen sizes.
   - Example: To adjust the blog header title for medium-sized screens, you could add:
     ```scss
     @media (min-width: 768px) and (max-width: 1023px) {
       .blog-header-title-card h1 {
         font-size: 48px;
       }
     }
     ```

4. **Conditional styling:**
   - Utilize the existing `conditional-styles` mixin or create your own to apply styles based on specific conditions.
   - Example: To hide a certain element only on the blog list page, you could add:
     ```scss
     .blog-list-page {
       @include conditional-styles("some-class") {
         .element-to-hide {
           display: none;
         }
       }
     }
     ```

5. **Theme customization:**
   - Modify or add styles for dark mode by using the `[data-theme="dark"]` selector.
   - Example: To change link colors in dark mode, you could add:
     ```scss
     [data-theme="dark"] {
       .blog-content a {
         color: #00ffff;
       }
     }
     ```

Remember to test your changes thoroughly across different devices and browsers to ensure a consistent experience for all users. You may also need to rebuild your Docusaurus site to see the changes take effect.

## Customize Styling

To further customize the blog styling, you can refer to the following examples:

1. **Adjusting blog post layout:**
   ```scss
   .blog-post-page {
     .blog-post {
       max-width: 800px;
       margin: 0 auto;
     }
   }
   ```

2. **Customizing blog list item appearance:**
   ```scss
   .blog-list-page {
     .blog-list-item {
       border: 1px solid #ddd;
       border-radius: 8px;
       padding: 1rem;
       margin-bottom: 1rem;
       
       &:hover {
         box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
       }
     }
   }
   ```

3. **Styling blog post metadata:**
   ```scss
   .blog-post-meta {
     font-size: 0.9rem;
     color: #666;
     margin-bottom: 1rem;
     
     .blog-post-date {
       font-weight: bold;
     }
   }
   ```

4. **Enhancing code block appearance:**
   ```scss
   .blog-post {
     pre {
       background-color: #f4f4f4;
       border-radius: 4px;
       padding: 1rem;
       overflow-x: auto;
     }
   }
   ```

5. **Improving blog post navigation:**
   ```scss
   .blog-post-nav {
     display: flex;
     justify-content: space-between;
     margin-top: 2rem;
     padding-top: 1rem;
     border-top: 1px solid #ddd;
     
     a {
       text-decoration: none;
       color: #0077cc;
       
       &:hover {
         text-decoration: underline;
       }
     }
   }
   ```

These examples demonstrate how to customize various aspects of your blog's appearance. Remember to adapt these styles to fit your specific design preferences and requirements.