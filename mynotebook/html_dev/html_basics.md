# HTML Basics

## Tags vs. Element
A tag refers to contents in angle-brackets
An Element refers to the tags (opening and closing tags) and the content between them.
```html
<h1> Heading 1 </h1>
```
<hr />

## Main HTML tags (Balises HTML)
- Headings tags (Balises de titres) goes from \<h1>\</h1> to \<h6>\</h6>.
- Paragraph tag: \<p> \</p>
- void elements:
  - Horizontal Rule: \<hr />
  - Break: \<br />
<hr />

## Lists
### Unordered list: Create a raw bullet points list
```html
<ul>
	<li>list item 1</li>
	<li>list item 2</li>
	<li>list item 3</li>
</ul>
```
The rendered output looks like this:
<ul>
	<li>list item 1</li>
	<li>list item 2</li>
	<li>list item 3</li>
</ul>

### Ordered list: Create a raw numbered list:
```html
<ol>
	<li>list item 1</li>
	<li>list item 2</li>
	<li>list item 3</li>
</ol>
```
The rendered output looks like this:
<ol>
	<li>list item 1</li>
	<li>list item 2</li>
	<li>list item 3</li>
</ol>

List nesting : Les listes s'imbriquent les unes dans les autres en les placant à l'interieur d'un élement \<li> \</li>.

Exemple:
```html
<ul>
    <li>01 Liste principale</li>
    <li>02 Liste principale</li>
    <li>03 Liste principale
	<ol>
	    <li>01 liste imbriquée</li>
	    <li>02 liste imbriquée</li>
	</ol>
    </li>
    <li>04 Liste principale</li>
</ul>
```
The rendered output looks like this:
<ul>
    <li>01 Liste principale</li>
    <li>02 Liste principale</li>
    <li>03 Liste principale
	<ol>
	    <li>01 liste imbriquée</li>
	    <li>02 liste imbriquée</li>
	</ol>
    </li>
    <li>04 Liste principale</li>
</ul>
<hr />

## Anchor elements
Anchor element allow the text to be enhanced with attributes, such as hyperlinks.

```html
<a href="https://www.google.com">Enhanced text with an hyperlink reference (href)</a>
```
The rendered output looks like this:

<a href="https://www.google.com">Enhanced text with an hyperlink reference (href)</a>
<hr />

## Image element
Allow to display an image. It is a void element (no closing tag)

Attributes:
- 'src': To locate the image source.
- 'alt': Alternative text description: important for accessibility
- etc.

```html
<img src="https://picsum.photos/100" alt="randomly generated photo"/>
```
