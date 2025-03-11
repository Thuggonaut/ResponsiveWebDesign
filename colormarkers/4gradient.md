# Linear gradient
- is a smooth color transition from one color to another.
- The CSS linear-gradient function accepts two or more colors, and  lets you control the direction of the transition along a line, and which colors are used.
- the linear-gradient function actually creates an image element, and is usually paired with the background property which can accept an image as a value.
- For example:
```css
.one {
  background: linear-gradient(red, yellow);
}
```

# Gradient direction
- is the direction of the line used for the transition. color1 and color2 are color arguments, which are the colors that will be used in the transition itself.
- These can be any type of color, including color keywords, hex, rgb, or hsl:
```css
linear-gradient(gradientDirection, color1, color2, ...);
```
- Apply a red-to-green gradient along a 90 degree line to the first marker:
```css
.one {
  background: linear-gradient(90deg, rgb(255, 0, 0), rgb(0, 255, 0));
}
```
- While the linear-gradient function needs a minimum of two color arguments to work, it can accept many color arguments.
- For example:
```css
.one {
  background: linear-gradient(90deg, rgb(255, 0, 0), rgb(0, 255, 0), rgb(0, 0, 255));
}
```


# Color stops
- allow you to fine-tune where colors are placed along the gradient line. 
- They are a length unit like px or percentages that follow a color in the linear-gradient function.
- For example, in this red-black gradient, the transition from red to black takes place at the 90% point along the gradient line, so red takes up most of the available space:
```css
.one {
  background: linear-gradient(90deg, red 90%, black);
}
```
- Apply different shades of red to each color argument in the linear-gradient function. The shades on the top and bottom edges of the marker will be darker, while the one in the middle will be lighter, as if there's a light above it:
```css
.red {
  background: linear-gradient(180deg, rgb(122, 74, 14) 0%, rgb(245, 62, 113) 50%, rgb(162, 27, 27) 100%);
}
```
- Another example:
```css
.green {
  background: linear-gradient(180deg, #55680D, #71F53E, #116C31);
}
```
- There are no color stops, but the green marker transitions at the same points as the red marker. 
- The linear-gradient function automatically calculates these values for you, and places colors evenly along the gradient line by default:
```css
.red {
  background: linear-gradient(180deg, rgb(122, 74, 14), rgb(245, 62, 113), rgb(162, 27, 27));
}
```
- If no gradientDirection argument is provided to the linear-gradient function, it arranges colors from top to bottom, or along a 180 degree line, by default.
```css
.red {
  background: linear-gradient(rgb(122, 74, 14), rgb(245, 62, 113), rgb(162, 27, 27));
}

.green {
  background: linear-gradient(#55680D, #71F53E, #116C31);
}
```
- Apply a gradient to the blue marker, this time using the hsl function as color arguments.
```css
.blue {
  background: linear-gradient(hsl(186, 76%, 16%), hsl(223, 90%, 60%), hsl(240, 56%, 42%));
}
```
