# CSS

## TABLE OF CONTENTS

- [Concepts](#concepts)
  - What is CSS?
  - What are the advantages of using CSS?
  - What are the limitations of CSS?
  - How to add CSS to a HTML file?
- [Preprocessors](#preprocessors)
  - What is a CSS Preprocessor?
  - Sass
  - Less
  - Stylus
  - Why to use them?
  - Sass VS Scss

<a name="concepts"/>

## Concepts

### What is CSS?

**Cascading Style Sheets** (CSS) is a simply designed language that allows to apply styles to web pages. It enables to do this independent of the HTML that makes up each web page.

### What are the advantages of using CSS?

- Separation of content from presentation: in this sense it contributes to a cleaner code, faster development, and flexibility for presenting the same content in multiple formats in mobile, desktop or laptop.
- Simplicity of web development and maintainance: it has a simple syntax that could make a huge impact, and also new changes could be atomic (in the sense that adding or removing a selector could be done without refactoring previous code).
- Improvement of bandwidth: the style sheets will be stored in the browser cache and they can be used on multiple pages, without having to download again.

### What are the limitations of CSS?

- Browser Compatibility: some style selectors are supported and some are not. See: https://caniuse.com
- Cross Browser issue: some selectors behave differently in a different browser (IE and Opera support CSS as different logic). I remember having problems with the outline (for the focus ring), floating elements, or the transform property.
- Ascending by selectors is not possible.
- No expressions.
- Pseudo-class not controlled by dynamic behavior.
- Rules, styles, targeting specific text not possible.

### How to add CSS to a HTML file?

There are three ways:

- **Inline CSS**: it is used to apply CSS on a single line or element. For example:
   ```
   <p style="color:blue">Hello world</p>
   ```
- **Internal or Embedded CSS**: it is used to apply CSS on a single document or page. It can affect all the elements of the page. It is written inside the `style` tag within `head` section of `html`.
   ```
   <style>
   p {color:blue}
   </style>
   ```
- **External CSS**: it is used to apply on multiple pages or all pages. There is a separate CSS file with a `.css` extension which contains only styles and should be linked to the HTML document using the `link` tag.
   ```
   <link rel="stylesheet" type="text/css" href="./myCssFile.css">
   ```

<a name="preprocessors"/>

## Preprocessors

### What is a CSS Preprocessor?

complete

### Sass

complete

### Less

complete

### Stylus

complete

### Why to use them?

complete

### Sass VS Scss

complete
