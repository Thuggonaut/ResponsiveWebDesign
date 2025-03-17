In aphabetical order:

# `# `vs. `.` in css
- The # symbol is used to select an element by its ID, while the . symbol is used to select elements by their class.


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

