# Viewport
- The viewport is the user's visible area of a web page within the browser window.
-  It is the portion of the document that is currently visible to the user, and it can change based on the size of the browser window or the device being used (like a mobile phone, tablet, or desktop).


# Viewport Units
- Allow you to size elements relative to the viewport dimensions:
  - vw (viewport width): 1vw is equal to 1% of the width of the viewport.
  - vh (viewport height): 1vh is equal to 1% of the height of the viewport.
  - vmin: The smaller value of vw or vh.
  - vmax: The larger value of vw or vh.


# Meta Viewport Tag
- Meta Tag: To control the viewport's size and scale on mobile devices, you often use the <meta> tag in the HTML <head> section:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```


# Horizontal scroll bar
- Removing the horizontal scroll bar:
```css
body {
  width: 100%;
  height: 100vh;
  margin: 0; /* 0 to remove default margin set by some browsers */
}
```
