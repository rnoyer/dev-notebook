# React Basics

## Babel
Ensure retro compatibility, compiling latest JS versions to understandable to every Browser.

## Basics modules to start

```js
import React from "react"
import ReactDOM from "react-dom"
```

## Basic React rendering
- An index.html will only contains an empty \<div> element with an id called "root" by convention.
- An index.js file will trigger React rendering from the ReactDOM imported library.

```js
// ReactDOM.render takes 2 arguments : 
//  -  An element to inject (only one)
//  -  An element to populate

ReactDOM.render(
<>
    <H1>Hello world</h1>
    <p>This is a paragraph</p>
</>,
document.getElementById("root"))
```
