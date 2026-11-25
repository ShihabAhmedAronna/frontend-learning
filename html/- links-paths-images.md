# HTML Links, Paths, Images & File Organization

## 1. Absolute URLs vs Relative URLs

An HTML link uses the `href` attribute to specify its destination.

There are two common ways to specify a destination.

### Absolute URL

An absolute URL contains the complete web address.

```html
<a href="https://www.example.com/about.html">About</a>
```

Use it when linking to an external website or a complete URL.

### Relative URL

A relative URL specifies a location relative to the current document or the website's configured base URL.

```html
<a href="about.html">About</a>
```

Use it to connect pages within the same website.

## 2. Understanding File Paths

Suppose your website has this structure:

```text
my-website/
│
├── index.html
├── about.html
│
├── pages/
│   └── contact.html
│
└── images/
    └── logo.png
```

The following paths explain how files connect.

| Path | Meaning |
|---|---|
| `about.html` | File in the current directory |
| `pages/contact.html` | File inside the pages folder |
| `../index.html` | Go up one directory, then open index.html |
| `images/logo.png` | Image inside the images folder |
| `/about.html` | Path from the website root |

### Example: From index.html

```html
<a href="pages/contact.html">Contact</a>

<img src="images/logo.png" alt="Website logo">
```

### Example: From pages/contact.html

```html
<a href="../index.html">Home</a>

<img src="../images/logo.png" alt="Website logo">
```

**Important:** Relative paths depend on the location of the current HTML document.

## 3. Internal Page Navigation

You can connect different sections of the same webpage using IDs.

```html
<nav>
    <a href="#about">About</a>
    <a href="#services">Services</a>
    <a href="#contact">Contact</a>
</nav>

<section id="about">
    <h2>About</h2>
    <p>About our website.</p>
</section>

<section id="services">
    <h2>Services</h2>
    <p>Our services.</p>
</section>

<section id="contact">
    <h2>Contact</h2>
    <p>Contact information.</p>
</section>
```

- `href="#about"` points to the element with `id="about"`.
- The `#` indicates a fragment identifier.
- IDs must be unique within the document.

## 4. Image Formats Used on Websites

Different image formats have different purposes.

| Format | Common Use |
|---|---|
| JPEG / JPG | Photographs |
| PNG | Images requiring transparency |
| SVG | Logos, icons and vector graphics |
| WebP | Web images with efficient compression |
| GIF | Simple animations |

### Adding an image

```html
<img src="images/photo.jpg" alt="A landscape">
```

### Image dimensions

```html
<img
    src="images/photo.jpg"
    alt="A landscape"
    width="600"
    height="400"
>
```

The `width` and `height` attributes define the image's displayed dimensions in CSS pixels. CSS can control its responsive presentation.

## 5. The Picture Element

The `<picture>` element allows the browser to choose between different image sources.

```html
<picture>
    <source srcset="images/photo.webp" type="image/webp">
    <source srcset="images/photo.png" type="image/png">
    <img src="images/photo.jpg" alt="A landscape">
</picture>
```

The browser selects a supported source. The `<img>` element provides the fallback.

## 6. Responsive Images with srcset

The `srcset` attribute allows browsers to choose an image based on available display space and device characteristics.

```html
<img
    src="images/photo-small.jpg"
    srcset="
        images/photo-small.jpg 480w,
        images/photo-medium.jpg 800w,
        images/photo-large.jpg 1200w
    "
    sizes="(max-width: 600px) 100vw, 80vw"
    alt="A landscape"
>
```

Important attributes:

- `src`: Fallback image.
- `srcset`: Available image sources and their widths.
- `sizes`: Describes the expected display width under different conditions.

## 7. Audio and Video

HTML supports multimedia without requiring external plugins for common media formats.

### Audio

```html
<audio controls>
    <source src="audio/music.mp3" type="audio/mpeg">
    Your browser does not support audio.
</audio>
```

### Video

```html
<video controls width="640" poster="images/thumbnail.jpg">
    <source src="videos/movie.mp4" type="video/mp4">
    Your browser does not support video.
</video>
```

Important attributes:

| Attribute | Purpose |
|---|---|
| `controls` | Displays playback controls |
| `autoplay` | Requests automatic playback |
| `muted` | Starts media muted |
| `loop` | Repeats playback |
| `poster` | Displays a video preview image |
| `preload` | Gives the browser a media-loading hint |

Autoplay may be restricted by browsers, particularly for media that plays with sound.

## 8. HTML Comments

Comments are notes in the HTML source that browsers do not display as normal webpage content.

```html
<!-- This is a comment -->

<header>
    <h1>My Website</h1>
</header>
```

Comments are useful for explaining sections of code, but they should not contain passwords or private information.

## 9. Organizing Website Files

A clean website project separates HTML documents from assets.

Example:

```text
my-website/
│
├── index.html
├── about.html
│
├── pages/
│   ├── contact.html
│   └── services.html
│
├── images/
│   ├── logo.png
│   └── banner.jpg
│
├── audio/
│   └── music.mp3
│
└── videos/
    └── introduction.mp4
```

This organization makes projects easier to understand and maintain.

## 10. Quick Revision

| Concept | Remember |
|---|---|
| Absolute URL | Complete web address |
| Relative URL | Path relative to a document or base URL |
| `href` | Link destination |
| `src` | Resource location |
| `../` | Go up one directory |
| `#id` | Navigate to an element by ID |
| `srcset` | Multiple image source candidates |
| `sizes` | Expected image display width |
| `<picture>` | Multiple image source options |
| `<audio>` | Audio content |
| `<video>` | Video content |
| `<!-- -->` | HTML comment |

**End of Day 02 — HTML Links, Paths, Images & File Organization.**
