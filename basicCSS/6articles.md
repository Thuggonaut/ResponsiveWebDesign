# article elements
- The article element is used to group related content together.
- For example:
```html
<article>
    <p>French Vanilla</p>
    <p>3.00</p>
</article>
<article>
    <p>Hazelnut</p>
    <p>4.00</p>
</article>
```

# display contents in a row
- p elements are block elements, so they take the full width of their parent. 
- We want them to behave like inline elements.
- The p elements are nested in an article element with the class attribute of item. 
- We can use the display property to change the display type of an element.
```css
.flavor {
	width: 75%;
	text-align: left;
}

.price {
	width: 25%;
	text-align: right;
}

.item p {
  display: inline-block;
}
```

```html
<h2>Coffee</h2>
<article class="item">
    <p class="flavor">French Vanilla</p><p class="price">3.00</p>
</article>
<article class="item">
    <p class="flavor">Hazelnut</p><p class="price">4.00</p>
</article>
```

# Add multple classes for a CSS rule to apply
- For example:
```css
.flavor, .dessert {
  text-align: left;
  width: 75%;
}
```
