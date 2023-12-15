# CSS Animations
## Basics

4 Basics concepts to CSS animation:
- la fonction  transform
- les pseudoéléments ;
- les @keyframes ;
- l'opacité, et les itérations.

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
## Performances
Browsers takes multiple steps in order to render CSS.
Each CSS properties will require one or multiple steps.
Three steps : Layout > Paint > Composition

Animating a button for example : Changing property 'Width' will need to recompute all 3 steps.
In other hand, 'Transform' will only recompute the composition step.

Low performance impact properties : Transform / opacity

## Animate using Transform
