# Attributes in HTML

**Attributes** are properties or characteristics added to HTML elements to define their behavior, appearance, or content. They are always defined within the opening tag of an element in the form of **name-value pairs**.

### General Structure of Attributes

```html
<tagname attributeName="attributeValue">Content</tagname>
```

---

## Key Characteristics of Attributes

1. **Optional**: Attributes are optional, but they enhance the functionality of an element.
2. **Key-Value Pair**: They are written as `attributeName="attributeValue"`.
3. **Case-Insensitive**: Attribute names are case-insensitive but conventionally written in lowercase.

---

## Common HTML Attributes

| Attribute | Description | Example |
|-----------|-------------|---------|
|`id`|Provides a unique identifier for the element.|`<div id="header"></div>`|
|`class`|Assigns one or more classes to an element for styling or scripting.|`<p class="text-bold"></p>`|
|`style`|Applies inline CSS styles to an element.|`<p style="color: red;">Hello</p>`|
|`title`|Adds a tooltip when the user hovers over the element.|`<a title="Click to visit Google">Google</a>`|
|`src`|Specifies the source URL for media elements like images, videos, or scripts.|`<img src="image.jpg">`|
|`alt`|Provides alternate text for an image if it cannot be displayed.|`<img src="image.jpg" alt="Description">`|
|`href`|Defines the URL of a link.|`<a href="https://example.com">Link</a>`|
|`target`|Specifies where to open the linked document.|`<a href="#" target="_blank">New Tab</a>`|
|`disabled`|Disables an element (commonly used for buttons or inputs).|`<input type="text" disabled>`|
|`value`|	Specifies the value of an input element.|`<input type="text" value="Default Text">`|
|`placeholder`|Provides a hint in an input field.|`<input type="text" placeholder="Enter Name">`|

---

#### Attribute Example

```
<a href="https://example.com" target="_blank" title="Visit Example">Click Here</a>
```

---

## HTML Event

**Events** are actions or occurrences that happen in the browser, often triggered by user interactions or browser activities. They allow developers to execute scripts when specific actions take place.

---

## Event Categories

1. Mouse Events
   - Triggered by mouse actions like clicks, hovering, or movement.
   - Examples:
     - `onclick`: Fires when an element is clicked.
     - `onmouseover`: Fires when the mouse pointer hovers over an element.
     - `onmouseout`: Fires when the mouse pointer leaves an element.
    
2. Keyboard Events
   - Triggered by keyboard actions like pressing or releasing keys.
   - Examples:
       - `onkeydown`: Fires when a key is pressed down.
       - `onkeyup`: Fires when a key is released.
       - `onkeypress`: Fires when a key is pressed (deprecated in modern browsers).
3. Form Events
   - Triggered by user interactions with form elements.
   - Examples:
       - `onsubmit`: Fires when a form is submitted.
       - `onfocus`: Fires when an element gains focus.
       - `onblur`: Fires when an element loses focus.
       - `onchange`: Fires when the value of an element changes.
5. Window/Document Event
   - Triggered by browser activities like loading or resizing.
   - Examples:
       - `onload`: Fires when a page or resource has loaded.
       - `onresize`: Fires when the browser window is resized.
       - `onunload`: Fires when a page is unloaded.
    
## How to Use Events

1. Inline Events
   - Events can be added directly to HTML elements.
```html
<button onclick="alert('Button Clicked!')">Click Me</button>
```

2. JavaScript Event Handlers

   - Events can be assigned in JavaScript for better separation od concerns.
  
```html
<button id="myButton">Click Me</button>
<script>
 document.getElementById("myButton").onclick = function() {
     alert("Button Clicked!");
 };
</script>
 ```

3. Event Listners

   - The `addEventListner` method is the most robust way to handle events.
```html
<button id="myButton">Click Me</button>
<script>
    document.getElementById("myButton").addEventListener("click", function() {
        alert("Button Clicked!");
    });
</script>
```


---


## Common Events

| Event | Description | Example |
|-------|-------------|---------|
|`onclick`|Triggers when an element is clicked.|`<button onclick="doSomething()">Click</button>`|
|`oncharge`|Fires when the value of an input changes.|`<input onchange="validate()">`|
|`onmouseover`|Fires when the mouse hovers over an element.|`<div onmouseover="highlight()">Hover Me</div>`|
|`onkeydown`|Fires when a key is pressed down.|`<input onkeydown="logKey()">`|
|`onload`|Fires when a page/resource finishes loading.|`<body onload="initPage()">`|
|`onfocus`|Fires when an element gains focus.|`<input onfocus="highlightField()">`|


---

### Events Example

```html
<form onsubmit="return validateForm()">
    <input type="text" id="username" placeholder="Enter Username" onblur="checkInput()">
    <button type="submit">Submit</button>
</form>
<script>
    function validateForm() {
        alert("Form Submitted!");
        return false; // Prevents form submission for demo purposes
    }
    function checkInput() {
        alert("Input Lost Focus!");
    }
</script>
```

---

## Combining Attributes and Events

```html
<input type="text" id="name" placeholder="Enter Name" onchange="validateName()" required>
```

Attributes define the properties of the element, while events define interactivity. Together, they make web pages dynamic and responsive. 
