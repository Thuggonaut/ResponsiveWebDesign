# background-color
- The background-color property sets the background color of an element.
- For example:
```css
body {
  background-color: black;
}
```

# link colour
- The default colour of a link is blue, and the default colour of a visited link is purple.
- We can change the colour of a link regardless of whether it has been visited by using the color property.
- For example:
```css
a {
  color: white;
}
```
- You change properties of a link when the link has actually been visited by using a pseudo-selector that looks like 
```css
a:visited { 
	propertyName: propertyValue; 
}
```
- For example:
```css
a:visited { 
	color: grey;
}
```
- You change properties of a link when the mouse hovers over them by using a pseudo-selector that looks like 
```css
a:hover { 
	propertyName: propertyValue; 
}
```
- For example:
```css
a:hover { 
	color: red;
}
```
- You change properties of a link when the link is actually being clicked by using a pseudo-selector that looks like 
```css
a:active { 
	propertyName: propertyValue; 
}
```
- For example:
```css
a:active { 
	color: green;
}
```
