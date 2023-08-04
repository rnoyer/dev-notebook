# Grid
As Flexbox is meant to manage 1D lyout, such as row or columns, grid is designed to handle 2D layout, such as a table.

## Grid display
```css
.container {
  width: 800px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr;
}
```


## Grid sizing

### grid-template-rows / grid-template-columns (grid container):
- Fixed size: 10px 10px 20px;
- Fractional size: 1fr 1fr 2fr;
- Minmax size: minmax(10px, 20px);
- Repeat: repeat(3, 10px);
- Auto size: auto;

### grid-auto-rows



## Grid Item Placement

- Grid containers
- Grid items

- Grid cells
- Grid Tracks (row tracks / columns tracks)

- Grid lines (gap)

### grid-column (+ grid-row):
- span 2:
- 4 / 6: (start / end)
- auto:
- 20%:
### grid-column-start (+ grid-row-start):


### grid-column-end (+ grid-row-end):


### order:
