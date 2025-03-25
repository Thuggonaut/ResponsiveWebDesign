# Pseudo elements
- special keywords that follow a selector

# ::before 
- The `::before` selector creates a pseudo-element which is the first child of the selected element


# ::after 
- The `::after` selector creates a pseudo-element which is the last child of the selected element. 


# content property
- The `content` property is used to set or override the content of the element. 
- By default, the pseudo-elements created by the `::before` and `::after` pseudo-selectors are empty, and the elements will not be rendered to the page. 
	- Setting the `content` property to an empty string `""` will ensure the element is rendered to the page while still being empty.
- e.g.
```css
.key .black--key::after {
	background-color: #1d1e22;
	content: ""; /*make pseudo elements empty */
}
```