# WEB_PERFORMANCE

## TABLE OF CONTENTS

- [BASICS](#basics)
  1. What is Web Performance?
  2. Why is web performance important?
  3. What are the main factors that affect web performance?
  4. What is the Perceived Performance?
  5. What is the Perceived Performance related to?
  6. How could be Perceived Performance improved?
  7. Loading Performance VS Render Performance
  8. What tools do you use to measure web performance?
  9. How do you optimize images for the web?
  10. How do you reduce the size of CSS and JavaScript files?
  11. How do you handle browser caching?
- [INTERMEDIATE](#intermediate)
  12. What is minification and how it can improve web performance?
  13. What is the impact of HTTP requests on web performance?
  14. What is the impact of using third-party scripts on web performance?
  15. Can you explain the concept of lazy loading?
  16. What is the difference between client-side and server-side caching?
  17. What is the role of a Content Delivery Network (CDN) in web performance?
  18. What are the benefits of using a front-end framework for web performance?
  19. How do you handle web page optimization for mobile devices?
  20. What is the role of website analytics in web performance optimization?
  21. What is the role of browser rendering and how does it affect web performance?
  22. What are the best practices for optimizing server-side performance?
- [ADVANCED](#advanced)
  23. How do you diagnose and fix common web performance issues like slow load times or high network latency?
  24. What is the difference between performance and scalability?
  25. How to optimize database performance in a web application?
  26. How to leverage serverless architectures to improve web performance?
  27. What is critical CSS?
  28. What are the benefits and drawbacks of using a microservices architecture?
  29. How to use browser dev tools to improve web performance?
  30. How to use A/B testing to improve web performance?
  31. What is predictive performance?
  32. How to optimize web performance in a multi-lingual or multi-regional website?
  33. How to use machine learning algorithms to optimize web performance?

<a name="basics"/>

## BASICS

### 1. What is Web Performance?

Web performance refers to how quickly site content loads and renders in a web browser, and how well it responds to user interaction.

### 2. Why is web performance important?

A better web performance is related to a better user experience. There is a correlation between speed and success of websites in terms of both revenue and usage.

### 3. What are the main factors that affect web performance?

The size of the page, the number of requests, the type and number of resources, and the server response time, among other factors.

### 4. What is the Perceived Performance?

Perceived performance, also known as user-perceived performance, is a measure of how fast a website feels to users, rather than how fast it actually loads. It refers to the amount of time it takes for a user to perceive that a webpage is loading and become usable.

### 5. What is the Perceived Performance related to?

Perceived performance is influenced by various factors such as the time it takes to render the initial content on the page, the responsiveness of the user interface, and the speed with which interactive elements become available.

### 6. How could be Perceived Performance improved?

To optimize perceived performance, web developers can use techniques such as lazy loading, progressive rendering, and prioritizing the loading of critical resources. These techniques can help ensure that users perceive a website to be loading quickly, even if some resources take longer to load in the background.

### 7. Loading Performance VS Render Performance

There are two parts of web performance: loading and render performance.

**Loading Performance**:

- Refers to how long it takes for a website to load all of its resources.
- Influenced by factors such as the size of the files, the speed of the server, and the user's internet connection.
- Typically measured using metrics such as the time to first byte (TTFB), the time to first paint (TTFP), and the time to interact (TTI).
- Optimized using techniques such as caching, minification, compression, and image optimization.

**Render performance**:

- Refers to how quickly a web page is displayed on the user's screen once the resources have finished loading.
- Influenced by factors such as the complexity of the web page, size and number of images and videos, and efficiency of the browser's rendering engine.
- Typically measured using metrics such as first contentful paint (FCP), first meaningful paint (FMP), and time to visually complete (TVC).
- Optimized using techniques such as image optimization, code splitting, lazy loading, optimize JavaScript and optimizing CSS.

### 8. What tools do you use to measure web performance?

There are various tools to measure web performance. For example: Google PageSpeed Insights, GTmetrix, Pingdom, WebPageTest, and Lighthouse. These tools analyze website speed, performance, and provide recommendations for improvement.

### 9. How do you optimize images for the web?

- Reducing the file size without compromising the quality. This can be achieved by using compression tools such as Adobe Photoshop, Squoosh, or TinyPNG.
- Adjusting image dimensions to the required size.
- Removing unnecessary metadata to reduce the file size.
- Choosing the appropriate image format such as JPEG, PNG, or WebP.
- Using responsive images and lazy loading can further optimize web performance.
