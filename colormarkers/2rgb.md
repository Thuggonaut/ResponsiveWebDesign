# RGB model
- additive, means that colors are created by adding different amounts of red, green, and blue light.
- As opposed to the CMYK model, which is subtractive, used in printing.
- each color can be represented as a combination of these three colors.
- each color ranges from 0 to 255.
- 0 means no color (black), where a color begins, and 255 means full color (white).
- the RGB color model is commonly used in digital displays, like TVs and computer screens.
- The CSS rgb function accepts values, or arguments, for red, green, and blue, and produces a color:
```css
.one {
  background-color: rgb(255, 0, 0);
}

.two {
  background-color: rgb(0, 255, 0);
}

.three {
  background-color: rgb(0, 0, 255);
}
```


# Primary/secondary colors
- red, yellow, and blue.
- when combined, create pure white. But for this to happen, each color needs to be at its highest intensity. 
- Secondary colors are the colors you get when you combine primary colors. 


# Tertiary colors
- are created by combining a primary with a nearby secondary color.
- For example:
```css
.one {
  background-color: rgb(255, 127, 0);
}
```

# Color wheel
- is a circle where similar colors, or hues, are near each other, and different ones are further apart. For example, pure red is between the hues rose and orange.
- Two colors that are opposite from each other on the color wheel are called complementary colors. 
- If two complementary colors are combined, they produce gray. But when they are placed side-by-side, these colors produce strong visual contrast and appear brighter.


# Hexadecimal color code
- is a six-digit code that represents the amount of red, green, and blue in a color.
- For example:
```css
.one {
  background-color: #00FF00; /* green */
}
```
- 00 is 0% of that color, and FF is 100%.
- Lower the intensity of green by setting the green value of the hex color to 7F.
```css
.one {
  background-color: #007F00; /* dark green */
}
```

