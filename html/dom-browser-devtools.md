# Browser Developer Tools, DOM & HTML Rendering

## 1. What is a Web Browser?

A web browser is software used to access and display websites.

Examples:

- Google Chrome
- Mozilla Firefox
- Microsoft Edge
- Safari
- Opera

A browser receives webpage resources such as HTML, CSS, JavaScript and images, then processes them to display a webpage.

## 2. What are Browser Developer Tools?

Browser Developer Tools (DevTools) are built-in browser features used by developers to inspect and debug websites.

In Google Chrome, DevTools can usually be opened using:

- `F12`
- `Ctrl + Shift + I`
- Right-click a webpage and select **Inspect**

### Important DevTools Tabs

| Tab         | Purpose                                           |
| ----------- | ------------------------------------------------- |
| Elements    | Inspect and edit HTML and CSS                     |
| Console     | View JavaScript messages and errors               |
| Sources     | Inspect website source files and debug JavaScript |
| Network     | Inspect network requests and responses            |
| Performance | Analyze webpage performance                       |
| Application | Inspect storage, cookies and service workers      |
| Security    | Inspect security information about the page       |

The available tabs may differ between browsers and browser versions.

## 3. Elements Panel

The Elements panel displays the webpage's DOM structure.

It allows developers to:

- Inspect HTML elements.
- View element attributes.
- Inspect CSS styles.
- Temporarily edit HTML.
- Temporarily change CSS.
- Examine element dimensions.

**Important:** Changes made directly in DevTools usually affect only the current browser session. They do not automatically update the original HTML files.

## 4. What is DOM?

DOM stands for Document Object Model.

The DOM is a programming interface that represents an HTML document as a tree of objects called nodes.

JavaScript can use the DOM to access and modify webpage content, structure and attributes.

Example HTML:

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>
</head>
<body>
    <h1>Welcome</h1>
    <p>This is my webpage.</p>
</body>
</html>
```

The browser creates a DOM representation of this document.

### Simplified DOM Tree

```text
Document
└── html
    ├── head
    │   └── title
    │       └── "My Website"
    │
    └── body
        ├── h1
        │   └── "Welcome"
        │
        └── p
            └── "This is my webpage."
```

This tree represents the parent-child relationships between document nodes.

## 5. DOM Nodes

A node is an individual object in the DOM tree.

Common node types:

| Node Type     | Meaning                                                                      |
| ------------- | ---------------------------------------------------------------------------- |
| Document node | Represents the entire document                                               |
| Element node  | Represents an HTML element                                                   |
| Text node     | Represents text inside an element                                            |
| Comment node  | Represents an HTML comment                                                   |
| Attribute     | Represents an element attribute; attributes are exposed through element APIs |

Example:

```html
<h1 id="title">Hello World</hdocs: add complete html5 reference1>
```

In this example:

- `<h1>` is an element.
- `id="title"` is an attribute.
- `Hello World` is a text node.

## 6. DOM vs HTML

HTML is the markup used to define a webpage's initial structure.

DOM is the browser's object-based representation of the document.

| HTML                           | DOM                                |
| ------------------------------ | ---------------------------------- |
| Markup language                | Programming interface              |
| Written in HTML files          | Created by the browser             |
| Defines document structure     | Represents document as objects     |
| Contains tags and attributes   | Contains nodes and properties      |
| Can be edited in a code editor | Can be accessed through JavaScript |

JavaScript can modify the DOM without directly changing the original HTML file.

## 7. What is the CSSOM?

CSSOM stands for CSS Object Model.

It is the browser's object-based representation of CSS stylesheets.

The browser uses CSSOM information to understand how elements should look.

Example CSS:

```css
h1 {
    color: blue;
    font-size: 30px;
}
```

The browser processes these CSS rules into a representation that can be used when calculating element styles.

## 8. How a Browser Renders a Webpage

Rendering means converting webpage resources into the visual content displayed on the screen.

A simplified rendering process:

1. Browser receives HTML.
2. Browser parses HTML and builds the DOM.
3. Browser processes CSS and builds the CSSOM.
4. Browser combines relevant DOM and CSSOM information to create the render tree.
5. Browser calculates element positions and dimensions through layout.
6. Browser paints visual elements.
7. Browser composites layers to display the final result.

### Rendering Process

```text
HTML
  |
  v
