# Combining CSS selectors

Combining selectors allows to save time and limit multiplication of selectors descriptions.

Multiple ways to combine selectors:

## Select Group of selectors (comma ',')
Apply to all of the listed selectors

```css
h1,h2,h3{
    color: red;
} /* This will apply the color red to all h1, h2 and h3 titles */
```

## Select child ('>')

Apply the CSS style only to the direct child selected

```css
div > p{
    color: red;
} /* This will apply the color red to all 'p' directly child of a 'div' element */
```
## Descendant selector (space ' ')

Apply the css to the selector on the right (the Descendant) if it is contained under the ancestor (left selector). The descendant can be direct or deeper regarding its ancestor.

```css
.box li {
  color: blue;
}/* This will apply the color blue to all 'li' elements having an ancestor selector with the class 'box' */
```

## Chaining selector (nothing between selector)
Will check wether all the selectors exist within a particular element, mentioned first.
```css
h1.big#box {
  color: blue;
}/* This will apply the color blue to all 'h1' having a class 'big' *AND* an id 'box' */
```

## Combining Combiners
It is possible to combine multiple combiners :'(

```css
ul > p.big{
  font-size: 0.5rem;
}/* Here we combined the ancestor/child + chaining selector */
```
