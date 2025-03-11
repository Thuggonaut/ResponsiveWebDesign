# Anchor elements

# Links to external pages
- a is short for anchor
- open/close tags <a href=""> and </a>
- a elements need a destination web address href and an anchor text
- For example:
```html
<a href="https://www.freecodecamp.org">this links to freecodecamp.org</a>
```
- The browser will display the text this links to freecodecamp.org as a link you can click.

# Links to internal pages
- Links to different sections within a webpage
- Creating an internal link:
	- usually further down the page
	- Assign a link's href attribute to a # hash symbol followed by the value of the id attribute of the element you want to link to.
	- Then, add the same id attribute to the element you are linking to.
	- An id attribute uniquely describes an element.
- For example:
```html
<a href="#contacts-header">Contacts</a> <!-- Internal anchor link -->
...
<h2 id="contacts-header">Contacts</h2> <!-- Target element and destination -->
```
- When users click the Contacts link, they'll be taken to the section of the webpage with the Contacts heading element.
- For example:
```html
<h2>CatPhotoApp</h2>
<main>

  <a href="#footer">Jump to Bottom</a>

  <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back.">

  <p>Kitty ipsum dolor</p>

</main>

<footer id="footer">Copyright Cat Photo App</footer>
```

# Nest an Anchor Element within a Paragraph
-  Nest links within other text elements.
- For example:
```html
<p>
  View more <a href="https://www.freecatphotoapp.com" target="_blank">cat photos</a>
</p>
```
- View more - normal text wrapped in p
- target= specifies where to open tab, _blank specifies new tab
- cat photos is the anchor text and will display the link to click


# Dead links using href="#"
- Often referred to as a "broken link," is a hyperlink that no longer leads to a valid destination. This can happen for several reasons:
	- The target webpage has been moved or deleted.
	- The URL has been changed or mistyped.
	- The server hosting the webpage is down.
- When users click on a dead link, they typically encounter a "404 Not Found" error or a similar message.
- For example:
```html
<p>Click here to view more <a href="#" target="_blank">cat photos</a>.</p>
```

# Turn an Image into a link
- by nesting them within an a element.
- For example:
```html
<a href="#"><img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back."></a>
```

