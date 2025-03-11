# style element
- You can add style to an element by specifying it in the style element and setting a property for it like this:
```html
element {
 property: value;
}
```
- This is called a type selector. We will use this to style the h1 and p elements.
- For example:
```html
<head>
    <meta charset="utf-8" />
    <title>Cafe Menu</title>
	<style>
      h1 {
        text-align: center;
      }
      p {
        text-align: center;
      }
    </style>
</head>
<main>
      <h1>CAMPER CAFE</h1>
      <p>Est. 2020</p>
      <section>
        <h2>Coffee</h2>
      </section>
    </main>
```
- But we can also add the same group of styles to many elements by creating a list of selectors. Each selector is separated with commas like this:
```
selector1, selector2 {
  property: value;
}
```
- For example:
```html
<style>
    h1, h2, p {
    	text-align: center;
    }
</style>
```