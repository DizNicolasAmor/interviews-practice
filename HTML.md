# HTML

## TABLE OF CONTENTS

- [Basics](#basics)
  - What is HTML5?
  - What are the differences between HTML and HTML5?
  - What are tags in HTML5?
  - What are the most basic tags?
  - What are elements in HTML5?
  - What are attributes in HTML5?
  - Relationship between CSS and HTML5
  - What are most important HTML5 structure elements?
  - What are input elements?
  - What is meant by web storage in HTML5?
  - How do you link to another web page using HTML5?
  - What are the three types of lists in HTML5?
- [Intermediate](#intermediate)
  - What are the key benefits of HTML5?
  - What is the role of formatting tags in HTML5?
  - What types of graphics are supported by HTML5?
  - What is new about the relationship between header and heading tags?
  - What are some of the new input types in HTML5?
  - What are image maps in HTML5?
  - What are the most important APIs in HTML5?
  - What is the role of DOCTYPE in HTML5?
  - What are the different types of storage in HTML5?
  - What is metadata in HTML5 and how is it specified?
  - What are the new tags for multimedia in HTML5?
- [Advanced](#advanced)
  . What is microdata?
  . How is the Geolocation API implemented?
  . What are some of the key global attributes?
  . What is the role of the WebSocket API?
  . When should <div> tags be used?
  . What is the role of the Web Workers API?
  . How can the performance of an HTML5 web page be measured?
  . How can HTML5 web pages be optimized?

<a name="basics"/>

## Basics

### What is HTML5?

HTML5 is a markup language used for structuring and displaying content on the internet. This includes animations, audio, images, and text, among many other things, and all without the need for additional software. HTML5 is the most recent and most advanced version of HTML.

### What are the differences between HTML and HTML5?

- HTML5 supports video, graphics, and audio, whereas HTML only supports them through third-party extensions.
- HTML5 is mobile-friendly, whereas HTML is not.
- HTML5 is compatible with all major web browsers, whereas HTML is not.
- HTML5 offers several options for local storage, whereas HTML only offers cookies.
- HTML5 supports multi-threading, whereas HTML operates only in one thread.

### What are tags in HTML5?

Tags are pieces of HTML5 code used to define the structure of the page. There are more than 100 tags, each one serving a unique purpose.

### What are the most basic tags?

The most basic tags are `<html>`, `<head>`, `<title>`, and `<body>`.

### What are elements in HTML5?

They are components that instruct the web browser how to structure and interpret the HTML5 document. Typically, they encompass an opening tag, a closing tag, and specified content between the opening and closing tags, depending on the type of tag used.

### What are attributes in HTML5?

Attributes are special properties or characteristics used within an element to modify its behavior. Attributes are specified within the opening tag and must be enclosed in quotation marks.

### Relationship between CSS and HTML5

CSS is a style sheet language used with HTML5 to format and display the elements specified by the markup language for the end user. While HTML5 defines the structure of a page, CSS specifies the document’s style.

### What are most important HTML5 structure elements?

- `<header>`, containing the header or top of the page
- `<footer>`, containing the footer or bottom of the page
- `<section>`, containing one section that is thematically similar to other sections
- `<article>`, containing standalone content
- `<nav>`, containing the navigation functionality of the page
- `<aside>`, containing secondary content

### What are input elements?

Input elements are used to create interactive controls that receive and process information from the user.

### What is meant by web storage in HTML5?

Web storage refers to HTML5’s new storage features. Previous HTML versions relied on cookies for storage in the server, but web storage now means data can be stored locally within the user’s browser. Web storage also offers a larger storage limit and is more secure.

### How do you link to another web page using HTML5?

The anchor tag, or `<a>`, is used with the `href` attribute to link to other web pages.

### What are the three types of lists in HTML5?

- **Ordered list**: which is used to group related items in a specific order.
- **Unordered list**: which is used to group related items in no particular order.
- **Description list**: which is used to group terms and their descriptions.

<a name="intermediate"/>

## Intermediate

### What are the key benefits of HTML5?

- Browsers and devices compatibility.
- Cleaner code.
- Native support for multimedia content.
- Quicker load times due to offline storage cache.
- Introduction of geolocation.

### What is the role of formatting tags in HTML5?

Formatting tags allow text to be stylized in HTML5 without the need for CSS. For example:

- `<b>`: makes text bold.
- `<i>`: italicizes text.
- `<u>`: underlines text.
- `<mark>`: highlights text.
- `<strong>`: marks text as important.

### What types of graphics are supported by HTML5?

Unlike previous versions, HTML5 offers inbuilt graphics features:

- **SVG** (Scalable Vector Graphics), used to create vector-based graphics, such as diagrams and icons.
- **Canvas**, used to draw graphics, such as shapes.

### What is new about the relationship between header and heading tags?

The `<header>` tag is used to design the header of a web page and can contain a range of elements including text, logos, or a navigation bar.

The `<h1>` tag is the textual part of the header and is used to specify the most important section of a piece of content. It’s often used alongside other header tags (through to `<h6>`) to format and prioritize content sections.

### What are some of the new input types in HTML5?

- Date.
- Time.
- Email.
- Tel (to enter a telephone number with a specific pattern).
- Range (to select a range of values on a slider).

### What are image maps in HTML5?

Image maps are images with several clickable areas that link to different web pages. They use the <map> and <area> tags. Coordinates are specified to segment the image into different areas and then relevant links are applied.

### What are the most important APIs in HTML5?

- Geolocation API.
- Web Speech API: provides speech recognition functionality.
- Clipboard API: provides copy, cut, and paste functionality.
- History API: provides access to the browser navigation history.
- Web Notifications API: used to send web based notifications to users.

### What is the role of DOCTYPE in HTML5?

All HTML pages (HTML5 included) need to have their document type declared in the first line of code. `DOCTYPE` instructs the browser how to interpret the document by indicating what type and version of markup language are being used.

For HTML5 documents the syntax is: `<!DOCTYPE html>`.

### What are the different types of storage in HTML5?

- **sessionStorage**: temporary storage available for the duration of the page session.
- **localStorage**: permanent storage available until data is deleted by the user.

### What is metadata in HTML5 and how is it specified?

Metadata is data that describes other data. In HTML, it provides additional information about the document, such as the description, author, and keywords. It helps browsers, search engines and other web applications better interpret a document.

The `<meta>` tag is used to define metadata about an HTML document. These tags are always enclosed within the `<head>` of the HTML document.

### What are the new tags for multimedia in HTML5?

HTML5 allows creating multimedia objects without the need for additional plugins. The new tags that facilitate this are:

- `<audio>`: used to embed audio content.
- `<video>`: used to embed video content.
- `<embed>`: used to embed content from an external source.
- `<source>`: used to embed multiple media resources.
- `<track>`: used to specify text tracks (such as subtitles) for audio and video content.

<a name="advanced"/>

## Advanced

### What is microdata?

It allows developers to define the custom semantics of elements. It is created using the `<itemscope>` element. Information about the item is then specified using the `<itemprop>` element.

It’s used to provide browsers and search engines with more information about the contents of the web page.

### How is the Geolocation API implemented?

This API uses the device’s GPS, WiFi or mobile signal to triangulate the user’s latitude and longitude coordinates. The user must give their permission before geolocation services can be used on their device.

From the developer, this API is implemented by calling the geolocation.navigator object.

### What are some of the key global attributes?

Global attributes are attributes that can be applied to all HTML5 elements. Some of the most important global attributes are:

    accesskey, used to specify a keyboard shortcut for an element
    class, used to assign one or more class names to an element
    dir, used to specify the base direction of the element’s text
    data-*, used to store custom data specific to the web page
    contenteditable, used to indicate whether the content is editable or not

### What is the role of the WebSocket API?

It facilitates two-way, interactive communication between the web browser and the web server. This enables a real-time, event-driven data transfer to and from the server.

### When should <div> tags be used?

When no other semantically appropriate element is available. Generally, for styling purposes or structural purposes like wrapping some HTML elements.

### What is the role of the Web Workers API?

The Web Workers API makes it possible to run scripts independently in a background thread, separate from the main execution thread of the HTML5 document. This allows developers to continue working on the page without affecting its performance, while scripts run in the background.

### How can the performance of an HTML5 web page be measured?

Measuring performance is an important step for developers to gauge the competitiveness of their web page and can be achieved using APIs and extensions. Popular solutions include the Navigation Timing API and the User Timing API.

These tools provide insights into specific performance metrics such as:

    Page load speed: The time it takes for the full page to load
    Time to interact: The time it takes for the user to be able to interact with the page
    Bounce rate: The proportion of users that leave the page without interacting with it
    Error rate: The proportion of visits to the page resulting in errors
    Conversion rate: The proportion of users that complete a specified action, such as subscribing to a mailing list

### How can HTML5 web pages be optimized?

If a web page is performing poorly, developers have several HTML5 optimization strategies at their disposal:

    Compress CPU-intensive assets such as high-resolution images
    Bundle code into single files to reduce the number of HTTP requests
    Minify code to remove all unnecessary whitespace
    Offload operations to the Graphics Processing Unit (GPU)
    Use CSS3 for animations and transitions
