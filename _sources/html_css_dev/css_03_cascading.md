# CSS Cascading

For a given HTML element, multiple conflicting CSS rules can exist. The cascading rule determine which one are applied or not.

With the cascade image in mind, there is different categories which stands for cascade stages, and the rule applied will be the one inside the lowest stage of the cascade.

There is 4 categories containing sub-categories, detailed below, from top to bottom.

## 4. Position

For multiple identical rules within a CSS selector, or for multiple identical CSS selector, the one applied is the lowest.
```css
/* CSS file */
h1{ color: blue;
    color: pink;} /* h1 will appear pink because it is the lowest property within the selector 'h1' */

p{color: blue;}
p{color: green;} /* p will appear green because it is the lowest CSS selector 'p' */
```
## 3. Specificity
It goes from the less specific selector, to the most specific.

<ol>
    <li value="4">Element selector</li>
    <li value="3">Class selector</li>
    <li value="2">Attribute selector</li>
    <li value="1">id selector</li>
</ol>

```css
/*4 Element selector */
h1{color: blue;}

/*3 Class selector */
.class-XXX{color: blue;}

/*2 Attribute selector */
li[draggable] {color: green;}

/*1 id selector */
#id-XXX{color: blue;}
```
## 2. Type
It goes from the farthest, to the closest CSS implementation regarding to the element.
<ol>
    <li value="3">External</li>
    <li value="2">Internal</li>
    <li value="1">Inline</li>
</ol>

## 1. Importance
The keyword "!important" next to a property will override any other rule.

```css
h1{
  color: blue; !important
  color: green;}
```

# Summarize
![cascading](../assets/images/css_cascading.png)
