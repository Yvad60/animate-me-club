## Infinite spinner

This project is about a simple spinner that spins infinitely in the center of the screen.

### Instructions

- Creating a spinner made of a collection of circles that spins around infinitely.
- The spinner should always be in the center of the screen.
- The spinner should spin at a constant speed.

### Approach

- **Creating the spinner**: added an empty `div` which will be the circle. The circle was given a fixed width and height that are equal which made it a square, by adding `border-radius` of `100%` made it a full perfect circle.
  The circle was not given a fill color instead it was given a `border` with a `dotted` style which mimics a circular line of dots

- **Centering the spinner**: The body which is a direct parent of the spinner container was displayed as a vertical flexbox it was forced to align its items in the center and justify them in the center. to Make the spinner in the center the body was given height of `100vh` to always fit the screen viewport

```css
body {
  display: flex;
  justify-content: "center";
  align-items: "center";
}
```

- **Animating the spinner**:
  - To move the spinner in a circular motion it should be rotated from `0deg` to `360deg` (the degree of a whole circle) and this was achieved using the CSS Transform rotate property.
  - The spinner movement was supposed to be done indefinitely therefore the animation iteration count was set to `infinite`.
  - To control the speed of the spinner while spinning the animation duration was used and set to `2.5s`

Reference

```css
.spinner {
  /*...other styles */
  /* animation: duration easing-function iteration-count animation-name */
  animation: 2.5s linear infinite spin;
}
@keyframes spin {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}
```

**Note**: The animation easing function is set to `linear` to ensure the spinner will move with a constant speed as mentioned in the instructions
