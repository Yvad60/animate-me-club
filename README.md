## Underground title

<!-- TODO: finish the readme description -->

This project is about a text title that animates with a reveal animation from the bottom

### Instructions

- Creating a title that animated revealing from the bottom
- The text should always be in the center of the screen.
- The text should also bounce after revealing

### Approach

- **Centering the text**: The body which is a direct parent of the title container was displayed as a flexbox it was forced to align its items in the center and justify them in the center. To align the text in the center the body was given height of `100vh` to always fit the screen viewport

```css
body {
  display: flex;
  justify-content: "center";
  align-items: "center";
}
```

- **Reveling text from the bottom**:

### Initial approach

- Initially, I created the text and beneath the text, I added a dummy `div` with the same background as the whole body to make it look like it is not even there, the `div` was positioned absolutely so it appeared on the top of everything.

- The title was initially translated 200px on the Y axis which made it positioned down and it got covered by the dummy `div` and with animation it got translated back to `0` which mimics the effect of the text moving up from the background

**Note**: The animation easing function is set to `linear` to ensure the spinner will move with a constant speed as mentioned in the instructions
