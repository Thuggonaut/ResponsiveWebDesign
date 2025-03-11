# Shadows
- The box-shadow property adds shadow effects around an element's frame.
```css
box-shadow: offsetX offsetY color;
```

# Offsets
- The first two values are the horizontal and vertical offsets of the shadow.
- Both offsetX and offsetY accept number values in px and other CSS units
- A positive offsetX value moves the shadow right and a negative value moves it left
- A positive offsetY value moves the shadow down and a negative value moves it up
- If you want a value of zero (0) for any or both offsetX and offsetY, you don't need to add a unit. Every browser understands that zero means no change.
- The height and width of the shadow is determined by the height and width of the element it's applied to. 


# Adding a shadow
- A simple red shadow around your marker that's 5 pixels to the right, and 5 pixels down:
```css
.red {
  background: linear-gradient(rgb(122, 74, 14), rgb(245, 62, 113), rgb(162, 27, 27));
  box-shadow: 5px 5px red;
}
```
- On the opposite side:
```css
.red {
  background: linear-gradient(rgb(122, 74, 14), rgb(245, 62, 113), rgb(162, 27, 27));
  box-shadow: -5px -5px red;
}
```

# Blur
- Reduces sharp edges and creates a blur effect.
```css
box-shadow: offsetX offsetY blurRadius color;
```
- If a blurRadius value isn't included, it defaults to 0 and produces sharp edges. The higher the value of blurRadius, the greater the blurring effect is.
- For example:
```css
.green {
  background: linear-gradient(#55680D, #71F53E, #116C31);
  box-shadow: 5px 5px 5px green;
}
```

# Expand
- Expands the shadow.
```css
box-shadow: offsetX offsetY blurRadius spreadRadius color;
```
- For example:
```css
.blue {
  background: linear-gradient(hsl(186, 76%, 16%), hsl(223, 90%, 60%), hsl(240, 56%, 42%));
  box-shadow: 0 0 0 5px blue
}

.red {
  background: linear-gradient(rgb(122, 74, 14), rgb(245, 62, 113), rgb(162, 27, 27));
  box-shadow: 0 0 20px 0 rgba(83, 14, 14, 0.8);
}
```
- For the green marker's box-shadow property, replace the named color with a hex color code. Use the values 3B for red, 7E for green, 20 for blue, and CC for the alpha channel:
```css
.green {
  background: linear-gradient(#55680D, #71F53E, #116C31);
  box-shadow: 0 0 20px 0 #3B7E20CC;
}
```
- Finally, for the blue marker's box-shadow property, replace the named color with the hsla function. Use the values 223 for hue, 59% for saturation, 31% for lightness, and 0.8 for the alpha channel:
```css
.blue {
  background: linear-gradient(hsl(186, 76%, 16%), hsl(223, 90%, 60%), hsl(240, 56%, 42%));
  box-shadow: 0 0 20px 0 hsla(223, 59%, 31%, 0.8);
}
```
