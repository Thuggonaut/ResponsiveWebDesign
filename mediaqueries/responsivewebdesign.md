# Responsive Web Design
- Responsive Design tells your webpage how it should look on different-sized screens.

# @media rule
- also known as a media query, is used to conditionally apply CSS. 
- Media queries are commonly used to apply CSS based on the viewport width using the `max-width` and `min-width` properties.
- In the below example the padding is applied to the `.card` class when the viewport is `960px` wide and below.
- e.g.
```css
@media (max-width: 960px) {
  .card {
    padding: 2rem;
  }
}
```


# Logical operators
- can be used to construct more complex media queries. 
- The `and` logical operator is used to query two media conditions.
- For example, a media query that targets a display width between `500px` and `1000px` would be:
```css
@media (min-width: 500px) and (max-width: 1000px) {

}
```

# overflow property
- The overflow property in CSS controls what happens when content is too big to fit in its container.
- The overflow property can have these main values:
	- `hidden` - Clips any content that overflows the container
	- `visible` - (Default) Content can overflow and will be shown outside the container
	- `scroll` - Adds scrollbars to the container, allowing users to scroll to see overflow content
	- `auto` - Similar to scroll, but only adds scrollbars when needed
	- `clip` - Like hidden, but more strict (doesn't create scrollable overflow)
- You can also set overflow separately for horizontal and vertical directions using:
	- `overflow-x` - Controls horizontal overflow
	- `overflow-y` - Controls vertical overflow
