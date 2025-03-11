# Send form data
- The action attribute of the form element determines where the form data is sent, e.g. URL specified in the action attribute.
- The method attribute of the form element determines how the form data is sent.
	- GET: Appends form data to the URL in name/value pairs. (method="get")
	- POST: Encodes form data and sends it in the body of the HTTP request. (method="post")
- For example:
```html
<form action='https://register-demo.freecodecamp.org' method="post"></form>
```


# Basic form setup

## 1. Add a form element:
```html
<form>
</form>
```

## 2. Add action for data to be sent to:
```html
<form action="/url-where-you-want-to-submit-form-data">
</form>
```

## 3. Add method for data to be sent with:
```html
<form action="/url-where-you-want-to-submit-form-data" method="get">
</form>
```
or
```html
<form action="/url-where-you-want-to-submit-form-data" method="post">
</form>
```

## 4. Add form fields:
```html
<form>
	<fieldset></fieldset>
</form>
```

## 5. Add labels:
```html
<form>
	<fieldset>
		<label>Name</label>
		<label>Email</label>
		<label>Password</label>
	</fieldset>
</form>
```

## 6. Display the labels on seperate lines:
- As label elements are inline by default, they are all displayed side by side on the same line.
- To make them appear on separate lines, add `display: block` to the label element, and add a margin of 0.5rem 0 for example
- The rem unit stands for root em, and is relative to the font size of the html element.
```css
label {
	display: block;
	margin: 0.5rem 0;
}
```

## 7. Add input fields:
- Don't forget the space after the colon
```html
<form>
	<fieldset>
        <label>Enter Your First Name: <input></label>
        <label>Enter Your Last Name: <input></label>
        <label>Enter Your Email: <input></label>
        <label>Create a New Password: <input></label>
      </fieldset>
</form>
```
- Following accessibility best practices, link the input elements and the label elements together using the for attribute:
```html
<fieldset>
    <label for="first-name">Enter Your First Name: <input id="first-name"/></label>
    <label for="last-name">Enter Your Last Name: <input id="last-name"/></label>
    <label for="email">Enter Your Email: <input id="email"/></label>
    <label for="new-password">Create a New Password: <input id="new-password"/></label>
</fieldset>
```

## 8. Specify the type of input:
- Specifying the type attribute of a form element is important for the browser to know what kind of data it should expect. 
- If the type is not specified, the browser will default to text.
- The following types are commonly used:
	- text
	- email (only allows emails with a @ and a . in the domain)
	- password (obscures the input, and warns if the site does not use HTTPS)
	- submit (creates a submit button)
- The first input element with a type of submit is automatically set to submit its nearest parent form element.
```html
<fieldset>
    <label for="first-name">Enter Your First Name: <input id="first-name" type="text"/></label>
    <label for="last-name">Enter Your Last Name: <input id="last-name" type="text"/></label>
    <label for="email">Enter Your Email: <input id="email" type="email"/></label>
    <label for="new-password">Create a New Password: <input id="new-password" type="password"/></label>
</fieldset>
<fieldset>
</fieldset>
	<input type="submit" value="Submit">
```

## 9. Make the form interactive:
- Use the required attribute to make an input field required.
```html
<label for="first-name">Enter Your First Name: <input id="first-name" type="text" required/></label>
<label for="last-name">Enter Your Last Name: <input id="last-name" type="text" required/></label>
```
- Use the minlength and maxlength attributes to limit the length of the input.
```html
<label for="new-password">Create a New Password: <input id="new-password" type="password" required minlength="8"/></label>
```
- Use the pattern attribute to define a regular expression that the password must match to be considered valid.
```html
<label for="new-password">Create a New Password: <input id="new-password" type="password" pattern="[a-z0-5]{8,}" required /></label>
```

## 10. Add radio buttons
- relate them to the same name, and only one can be selected
```html
<label><input type="radio" name="account-type" /> Personal</label>
<label><input type="radio" name="account-type" /> Business</label>
```

## 11. Add a legend:
- Using the required attribute on both the radio buttons will cause confusion to users, as they will think they need to select both.
- To solve this, you can provide context of what is needed by adding a legend element with text Account type (required) before the label elements within the second fieldset. 
- Then add the checked attribute to the Personal input to ensure the form is submitted with the required data in it.
```html
<fieldset>
    <legend>Account type (required)</legend>
    <label><input type="radio" name="account-type" checked/> Personal</label>
    <label><input type="radio" name="account-type" /> Business</label>
</fieldset>
```
- Follow accessibility best practices by linking the input elements and the label elements in the second fieldset
```html
<fieldset>
    <legend>Account type (required)</legend>
    <label for="personal-account"><input id="personal-account" type="radio" name="account-type" checked/> Personal</label>
    <label for="business-account"><input id="business-account" type="radio" name="account-type" /> Business</label>
</fieldset>
```

## 12. Add a checkbox
- Use the checked attribute to make the checkbox selected by default.
```html
<label for="terms-and-conditions"><input id="terms-and-conditions" type="checkbox" required /> I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/"> terms and conditions</label>
```

## 13. Allow user upload of files:
```html
<fieldset>
    <label><input type="file"> Upload a profile picture:</label>
</fieldset>
```

## 14. Digit inputs
```html
<fieldset>
    <label>Upload a profile picture: <input type="file" /></label>
    <label><input type="number" min="13" max="120"> Input your age (years):</label>
</fieldset>
```

