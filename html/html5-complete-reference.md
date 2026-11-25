# Complete HTML5 Reference & Final Revision

## 1. What is HTML?

HTML stands for HyperText Markup Language.

It is the standard markup language used to structure content on webpages.

HTML defines:
- Headings
- Paragraphs
- Links
- Images
- Lists
- Tables
- Forms
- Multimedia
- Page structure

HTML is not a programming language. It is a markup language.

## 2. HTML Element Structure

An HTML element usually consists of an opening tag, content and a closing tag.

```html
<p>This is a paragraph.</p>
```

- `<p>` is the opening tag.
- `This is a paragraph.` is the content.
- `</p>` is the closing tag.

Some elements are void elements and do not have closing tags.

Examples:

```html
<img src="photo.jpg" alt="A photo">
<br>
<hr>
<input type="text">
<meta charset="UTF-8">
```

## 3. HTML Attributes

Attributes provide additional information about HTML elements.

Example:

```html
<a href="https://example.com" target="_blank">
    Visit Website
</a>
```

Here:
- `href` specifies the destination.
- `target` specifies where to open the destination.

Common attributes:

| Attribute | Purpose |
|---|---|
| `id` | Unique identifier for an element |
| `class` | Groups elements for styling or scripting |
| `href` | Link destination |
| `src` | Resource location |
| `alt` | Alternative text for an image |
| `title` | Additional advisory information |
| `style` | Inline CSS |
| `name` | Name of a form control |
| `value` | Value associated with a form control |
| `type` | Specifies an element's type |
| `placeholder` | Displays a hint inside an input |
| `required` | Makes a form field mandatory |
| `disabled` | Disables a form control |
| `readonly` | Makes a form control read-only |

## 4. HTML Document Structure

A standard HTML5 document:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="My first webpage">
    <title>My Website</title>
</head>
<body>

    <header>
        <h1>My Website</h1>
    </header>

    <main>
        <p>Welcome to my website.</p>
    </main>

    <footer>
        <p>Copyright 2026</p>
    </footer>

</body>
</html>
```

## 5. Text Elements

| Element | Purpose |
|---|---|
| `<h1>` to `<h6>` | Headings |
| `<p>` | Paragraph |
| `<br>` | Line break |
| `<hr>` | Thematic break |
| `<strong>` | Strong importance |
| `<em>` | Emphasis |
| `<b>` | Draws attention without adding importance |
| `<i>` | Alternate voice or mood |
| `<u>` | Non-textual annotation |
| `<mark>` | Highlighted text |
| `<small>` | Side comments or small print |
| `<del>` | Deleted text |
| `<ins>` | Inserted text |
| `<sub>` | Subscript |
| `<sup>` | Superscript |
| `<blockquote>` | Extended quotation |
| `<q>` | Short inline quotation |
| `<code>` | Code fragment |
| `<pre>` | Preformatted text |

Example:

```html
<h1>HTML Learning</h1>

<p>HTML is used to structure webpages.</p>

<p><strong>Important:</strong> Learn semantic HTML.</p>

<p>Water formula: H<sub>2</sub>O</p>

<p>Mathematical expression: x<sup>2</sup></p>

<mark>Highlighted text</mark>
```

## 6. Links

The `<a>` element creates hyperlinks.

```html
<a href="https://example.com">Visit Website</a>
```

Open in a new tab:

```html
<a href="https://example.com" target="_blank" rel="noopener noreferrer">
    Visit Website
</a>
```

Internal section navigation:

```html
<a href="#contact">Go to Contact</a>

<section id="contact">
    <h2>Contact</h2>
</section>
```

## 7. Lists

### Ordered List

Displays items in a numbered sequence.

```html
<ol>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ol>
```

### Unordered List

Displays items with bullets.

```html
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ul>
```

### Description List

Displays terms and their descriptions.

```html
<dl>
    <dt>HTML</dt>
    <dd>Structures webpages.</dd>

    <dt>CSS</dt>
    <dd>Styles webpages.</dd>
</dl>
```

## 8. Images

The `<img>` element displays images.

```html
<img src="images/photo.jpg" alt="A landscape" width="400">
```

Important attributes:
- `src`: Image location.
- `alt`: Alternative text.
- `width`: Displayed width.
- `height`: Displayed height.

## 9. Tables

Important table elements:

| Element | Purpose |
|---|---|
| `<table>` | Creates a table |
| `<caption>` | Table title |
| `<tr>` | Table row |
| `<th>` | Header cell |
| `<td>` | Data cell |
| `<thead>` | Header section |
| `<tbody>` | Main data section |
| `<tfoot>` | Footer section |

Example:

```html
<table>
    <caption>Student Results</caption>

    <thead>
        <tr>
            <th>Name</th>
            <th>Marks</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>Aronno</td>
            <td>85</td>
        </tr>
    </tbody>
</table>
```

### Colspan and Rowspan

- `colspan` makes a cell span multiple columns.
- `rowspan` makes a cell span multiple rows.

```html
<table border="1">
    <tr>
        <th colspan="2">Student Information</th>
    </tr>
    <tr>
        <td>Name</td>
        <td>Aronno</td>
    </tr>
</table>
```

## 10. Forms

The `<form>` element collects user input.

```html
<form action="/submit" method="post">

    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required>

    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>

    <button type="submit">Submit</button>

