# typography
- styling texts for readability

# Borders
- In this example:
```css
.label {
	border: 2px solid black;
	width: 270px;
	margin: 20px auto;
	padding: 0 7px;
}
```
- with your browser's developer tools, you may notice that it's actually 288 pixels wide instead of 270. This is because, by default, the browser includes the border and padding when determining an element's size.
- To solve this, reset the box model by creating a `*` selector and giving it a <box-sizing> property of <border-box>.


# Spacing
- Horizontal spacing between equally important elements can increase the readability of your text.

- First, we want to apply spacing to only a portion of the text using the <span> element. 
- The <span> element is used to style a specific part of the text without affecting the surrounding text. 
```css
<p class="bold">Serving size <span>2/3 cup (55g)</span></p>
```
- then, we can add the horizontal spacing using <flex>. 
- In your <p> selector, add a <display> property set to <flex> and a <justify-content> property set to space-between.

# Styles
- The <rem> unit stands for <root em>, and is relative to the font size of the <html> element.
- setting the <font-size> to <0.85rem> would calculate to roughly <13.6px> (remember that you set your html to have a <font-size> of <16px>).

- The `:not` pseudo-selector can be used to select all elements that do not match the given CSS rule.
```css
div:not(#example) {
  color: red;
}
```
- This selects all <div> elements without an <id> of <example>.