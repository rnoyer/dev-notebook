# CSS Basics
CSS means Cascading Style Sheets. It will define how HTML elements will be displayed, using custom parameters.
## CSS implementations
3 Ways of adding CSS in a webpage: Inline, Internal and External

## Inline
```html
<tag style="css" />
```
It goes within the same line of a particular html element using a "style" attribute.
It is not recommanded to use inline styles for an entire webpage. It is used for very specific section, for testing purpose, or when you want to change only one element.

## Internal
```html
<head>
    [...]
    <style>css</style>
    [...]
</head>
```
All of the css is stored inside the element \<style>\</style> inside the head element of the page.


## External
```html
<head>
    [...]
    <link rel="stylesheet" href="styles.css" />
    [...]
```
A separate file contains all of the CSS properties. In the HTML page the CSS file is called with an \<link /> element.
## Takeaways
| CSS implementation|Usage                          |
|:-----------------:|-------------------------------|
|   Inline          |Target one specific element   |
|   Internal        |Target one page                |
|   External        |Target the whole website       |

## CSS Selectors
A CSS file is composed with sets of "propertie:value" (e.g. color:blue). These sets of parameters are enclosed into curly brackets, and assigned to a selector. A selector denote to what elements in the HTML file the parameters will be applied to.
```css
/* CSS file */
h1{
    color:blue
}
/* In this example, the color blue will be applied to all of the <h1></h1> tags */
```
There are 4 types of selectors.
### Element selector
An element selector will target a particular HTML tag (such as paragraph, headings levels, etc.).

### Class selector
Styles will be applied only to elements containing the right same "class" attribute.
Example:
```css
/* CSS file */
.red-heading{
    color:red
}
```
```html
<!-- HTML file -->
<h2 class="red-heading">This will be red</h2>
<h2>This will NOT be red</h2>
<h2>This will NOT be red</h2>
```

### ID selector
Work the same way as class selector.
The difference is the usage: it used to make a unique modification to a particular element in the HTML page.

Example:
```css
/* CSS file */
#main{
    color:red
}
```
```html
<!-- HTML file -->
<h2 id="main">This will be red</h2>
<h2>This will NOT be red</h2>
<h2>This will NOT be red</h2>
```
### Attribute selector
Will be applied to a particular element with a particular attribute or the value of an attribute.

Example: Applying style to all paragraph elements with a "draggable" element.
```css
/* CSS file */
p[draggable]{
    color:red
}
p[draggable=false]{
    background:blue
}
```
```html
<!-- HTML file -->
<p draggable="false">This will be red with no background color</p>
<p draggable="true">This will be red with blue background color</p>
<p draggable="true">This will be red with blue background color</p>
```

### Universal selector
This selector apply to ALL elements of the HTML file.
```css
/* CSS file */
*{
    color:red
}
```