</form>
```

### Common Input Types

| Type | Purpose |
|---|---|
| `text` | Text input |
| `password` | Password input |
| `email` | Email input |
| `number` | Numeric input |
| `tel` | Telephone input |
| `date` | Date selection |
| `time` | Time selection |
| `radio` | Single selection from a group |
| `checkbox` | Independent selection |
| `file` | File selection |
| `submit` | Form submission |
| `search` | Search input |
| `url` | URL input |
| `range` | Range control |
| `color` | Color selection |

### Other Form Elements

| Element | Purpose |
|---|---|
| `<label>` | Describes an input |
| `<textarea>` | Multi-line text input |
| `<select>` | Dropdown control |
| `<option>` | Dropdown option |
| `<button>` | Button |
| `<fieldset>` | Groups related form controls |
| `<legend>` | Describes a fieldset |
| `<datalist>` | Provides suggested input options |
| `<output>` | Represents a calculated result |

## 11. Semantic HTML

Semantic elements describe the meaning and role of content.

| Element | Purpose |
|---|---|
| `<header>` | Header content |
| `<nav>` | Navigation |
| `<main>` | Main content |
| `<section>` | Related content group |
| `<article>` | Independent content |
| `<aside>` | Supplementary content |
| `<footer>` | Footer content |
| `<figure>` | Self-contained media |
| `<figcaption>` | Media caption |
| `<time>` | Date or time |

## 12. Audio and Video

### Audio

```html
<audio controls>
    <source src="audio.mp3" type="audio/mpeg">
</audio>
```

### Video

```html
<video controls width="640">
    <source src="video.mp4" type="video/mp4">
</video>
```

## 13. Iframes

An iframe embeds another webpage or external content inside the current webpage.

```html
<iframe
    src="https://example.com"
    title="Example website"
    width="600"
    height="400">
</iframe>
```

Only embed websites and content that permit it.

## 14. HTML Entities

HTML entities represent reserved characters or special symbols.

| Entity | Result |
|---|---|
| `&lt;` | < |
| `&gt;` | > |
| `&amp;` | & |
| `&quot;` | " |
| `&nbsp;` | Non-breaking space |
| `&copy;` | © |
| `&reg;` | ® |
| `&euro;` | € |

Example:

```html
<p>5 &lt; 10</p>
<p>Copyright &copy; 2026</p>
```

## 15. HTML Metadata

Metadata provides information about a webpage.

Common metadata elements:

```html
<head>
    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <meta name="description" content="Learn HTML fundamentals">

    <title>HTML Tutorial</title>

    <link rel="icon" href="favicon.ico">
</head>
```

## 16. HTML Accessibility

Accessibility makes webpages usable by people with different abilities.

Important practices:

1. Use semantic HTML.
2. Provide meaningful alternative text for informative images.
3. Connect form labels with their inputs.
4. Use logical heading order.
5. Use descriptive links.
6. Support keyboard navigation.
7. Use native buttons and links.
8. Use ARIA when native HTML is insufficient.

Example:

```html
<label for="email">Email:</label>
<input type="email" id="email" name="email">
```

## 17. HTML SEO Fundamentals

SEO stands for Search Engine Optimization.

Important HTML features:

- Descriptive `<title>`.
- Useful meta description.
- Logical heading structure.
- Descriptive links.
- Meaningful image alternative text.
- Semantic page structure.

Example:

```html
<head>
    <title>HTML Learning Guide</title>

    <meta
        name="description"
        content="A beginner-friendly guide to HTML."
    >
</head>
```

## 18. HTML File Organization

A basic website can be organized like this:

```text
my-website/
│
├── index.html
├── about.html
│
├── pages/
│   └── contact.html
│
├── images/
│   └── logo.png
│
├── audio/
│   └── audio.mp3
│
└── videos/
    └── video.mp4
```

Relative paths connect these files.

Examples:

```html
<a href="about.html">About</a>

<a href="pages/contact.html">Contact</a>

<img src="images/logo.png" alt="Website logo">
```

## 19. HTML Best Practices

1. Use `<!DOCTYPE html>`.
2. Set the correct `lang` attribute.
3. Use UTF-8 encoding.
4. Include the viewport meta tag.
5. Use semantic elements where appropriate.
6. Keep headings in a logical order.
7. Use unique IDs.
8. Quote attribute values.
9. Use lowercase element and attribute names.
10. Keep indentation consistent.
11. Use meaningful `alt` text.
12. Use links for navigation.
13. Use buttons for actions.
14. Avoid unnecessary elements.
15. Validate HTML markup.
16. Keep HTML focused on structure and content.

## 20. Important HTML Concepts to Remember

| Concept | Meaning |
|---|---|
| HTML | HyperText Markup Language |
| Element | HTML tag structure and its content |
| Attribute | Additional information about an element |
| Semantic HTML | HTML elements with meaningful roles |
| DOM | Document Object Model |
| Metadata | Information about a webpage |
| Hyperlink | A connection to another resource |
| Relative URL | Location relative to a document or base URL |
| Absolute URL | Complete web address |
| Form | Collects user input |
| Validation | Checking markup against standards |
| Accessibility | Making websites usable by different people |
| SEO | Search Engine Optimization |

## 21. Official HTML Learning Resources

- MDN HTML Guide: https://developer.mozilla.org/en-US/docs/Web/HTML
- HTML Living Standard: https://html.spec.whatwg.org/
- W3C Validator: https://validator.w3.org/
- W3Schools HTML Reference: https://www.w3schools.com/html/

**End of Day 02 — HTML5 Complete Reference & Revision.**
