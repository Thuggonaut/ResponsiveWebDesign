# CSS files
- Usefule since there would be many styles, we can use css files to manage them.
- Ensure to exclude the <style> tag when using css files:
```css
h1, h2, p {
  text-align: center;
}
```
- Link the css file to the html file by using the link element in the head element.
- The rel attribute specifies the relationship between the current document and the linked resource.
- For example:
```html
<head>
    <meta charset="utf-8" />
    <title>Cafe Menu</title>
    <link rel="stylesheet" href="styles.css">
</head>
```