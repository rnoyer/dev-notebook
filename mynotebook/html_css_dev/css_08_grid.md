# Grid
As Flexbox is meant to manage 1D layout, such as row or columns, grid is designed to handle 2D layout, such as a table.

## CSS grid terms:
- **Grid containers:** Main \'\<div>' containing the whole layout.
- **Grid items:** Items created inside the container (usually \'\<div>').
- **Grid Tracks (row tracks / columns tracks):** Every columns and rows defined with 'grid-template-rows / -columns' are tracks.
- **Grid cells:** Smallest unit in a container. Grid items are composed with one or more cells.
- **Grid lines :** Gaps between items. Each line have a corresponding number starting at 1.

## Grid display
```css
.container {
  width: 800px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  gap: 10px;
}
```


## Grid sizing

### grid-template-rows: / grid-template-columns: (grid container):
These two parameters allows to define the global grid layout in the container. It defines:
- The number of rows and columns
- The size of each cells (items)

Items can be defined with differents attributes:

- Fixed size: 10px 10px 20px; // Not responsive.
- Fractional size: 1fr 1fr 2fr; // Ratios.
- Minmax size: minmax(10px, 20px); // Set limits to grow and shrink.
- Repeat: repeat(3, 10px); // Apply same attributes multiple times (Here 3x 10px).
- Auto size: auto; //

Examples:
```css
.container {
  display: grid;
  grid-template-rows: 10px auto;/* The 2nd row (auto) will fit to its content. */
  grid-template-columns: 10px auto;/*The 2nd col. will fill the remaining screen width. */
}
```

### grid-template:
Will define 'grid-template-rows' and 'grid-template-columns' in one line:
```css
.container {
  display: grid;
  grid-template: /*rows attributes*/ / /*columns attributes*/ ;
}
```

### grid-auto-rows / grid-auto-columns
These parameters defines how extra items should behave. <br/>
It takes sames attributes as 'grid-template-rows / -columns'.

## Grid Item Placement

### grid-column (+ grid-row):
This parameter define how many cells the item will occupy horizontally (grid-column) and vertically (grid-row).
- span 2: will spread over 2 cells.
- 4 / 6: (start / end)
- auto:
- 20%:

### grid-column-start (+ grid-row-start):
Override items default placement, giving the starting line of the item.

### grid-column-end (+ grid-row-end):
Override items default placement, giving the ending line of the item.

### grid area:
This property concatenate successively:
1. grid-column-start
2. grid-row-start
3. grid-column-end
4. grid-row-end
```
/!\ If "grid-area" is used for one item, it should be used for all the other items in order to work properly.
```
Example:
```css
.item {
grid area: 2 / 1 / 3 / 3;
}
```

### order:
Each item is placed by default, following is predecessor, and placed from left to right and from top to bottom.

The 'order' property overwrite this behavior and allow to cutomize the order of the items. Default is '0'.
