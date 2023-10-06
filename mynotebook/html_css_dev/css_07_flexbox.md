# Flexbox

## Flexbox Display
display: flex;
display: inline-flex;


flex-basis: 100px

## Flexible layout
Test properties here: https://appbrewery.github.io/flex-layout/

### Properties for the parent: flex container

#### flex-direction:
Define the main axis, and therefore the cross axis.
- row; (default)
- column;

#### flex-wrap:
Manage the way items will behave if there is not enough space to fit all the items on screen in one single line.
- nowrap; (default) Items will stay aligned, and will be off the screen.
- wrap; items will automatically move on to the next line.

#### justify-content:
How items behave when there is more space than needed in the main axis.
- Flex-start; / flex-end; items are placed to the left / right
- center; will center all items in the middle
- space-between; / space-around; / space-evenly; will separate items with space between, according to the corresponding property.

#### align-items (+height / +flex-wrap:nowrap;):
Manage the position of items along the cross-axis. It will use the space defined by the 'height' property.
- Flex-start; / flex-end; / enter; / baseline; / stretch; Behave accordingly.

```
/!\ When flex-wrap is set to 'wrap' the property 'align-items (+height)' is disabled. align-content (+height)' is the only property able to manage items on the cross axis.
```

#### align-content (+height / +flex-wrap:wrap;):
Manage the position of items along the cross axis WHEN flex-wrap is set to 'wrap', which means items will move to multiple lines when the screen get to short.
```
/!\ When flex-wrap is set to 'wrap' the property 'align-items (+height)' is disabled. align-content (+height)' is the only property able to manage items on the cross axis.
```
### Properties for the children: flex items

#### order:
Allow to rearrange items order.
- Bigger number are placed at the end.
- Default value is 0.
- Negative number are possible

#### align-self:
Allow a specific item to over rule the 'align-items' property
- Flex-start; / flex-end; / enter; / baseline; / stretch; Same behavior as 'align-items'.

### Flex sizing (flex items properties)

An item max-size and min-size is define with multiple properties.
The algorithm will in order, look if min/max-width is set and apply it. If not, look for flex-basis, etc.
```
content width << width:; << flex-basis:; << min-width: / max-width:;
```
#### width:
As long as there is enough space, this parameter will be implemented. If there is not enough space, item will shrink to its minimum 'content width'.

### flex-basis:
The 'flex-basis:' property overide the 'width:' property.
- flex-basis: auto; (default) will automatically set space to items, depending on the amount of text in it. (which is weird).
- flex-basis: 0; will give **equal** space to every items.
- flex-basis: 1;
- flex-basis: 100px;

#### min-width: / max-width:
Will overide the 'flex-basis' and 'width:' properties, **unless they are inside the boundaries of the 'min/max-width' properties.**

By default: lets assume our item contain a paragraph with multiple words in it.
- min-width is equal to the longest word.
- max-width is  equal to the total length of all the words.
- It can be set manually with a custom value.

#### flex-grow:
- '0': Restrict item only to grow until its 'flex-basis' size at max.
- '1': allow item stretch to occupy the whole container, ignoring flex-basis if there is more room available.

#### flex-shrink:
- '0': Restrict item only to shrink until its 'flex-basis' size at max.
- '1': allow item shrink to the 'min-width:', ignoring flex-basis if there is not enough space.
#### flex:
As grow:, shrink: and flex-basis:
- flex: 1 1 0; set in order: grow shrink flex-basis
- flex: 1; set automatically grow, shrink and flex-basis to 1 1 0.
- flex: 2; change the ratio of an item. In this example, the item will takes twice the size of a regular item.
