# div element
- The div element is used mainly for design layout purposes.
- It's used to group HTML elements together and apply styles to all of them at once.
- For example:
```html
<body>
    <div id="menu">
    <main>
      <h1>CAMPER CAFE</h1>
      <p>Est. 2020</p>
      <section>
        <h2>Coffee</h2>
      </section>
    </main>
    </div>
</body>
```

# id selector
- The id selector is used to select an element with a specific id attribute.
- An id selector is defined by placing the hash symbol # directly in front of the element's id value.
- For example:
```css
#menu {
  width: 300px; /* prevent div from taking the full width of the page, can also use % */
  background-color: burlywood;
  margin-left: auto; /* auto will center the div with margins (invisible space) */
  margin-right: auto;
}
```

# class selector
- The class selector is used to select all elements with a specific class attribute.
- A class selector is defined by placing a period . directly in front of the class name.
- For example:
```css
.menu {
  width: 80%;
  background-color: burlywood;
  margin-left: auto;
  margin-right: auto;
}
```

# body selector
- can use a background-image to set a background image for the body element.
- For example:
```css
body {
  background-image: url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg);
}
```