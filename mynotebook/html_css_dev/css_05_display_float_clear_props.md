# Properties: Display, Float and Clear

## CSS Display
'Display' define the space the element takes in the webpage.
### display: block
- By default,the element will take the whole width of the page. The Height will be fitted to its content.
- Width and Height sizes can be set with eponymes props.
- Multiple 'block' elements will stack vertically only.

### display: inline
- inline elements will fit its content in Height AND width.
- Size CAN NOT be set manually.
- Multiple 'inline' elements will stack horizontally until the end of the webpage, and then below.
### display: inline-block
- Possible to set Height and width (block)
- Will stack horizontally (inline)
### display: none
- Will hide the element completely

## CSS Float
'Float' allow an element to be wrapped around by other element.
Main usage: Paragraph wrap an image just like in a newspapers.
### float: left
- image is placed on the left top corner and the text will wrap it on its right.
### float: right
- image is placed on the right top corner and the text will wrap it on its left.

## CSS Clear
'Clear' allow an element to NOT wrap a floating element.
### clear: left
- Will cancel the 'float: left' outcomes.
### clear: right
- Will cancel the 'float: right' outcomes.
### clear:
- Will cancel both 'float: left' and 'float: right' outcomes.
