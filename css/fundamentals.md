# CSS Fundamentals — Day 03

## 1. What is CSS?

CSS stands for **Cascading Style Sheets**.

It is a stylesheet language used to control the appearance and layout of HTML documents.

CSS can control:

- Text color and size
- Background colors and images
- Width and height
- Spacing
- Borders
- Element positioning
- Page layouts
- Responsive designs

### HTML vs CSS

| HTML | CSS |
|---|---|
| Defines webpage structure | Controls webpage appearance |
| Uses elements and tags | Uses selectors and declarations |
| Creates headings, paragraphs, images | Styles headings, paragraphs, images |

Example:

HTML:
```html
<h1>Hello World</h1>
```

CSS:
```css
h1 {
    color: blue;
    font-size: 32px;
}
```

The HTML creates the heading, while CSS makes its text blue and changes its size.

## 2. CSS Syntax

A CSS rule contains a selector and a declaration block.

```css
h1 {
    color: blue;
    font-size: 32px;
}
```

Understanding the parts:

| Part | Meaning |
|---|---|
| `h1` | Selector |
| `{ }` | Declaration block |
| `color` | Property |
| `blue` | Property value |
| `color: blue;` | Declaration |

**General syntax:**

```css
selector {
    property: value;
}
```

A CSS rule can contain multiple declarations.

```css
p {
    color: gray;
    font-size: 18px;
    text-align: left;
}
```

Each declaration normally ends with a semicolon.

## 3. Three Ways to Add CSS

There are three common methods.

### A. Inline CSS

CSS is written directly inside an HTML element using the `style` attribute.

```html
<h1 style="color: blue;">Hello World</h1>
```

Advantages:
- Quick for a small, one-off style.

Disadvantages:
- Difficult to maintain across many elements.
- Mixes presentation with HTML structure.
- Not suitable for organizing larger websites.

### B. Internal CSS

CSS is written inside a `<style>` element, usually in the HTML document's `<head>`.

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>

    <style>
        h1 {
            color: blue;
        }

        p {
            font-size: 18px;
        }
    </style>
</head>
<body>
    <h1>Hello World</h1>
    <p>Welcome to my website.</p>
</body>
</html>
```

Useful for:
- A single HTML page.
- Small demonstrations.

### C. External CSS

CSS is written in a separate `.css` file and connected to HTML using the `<link>` element.

HTML:
```html
<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Hello World</h1>
    <p>Welcome to my website.</p>
</body>
</html>
```

CSS (`style.css`):
```css
h1 {
    color: blue;
}

p {
    font-size: 18px;
}
```

Advantages:
- Keeps HTML and CSS separate.
- Makes styles easier to maintain.
- Allows multiple HTML pages to use the same stylesheet.

**Important:** External CSS is the standard approach for organizing styles in most multi-page websites.

## 4. CSS Selectors

A selector identifies which HTML elements a CSS rule should style.

### A. Element Selector

Selects all elements with a particular HTML tag.

```css
p {
    color: gray;
}
```

This selects every `<p>` element.

### B. Class Selector

Selects elements with a particular class.

HTML:
```html
<p class="highlight">Important information</p>
<p>Normal paragraph</p>
```

CSS:
```css
.highlight {
    color: red;
}
```

A class selector starts with a dot (`.`).

One class can be used by multiple HTML elements.

### C. ID Selector

Selects an element with a particular ID.

HTML:
```html
<h1 id="main-title">Welcome</h1>
```

CSS:
```css
#main-title {
    color: green;
}
```

An ID selector starts with a hash (`#`).

An ID should be unique within an HTML document.

### D. Universal Selector

Selects all elements.

```css
* {
    margin: 0;
}
```

The `*` symbol is called the universal selector.

### E. Grouping Selector

Applies the same styles to multiple selectors.

```css
h1, h2, p {
    font-family: Arial, sans-serif;
}
```

The comma separates the selectors.

### F. Descendant Selector

Selects elements that are inside another element, at any descendant level.

```css
div p {
    color: blue;
}
```

This selects all `<p>` elements inside a `<div>`.

### G. Child Selector

Selects only direct children of an element.

```css
div > p {
    color: red;
}
```

This selects `<p>` elements that are direct children of `<div>`.

### Selector Summary

