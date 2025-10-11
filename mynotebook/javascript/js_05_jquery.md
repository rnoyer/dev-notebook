# jQuery
Most popular JS library mainly used to shorten code, when it comes to manipulating DOM.

## Basics

### Selecting elements
The sign `$` replace `document.querySelector` and `document.querySelectorAll`
```js
// without jQuery
document.querySelector("h1")
// with jQuery
$("h1")

// without jQuery
document.querySelectorAll("button")
// with jQuery
$("button")
```
```js
// Getting CSS property
$("h1").css("font-size")
// Setting CSS property
$("h1").css("color","red")
```
```js
// Set a class to an element
$("h1").addClass("my-Class another-Class")
// Unset a class to an element
$("h1").removeClass("my-Class")
// Query if an element has a specific class
$("h1").hasClass("myClass"); // will return a boolean
```
```js
// Add text
$("h1").text("hello")

// equivalent of innerHtml (also interpret html tags)
$("h1").text("<em>hello</em>")
```
