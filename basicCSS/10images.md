# Centering an image
- img elements are "like" inline elements, so they don't take up the full width of their parent element.
- To center an image, we can set the width of the image and the margin-left property of the parent element to auto.
- For example:
```css
img {
	display: block;
	margin-left: auto;
	margin-right: auto;
	margin-top: -25px; /* This moves the image up so it appears centered. h elements have default top and bottom margin space */
}
```

