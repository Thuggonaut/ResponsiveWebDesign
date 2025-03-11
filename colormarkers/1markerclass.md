# Markers
- These are specific classes that are often used to denote elements that serve as markers or indicators. 
- For example, a class named .marker might be used to style elements that represent points on a graph, markers on a map, or any other visual indicators.
- While all marker classes are classes, not all classes are marker classes. Classes can serve a wide range of purposes beyond just marking or highlighting elements.
- Examples:
- A  CSS rule that targets the class marker:
```css
.marker {
  background-color: red;
}
```
- An empty div element doesn't take up any space.
- we can add some space by setting the width and height properties.
```css
.marker {
  background-color: red;
  width: 200px;
  height: 25px;
}
```

# Center a marker
- The margin shorthand property makes it easy to set multiple margin areas at the same time.
- To center your marker on the page, set its margin property to auto. 
- For example:
```css
.marker {
  width: 200px;
  height: 25px;
  margin: auto;
  background-color: red;
}
```

# Creating a container
- For example:
```html
<div class="container">
  <div class="marker">
  </div>
  <div class="marker">
  </div>
  <div class="marker">
  </div>
</div>
```
- While you have three separate marker div elements, they look like one big rectangle. Let's add some space between them to make it easier to see each element.
- When the shorthand margin property has two values, it sets margin-top and margin-bottom to the first value, and margin-left and margin-right to the second value.
- For example:
```css
.marker {
  width: 200px;
  height: 25px;
  background-color: red;
  margin: 10px auto;
}
```

# Multiple classes:
- You can apply multiple classes to the same element by separating the class names with a space.
- For example, the following adds both the animal and dog classes to a div element:
```html
<div class="animal dog">
```
- If you add multiple classes to an HTML element, the styles of the first classes you list may be overridden by later classes.
- For example:
```css
.one {
  background-color: red;
}

.two {
  background-color: green;
}

.three {
  background-color: blue;
}
```
```html
<div class="container">
  <div class="marker one">
  </div>
  <div class="marker two">
  </div>
  <div class="marker three">
  </div>
</div>
```
