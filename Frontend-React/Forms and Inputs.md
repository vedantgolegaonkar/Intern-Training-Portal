# Forms in HTML

A **form** in HTML is a container for collecting user inputs and sending them to a server for processing. It is created using the `<form>` element.


### Key Attributes of `<form>`:
1. `action`: Specifies the URL where the form data will be sent.

```html
<form action="submit.php"></form>
```

2. `method`: Defines the HTTP method used to send the form data:

- `GET`: Appends data to the URL (visible to users). Suitable for non-sensitive data.
- `POST`: Sends data in the body of the request. Preferred for sensitive data.

```html
<form action="submit.php" method="POST"></form>
```

3. `enctype`: Specifies how the form data should be encoded when submitted. Common values:

- `application/x-www-form-urlencoded` (default).
- `multipart/form-data` (for file uploads).
  
4. `name`: Assigns a name to the form, which can be used in scripts.

5. `target`: Specifies where to display the response (e.g., `_self`, `_blank`).

```html
<form action="/submit" method="POST">
    <label for="name">Name:</label>
    <input type="text" id="name" name="user_name">
    <button type="submit">Submit</button>
</form>
```

---

# Inputs in HTML

Inputs are the elements within a form that allow users to provide data. The `<input>` tag is one of the most versatile elements for capturing user input.

#### Common Input Types:

| Input Type | Description | Example |
|------------|-------------|---------|
|`text`|A single-line text field for general input.|`<input type="text" name="username">`|
|`password`|A single-line text field that hides the input (e.g., passwords).|`<input type="password" name="password">`|
|`email`|A field for email addresses with built-in validation.|`<input type="email" name="user_email">`|
|`number`|A field for numeric input with optional min/max/step attributes.|`<input type="number" min="1" max="100">`|
|`checkbox`|A box for selecting one or multiple options.|`<input type="checkbox" name="subscribe">`|
|`radio`|A circular button for selecting one option from a group.|`<input type="radio" name="gender">`|
|`date`|A field for selecting a date.|`<input type="date" name="dob">`|
|`file`|A field for file uploads.|`<input type="file" name="upload">`|
|`submit`|A button to submit the form.|`<input type="submit" value="Submit">`|
|`reset`|A button to reset the form fields to their default values.|`<input type="reset" value="Reset">`|
|`hidden`|An invisible input for passing data silently.|`<input type="hidden" name="token">`|

---

#### Attributes of `<input>`:

1. `type`: Specifies the type of input.
2. `name`: Assigns a name to the input for identifying the data in form submissions.
3. `id`: Links the input with a `<label>` for accessibility.
4. `placeholder`: Displays a hint inside the input field.

```html
   <input type="text" placeholder="Enter your name">
```
5. `required`: Makes the input field mandatory.
6. `value`: Specifies a default value for the input field.
7. `maxlength` and `minlength`: Define the character limits for text inputs.
8. `readonly`: Makes the input non-editable.
9. `disabled`: Disables the input field.

---

#### Input Example:

```html
<form action="/submit" method="POST">
    <label for="email">Email:</label>
    <input type="email" id="email" name="user_email" placeholder="Enter your email" required>
    <label for="password">Password:</label>
    <input type="password" id="password" name="user_password" required>
    <button type="submit">Login</button>
</form>
```

---

### Advance Inputs and Forms

1. **Text Areas**: For multi-line text inputs.
```html
<textarea name="message" rows="4" cols="50"></textarea>
```

2. **Dropdown Menus**: For selecting options:
```html
<select name="options">
    <option value="option1">Option 1</option>
    <option value="option2">Option 2</option>
</select>
```

3. **Buttons**: For custom actions:
```html
<button type="button" onclick="alert('Clicked!')">Click Me</button>
``` 

5. **Validation**: Modern browsers automatically validate inputs with attributes like `required`, `pattern`, `maxlength`, etc.
