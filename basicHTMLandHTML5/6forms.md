# Create a web form
- input elements are used to get inputs from users
- input elements are void (self-closing)
- For example:
```html
<input type="text">
```

# Placeholder text
- Placeholder text is what is displayed in your input element before your user has inputted anything.
- For example:
```html
  <input type="text" placeholder="cat photo URL">
```

# Action attributes
- web forms can submit data to a server using nothing more than pure HTML. 
- You can do this by specifying an action attribute on your form element.
- For example:
```html
<form action="https://www.freecatphotoapp.com/submit-cat-photo">
  <input type="text" placeholder="cat photo URL">
</form>
```

# Submit button
- Clicking this button will send the data from your form to the URL you specified with your form's action attribute.
- For example:
```html
<form action="https://www.freecatphotoapp.com/submit-cat-photo">
  <input type="text" placeholder="cat photo URL">
  <button type="submit">Submit</button>
</form>
```

# Require input fields using HTML5
- required attribute
- require specific form fields so that your user will not be able to submit your form until it is filled out.
- For example:
```html
<form action="https://www.freecatphotoapp.com/submit-cat-photo">
    <input type="text" placeholder="cat photo URL"required>
    <button type="submit">Submit</button>
  </form>
```

# Create a Set of Radio Buttons
- radio buttons are a set of options where only one option can be selected.
- radio buttons are a type of input element.
- Each radio button can be nested within its own label element.
- By wrapping an input element inside of a label element it will automatically associate the radio button input with the label element surrounding it.
- All related radio buttons should have the same name attribute to create a radio button group. 
- By creating a radio group, selecting any single radio button will automatically deselect the other buttons within the same group ensuring only one answer is provided by the user.
- For example:
```html
<form action="https://www.freecatphotoapp.com/submit-cat-photo">
  <label>
      <input type="radio" name="indoor-outdoor">Indoor
  </label>
  <button type="submit">Submit</button>
</form>
```
- It's best practice to set a for attribute on the label element, with a value that matches the value of the id attribute of the input element. 
- This allows assistive technologies to create a linked relationship between the label and the related input element.
- For example:
```html
<form action="https://www.freecatphotoapp.com/submit-cat-photo">
  <label for="indoor">
    <input id="indoor" type="radio" name="indoor-outdoor">Indoor
  </label>
  <label for="outdoor">
    <input id="outdoor" type="radio" name="indoor-outdoor">Outdoor
  </label><br>
  <button type="submit">Submit</button>
</form>
```

# Use the value attribute
- allows you to specify the value that will be sent when a checkbox is selected.
- The form data for the button is based on its name and value attributes.
- Your radio buttons do not have a value attribute, the form data will include indoor-outdoor=on, which is not useful when you have multiple buttons.
- We set the button's value attribute to the same value as its id attribute.
- For example:
```html
<label><input id="indoor" type="radio" name="indoor-outdoor" value="indoor"> Indoor</label>
<label><input id="outdoor" type="radio" name="indoor-outdoor" value="outdoor"> Outdoor</label>
```

# Fieldset elements
- used to group related inputs and labels together in a web form.
- fieldset elements are block-level elements, so they will appear on a new line.
- For example:
```html
<fieldset>
  <label><input id="indoor" type="radio" name="indoor-outdoor" value="indoor"> Indoor</label>
  <label><input id="outdoor" type="radio" name="indoor-outdoor" value="outdoor"> Outdoor</label>
</fieldset>
```

# Legend elements
- acts as a caption for the content of the fieldset.
- Giving users context about what they should enter in the specific part of the form.
- For example:
```html
<fieldset>
  <legend>Is your cat an indoor or outdoor cat?</legend>
  <label><input id="indoor" type="radio" name="indoor-outdoor" value="indoor"> Indoor</label>
</fieldset>
```

# Create a Set of Checkboxes
- may have more than one answer.
- Checkboxes are a type of input element.
- Each checkbox can be nested within its own label element.
- By wrapping an input element inside of a label element it will automatically associate the checkbox input with the label element surrounding it.
- All related checkboxes should have the same name attribute to create a checkbox group. 
- It is best practice to explicitly define the relationship between a checkbox input and its corresponding label by setting the for attribute on the label element to match the id attribute of the associated input element.
- For example:
```html
<fieldset>
  <legend>What's your cat's personality?</legend>
  <input id="loving" type="checkbox" name="personality" value="loving"> <label for="loving">Loving</label>
  <input id="lazy" type="checkbox" name="personality" value="lazy"> <label for="lazy">Lazy</label>
  <input id="energetic" type="checkbox" name="personality" value="energetic"> <label for="energetic"> Energetic</label>
</fieldset>
```

# checked attribute
- Used to make a checkbox checked or radio button selected by default.
- There's no need to set a value to the checked attribute. Instead, just add the word checked to the input element.
- For example:
```html
<fieldset>
  <legend>Is your cat an indoor or outdoor cat?</legend>
  <label><input id="indoor" type="radio" name="indoor-outdoor" value="indoor" checked> Indoor</label>
  <label><input id="outdoor" type="radio" name="indoor-outdoor" value="outdoor"> Outdoor</label>
</fieldset>
```

