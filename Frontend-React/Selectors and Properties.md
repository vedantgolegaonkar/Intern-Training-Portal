# CSS Selectors and Properties

CSS (Cascading Style Sheets) is used to style HTML elements, making webpages visually appealing and interactive. Two foundational concepts in CSS are selectors and properties, which work together to style HTML elements.

---

# 1. Selectors
**Selectors** are patterns used in CSS to target HTML elements for styling. They define which elements will be affected by the styles.

## Types of Selectors
**a. Basic Selectors**

| Selector Type | Syntax |Description| Example |
|---------------|--------|-----------|---------|
|Universal|`*`|Targets all elements on the page.|`* { margin: 0; }`|
|Type|`tagname`|Targets all elements of a specific tag.|`p { color: blue; }`|
|Class|`.classname`|Targets all elements with a specific class attribute.|`.btn { background: green; }`|
|ID|`#idname`|Targets a single element with a specific ID.|`#header { font-size: 20px; }`|


**b. Attribute Selectors**

|Selector Type|Syntax|Description|Example|
|--------------|-----|-----------|-------|
|[attribute]|`[attr]`|Targets elements with a specific attribute.|`[type="text"] { color: red; }`|
|[attribute=value]|`[attr=value]`|Targets elements with an attribute matching a value.|`[href="https://example.com"] { color: green; }`|

**c. Grouping and Combining Selectors**

| Selector Type | Syntax |Description| Example |
|---------------|--------|-----------|---------|
|Grouping|`selector1, selector2`|Applies the same style to multiple selectors.|`h1, h2 { font-family: Arial; }`|
|Descendant|`ancestor descendant`|Targets elements within a specific ancestor.|`div p { font-size: 14px; }`|
|Child|`parent > child`|Targets direct child elements of a parent.|`ul > li { margin: 5px; }`|
|Adjacent|`element1 + element2`|Targets the next sibling element immediately after another.|`h1 + p { color: gray; }`|
|General|`element1 ~ element2`|Targets all siblings after a specified element.|`h1 ~ p { color: blue; }`|

**d. Pseudo-Classes and Pseudo-Elements**

| Type | Syntax |Description| Example |
|---------------|--------|-----------|---------|
|Pseudo-Class|`selector:pseudo-class`|Targets elements based on their state or position.|`a:hover { color: red; }`|
|Pseudo-Elements|`selector::pseudo-el`|Targets a specific part of an element.|`p::first-line { font-weight: bold; }`|

---


# 2. Properties

**Properties** define the styles applied to selected elements. They are written as **property-value pairs** inside curly braces {}.

### Basic Syntax 
```html
selector {
    property: value;
}
```

---

### COmmon CSS Properties

**a. Text and Font Properties**

|Property|Description|Example|
|--------|-----------|-------|
|`color`|Sets the text color.|`color: blue;`|
|`font-size`|Sets the size of the font.|`font-size: 16px;`|
|`font-family`|Specifies the font.|`font-family: Arial;`|
|`text-align`|Aligns text horizontally.|`text-align: center;`|
|`text-decoration`|Adds or removes text decorations.|`text-decoration: underline;`|

**b. Background and Border Properties**

|Property|Description|Example|
|--------|-----------|-------|
|`background-color`|Sets the background color of an element.|`background-color: yellow;`|
|`background-image`|Sets an image as the background.|`background-image: url('img.jpg');`|
|`border`|Sets the style, width, and color of a border.|`border: 2px solid red;`|
|`border-radius`|Rounds the corners of an element.|`border-radius: 10px;`|

**c. Box Model Properties**

|Property|Description|Example|
|--------|-----------|-------|
|`margin`|Sets the space outside an element.|`margin: 10px;`|
|`padding`|Sets the space inside an element, around content.|`padding: 5px;`|
|`width`|Sets the width of an element.|`width: 200px;`|
|`height`|Sets the height of an element.|`height: 100px;`|

**d. Display and Positioning**

|Property|Description|Example|
|--------|-----------|-------|
|`display`|Specifies how an element is displayed.|`display: block;`|
|`position`|Specifies the positioning method.|`position: absolute;`|
|`top`,`left`|Sets the position relative to its container.|`top: 20px; left: 50px;`|

---

## Example: Using Selectors and Properties Together

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Selectors and Properties Example</title>
    <style>
        /* Universal Selector */
        * {
            margin: 0;
            padding: 0;
        }

        /* Type Selector */
        h1 {
            color: blue;
            text-align: center;
        }

        /* Class Selector */
        .intro {
            font-size: 18px;
            color: gray;
        }

        /* ID Selector */
        #main {
            background-color: lightgray;
            padding: 20px;
            border-radius: 10px;
        }

        /* Pseudo-Class Selector */
        a:hover {
            color: red;
        }
    </style>
</head>
<body>
    <h1>Welcome to CSS Basics</h1>
    <p class="intro">This is an introduction to CSS selectors and properties.</p>
    <div id="main">
        <p>This section is styled using an ID selector.</p>
    </div>
    <a href="#">Hover over me</a>
</body>
</html>
```

## Conclusion
- Selectors are used to target specific HTML elements.
- Properties define the styles for the targeted elements.
- Together, they form the core of CSS, allowing developers to create visually appealing and user-friendly designs.