| Selector | Example | Meaning |
|---|---|---|
| Element | `p` | All paragraph elements |
| Class | `.box` | Elements with class `box` |
| ID | `#header` | Element with ID `header` |
| Universal | `*` | All elements |
| Grouping | `h1, p` | Both headings and paragraphs |
| Descendant | `div p` | Paragraphs inside a div |
| Child | `div > p` | Direct child paragraphs |

## 5. CSS Colors

CSS supports different color formats.

### A. Color Names

```css
h1 {
    color: red;
}
```

Examples:
- `red`
- `blue`
- `green`
- `black`
- `white`
- `orange`

### B. HEX Colors

HEX uses hexadecimal values to represent colors.

```css
h1 {
    color: #ff0000;
}
```

Examples:

| HEX | Color |
|---|---|
| `#ff0000` | Red |
| `#00ff00` | Green |
| `#0000ff` | Blue |
| `#000000` | Black |
| `#ffffff` | White |

### C. RGB Colors

RGB stands for Red, Green and Blue.

```css
p {
    color: rgb(255, 0, 0);
}
```

Each color channel normally ranges from 0 to 255.

### D. RGBA Colors

RGBA adds an alpha channel for transparency.

```css
div {
    background-color: rgba(0, 0, 255, 0.5);
}
```

The alpha value ranges from `0` (fully transparent) to `1` (fully opaque).

### E. HSL Colors

HSL stands for:

- Hue
- Saturation
- Lightness

```css
h1 {
    color: hsl(0, 100%, 50%);
}
```

These are different ways to represent colors in CSS.

## 6. CSS Background Properties

Background properties control the background of an element.

### Background Color

```css
body {
    background-color: lightgray;
}
```

### Background Image

```css
body {
    background-image: url("background.jpg");
}
```

### Background Repeat

```css
body {
    background-repeat: no-repeat;
}
```

Other common values:
- `repeat`
- `repeat-x`
- `repeat-y`
- `no-repeat`

### Background Size

```css
body {
    background-size: cover;
}
```

Common values:
- `cover` — scales the image to cover the background area.
- `contain` — scales the image so the entire image fits.
- `auto` — uses the image's natural dimensions where applicable.

### Background Position

```css
body {
    background-position: center;
}
```

### Background Shorthand

Multiple background properties can be written together.

```css
body {
    background: lightgray url("background.jpg") no-repeat center / cover;
}
```

## 7. CSS Text Properties

Text properties control the appearance and alignment of text.

### Color

```css
p {
    color: navy;
}
```

### Text Alignment

```css
h1 {
    text-align: center;
}
```

Common values:
- `left`
- `right`
- `center`
- `justify`

### Text Decoration

```css
a {
    text-decoration: none;
}
```

Common values:
- `none`
- `underline`
- `overline`
- `line-through`

### Text Transform

```css
h1 {
    text-transform: uppercase;
}
```

Common values:
- `uppercase`
- `lowercase`
- `capitalize`
- `none`

### Text Indentation

```css
p {
    text-indent: 30px;
}
```

Controls the indentation of the first line of text.

### Letter Spacing

```css
h1 {
    letter-spacing: 2px;
}
```

Controls the spacing between letters.

### Word Spacing

```css
p {
    word-spacing: 5px;
}
```

Controls the spacing between words.

### Line Height

```css
p {
    line-height: 1.6;
}
```

Controls the height of each line of text.

## 8. CSS Font Properties

Font properties control how text characters appear.

### Font Family

```css
body {
    font-family: Arial, sans-serif;
}
```

Common font families:
- Arial
- Verdana
- Georgia
- Times New Roman
- Courier New

A fallback font can be provided after a comma.

### Font Size

```css
h1 {
    font-size: 32px;
}
```

### Font Weight

```css
p {
    font-weight: bold;
}
```

Common values:
- `normal`
- `bold`
- `100` to `900` (where supported by the font)

### Font Style

```css
p {
    font-style: italic;
}
```

Common values:
- `normal`
- `italic`
- `oblique`

### Font Shorthand

Several font properties can be combined.

```css
p {
    font: italic bold 18px Arial, sans-serif;
}
```

## 9. CSS Units

CSS units define measurements such as size, spacing and dimensions.

There are two major categories.

### A. Absolute Units

Absolute units represent fixed measurements.

| Unit | Meaning |
|---|---|
| `px` | CSS pixel |
| `cm` | Centimeter |
| `mm` | Millimeter |
| `in` | Inch |
| `pt` | Point |

Example:

```css
h1 {
    font-size: 32px;
}
```

### B. Relative Units

Relative units depend on another measurement or context.

