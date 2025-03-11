# Create a section element
- used to define sections in a document, such as chapters, headers, footers, or any other sections of the document. 
- groups related elements together.
- It is a semantic element that helps with SEO and accessibility.
- For example:
```html
<section>
    <h2>Cat Photos</h2>
    <p>Everyone loves <a href="https://cdn.freecodecamp.org/curriculum/cat-photo-app/running-cats.jpg">cute cats</a> online!</p>
    <p>See more <a target="_blank" href="https://freecatphotoapp.com">cat photos</a> in our gallery.</p>
    <a href="https://freecatphotoapp.com"><img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back."></a>
</section>

<section>
    <h2>Cat Lists</h2>
	<h3>Things cats love:</h3>
	<ul>
        <li>cat nip</li>
        <li>laser pointers</li>
        <li>lasagna</li>
    </ul>

    <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/lasagna.jpg" alt="A slice of lasagna on a plate.">
</section>
```

# Figure elements
- represents self-contained content and will allow you to associate the content with a caption using the figcaption element.
- For example:
```html
<figure>
    <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/lasagna.jpg" alt="A slice of lasagna on a plate.">
	<figcaption>Cats love lasagna.</figcaption>
</figure>
```

# Emphasize Text with the em Element
- used to emphasize text.
- For example:
```html
<figcaption>Cats <em>love</em> lasagna.</figcaption>
```
- italicizes the text.

# Strong Element
- used to indicate importance of text.
- For example:
```html
<figcaption>Cats <strong>hate</strong> other cats.</figcaption>
```
- makes the text bold.