## 15. Dropdown menus
- The select element is a container for a group of option elements, and the option element acts as a label for each dropdown option. Both elements require closing tags.
```html
<fieldset>
    <label>Upload a profile picture: <input type="file" /></label>
    <label>Input your age (years): <input type="number" min="13" max="120" /></label>
    <label>How did you hear about us?
        <select>
            <option>(select one)</option>
            <option>freeCodeCamp News</option>
            <option>freeCodeCamp YouTube Channel</option>
            <option>freeCodeCamp Forum</option>
            <option>Other</option>
        </select>
    </label>
</fieldset>
```
- Submitting the form with an option selected would not send a useful value to the server.
- As such, each option needs to be given a value attribute. 
- With the value attribute, the selected option will be sent as the text content of the option element to the server.
```html
<label>How did you hear about us?
    <select>
        <option value="">(select one)</option>
        <option value="1">freeCodeCamp News</option>
        <option value="2">freeCodeCamp YouTube Channel</option>
        <option value="3">freeCodeCamp Forum</option>
        <option value="4">Other</option>
    </select>
</label>
```

## 16. Add a textarea
- The textarea element acts like an input element of type text but can create a multi-line text input, and an initial number of text rows and columns.
```html
<label>Provide a bio <textarea></textarea></label>
```
- best practice:
```html
<fieldset>
    <label for="profile-picture">Upload a profile picture: <input type="file" id="profile-picture" /></label>
    <label for="age">Input your age (years): <input id="age" type="number" min="13" max="120" /></label>
    <label for="referrer">How did you hear about us?
        <select id="referrer">
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
        </select>
    </label>
    <label for="bio">Provide a bio:
        <textarea id="bio"></textarea>
    </label>
</fieldset>
```
- adjust the size of the textarea by adding rows and cols attributes.
```html
<label for="bio">Provide a bio:
    <textarea id="bio" rows="3" cols="30"></textarea>
</label>
```

## 17. Add a placeholder
- The placeholder attribute provides a hint to the user about what to enter in the input field.
```html
<label for="bio">Provide a bio:
    <textarea id="bio" rows="3" cols="30" placeholder="I like coding on the beach..."></textarea>
</label>
```

## 18. Name attributes
- With form submissions, it is useful, and good practice, to provide each submittable element with a name attribute. This attribute is used to identify the element in the form submission.
```html
<fieldset>
    <label for="first-name">Enter Your First Name: <input id="first-name" type="text" required name="first name"/></label>
    <label for="last-name">Enter Your Last Name: <input id="last-name" type="text" required name="last name"/></label>
    <label for="email">Enter Your Email: <input id="email" type="email" required name="email"/></label>
    <label for="new-password">Create a New Password: <input id="new-password" type="password" pattern="[a-z0-5]{8,}" required name="password"/></label>
</fieldset>
```

## 19. Spruce it up!
```css
h1, p {
  margin: 1em auto;
  text-align: center;
}

form {
  margin: 0 auto;
  max-width: 500px;
  min-width: 300px;
  width: 60vw;
  padding-bottom: 2rem;
}

/* Remove fieldset default border */
fieldset {
  border: none;
  padding-top: 2rem;
  padding-bottom: 2rem;
  padding-left: 0;
  padding-right: 0;
}
```
- Give the fieldset elements some separation:
```css
fieldset {
  border: none;
  padding: 2rem 0;
  border-bottom: 3px solid #3b3b4f;
}
```
- You can select the last element of a specific type using the last-of-type CSS pseudo-class, like this:
```css
p:last-of-type { }
```
- For example:
```css
fieldset:last-of-type {
  border-bottom: none;
}
```
- Have the label text appear above the form elements.
- Make the child elements take up the full width of their parent elements.
```css
input, textarea, select {
  width: 100%;
  margin-top: 10px;
  margin-bottom: 0;
  margin-left: 0;
  margin-right: 0;
}
```
- Have the input and label elements sit on the same line.
```css
.inline {
  width: unset; /* Overrides the earlier width: 100% */
  margin-right: 0.5em;
  margin-left: 0;
  margin-top: 0;
  margin-bottom: 0;
  vertical-align: middle; /* Aligns the elements in the middle of the line */
}
```
```html
<fieldset>
        <legend>Account type (required)</legend>
        <label for="personal-account"><input class="inline" id="personal-account" type="radio" name="account-type" checked /> Personal</label>
        <label for="business-account"><input class="inline" id="business-account" type="radio" name="account-type" /> Business</label>
      </fieldset>
```
- Make the input and textarea elements blend with the background theme:
```css
input, textarea {
  background-color: #0a0a23;
  border: 1px solid #0a0a23;
  color: #ffffff; /* White text */
  min-height: 2em; /* Input height */
}
```

## 20. Style the submit button
- Using the attribute selector, which selects an element based on the given attribute value:
```css
input[name="password"]
```
- For example:
```css
input[type="submit"] {
  display: block;
  width: 60%;
  margin: 0 auto; /* Centers the button */
  height: 2em;
  font-size: 1.1rem;
  background-color: #3b3b4f;
  border-color: white;
  min-width: 300px;
}
```
- Make the input the same size as the other input elements, to combat the default CSS properties:
```css
input[type="file"] {
  padding: 1px 2px;
}
```
- Make the input for the terms and conditions inline by adding the appropriate class:
```html
<label for="terms-and-conditions"><input class="inline" id="terms-and-conditions" type="checkbox" required /> I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/"> terms and conditions</a></label>
```