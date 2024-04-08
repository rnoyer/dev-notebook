# DOM: Document Object Model

## Introduction
Inserting javascript code into a webpage can be done in 3 differents ways, just like CSS: Inline, Internal or External.

### Inline JS
```html
<body onload="alert('Some JS here');">
  <h1>Hello</h1>
</body>
```

### Internal JS
```html
<body>
  <h1>Hello</h1>
  <script type="text/javascript">
    alert("Some JS here");
  </script>
</body>
```
### External JS
```js
alert("Some JS here");
```
```html
<body>
  <h1>Hello</h1>
  <script src="#" charset="utf-8"></script>
</body>
```

## Manipulate DOM

```js
var head = document.firstElementChild;
head.innerHTML = "foo";
head.style.color = "red";
```

### Retrieve DOM element
```js
document.getElementsByTagName("li")[0];
document.getElementsByClassName("htmlClass")[0];
document.getElementById("title");

document.querySelector("input").click();
document.querySelectorAll("input")[0].click();

document.firstElementChild;
document.firstElementChild.firstElementChild;
document.lastElementChild;

```
### Set attributes and classes

- Set attributes
There's 2 ways to set attributes :
```js
// Using setAttribute method : allow to set HTML attributes as well as customs attributes
myDOMElement.setAttribute("attributeName", "attributeValue");

// Adding any HTML attribute as a parameter
myDOMElement.attributeName= "attributeValue";

```

- Set Classes
```js
document.querySelector("h1").classList.add("huge");
document.querySelector("h1").classList.remove("huge");
document.querySelector("h1").classList.toggle("huge");
```
### Create and Add new elements

```js
// Create un new element, stored in a variable
let myNewElement = document.createElement("div");

// Retrieve an existing element where to put it under
let parentElement = document.gelElementById("container");

// Add our new element as a child of parentElement
parentElement.appendChild(myNewElement);

// There is multiple methods to add elements
parentElement.append(myNewElement, anotherNewElement) // Add after the last child of parentElement

```

### Other
- Other actions
```js
.click();
.appendChild();
```

### Text Manipulation
```js
document.querySelector("h1").innerHTML = "<em>BYBYE</em>";
document.querySelector("h1").textContent = "BYE BABE";
```
```js
document.querySelector("h1").innerHTML = "<em>BYBYE</em>";
document.querySelector("h1").textContent = "BYE BABE";
```
### Elements manipulation
- Retrieve attributes list for an element:
```js
document.querySelector("a").attributes;
```
- Retrieve value for a specific attribute:
```js
document.querySelector("a").getAttribute("href");
```
- Change attribute value
```js
document.querySelector("a").setAttribute("href","https://www.bing.com");
```

### Separation of concern
In order to change styling with javascript for good reasons (I mean, there is), we have at least 2 options:
 - First : The dirty one > Consist in changing directly the style using .style method
 ```js
document.querySelector("h1").style.fontSize = "10rem";
```
 - Second : The better one > consist in manipulating classes of an element. Here, styling is kept in CSS, and Javascript only toggle it.
 ```js
 document.querySelector("button").classList.add("invisible");
 document.querySelector("button").classList.remove("invisible");
 document.querySelector("button").classList.toggle("invisible");
```

### Listen to event

 ```js
// Get an element to Listen to
allButtons = document.querySelector("button")

// Write a function which will be trigger on the event
function handleClick(){
  alert("clicked");
}

// The addEventListener method takes 2 params at least :
//   1- The type of event ( a click, a mouseover, a change, etc.)
//   2- The function to trigger
allButtons.addEventListener("click",handleClick)
```
