In aphabetical order:

# `# `vs. `.` in css
- The # symbol is used to select an element by its ID, while the . symbol is used to select elements by their class.


# calc()
- The `calc()` function allows you to calculate a value based on other values. 
- For example, you can use it to calculate the width of the viewport minus the margin of an element:
```css
.example {
  margin: 10px;
  width: calc(100% - 20px);
}
```


# child combinator selector `>`
- used between selectors to target only elements that match the second selector and are a direct child of the first selector.
- This can be helpful when you have deeply nested elements and want to control the scope of your styling.
```css
div > p {
color: blue;
}
```
- In this example, only `<p>` elements that are direct children of a `<div>` will be styled with blue text. If a `<p>` is nested inside another element within the `<div>`, it will not be affected.


# max function
- returns the largest of a set of comma-separated values. For example:
```css
img {
  width: max(250px, 25vw);
}
```
- In the above example, the width of the image will be 250px if the viewport width is less than 1000 pixels. If the viewport width is greater than 1000 pixels, the width of the image will be 25vw. This is because 25vw is equal to 25% of the viewport width.


# z-index property
- `z-index` controls the stacking order of elements on the page (think of layers in Photoshop). 
- Basic concept:
	- Higher z-index = closer to viewer (appears on top)
	- Lower z-index = further from viewer (appears behind)
	- Default z-index is 0
	- Only works on positioned elements (position: relative, absolute, fixed, or sticky)
- Common values:
```css
.behind {
    z-index: -1;    /* behind default elements */
}
.default {
    z-index: 0;     /* default stacking level */
}
.front {
    z-index: 1;     /* in front of default elements */
}
.emergency {
    z-index: 999;   /* way in front (common for modals/popups) */
}
```