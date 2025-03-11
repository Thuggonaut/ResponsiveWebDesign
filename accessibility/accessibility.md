# Accessibility
- Accessibility is making your webpage easy for all people to use – even people with disabilities.
- Learn accessibility tools such as keyboard shortcuts, ARIA attributes, and design best practices.


# SEO
- SEO (Search Engine Optimization) is the process of improving your website's visibility and ranking on search engines like Google, Bing, and Yahoo.
- e.g. 
```html
<meta name="description" content="freeCodeCamp Accessibility Quiz practice project"/>
```


# Semantic HTML elements
- Navigation is a core part of accessibility, and screen readers rely on you to provide the structure of your page. This is accomplished with semantic HTML elements.


# section element
- sematically seperate the content
- `<section>`


# nav element
- used to define a section of a webpage that contains navigation links. It helps to group together links that allow users to navigate through different sections of the website or application.


# navigate to different sections
- In HTML, the # symbol in an anchor (<a>) tag's href attribute is used to create a link to a specific section within the same page. It refers to an element with a corresponding id attribute.
- This allows users to jump to different sections of the same page without reloading it.
- e.g.
```html
<li><a href="#student-info">INFO</a></li>
<li><a href="#html-questions">HTML</a></li>
<li><a href="#css-questions">CSS</a></li>
```


# `# `vs. `.` in css
- The # symbol is used to select an element by its ID, while the . symbol is used to select elements by their class.


# max function
- returns the largest of a set of comma-separated values. For example:
```css
img {
  width: max(250px, 25vw);
}
```
- In the above example, the width of the image will be 250px if the viewport width is less than 1000 pixels. If the viewport width is greater than 1000 pixels, the width of the image will be 25vw. This is because 25vw is equal to 25% of the viewport width.


# child combinator selector `>`
- used between selectors to target only elements that match the second selector and are a direct child of the first selector.
- This can be helpful when you have deeply nested elements and want to control the scope of your styling.
```css
div > p {
color: blue;
}
```
- In this example, only `<p>` elements that are direct children of a `<div>` will be styled with blue text. If a `<p>` is nested inside another element within the `<div>`, it will not be affected.


# role attribute
- To increase the page accessibility, the role attribute can be used to indicate the purpose behind an element on the page to assistive technologies. 
- The role attribute is a part of the Web Accessibility Initiative (WAI), and accepts preset values.
- Every region role requires a label, which helps screen reader users understand the purpose of the region. 
- One method for adding a label is to add a heading element inside the region and then reference it with the aria-labelledby attribute.
- For example:
```html
<main>
			<form action="https://freecodecamp.org/practice-project/accessibility-quiz" method="post">
				<section role="region" aria-labelledby="student-info">
					<h2 id="student-info">Student Infomation</h2>
				</section>
				<section role="region" aria-labelledby="html-questions">
					<h2 id="html-questions">HTML Questions</h2>
				</section>
				<section role="region" aria-labelledby="css-questions">
					<h2 id="css-questions">CSS Questions</h2>
				</section>
			</form>
		</main>
```


# typeface
- Typeface plays an important role in the accessibility of a page. 
- Some fonts are easier to read than others, and this is especially true on low-resolution screens.

# Placeholders
- can be confusing, seeming there is already a value. Rely on the label instead.

# Hide text for only screen readers to read
- There is a common pattern to visually hide text for only screen readers to read.
- This pattern is to set the following CSS properties:
```css
.sc-only {
	position: absolute;
	width: 1px;
	height: 1px;
	overflow: hidden;
	clip: rect(0, 0, 0, 0);
	clip-path: inset(50%);
	white-space: nowrap;
}
```
- sc-only (screen readers only)



# style guide
- https://design-style-guide.freecodecamp.org/ 