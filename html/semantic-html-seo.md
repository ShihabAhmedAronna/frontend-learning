# HTML5 Document Structure, Semantic HTML & SEO

## 1. HTML Document Structure

Every HTML5 webpage follows a standard document structure.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="A short description of the webpage">
    <title>My Website</title>
</head>
<body>

    <header>
        <h1>My Website</h1>
    </header>

    <main>
        <h2>Welcome</h2>
        <p>This is my webpage.</p>
    </main>

    <footer>
        <p>Copyright 2026</p>
    </footer>

</body>
</html>
```

### Important Elements

| Element                  | Purpose                                                    |
| ------------------------ | ---------------------------------------------------------- |
| `<!DOCTYPE html>`        | Declares that the document uses HTML5                      |
| `<html>`                 | Root element of the webpage                                |
| `lang="en"`              | Declares the language of the page                          |
| `<head>`                 | Contains webpage information and metadata                  |
| `<meta charset>`         | Defines character encoding                                 |
| `<meta name="viewport">` | Helps webpages display correctly on different screen sizes |
| `<title>`                | Defines the browser tab title                              |
| `<body>`                 | Contains visible webpage content                           |

## 2. Semantic HTML

Semantic HTML means using HTML elements according to their meaning rather than choosing elements only for their appearance.

### Non-semantic HTML

```html
<div>
    <div>My Website</div>
    <div>Navigation</div>
    <div>Main Content</div>
</div>
```

### Semantic HTML

```html
<header>
    <h1>My Website</h1>
</header>

<nav>
    Navigation links
</nav>

<main>
    Main content
</main>
```

Semantic HTML helps browsers, search engines and assistive technologies understand webpage structure.

### Important Semantic Elements

| Element        | Purpose                                          |
| -------------- | ------------------------------------------------ |
| `<header>`     | Introductory content or page header              |
| `<nav>`        | Contains navigation links                        |
| `<main>`       | Contains the main content of the page            |
| `<section>`    | Groups related content                           |
| `<article>`    | Represents independent content                   |
| `<aside>`      | Contains supplementary content                   |
| `<footer>`     | Contains footer information                      |
| `<figure>`     | Represents self-contained media or illustrations |
| `<figcaption>` | Provides a caption for a figure                  |
| `<time>`       | Represents a date or time                        |

### Section vs Article

- `<section>` groups related content under a common theme.
- `<article>` represents independent content that can stand on its own, such as a blog post or news article.

Example:

```html
<main>
    <section>
        <h2>Latest News</h2>

        <article>
            <h3>Technology News</h3>
            <p>Technology is changing rapidly.</p>
        </article>

        <article>
            <h3>Science News</h3>
            <p>New discoveries are being made.</p>
        </article>
    </section>
</main>
```

## 3. Common HTML Page Layout

A typical webpage may use the following structure:

```html
<body>

    <header>
        <h1>My Website</h1>
    </header>

    <nav>
        <a href="/">Home</a>
        <a href="/about">About</a>
        <a href="/contact">Contact</a>
    </nav>

    <main>
        <article>
            <h2>Welcome</h2>
            <p>This is the main article.</p>
        </article>

        <aside>
            <h3>Related Information</h3>
            <p>Additional information goes here.</p>
        </aside>
    </main>

    <footer>
        <p>Copyright 2026</p>
    </footer>

</body>
```

CSS controls the actual positioning, spacing and appearance of these elements.

## 4. HTML SEO Fundamentals

SEO stands for Search Engine Optimization.

It involves improving webpages so search engines can understand their content and potentially show them in relevant search results.

### 4.1 Title Tag

The title appears in the browser tab and is commonly used as the title of a search result.

```html
<title>Learn HTML - Frontend Development</title>
```

A good title should clearly describe the webpage.

### 4.2 Meta Description

The meta description provides a short summary of the webpage.

```html
<meta name="description" content="Learn HTML fundamentals and semantic elements.">
```

Search engines may use this description in search results.

### 4.3 Heading Hierarchy

HTML provides six heading levels, from `<h1>` to `<h6>`.

```html
<h1>HTML Tutorial</h1>

