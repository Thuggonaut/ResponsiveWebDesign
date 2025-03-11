# Descriptive tags
- Helps with Search Engine Optimization (SEO) and accessibility
- <main>
- <header>
- <footer>
- <article>
- <video>
- <section>
- <nav>
- <aside>
- For example:
```html
<main> 
  <h1>Hello World</h1> <!-- Child element -->
  <p>Hello Paragraph</p> <!-- Child element -->
</main>
```


# Element differences
- The difference between nesting elements inside <body>, <div>, <main>, <fieldset>, or <section> on a single page relates to their semantic meaning, structure, and intended use. Here’s a breakdown of each:
1. <body>
Purpose: The <body> element is the main container for all the content that is displayed on the web page.
Use Case: All visible elements (text, images, links, etc.) must be placed inside the <body>. It serves as the root of the document's content.

2. <div>
Purpose: A generic container with no semantic meaning.
Use Case: Used for grouping elements for styling or scripting purposes. It does not convey any specific meaning about the content it contains. It’s often used when no other semantic element is appropriate.

3. <main>
Purpose: Represents the main content of the document. There should be only one <main> element per page.
Use Case: It should contain content that is directly related to the central topic of the page. It helps search engines and assistive technologies identify the primary content.

4. <section>
Purpose: Represents a thematic grouping of content, typically with a heading.
Use Case: Used to divide content into distinct sections that are related. Each section can have its own heading, making it easier to navigate and understand the structure of the content.

5. <fieldset>
Purpose: Used to group related elements within a form, often with a <legend> to provide a caption.
Use Case: Ideal for organizing form controls, making it clear which controls are related to each other. It enhances accessibility for users of assistive technologies.

Summary of Differences:

Semantics: Using the appropriate element improves the meaning of your HTML, which is beneficial for SEO and accessibility.

Accessibility: Screen readers and other assistive technologies can better interpret the structure and purpose of your content based on the elements used.

Styling and Layout: Different elements can have default styles or behaviors that can be leveraged in CSS. For example, <section> and <main> may have different default margins or padding compared to <div>.