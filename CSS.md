# CSS

## TABLE OF CONTENTS

- [Concepts](#concepts)
  - What is CSS?
  - What are the advantages of using CSS?
  - What are the limitations of CSS?
  - How to add CSS to a HTML file?
  - Which type of CSS addition has the highest priority?
  - What is the Box model?
- [Selectors](#selectors)
  - Universal Selector
  - Element Type Selector
  - ID Selector
  - Class Selector
  - Descendant Combinator
  - Child combinator
  - General Sibling Combinator
  - Adjacent Sibling Combinator
  - Attribute Selector
- [Frameworks](#frameworks)
   - What is a CSS framework?
   - Name some CSS frameworks
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

### Which type of CSS addition has the highest priority?

- **Inline has the highest priority**. It overrides the other styles.
- **Internal or Embedded stands second** in the priority list and overrides the styles in the external style sheet.
- **External style sheets have the least priority**. If there are no styles defined either in the inline or internal style sheet then external style sheet rules are applied for the HTML tags.

### What is the Box model?

The Box model is used to define the design and layout of CSS elements. The web browser renders every element as a rectangular box according to the CSS box model. Its elements are:

- **Margin**: it is the area surrounding the border. It is transparent.
- **Border**: it is the area between the box’s padding and margin.
- **Padding**: it is the space around the content area and within the border box. It is transparent.
- **Content**: it represents the content like text, images or other media content.

<a name="frameworks"/>

## Selectors

A CSS selector is the part of a CSS ruleset that actually selects the content you want to style.

### Universal Selector

The universal selector works like a wildcard character, selecting all elements on a page. Syntax:

```
* {
  color: "green";
}
```

### Element Type Selector

This selector matches one or more HTML elements of the same name. Syntax:

```
ul {
  background: #FFF;
}
```

### ID Selector

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

### Class Selector

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

### Descendant Combinator

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

### Child Combinator

It only targets immediate child elements.

```
#container> .box {
	color: blue;
}

<div id="container">
	<div class="box">It is affected.</div>
	
	<div>
		<div class="box">It is not affected.</div>
	</div>
</div>
```

### General Sibling Combinator

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

In this example, all paragraph elements (<p>) will be styled with the specified rules, but only if they are siblings of <h2> elements. There could be other elements in between the <h2> and <p>, and the styles would still apply.

### Adjacent Sibling Combinator

It uses the plus symbol (+), and is almost the same as the general sibling selector. The difference is that the targeted element must be an immediate sibling, not just a general sibling.

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

### Attribute Selector

It targets elements based on the presence or value of HTML attributes, and is declared using square brackets.

```
input[type="text"] {
	outline: 1px solid blue;
}

<input type="text">
```

<a name="frameworks"/>

## Frameworks

### What is a CSS framework?

It is a preplanned library that contains several CSS stylesheets ready for use by web developers and designers.

### Name some CSS frameworks

The frequently used CSS frameworks are:

- Bootstrap
- Foundation
- Bulma
- Semantic UI
- Tailwind
- Ulkit

<a name="preprocessors"/>

## Preprocessors

### What is a CSS Preprocessor?

It is a tool that extends the functionality of vanilla CSS through its own scripting language. It helps us to use complex logical syntax like variables, functions, mixins, code nesting, and inheritance, among others.

### Sass

"Syntactically Awesome Style Sheets" can be written in two different syntaxes using SASS or SCSS.

### Less

complete

### Stylus

complete

### Why to use them?

complete

### Sass VS Scss

- **Syntax**: "SCSS" is the first syntax, and it uses the extension of `.scss`. "SASS" is the other syntax, and it uses the extension of `.sass`.
- **CSS compatibility**: SCSS is fully CSS compatible. It provides CSS-friendly syntax to closing the gap between SASS and CSS. SCSS is called Sassy CSS. You can covert the valid CSS document into SASS by simply changing the extension from `.css` to `.scss`.
