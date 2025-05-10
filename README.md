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

# CSS

<hr />

1. Position, Difference in relative and absolute?
- Relative: Stay where you are normally, but now I can move you a little bit with top, left, right, or bottom.
- Absoulte: Forget where you were supposed to be. Go exactly here, using top, left, right, or bottom — and find the nearest ancestor that has a position set. In above code i gave absolute to my parent div so now it'll take position from that parent. That parent position can be sticky, fixed, relative or absolute.
- Fixed: It'll fixed to the screen even when we scroll.
- Sticky: It'll stick to screen when we scroll to that div, from that it'll be sticky. Important: we must give top in this case.
- Inherit: it just inherits whatever the parent has
- Static: default 
```html
<style>
    .parent{
      border: 1px solid red;
      background-color: cyan;
      padding: 10px;
      /* position: sticky; */
      margin-top: 50px;
      height: 6000px;
    } 
    .box1 {
      position: relative;
      top: 0;
      border: 1px solid red;
      background-color: lightgreen;
      padding: 20px;
    }
    .box2 {
      border: 1px solid red;
      background-color: lightyellow;
      padding: 20px;
    }
    .box3 {
      border: 1px solid red;
      background-color: lightpink;
      padding: 20px;
    }
    .box4 {
      border: 1px solid red;
      background-color: lightgray;
      padding: 20px;
    }
  </style>

  <div class="parent">
    <div class="box1">Box 1</div>
    <div class="box2">Box 2</div>
    <div class="box3">Box 3</div>
    <div class="box4">Box 4</div>
  </div>
```
<hr />

2. What is z-index in css:
- To overlap elements with one another like if box2 should be over box1 then use z-index.
- To make z-index work we need to make position relative. Also give top and left right.
- By default box 1 is on top of box 2, to make box 2 on top use z-index and position on both style of boxes.
```html
.box1 {
      position: relative;
      top: 20px;
      border: 1px solid red;
      background-color: lightgreen;
      padding: 20px;
      z-index: 0;
    }
    .box2 {
      position: relative;
      border: 1px solid red;
      background-color: lightyellow;
      padding: 20px;
      z-index: 2;
    }
```
<hr />

3. min and max in media query?
```css
@media (min-width: 600px) {
  /* if style reached 600 and more apply given style */
  background-color: red;
}

@media (max-width: 600px) {
  /* if style reached 600 and below apply given style */
  background-color: cyan;
}
```
<hr />

4. Bootstrap grid. Explain bootstrap follows mobile first approach?
```html
<div class="row">
  <div class="col-lg-4">text</div>
  <div class="col-lg-4">text</div>
  <div class="col-lg-4">text</div>
</div>
```
- Bootstrap grid follows min approch for all except extra small.
- In above eg: if the screen size is 992px and more then follow style.
- Bootstrap follows mobile first approacch, that means it'll be col-12 if the col is not defined.
- In above example i have given 4 cols for lg only so for lg till end it'll be col-4 below lg screen size it'll be col-12 
<hr />

5. If we give only col and no screen size?
- If we give only col and no screen size, it'll follow same size for each screen.
```html
<div class="row">
  <div class="col-4">text</div>
  <div class="col-4">text</div>
  <div class="col-4">text</div>
</div>
```
- It'll be col-12 for each screen
<hr />

5. If we give lg and md both?
```html
<div class="row">
  <div class="col-lg-4 col-md-6" style="background-color: aliceblue; padding: 10px; border: 1px solid black;">text</div>
  <div class="col-lg-4 col-md-6" style="background-color: aliceblue; padding: 10px; border: 1px solid black;">text</div>
  <div class="col-lg-4 col-md-6" style="background-color: aliceblue; padding: 10px; border: 1px solid black;">text</div>
</div>
```
- For large screen it'll be 4 cols i.e 992 till end
- For medium screen it'll be 6 cols i.e 768 till end i.e till 991. From 768 - 991 it'll be md.
<hr />

6. Gutter?
- In bootstrap for gutter to work, we need inner div inside col.
<hr />

7. Pseudo-classes?
- :hover`, `:focus`, `:nth-child`, `:first-child`, `:last-child`
```html
button:hover {
  background-color: blue;
  color: white;
}

li:first-child {
  font-weight: bold;
}

li:nth-child(2) {
  font-weight: bold;
}
```
<hr />

8. Pseudo-elements
- ::before, ::after
- We must give content when working with this elements.
- Like a line below the text using just 
- It inserts content before the actual content inside an element.
- It doesn't exist in your HTML; it’s created with CSS.
- You must use the content property for it to work.
- Likewise for after.
- Eg: Like we want to give underline below the content 
- Simple example:
```html
button::before {
  content: "";
}
```
- To give vertical line before the element.
```html
button::before {
  content: "";
  height: 2px;
  position: relative;
  margin-top: 5px;
  border: 1px solid black;
}
```
<hr />

9. What is object-fit and object-position?
- object-fit controls how an image (or video) fits inside its container when the image's size and the container's size don't match.
```html
img {
  width: 200px;
  height: 300px;
  object-fit: cover;
  object-position: top right;
}
```
- when image is cropped focus on top right part of the image.
<hr />

10. Backdrop-filter?
- Like we have in bootstrap modal, background effect.

11. Difference in css & scss?
- SCSS is great when your project is growing, and you want consistent styling, reusability, and easier maintenance.
- A CSS preprocessor: you write in SCSS, and it gets compiled into CSS.
- Adds powerful features not in regular CSS like:
<ul>
  <li>Variables</li>
  <li>Nesting</li>
  <li>Mixins</li>
  <li>Functions</li>
  <li>Partials</li>
</ul>
- Variable Eg:
```html
$primary-color: #3498db;
.button {
  background-color: $primary-color;
}
.header {
  border-bottom: 2px solid $primary-color;
}
```
- Nesting Eg:
```html
.card {
  padding: 20px;
  .title {
    font-size: 1.2rem;
  }
}
```
- Mixins Eg:
```html
@mixin flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

.box {
  @include flex-center;
}
```
<hr />

12. Display in css?
- inline, block, inline-block, none, flex, grid
- In normal inline block when we give height and width it wont work but when we give inline-block we can set height and width.
<hr />

13. Display flex, what is justify-content and align-item?
- justify-content: left right
- align-item: top, bottom
```html
.txt {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: red;
  height: 200px;
  width: 200px;
}
```
- If we want to align item each corner use justify-content: space-between.
- If want to change and make it column wise the use flex-direction: column, default is row.
- If there are many cols we can wrape it i.e when there is no space just shift below. Here if we have more than one line, we use align-content: center and so on likewise above.
- Use gap to give gap between contents, column-gap, row-gap: 10px.
<hr />







