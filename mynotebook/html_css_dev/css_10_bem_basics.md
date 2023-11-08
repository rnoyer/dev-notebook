# BEM Convention

BEM stands for "Block - Element - Modifier". It is a naming convention in order to make CSS files easier to read and maintain.

Each HTML element will get its own class, and the naming convention will be determined depending on the role of the element, or the modifications applied to it.

## Block
A block is an "independent entity with its own meaning". It represents a part of the webpage. It can refers to a semantic HTML tag, or an other major part (eg. navbar, hero).

Naming convention for Blocks: starts with "b-" followed with its name.
```css
.b-navbar
.b-hero
.b-text-input
```

## Elements
An element is a part of a block. It has no meaning outside of the block it belongs (eg. menu items, rows, cells).

Elements are named starting with the block name it depends on, then two underscores:
```css
.b-navbar__button
.b-text-input__text-field
```

## Modifiers
Modifiers represent a change in the state or properties of an element or a block.

Just like elements, Modifiers names are preceeded with its block name, or its element name followed with one underscore:
```css
.b-text-input_disabled
.b-navbar__button_red
```