| Unit | Meaning |
|---|---|
| `%` | Relative to a relevant parent or reference dimension |
| `em` | Relative to the element's computed font size for font-size; otherwise context-dependent |
| `rem` | Relative to the root element's font size |
| `vw` | 1% of viewport width |
| `vh` | 1% of viewport height |

Example:

```css
.container {
    width: 80%;
}

h1 {
    font-size: 2rem;
}

section {
    min-height: 50vh;
}
```

### PX vs REM

- `px` is a CSS pixel unit.
- `rem` is relative to the root element's font size.
- Relative units are useful when building flexible layouts and accessible interfaces.

## 10. CSS Borders

Borders are drawn around an element.

### Border Width

```css
div {
    border-width: 2px;
}
```

### Border Style

```css
div {
    border-style: solid;
}
```

Common values:
- `solid`
- `dashed`
- `dotted`
- `double`
- `none`

### Border Color

```css
div {
    border-color: black;
}
```

### Border Shorthand

```css
div {
    border: 2px solid black;
}
```

The shorthand combines width, style and color.

### Border Radius

```css
button {
    border-radius: 8px;
}
```

Controls the rounding of corners.

## 11. CSS Width and Height

These properties control an element's dimensions.

```css
div {
    width: 300px;
    height: 200px;
}
```

Other useful dimension properties:

```css
.container {
    min-width: 200px;
    max-width: 900px;
    min-height: 100px;
    max-height: 500px;
}
```

| Property | Meaning |
|---|---|
| `width` | Sets the width |
| `height` | Sets the height |
| `min-width` | Sets the minimum width |
| `max-width` | Sets the maximum width |
| `min-height` | Sets the minimum height |
| `max-height` | Sets the maximum height |

## 12. CSS Comments

Comments help explain CSS code.

```css
/* This is a CSS comment */

h1 {
    color: blue;
}
```

Comments are ignored by the browser when applying styles.

## 13. Complete HTML and CSS Example

This example demonstrates the basic connection between HTML and an external CSS file.

### index.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First CSS Page</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <h1 id="main-title">Welcome to CSS</h1>

        <p class="description">
            CSS makes websites beautiful and organized.
        </p>

        <a href="https://developer.mozilla.org/">
            Learn More
        </a>
    </div>

</body>
</html>
```

### style.css

```css
body {
    background-color: #f2f2f2;
    font-family: Arial, sans-serif;
}

.container {
    background-color: white;
    width: 80%;
    max-width: 600px;
    margin: 40px auto;
    padding: 20px;
    border: 1px solid #dddddd;
    border-radius: 8px;
}

#main-title {
    color: #2563eb;
    text-align: center;
    font-size: 32px;
}

.description {
    color: #555555;
    font-size: 18px;
    line-height: 1.6;
}

a {
    color: #2563eb;
    text-decoration: none;
}
```

### What does this example demonstrate?

- HTML creates the page structure.
- The external stylesheet connects through `<link>`.
- `body` styles the page background and font.
- `.container` selects an element by class.
- `#main-title` selects an element by ID.
- `margin` and `padding` control spacing.
- `border` and `border-radius` style the container.
- Text properties control the heading and paragraph.

## 14. Quick Revision

| Topic | Important Point |
|---|---|
| CSS | Cascading Style Sheets |
| CSS Rule | Selector + Declaration Block |
| Property | The feature being styled |
| Value | The setting assigned to a property |
| Inline CSS | CSS inside the `style` attribute |
| Internal CSS | CSS inside the `<style>` element |
| External CSS | CSS in a separate `.css` file |
| Element Selector | Selects HTML tags |
| Class Selector | Starts with `.` |
| ID Selector | Starts with `#` |
| Universal Selector | `*` |
| HEX | Hexadecimal color representation |
| RGB | Red, Green, Blue |
| RGBA | RGB with alpha transparency |
| HSL | Hue, Saturation, Lightness |
| `px` | CSS pixel |
| `rem` | Relative to root font size |
| `vw` | Viewport width unit |
| `vh` | Viewport height unit |
| `border-radius` | Rounds element corners |

## 15. Official Learning Resources

- MDN CSS Introduction: https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Styling_basics
- MDN CSS Reference: https://developer.mozilla.org/en-US/docs/Web/CSS/Reference
- W3Schools CSS Tutorial: https://www.w3schools.com/css/

**End of Day 03 — Lesson 01: CSS Fundamentals.**
