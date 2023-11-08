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
## Retrieve element from tree
```js
document.firstElementChild;
document.firstElementChild.firstElementChild;
```

```js
document.lastElementChild;
```
## Manipulate HTML

```js
var head = document.firstElementChild;
head.innerHTML = "foo";
head.style.color = "red";
```

## Perform action
```js
document.getElementsByTagName("li")[0];
document.getElementsByClassName("htmlClass")[0];
document.getElementById("title");

document.querySelector("input").click();
document.querySelectorAll("input")[0].click();

```
### Methods
```js
.click();
.appendChild();
.setAttribute();

document.querySelector("h1").classList.add("huge");
document.querySelector("h1").classList.remove("huge");
document.querySelector("h1").classList.toggle("huge");
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