<h2>HTML Fundamentals</h2>
<h3>HTML Elements</h3>

<h2>Semantic HTML</h2>
<h3>Semantic Elements</h3>
```

Headings should organize content in a logical hierarchy.

### 4.4 Image Alternative Text

The `alt` attribute provides a text alternative for an image.

```html
<img src="html-logo.png" alt="HTML5 logo">
```

It helps screen reader users understand images and provides alternative information if an image cannot load.

### 4.5 Descriptive Links

Use meaningful link text that explains the destination.

```html
<a href="https://developer.mozilla.org/">
    Read HTML documentation
</a>
```

Avoid vague link text such as "click here" when a descriptive alternative is possible.

## 5. Open Graph Metadata

Open Graph metadata helps social platforms generate previews when someone shares a webpage link.

```html
<meta property="og:title" content="My Website">
<meta property="og:description" content="My frontend learning website">
<meta property="og:type" content="website">
```

These tags are normally placed inside the `<head>` element.

## 6. Favicon

A favicon is the small icon displayed in a browser tab.

```html
<link rel="icon" href="favicon.ico">
```

This element belongs inside `<head>`.

## 7. External Links

The `target="_blank"` attribute opens a link in a new browsing context, usually a new tab.

```html
<a href="https://example.com"
   target="_blank"
   rel="noopener noreferrer">
    Visit Website
</a>
```

The `rel` attribute values shown here provide additional security and privacy protection when opening external links in a new tab.

## 8. HTML Accessibility Fundamentals

Accessibility means making webpages usable by people with different abilities and assistive technologies.

Important practices:

1. Use semantic HTML elements.
2. Provide meaningful `alt` text for informative images.
3. Connect form labels with their inputs.
4. Use headings in a logical order.
5. Make links descriptive.
6. Use buttons for actions and links for navigation.
7. Ensure interactive elements can be operated using a keyboard.
8. Use the correct language attribute on the `<html>` element.

Example of an accessible form label:

```html
<label for="email">Email Address:</label>
<input type="email" id="email" name="email">
```

The `for` attribute of the label matches the `id` of the input.

## 9. HTML Validation

HTML validation checks whether markup follows HTML standards.

A validator can identify problems such as:

- Incorrectly nested elements.
- Missing required attributes.
- Invalid element usage.
- Structural markup errors.

Official validation tool:

[https://validator.w3.org/](https://validator.w3.org/)

## 10. Important HTML Best Practices

1. Always use `<!DOCTYPE html>`.
2. Set the correct language using the `lang` attribute.
3. Use UTF-8 character encoding.
4. Include the viewport meta tag.
5. Use meaningful page titles.
6. Use semantic elements where appropriate.
7. Keep heading hierarchy logical.
8. Write readable and properly indented code.
9. Use lowercase HTML element and attribute names.
10. Always quote attribute values.
11. Provide alternative text for meaningful images.
12. Use unique `id` values within a document.
13. Use `<button>` for actions and `<a>` for navigation.
14. Validate HTML to identify markup errors.

## 11. Quick Revision

| Concept                    | Remember          |
| -------------------------- | ----------------- |
| HTML5 document declaration | `<!DOCTYPE html>` |
| Root element               | `<html>`          |
| Metadata container         | `<head>`          |
| Visible webpage content    | `<body>`          |
| Main content               | `<main>`          |
| Navigation                 | `<nav>`           |
| Independent content        | `<article>`       |
| Related content group      | `<section>`       |
| Supplementary content      | `<aside>`         |
| Page footer                | `<footer>`        |
| Browser tab title          | `<title>`         |
| Search description         | Meta description  |
| Image alternative text     | `alt`             |
| Social sharing preview     | Open Graph        |
| Browser tab icon           | Favicon           |
| HTML standards checking    | HTML Validator    |

**End of Day 02 — Semantic HTML, Document Structure and SEO.semantic-html-seo.md**
