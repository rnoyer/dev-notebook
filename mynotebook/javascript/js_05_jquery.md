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
### Manipulating CSS elements
```js
// Getting CSS property
$("h1").css("font-size")
// Setting CSS property
$("h1").css("color","red")
```
### Manipulating classes
```js
// Set a class to an element
$("h1").addClass("my-Class another-Class")
// Unset a class to an element
$("h1").removeClass("my-Class")
// Query if an element has a specific class
$("h1").hasClass("myClass"); // will return a boolean
```
### Manipulating text
```js
// Set text
$("h1").text("hello")
// Get text
$("h1").text()

// equivalent of innerHtml (also interpret html tags)
$("h1").text("<em>hello</em>")
```
### Manipulating attributes
```js
// Set attribute
$("a").attr("href", "http://www.yahoo.com")
$("a").attr("class", "my-Class") // also works with classes, as it is a regular attribute.

// Get attributes
$("a").attr("href")
```
### Manipulating event listeners
There is two way to set event listeners
```js
$("h1").click(() => {
  $("h1").text("clicked!")
})
```
```js
// Here a more concise way, and close to JS. 'on' method takes 2 parameters: the event type (click, mouseover, etc.) and the function to execute.
$("h1").on("click",() => {
  $("h1").text("clicked!")
})
```
### Add/remove HTML elements
There is four positional method :
- before / after:  Place the new element next to the selected element
- prepend / append: Place the new element **inside** the selected one, before or after its content.

```js
// Add element before another one
$("h1").before("<button>surprise!</button")

//remove element
$("h1").remove()
```