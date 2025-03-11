# Marker sleeves
- Styles applied to enhance visual markers.


# Opacity
- The opacity property can be used to control the transparency of a marker.
- With the value 0, or 0%, the element will be completely transparent, and at 1.0, or 100%, the element will be completely opaque like it is by default.
- For example:
```css
.sleeve {
  width: 110px;
  height: 25px;
  background-color: white;
  opacity: 0.5;
}
```
- Similar to the opacity property, the alpha channel controls how transparent or opaque a color is.
- To add an alpha channel to an rgb color, use the rgba function instead.
- The rgba function works just like the rgb function, but takes one more number from 0 to 1.0 for the alpha channel:
```css
rgba(redValue, greenValue, blueValue, alphaValue);
```
- For example:
```css
.sleeve {
  width: 110px;
  height: 25px;
  background-color: rgba(255, 255, 255, 50%)
}
```
- Your sleeve is looking good, but it would look even better if it was positioned more toward the right side of the marker. 
```html
<div class="marker red">
  <div class="cap"></div>
  <div class="sleeve"></div>
</div>
```
```css
.cap {
  width: 60px;
  height: 25px
}
```
- It looks like your sleeve disappeared - What happened is that your new cap div is taking up the entire width of the marker, and is pushing the sleeve down to the next line.
- This is because the default display property for div elements is block. So when two block elements are next to each other, they stack like actual blocks. For example, your marker elements are all stacked on top of each other.
- To fix this, you can set the display property of the sleeve and cap divs to inline-block. 
```css
.sleeve, .cap {
  display: inline-block;
}
```
