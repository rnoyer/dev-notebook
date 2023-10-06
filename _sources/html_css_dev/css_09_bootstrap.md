# Bootstrap Framework basics

## 12 columns system
```html
<div class="container">
  <div class="col-2"></div>
  <div class="col-6"></div>
  <div class="col-4"></div>
</div>
```

## Breakpoints
Bootstrap Breakpoints define the limit in pixel where the aligned items can no longer fit horizontally, and instead, are placed one under another, and occupy 100% of the container's width.
```html
<div class="container">
  <div class="col-sm-2"></div>
  <div class="col-sm-6"></div>
  <div class="col"></div> //adjust in size to fill remaining width space.
</div>
```
Multiple breakpoints:
```html
<div class="container">
  <div class="col-sm-12 col-md-8 col-lg-4"></div>
</div>
```
See documentation for breakpoints list: https://getbootstrap.com/docs/5.0/layout/breakpoints/
