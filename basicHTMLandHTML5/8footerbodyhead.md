# footer element
- used to contain information about the author, copyright, contact information, sitemap, and other links.
- It's usually the last element inside the body element, after the main element.
- For example:
```html
<footer>
  <p>No Copyright - <a href="https://www.freecodecamp.org">freeCodeCamp.org</a></p>
</footer>
```

# body element
- All page content that is rendered to a page is contained within the body element.
- For example:
```html
<body>
  <h1>Hello World</h1>
</body>
```

# head element
- Contains metadata about the page such as the title, character set, styles, and scripts. Information that isn't displayed on the page.
- For example:
```html
<html>
  <head>
  </head>
  <body>
  </body>
</html>
```

# title element
- determines what browsers show in the title bar or tab for the page.
- For example:
```html
<head>
  <title>CatPhotoApp</title>
</head>
```

# html element
- The root element that wraps all the content on the page.
- You can also specify the language of your page by adding the lang attribute to the opebing html tag.
- For example:
```html
<html lang="en">
</html>
```


# Declaration string
- All pages should begin with <!DOCTYPE html>. 
- This special string is known as a declaration and ensures the browser tries to meet industry-wide specifications.
- <!DOCTYPE html> tells browsers that the document is an HTML5 document which is the latest version of HTML.
- For example:
```html
<!DOCTYPE html>
<html lang="en">
```

# meta element
- You can set browser behavior by adding meta elements in the head.
- For example:
```html
<head>
  <meta charset="utf-8"> <!-- tells the browser how to encode characters for the page -->
  <title>CatPhotoApp</title>
</head>
```
