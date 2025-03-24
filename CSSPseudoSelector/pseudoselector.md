# Pseudo Selectors
- You can use CSS pseudo selectors to change specific HTML elements.
	- e.g. change the style of an element when you hover over it with your mouse
	- trigger other events on your webpage


# Hide elements
- Using the `aria-hidden` attribute:
<div id="years" aria-hidden="true">


# sr-only class
- You can use CSS to make elements with this class completely hidden from the visual page, but still be announced by screen readers.
- The CSS you are about to write is a common set of properties used to ensure elements are completely hidden visually.
- The `span[class~="sr-only"]` selector will select any span element whose class includes `sr-only`. e.g.
```css
span[class~="sr-only"] {
	border: 0;
}
```


# clip property
- The CSS `clip` property is used to define the visible portions of an element. 
- The `clip-path` property determines the shape the `clip` property should take. 
- e.g. Setting the `clip-path` property to the value of inset(50%), forming the clip-path into a rectangle within the element: 
```css
span[class~="sr-only"] {
	border: 0;
	clip: rect(1px, 1px, 1px, 1px); /* define the visible portions of an element */
	clip-path: inset(50%); /* forming the clip-path into a rectangle within the element */
}
```


# Remove elements out of document flow
- `position: absolute;`
- This will ensure that not only are they no longer visible, but they are not even within the page view.


# :first-of-type
- The `:first-of-type` pseudo-selector is used to target the first element that matches the selector.


# :last-of-type
- The `:last-of-type` pseudo-selector does the exact opposite - it targets the last element that matches the selector. 


# Reversing order of elements for screen readers
- `flex-direction: column-reverse;`
- In this case, search engines and screen readers encounter the content in a logical order (footer → main → header), while visually it appears as you'd expect (header → main → footer).
- If you don't need these benefits, then yes, it would be simpler to just order the HTML elements in the way you want them to appear.


# :not()
- The `:not()` pseudo-selector is used to target all elements that do not match the selector.

# !important keyword
- Use the `!important` keyword to ensure these properties are always applied, regardless of order or specificity.
- Ensures properties do not get overwritten
- Using `!important` should be a last resort, while `:not()` is a standard way to write more precise selectors.


# [attribute="value"]
- The `[attribute="value"]` selector targets any element that has an attribute with a specific value.
- e.g.
```css
tr[class="total"] {
	border-bottom: 4px double #0a0a23;
	font-weight: bold;
}

/*or to target the th elements within tr elements */

tr[class="total"] th {
	text-align: left;
	padding: 0.5rem 0 0.25rem 0.5rem;
}
```
- In this example,
```css
tr[class="total"] {
  border-bottom: 4px double #0a0a23;
  font-weight: bold;
}

tr.total td {
	text-align: right;
	padding: 0 0.25rem;
}
```
- The key difference between `tr[class="total"]` and `tr.total` is that the first will select `tr` elements where the only class is `total`. 
- The second will select `tr` elements where the class includes `total`.


# :nth-of-type()
- The `:nth-of-type()` pseudo-selector is used to target specific elements based on their order among siblings of the same type. 
- e.g.
```css
tr.total td:nth-of-type(3) {
	padding: 0.5rem;
}
```

# :hover
- Changes the effect when hovering over a link
- e.g.
```css
tr.total:hover {
	background-color: #99c9ff;
}
```

# linear-gradient()
- Sets the background image of an element
- e.g.
```css
tr[class="data"] {
	background-image: linear-gradient(to bottom, #dfdfe2 1.845rem, white 1.845rem);
}
```