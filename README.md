# HTML:

1. Head & Meta tag uses?
- The head tag in HTML is used to contain metadata and settings for the web page — information that is not displayed directly on the page but is essential for the browser and other services.
<hr>

2. Whats viewport?
- It is usefull for responsiveness. Without viewport browser will be default to 980 px for all devices?
<hr>

3. Meta tag use?
- It contains meta data about the webpage. It has decsiption, keyword and viewport.
- description: contains desc of website
- keyword: contains comma seperated tags
- viewport: for responsiveness.
<hr>

4. How to make site seo friendly?
- Use semantic HTML5 elements like <article>, <header>, <footer>, <nav> for better crawlability.
- Ensure fast loading and mobile-friendliness (impacts SEO).
- Use proper heading tags (h1, h2...) with keywords.
<hr>

5. New tags in html5?
- header, footer, nav, article, section, address etc.
- Also, new input types in HTML5: email, url, tel, range, color, date, time, search, etc.
<hr>

6. What is sementic tags in html?
- This are html 5 tags only. Like above.
- Eg: its like a lable in a story book which makes reader or search engine understand what picture is doing what.
- It makes crawlers and web browser understand site better and rank it better.
- A site can be made without using sementic tags like:
```html
<div class="header"></div>
````
<hr>

7. What are HTML Attributes?
8. What is a marquee in HTML?
9. Define the list types in HTML.
10. How do you align list elements in an HTML file?
11. What is an element in HTML? Difference in element and tag?
12. What are void elements in HTML? What is self closing tags?
13. What is white space in HTML?
14. What is the difference between “display: none” and “visibility: hidden” when used as attributes to the HTML element?
- Elements with “display: none” are not visible and do not take up any space on the page, while elements with “visibility: hidden” are not visible but still take up space.
<hr>

15. What is the difference between link tag link and anchor tag a?
- The link tag links external resources, such as CSS stylesheets, to an HTML document. The a tag creates links to other pages or resources within the same document.
<hr>

16. When to use scripts in the head and when to use scripts in the body?
- When the page is not loaded then use it in head else use it at end of body after thr dom is loaded fully(best practice). 
<hr>

17. What are inline and block elements in HTML5?
18. What is the difference between <figure> tag and <img> tag?
- figure tag to primarily group related content, such as an image and its caption or a code block and description. Examples of this type of material include diagrams, pictures, codes, and illustrations.
<hr>

19. Storage in html? Session and local
- SessionStorage stores data only for the current session. The data is deleted when the tab or window is closed; local storage stores data with no expiration date and persists until deleted. Thus, LocalStorage stores data with no expiration time, while SessionStorage only retains data for the duration of the page session.
```text
# Session Storage
sessionStorage.setItem("username", "Alice");

const user = sessionStorage.getItem("username");
console.log(user); // "Alice"

# Local Storage
// Save data
localStorage.setItem("username", "Alice");

// Get data
let user = localStorage.getItem("username"); // "Alice"

// Remove data
localStorage.removeItem("username");

// Clear all data
localStorage.clear();
```
<hr>

20. How can we include audio or video in a webpage?
- Using audio and video tag.
```html
<audio controls>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

Same with video
```
<hr>

30. Create Draggable image in html5?
- Using draggable = "true"
<hr>

31. What are the different approaches to making an image responsive?
- CSS: Set the CSS width attribute to 100% and the height to auto if you want the picture to respond by scaling up and down.
<hr>

32. 








