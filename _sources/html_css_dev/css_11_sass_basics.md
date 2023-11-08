# Sass basics

Sass allows to write CSS code with a different syntax : concise and readable.

There is two types of syntax, and therefor, two types of files:

## .sass syntax
Python like syntax: works with indentations and line breaks:
```sass
.nav
  text-align: right

 .nav__link
    font-size: 15px
    padding-left: 30px

  .nav__link--purple
      color: #a5b4fc;
```

##  scss syntax
```scss
.nav {
    text-align: right;
    .nav__link {
        font-size: 15px;
        padding-left: 30px;
        .nav__link--purple {
            color: #a5b4fc;
    }
  }
}
```
### Main specificities:
- Selectors can be nested
- Variables:

```scss
$main-color: red;
.header {
  background-color: $main-color;
}
.footer {
  background-color: $main-color;
}
```
- Mixins: A set of CSS properties, called in a selector using "@include":
```scss
@mixin theme($theme: DarkGray) {
  background: $theme;
  box-shadow: 0 0 1px rgba($theme, .25);
  color: #fff;
}

.info {
  @include theme;
}
.alert {
  @include theme($theme: DarkRed);
}
}
```
- Media queries: With Sass, media queries are nested under selectors, rather than the opposite in CSS:
```scss
.intro {
  display: flex;
  flex-direction: row;
  align-items: flex-start;

  @media (max-width: 996px) {
    flex-direction: column;
    align-items: center;
  }
}
```
