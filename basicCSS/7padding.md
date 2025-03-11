# Padding spaces
- The padding property adds space inside the element, between the content and the border.
- For example:
```css
.menu {
  padding-left: 20px;
  padding-right: 20px;
  padding-top: 20px;
  padding-bottom: 20px;
}
```
- if all the padding values are the same, we can use the padding property to set the padding for all four sides.
```css
.menu {
  padding: 20px;
}
```

# max-width property
- The max-width property sets the maximum width of an element.
- The current width of the menu will always take up 80% of the body element's width. On a very wide screen, the coffee and dessert appear far apart from their prices.
- We can use the max-width property to prevent it from growing too wide.
- For example:
```css
.menu {
  width: 80%;
  max-width: 500px;
  background-color: burlywood;
  margin-left: auto;
  margin-right: auto;
  padding: 20px;
}
```