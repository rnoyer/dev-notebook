# Media Queries
Media queries allows to apply different CSS depending on various characteristics, such as screen resolution.

It can do more but it is not detailed here. For more infos check [Mozilla web docs here.]('https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries')

```css
/* CSS file */
@media (max-width: 680px){
  .css rules{
    prop: value;
  }
}
```
- max-width: Will apply the rule when the browser viewport is smaller than the max-width
- min-width: Will apply the rule

Characteristics can be combined with an 'AND' operator. It allows to define a starting + ending characterictics.
```css
/* CSS file */
@media (min-width: 680px) and (max-width:1440px) {
  .css rules{
    prop: value;
  }
}
```