DOM
  |
  |              CSS
  |               |
  |               v
  |             CSSOM
  |               |
  v               v
      Render Tree
           |
           v
         Layout
           |
           v
          Paint
           |
           v
       Compositing
           |
           v
     Displayed Webpage
```

This is a simplified model. Modern browsers may perform some of these operations differently or in parallel.

## 9. Important Rendering Terms

### DOM

Represents the document structure.

### CSSOM

Represents the stylesheets and CSS rules.

### Render Tree

Contains the visual elements and their computed styles needed for rendering.

Elements that do not generate visual boxes, such as elements with `display: none`, are not included in the render tree.

### Layout

Calculates the position and dimensions of elements.

It is also commonly called reflow.

### Paint

Draws visual properties such as:

- Text
- Colors
- Borders
- Backgrounds
- Shadows

### Compositing

Combines rendered layers into the final displayed image.

## 10. Console Panel

The Console panel displays messages from JavaScript and the browser.

Common message types:

| Type    | Meaning               |
| ------- | --------------------- |
| `log`   | General information   |
| `info`  | Informational message |
| `warn`  | Warning               |
| `error` | Error                 |
| `debug` | Debugging information |

Example JavaScript:

```javascript
console.log("Website loaded");
console.warn("This is a warning");
console.error("This is an error");
```

Developers use the Console to identify problems while building websites.

## 11. Network Panel

The Network panel displays requests made by a webpage.

It can show:

- HTML requests
- CSS requests
- JavaScript requests
- Image requests
- Font requests
- API requests

Important information:

| Information | Meaning                      |
| ----------- | ---------------------------- |
| Name        | Requested resource           |
| Status      | HTTP response status         |
| Type        | Resource type                |
| Size        | Transferred resource size    |
| Time        | Request duration             |
| Waterfall   | Timeline of network activity |

Common HTTP status codes:

| Status | Meaning                    |
| ------ | -------------------------- |
| 200    | OK                         |
| 301    | Moved Permanently          |
| 302    | Found / Temporary Redirect |
| 304    | Not Modified               |
| 400    | Bad Request                |
| 401    | Unauthorized               |
| 403    | Forbidden                  |
| 404    | Not Found                  |
| 500    | Internal Server Error      |
| 503    | Service Unavailable        |

## 12. Common Browser Errors

### 404 Not Found

The requested resource could not be found.

Possible causes:

- Incorrect URL.
- Incorrect file path.
- Resource does not exist.

### 403 Forbidden

The server refuses to allow access to the requested resource.

### 500 Internal Server Error

The server encountered an unexpected problem.

### JavaScript Error

An error occurs while JavaScript is running.

The Console panel can help identify the error message and its location.

## 13. Important DevTools Concepts

| Concept     | Meaning                                             |
| ----------- | --------------------------------------------------- |
| Inspect     | Examine webpage elements                            |
| DOM         | Object representation of HTML                       |
| CSSOM       | Object representation of CSS                        |
| Console     | View messages and errors                            |
| Network     | Inspect resource requests                           |
| Debugging   | Finding and understanding problems                  |
| Rendering   | Converting webpage resources into displayed content |
| Layout      | Calculating element positions and dimensions        |
| Paint       | Drawing visual elements                             |
| Compositing | Combining rendered layers                           |

## 14. Official Learning Resources

- Chrome DevTools: [https://developer.chrome.com/docs/devtools/](https://developer.chrome.com/docs/devtools/)
- MDN DOM Guide: [https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model)
- MDN Rendering Performance: [https://developer.mozilla.org/en-US/docs/Web/Performance/Guides/Rendering](https://developer.mozilla.org/en-US/docs/Web/Performance/Guides/Rendering)

**End of Day 02 — Browser Developer Tools, DOM & HTML Rendering.**
