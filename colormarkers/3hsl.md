# HSL model
- The HSL color model, or hue, saturation, and lightness, is another way to represent colors.
- The CSS hsl function accepts 3 values: a number from 0 to 360 for hue, a percentage from 0 to 100 for saturation, and a percentage from 0 to 100 for lightness.
- If you imagine a color wheel, the hue red is at 0 degrees, green is at 120 degrees, and blue is at 240 degrees.
- Saturation is the intensity of a color from 0%, or gray, to 100% for pure color. You must add the percent sign % to the saturation and lightness values.
- Lightness is how bright a color appears, from 0%, or complete black, to 100%, complete white, with 50% being neutral.
- For example:
```css
.blue {
  background-color: hsl(240, 100%, 50%);
}
```
