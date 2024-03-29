# HTML

## TABLE OF CONTENTS

- [Basics](#basics)
  - 1 What is HTML5?
  - 2 What are the differences between HTML and HTML5?
  - 3 What are tags in HTML5?
  - 4 What are elements in HTML5?
  - 5 What are attributes in HTML5?
  - 6 Relationship between CSS and HTML5
  - 7 What are most important HTML5 structure elements?
  - 8 What are input elements?
  - 9 What is meant by web storage in HTML5?
  - 10 How do you link to another web page using HTML5?
  - 11 What are the three types of lists in HTML5?
- [Intermediate](#intermediate)
  - 12 What is Semantic HTML?
  - 13 What are the key benefits of HTML5?
  - 14 What is the role of formatting tags in HTML5?
  - 15 What types of graphics are supported by HTML5?
  - 16 What is new about the relationship between header and heading tags?
  - 17 What are some of the new input types in HTML5?
  - 18 What are image maps in HTML5?
  - 19 What are the most important APIs in HTML5?
  - 20 What is the role of DOCTYPE in HTML5?
  - 21 What are the different types of storage in HTML5?
  - 22 What is metadata in HTML5 and how is it specified?
- [Advanced](#advanced)
  - 23 What are the new tags for multimedia in HTML5?
  - 24 What is microdata?
  - 25 How is the Geolocation API implemented?
  - 26 What are global attributes?
  - 27 What is the role of the WebSocket API?
  - 28 When should `<div>` tags be used?
  - 29 What is the role of the Web Workers API?
  - 30 How can the performance of an HTML5 web page be measured?
  - 31 How can HTML5 web pages be optimized?
  - 32 Explain the concept of "shadow DOM" in the context of web components.
  - 33 How does shadow DOM encapsulation work?

<a name="basics"/>

## Basics

### 1. What is HTML5?

HTML5 is a markup language used for structuring and displaying content on the internet. This includes animations, audio, images, and text, among many other things, and all without the need for additional software. HTML5 is the most recent and most advanced version of HTML.

### 2. What are the differences between HTML and HTML5?

- HTML5 supports video, graphics, and audio, whereas HTML only supports them through third-party extensions.
- HTML5 is mobile-friendly, whereas HTML is not.
- HTML5 is compatible with all major web browsers, whereas HTML is not.
- HTML5 offers several options for local storage, whereas HTML only offers cookies.
- HTML5 supports multi-threading, whereas HTML operates only in one thread.

### 3. What are tags in HTML5?

Tags are pieces of HTML5 code used to define the structure of the page. There are more than 100 tags, each one serving a unique purpose.

The most basic tags are `<html>`, `<head>`, `<title>`, and `<body>`.

### 4. What are elements in HTML5?

They are components that instruct the web browser how to structure and interpret the HTML5 document. Typically, they encompass an opening tag, a closing tag, and specified content between the opening and closing tags, depending on the type of tag used.

### 5. What are attributes in HTML5?

Attributes are special properties or characteristics used within an element to modify its behavior. Attributes are specified within the opening tag and must be enclosed in quotation marks.

### 6. Relationship between CSS and HTML5

CSS is a style sheet language used with HTML5 to format and display the elements specified by the markup language for the end user. While HTML5 defines the structure of a page, CSS specifies the document’s style.

### 7. What are most important HTML5 structure elements?

- `<header>`, containing the header or top of the page
- `<footer>`, containing the footer or bottom of the page
- `<section>`, containing one section that is thematically similar to other sections
- `<article>`, containing standalone content
- `<nav>`, containing the navigation functionality of the page
- `<aside>`, containing secondary content

### 8. What are input elements?

Input elements are used to create interactive controls that receive and process information from the user.

### 9. What is meant by web storage in HTML5?

Web storage refers to HTML5’s new storage features. Previous HTML versions relied on cookies for storage in the server, but web storage now means data can be stored locally within the user’s browser. Web storage also offers a larger storage limit and is more secure.

### 10. How do you link to another web page using HTML5?

The anchor tag, or `<a>`, is used with the `href` attribute to link to other web pages.

### 11. What are the three types of lists in HTML5?

- **Ordered list**: which is used to group related items in a specific order.
- **Unordered list**: which is used to group related items in no particular order.
- **Description list**: which is used to group terms and their descriptions.

<a name="intermediate"/>

## Intermediate

### 12. What is Semantic HTML?

Semantic HTML refers to syntax that makes the HTML more comprehensible by better defining the different sections and layout of web pages. It makes web pages more informative and adaptable, allowing browsers and search engines to better interpret content.

It is also good for a11y since Screen Readers respond to that good practices. Consider structural navigation (an a11y user could navigate throw the structue page).

The following HTML tags are examples of Semantics: `<header>`, `<nav>`, `<section>`, `<article>`, `<aside>`, `<footer>`.

### 13. What are the key benefits of HTML5?

- Browsers and devices compatibility.
- Cleaner code.
- Native support for multimedia content.
- Quicker load times due to offline storage cache.
- Introduction of geolocation.

### 14. What is the role of formatting tags in HTML5?

Formatting tags allow text to be stylized in HTML5 without the need for CSS. For example:

- `<b>`: makes text bold.
- `<i>`: italicizes text.
- `<u>`: underlines text.
- `<mark>`: highlights text.
- `<strong>`: marks text as important.

### 15. What types of graphics are supported by HTML5?

Unlike previous versions, HTML5 offers inbuilt graphics features:

- **SVG** (Scalable Vector Graphics), used to create vector-based graphics, such as diagrams and icons.
- **Canvas**, used to draw graphics, such as shapes.

### 16. What is new about the relationship between header and heading tags?

The `<header>` tag is used to design the header of a web page and can contain a range of elements including text, logos, or a navigation bar.

The `<h1>` tag is the textual part of the header and is used to specify the most important section of a piece of content. It’s often used alongside other header tags (through to `<h6>`) to format and prioritize content sections.

### 17. What are some of the new input types in HTML5?

- Date.
- Time.
- Email.
- Tel (to enter a telephone number with a specific pattern).
- Range (to select a range of values on a slider).

### 18. What are image maps in HTML5?

Image maps are images with several clickable areas that link to different web pages. They use the `<map>` and `<area>` tags. Coordinates are specified to segment the image into different areas and then relevant links are applied.

### 19. What are the most important APIs in HTML5?

- Geolocation API.
- Web Speech API: provides speech recognition functionality.
- Clipboard API: provides copy, cut, and paste functionality.
- History API: provides access to the browser navigation history.
- Web Notifications API: used to send web based notifications to users.

### 20. What is the role of DOCTYPE in HTML5?

All HTML pages (HTML5 included) need to have their document type declared in the first line of code. `DOCTYPE` instructs the browser how to interpret the document by indicating what type and version of markup language are being used.

For HTML5 documents the syntax is: `<!DOCTYPE html>`.

### 21. What are the different types of storage in HTML5?

- **sessionStorage**: temporary storage available for the duration of the page session.
- **localStorage**: permanent storage available until data is deleted by the user.

### 22. What is metadata in HTML5 and how is it specified?

Metadata is data that describes other data. In HTML, it provides additional information about the document, such as the description, author, and keywords. It helps browsers, search engines and other web applications better interpret a document.

The `<meta>` tag is used to define metadata about an HTML document. These tags are always enclosed within the `<head>` of the HTML document.

<a name="advanced"/>

## Advanced

### 23. What are the new tags for multimedia in HTML5?

HTML5 allows creating multimedia objects without the need for additional plugins. The new tags that facilitate this are:

- `<audio>`: used to embed audio content.
- `<video>`: used to embed video content.
- `<embed>`: used to embed content from an external source.
- `<source>`: used to embed multiple media resources.
- `<track>`: used to specify text tracks (such as subtitles) for audio and video content.

### 24. What is microdata?

It allows developers to define the custom semantics of elements. It is created using the `<itemscope>` element. Information about the item is then specified using the `<itemprop>` element.

It’s used to provide browsers and search engines with more information about the contents of the web page.

### 25. How is the Geolocation API implemented?

This API uses the device’s GPS, WiFi or mobile signal to triangulate the user’s latitude and longitude coordinates. The user must give their permission before geolocation services can be used on their device.

From the developer, this API is implemented by calling the geolocation.navigator object.

### 26. What are global attributes?

They are attributes that can be applied to all HTML5 elements, such as:

- **accesskey**: used to specify a keyboard shortcut for an element.
- **class**: used to assign one or more class names to an element.
- **dir**: used to specify the base direction of the element’s text.
- **data-**: used to store custom data specific to the web page.
- **contenteditable**:, used to indicate whether the content is editable or not.

### 27. What is the role of the WebSocket API?

It facilitates two-way, interactive communication between the web browser and the web server. This enables a real-time, event-driven data transfer to and from the server.

### 28. When should `<div>` tags be used?

When no other semantically appropriate element is available. Generally, for styling purposes or structural purposes like wrapping some HTML elements.

### 29. What is the role of the Web Workers API?

It allows to run scripts independently in a background thread, separate from the main execution thread of the HTML5 document.

### 30. How can the performance of an HTML5 web page be measured?

Using the **Navigation Timing API** and the **User Timing API**. They provide insights about:

- Page load speed.
- Time to interact.
- Bounce rate: the proportion of users that leave the page without interacting with it.
- Error rate: the proportion of visits to the page resulting in errors.
- Conversion rate: the proportion of users that complete a specified action, such as subscribing to a mailing list.

### 31. How can HTML5 web pages be optimized?

- Compress heavy assets such as high-resolution images.
- Bundle code into single files to reduce the number of HTTP requests.
- Minify code to remove all unnecessary whitespace.
- Offload operations to the Graphics Processing Unit (GPU).
- Use CSS3 for animations and transitions.

### 32. Explain the concept of "shadow DOM" in the context of web components.

The "shadow DOM" is a fundamental concept that enables the encapsulation of HTML, CSS, and JavaScript within a custom element. It creates a scoped and isolated subtree where the component's internals are hidden from the outside document. This encapsulation is crucial for avoiding style and naming conflicts and allows developers to build self-contained and reusable components that don't interfere with the rest of the page.

### 33. How does shadow DOM encapsulation work?

It works by creating a separate, isolated DOM subtree within a custom element. It shields the component's internal structure, preventing styles and elements within the shadow DOM from affecting the outer document, and vice versa. This isolation is achieved through the use of shadow DOM selectors and CSS encapsulation, making it challenging for external styles or scripts to interfere with the component's behavior.
