# CSS Animations
## Basics
At least 5 requirements are needed to set up a CSS animation:
- a CSS property to change
- An initial value for this property
- An ending value
- a duration
- a pseudo-class to trigger the animation
```css
.b-my-block__element{
  width: 150px;
  background-color: aliceblue;
  padding: 10px 10px;
  margin: 5px;
  transition: transform 200ms;  /* transformation used */
}
.b-my-block__element:hover{     /* pseudoclass used */
  transform: scale(1.15);       /* transformation used */
}
```
