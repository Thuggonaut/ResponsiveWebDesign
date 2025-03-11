# Borders
- For a border to be visible, you need to set its width and style.
```css
.sleeve {
  width: 110px;
  height: 25px;
  background-color: rgba(255, 255, 255, 0.5);
  border-left-width: 10px;
  border-left-style: solid;
  border-left-color: black;
}
```
- The border-left shorthand property lets you to set the left border's width, style, and color at the same time:
```css
border-left: width style color;
```
- For example:
```css
.sleeve {
  border-left: 10px solid rgba(0, 0, 0, 0.75);
}
```
```html
<div class="container">
  <div class="marker red">
    <div class="cap"></div>
    <div class="sleeve"></div>
  </div>
  <div class="marker green">
    <div class="cap"></div>
    <div class="sleeve"></div>
  </div>
  <div class="marker blue">
    <div class="cap"></div>
    <div class="sleeve"></div>
</div>
```	
