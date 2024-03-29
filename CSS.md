# CSS

## TABLE OF CONTENTS

- [BASIC](#basic)
  - 1 What is CSS?
  - 2 What are the advantages of using CSS?
  - 3 What are the limitations of CSS?
  - 4 How to add CSS to a HTML file?
  - 5 Which type of CSS addition has the highest priority?
  - 6 What is the Box model?
  - 7 What is the "block" box model?
  - 8 What is the "inline" box model?
  - 9 What is the "inline-block" box model?
  - 10 What is the "flex" and "inline-flex" box model?
  - 11 What is the "grid" box model?
- [INTERMEDIATE](#intermediate)
  - 12 What is the difference between flexbox and grid?
  - 13 What is a CSS selector?
  - 14 What is the Universal Selector?
  - 15 What is the Element Type Selector?
  - 16 What is the ID Selector?
  - 17 What is the Class Selector?
  - 18 What is the Descendant Combinator?
  - 19 What is the Child combinator?
  - 20 What is the General Sibling Combinator?
  - 21 What is the Adjacent Sibling Combinator?
  - 22 What is the Attribute Selector?
- [ADVANCED](#advanced)
  - 23 What is a CSS framework?
  - 24 Name some CSS frameworks
  - 25 Why use CSS frameworks?
  - 26 Bootstrap, Bulma, Foundation and Materialize
  - 27 What is a CSS Preprocessor?
  - 28 Sass
  - 29 Sass VS Scss
  - 30 Less
  - 31 Sass VS Less
  - 32 Stylus
  - 33 Sass VS Less VS Stylus

<a name="basic"/>

## BASIC

### 1. What is CSS?

**Cascading Style Sheets** (CSS) is a simply designed language that allows to apply styles to web pages. It enables to do this independent of the HTML that makes up each web page.

### 2. What are the advantages of using CSS?

- Separation of content from presentation: in this sense it contributes to a cleaner code, faster development, and flexibility for presenting the same content in multiple formats in mobile, desktop or laptop.
- Simplicity of web development and maintainance: it has a simple syntax that could make a huge impact, and also new changes could be atomic (in the sense that adding or removing a selector could be done without refactoring previous code).
- Improvement of bandwidth: the style sheets will be stored in the browser cache and they can be used on multiple pages, without having to download again.

### 3. What are the limitations of CSS?

- Browser Compatibility: some style selectors are supported and some are not. See: https://caniuse.com
- Cross Browser issue: some selectors behave differently in a different browser (IE and Opera support CSS as different logic). I remember having problems with the outline (for the focus ring), floating elements, or the transform property.
- Ascending by selectors is not possible.
- No expressions.
- Pseudo-class not controlled by dynamic behavior.
- Rules, styles, targeting specific text not possible.

### 4. How to add CSS to a HTML file?

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

### 5. Which type of CSS addition has the highest priority?

- **Inline has the highest priority**. It overrides the other styles.
- **Internal or Embedded stands second** in the priority list and overrides the styles in the external style sheet.
- **External style sheets have the least priority**. If there are no styles defined either in the inline or internal style sheet then external style sheet rules are applied for the HTML tags.

### 6. What is the Box model?

The Box model is used to define the design and layout of CSS elements. The web browser renders every element as a rectangular box according to the CSS box model. Its elements are:

- **Margin**: it is the area surrounding the border. It is transparent.
- **Border**: it is the area between the box’s padding and margin.
- **Padding**: it is the space around the content area and within the border box. It is transparent.
- **Content**: it represents the content like text, images or other media content.

### 7. What is the "block" box model?

The `display: block` elements make a whole new box to work on. It breaks the flow of the elements and will take up as much space as it can. This model is vertically biased.

### 8. What is the "inline" box model?

The `display: inline` elements stay inline with its neghboring content. Things like a span would render imperceptable to the user because it stays within the content. This model is horizontally biased.

### 9. What is the "inline-block" box model?

This property takes the benefits of both block and inline-level elements.

Syntax: `.box { display: inline-block; }`

- You will be able to apply `width` and `height` to elements, which we cannot do with inline elements.
- You can also place those elements side by side, which we cannot do with block-level elements.

### 10. What is the "flex" and "inline-flex" box model?

**Flex**

It is also called a `flexible box model`. It is a layout model that provides an easy and clean way to arrange items within a container. Flexbox was created for small-scale layouts. It is responsive and mobile-friendly.

Syntax: `.main-container { display: flex; }`

Flex Properties:

- flex-direction
- flex-wrap
- flex-flow
- justify-content
- align-items
- align-content

**Inline-Flex**

This property makes the flex container as an inline-level flex element. The container takes the necessary space as large as its children.

Syntax: `.main-container { display: inline-flex; }`

### 11. What is the "grid" box model?

It is a CSS property that offers a grid-based layout system, with rows and columns, making it easier to design web pages without floats and positioning. It is a 2-dimensional system, meaning it can handle both columns and rows, unlike flexbox which is largely a 1-dimensional system.

<a name="intermediate"/>

## INTERMEDIATE

### 12. What is the difference between flexbox and grid?

1. **Dimension**: Flexbox si one-dimensional (it only deals with either columns or rows) while Grid is two-dimensional (it allows flexible widths as a unit of length).
2. **Features**: Flexbox can push content element to extreme alignment while Grid can flex combination of items through space-occupying.
3. **Support Type**: Flexbox is "Content First" while Grid is "Layout First".

### 13. What is a CSS selector?

A CSS selector is the part of a CSS ruleset that actually selects the content you want to style.

### 14. What is the Universal Selector?

The universal selector works like a wildcard character, selecting all elements on a page. Syntax:

```
* {
  color: "green";
}
```

### 15. What is the Element Type Selector?

This selector matches one or more HTML elements of the same name. Syntax:

  ```
  ul {
    background: #FFF;
  }
  ```

### 16. What is the ID Selector?

This selector matches any HTML element that has an ID attribute with the same value as that of the selector. Syntax:

  ```
  // CSS
  #container {
    width: 960px;
    margin: 0 auto;
  }

  // HTML
  <div id="container"></div>
  ```

### 17. What is the Class Selector?

The class selector also matches all elements on the page that have their class attribute set to the same value as the class. Syntax:

  ```
  // CSS
  .box {
    padding: 10px;
    margin: 10px;
    width: 240px;
  }

  // HTML
  <div class="box"></div>
  ```

### 18. What is the Descendant Combinator?

The descendant selector or, more accurately, the descendant combinator lets you combine two or more selectors so you can be more specific in your selection method.

  ```
  #container .box {
    color: blue;
  }

  <div id="container">
    <div class="box"></div>
    <div class="box-2"></div>
  </div>
  ```

This declaration block will apply to all elements that have a class of box that is inside an element with an ID of the container.

### 19. What is the Child combinator?

It only targets immediate child elements.

  ```
  #container > .box {
    color: blue;
  }

  <div id="container">
    <div class="box">It is affected.</div>

    <div>
      <div class="box">It is not affected.</div>
    </div>
  </div>
  ```

### 20. What is the General Sibling Combinator?

It matches elements based on sibling relationships. The selected elements are beside each other in the HTML.

  ```
  h2 ~ p {
    margin-bottom: 20px;
  }

  <h2>Title</h2>
  <p>Paragraph example.</p>
  <p>Paragraph example.</p>
  <p>Paragraph example.</p>
  <div class=”box”>
    <p>Paragraph example.</p>
  </div>
  ```

In this example, all paragraph elements `(<p>)` will be styled with the specified rules, but only if they are siblings of `<h2>` elements. There could be other elements in between the `<h2>` and `<p>`, and the styles would still apply.

### 21. What is the Adjacent Sibling Combinator?

It uses the plus symbol `(+)`, and is almost the same as the general sibling selector. The difference is that the targeted element must be an immediate sibling, not just a general sibling.

  ```
  p + p {
    background: red;
  }

  <h2>Title</h2>
  <p>Not styled.</p>
  <p>Styled.</p>
  <p>Styled.</p>

  <div class=”box”>
    <p>Not styled.</p>
    <p>Styled.</p>
  </div>
  ```

### 22. What is the Attribute Selector?

It targets elements based on the presence or value of HTML attributes, and is declared using square brackets.

  ```
  input[type="text"] {
    outline: 1px solid blue;
  }

  <input type="text">
  ```
  - 16. What is the ID Selector?

<a name="advanced"/>

## ADVANCED

### 23. What is a CSS framework?

It is a preplanned library that contains several CSS stylesheets ready for use by web developers and designers.

### 24. Name some CSS frameworks

The frequently used CSS frameworks are:

- Bootstrap
- Foundation
- Bulma
- Semantic UI
- Tailwind
- Ulkit

### 25. Why use CSS frameworks?

- Speeds up the development.
- Enables cross-browser functionality.
- Enforces good web design habits.
- Gives clean and symmetrical layouts.
- Make a styling workflow productive, clean, and maintainable.

### 26. Bootstrap, Bulma, Foundation and Materialize

**Bootstrap**

- Pros:
  - Responsiveness.
  - Consistent & Flexible.
  - HTML, CSS, and JS framework.
  - Customizable.
  - Large Community.
  - Excellent Documentation.
  - MIT License, therefore it is free to use and free to distribute.
- Cons:
  - Javascript is tied to jQuery.
- Ideal for:
  - CSS beginners.
  - A developer with little JS knowledge can use Bootstrap components without writing a line in JS.

**Bulma**

- Pros:
  - Lightweight.
  - Easy to Use.
  - Responsive Design.
  - Based on Flexbox.
  - Highly customizable and modularizable.
  - Simple syntax.
- Cons:
  - Community support is limited.
  - Less documentation.
  - Less flexibility.
  - Limited browser support.
- Ideal For:
  - From beginner to pro, any developer can use it due to its simplicity.

**Foundation**

- Pros:
  - Device agnostic.
  - Responsive.
  - Easy to use.
  - Modern Look.
  - Customizable.
  - Good Documentation.
- Cons:
  - Limited browser support.
  - Heavy/large.
- Ideal For:
  - Professional, highly skilled developers and designers whose aim is to create a unique website and who wants to customize the framework.

**Materialize**

- Pros:
  - Flexible Grids.
  - Offers the finest of the customization abilities.
  - Possess a robust grid system.
  - Supports the rapid development of projects.
  - Contains a set of templates and readily available codes.
  - Offers services for sites as well as emails.
  - JS & jQuery both version available.
- Cons:
  - Community support is limited.
  - Complexity in customization.
  - Modification of code is tough.
- Ideal For:
  - It is accessible to everyone and easy to pick up quickly.

### 27. What is a CSS Preprocessor?

It is a tool that extends the functionality of vanilla CSS through its own scripting language. It helps us to use complex logical syntax like variables, functions, mixins, code nesting, and inheritance, among others.

### 28. Sass

"Syntactically Awesome Style Sheets" can be written in two different syntaxes using SASS or SCSS.

### 29. Sass VS Scss

- **Syntax**: "SCSS" is the first syntax, and it uses the extension of `.scss`. "SASS" is the other syntax, and it uses the extension of `.sass`.
- **CSS compatibility**: SCSS is fully CSS compatible. It provides CSS-friendly syntax to closing the gap between SASS and CSS. SCSS is called Sassy CSS. You can covert the valid CSS document into SASS by simply changing the extension from `.css` to `.scss`.

### 30. Less

**Leaner Style Sheet** is dynamic in nature and efficiently enables customization and reusability. It supports cross-browser friendly. It is JavaScript-based and has very precise error reporting along with indicating the exact location of the error.

### 31. Sass VS Less

- **Syntax**: little differences.
- **Features**: similar behavior since both allow to use complex logic in CSS via variables, mixins, and so on.
- **Error log**: *Less* is more precise about error reporting with an indication of the location of the error.

### 32. Stylus

It was launched in 2010 by former Node JS developer TJ Holowaychuk, nearly 4 years after the release of Sass and 1 year after the release of LESS. The stylus is written Node JS and fits perfectly with JS stack. The idea is to have **the logical power of Sass and the simplicity of Less**.

### 33. Sass VS Less VS Stylus

All three CSS pre-processors considered in this article are mostly capable of the same things at their core and really just go about implementation and syntax differently.

- **Sass** permit advanced logic and algorithms and allow us to write custom functions. It also has the largest adoption and an active community.
- **Less** has the fewest features and logic-based functionality, but it compiles very easily on the front-end hence it thrives on serverless architectures. It has a flexible syntax and more adoption than Stylus.
- **Stylus** has a highly concise and flexible syntax and easily integrates with Node projects. Another advantage is its powerful built-in functions and is capable of handling heavy computing.
