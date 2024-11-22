# 1. Flexbox (Flexible Box Layout)

The **Flexbox** layout module is ideal for one-dimensional layouts—either in a row (**horizontal**) or a column (**vertical**). It helps distribute space dynamically and align items efficiently, even when the size of the items is unknown.

## Key Features of Flexbox
  - Works in one dimension (row or column).
  - Aligns items horizontally, vertically, or both.
  - Distributes free space among items.
  - Reorders items within the container.

### Terminology
  - **Flex container**: The parent element where the flexbox layout is applied.
  - **Flex items**: The child elements inside the container.

### CSS Properties

**Flex Container Properties**

1. `display: flex;`
   - Enables flexbox for the container.
2. `flex-direction`
   - Defines the direction of the main axis.
   - Values:
       - `row` (default): Items are placed horizontally from left to right.
       - `row-reverse`: Items are placed horizontally from right to left
       - `column`: Items are placed vertically from top to bottom.
       - `column-reverse`: Items are placed vertically from bottom to top.

```html
.container {
    display: flex;
    flex-direction: row;
}
```

3. `justify-content`
   - Aligns items along the main axis
   - Values:
       - `flex-start` (default): Items are aligned at the start.
       - `flex-end`: Items are aligned at the end.
       - `center`: Items are centered.
       - `space-between`: Items are evenly spaced; no space at edges.
       - `space-around`: Items have equal space around them.

```html
.container {
    justify-content: space-between;
}
```

4. `align-items`
   - Aligns items along the cross axis (perpendicular to the main axis).
   - Values:
       - `stretch` (default): Items stretch to fill the container.
       - `flex-start`: Items align at the start.
       - `flex-end`: Items align at the end.
       - `center`: Items align at the center.
       - `baseline`: Items align based on their text baseline.

```html
.container {
    align-items: center;
}
```

5. `flex-wrap`
   - Controls whether items wrap onto multiple lines
   - Values:
       - `nowrap` (default): All items remain on a single line.
       - `wrap`: Items wrap onto multiple lines.
       - `wrap-reverse`: Items wrap onto multiple lines in reverse order.

```html
.container {
    flex-wrap: wrap;
}
```

6. `align-content`
   - Aligns rows of items when there are multiple lines.
   - Works only with `flex-wrap`.
   - Values: `flex-start`, `flex-end`, `center`, `space-between`, `space-around`, `stretch`.
  

### Flex Item Properties

1. `flex`
   - A shorthand for `flex-grow`, `flex-shrink`, and `flex-basis`.
   - Example:
```html
.item {
    flex: 1; /* Items grow to fill space equally */
}
```

2. `order`

   - Controls the order of items.
   - Default: `0`. Lower numbers appear first.
  
   - 
3. `align-self`

   - Overrides `align-items` for a specific item.
  


---

# 2. CSS Grid Layout

The **CSS** Grid layout module is a two-dimensional system that allows you to design layouts in rows and columns. It’s more powerful for complex layouts compared to Flexbox.

## Key Features of CSS Grid
   - Works in two dimensions: rows and columns.
   - Defines areas of the layout explicitly.
   - Places elements based on a grid template.

     
### Terminology
   - **Grid container**: The parent element where the grid layout is applied.
   - **Grid items**: The child elements inside the container.
   - **Grid lines**: Invisible lines that define rows and columns.


### CSS Properties

#### Grid Container Properties

1. `display: grid;`

   - Enables grid layout for the container.
   - Example:

```html
.container {
    display: grid;
}
```

2. `grid-template-rows` & `grid-template-columns`

   - Defines the size of rows and columns.
   - Values: Lengths (`px`, `%`, `em`, etc.), `auto`, or `fr` (fractional units).
   - Example:
```html
.container {
    grid-template-rows: 100px 200px; /* 2 rows: 100px and 200px */
    grid-template-columns: 1fr 2fr; /* 2 columns: 1/3 and 2/3 of space */
}
```


3. `grid-gap` (or `gap`)

   - Specifies spacing between rows and columns.
   - Example:
```html
.container {
    gap: 20px;
}
```


4. `grid-template-areas`

   - Names specific areas of the grid.
   - Example:
```html
.container {
    grid-template-areas: 
        "header header"
        "sidebar content";
}
```


5. `justify-items` & `align-items`

   - Align items within their grid cells along the horizontal and vertical axes.


6. `justify-content` & `align-content`

   - Align the entire grid within the container.

#### Grid Item Properties

1. `grid-column` & `grid-row`

   - Specifies the start and end lines for a grid item.
   - Example:

```html
.item {
    grid-column: 1 / 3; /* Spans columns 1 to 3 */
    grid-row: 2 / 4; /* Spans rows 2 to 4 */
}
```


2. `grid-area`

   - Assigns an item to a named grid area.

---


## Flexbox vs. Grid

|Feature|Flexbox|CSS Grid|
|-------|-------|--------|
|Layout Type|One-Dimensional|Two-Dimensional|
|Use Case|Aligning items in a row or column|Complex layouts with rows and columns|
|Alignment|Performed along the main and cross axes|Aligns in rows,columns, or both|
|Complexity|Simpler for smaller tasks|More powerful for large-scale layouts|


---

## When to Use
   - **Flexbox**: Use when aligning items in a single row or column, such as navigation bars or buttons.
   - **CSS Grid**: Use for defining complete page layouts or sections with rows and columns, such as dashboards or galleries.


Both modules can complement each other in complex designs!



































