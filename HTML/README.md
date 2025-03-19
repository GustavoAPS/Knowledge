# HTML

HTML (HyperText Markup Language), is a markup language used to structure web pages, it is used alongside CSS and JavaScript to power the Web.

## Table of Contents

- [First Steps](references/first_steps)
- [HTML Boilerplate](#boilerplate)
- [Interview Questions]()


## Basics
- A project generally has a file called `index.html`, which serves as the main file.
- Elements in an HTML page are defined using tags, like `<tag_name></tag_name>`. The first tag is the opening tag, and the second one (with `/`) is the closing tag.
- A standard HTML file includes the `<html></html>` tags. The `lang` attribute can be used to define the page's language for accessibility purposes.
- HTML files are structured with two main sections: 
  - **Head (`<head>`)**: Contains metadata, settings, and the page title (`<title>` tag).
  - **Body (`<body>`)**: Contains visible elements such as text, images, and buttons.
- HTML elements can be nested inside one another.
- Elements may have attributes that provide additional information. Attributes are placed inside the opening tag. Example:
  ```html
  <a href="https://www.google.com">Google</a>
  ```
- **Classes and IDs:**
  - Classes (`class`) are used to apply styles to multiple elements.
  - IDs (`id`) are unique identifiers for a single element.
  Example:
  ```html
  <p class="paragraph-style">This is a paragraph.</p>
  <p id="unique-style">This is a unique paragraph.</p>
  ```

### HTML Boilerplate
A boilerplate is a standard template that includes the basic structure needed for an HTML document:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HTML Boilerplate</title>
</head>
<body>
  <h1>Welcome to HTML</h1>
</body>
</html>
```

### Intermediate/Advanced HTML
- Some characters in HTML, such as `<` and `>`, are reserved. To display them as text, use HTML entities:
  ```html
  &lt; for <  
  &gt; for >  
  ```
- Accessibility improvements can be made using ARIA attributes.
- Use semantic elements to enhance readability and SEO.

[Back to Home](../index.html)




## Boilerplate

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body></body>
</html>

```

### Semantics
Semantics in HTML refers to using elements that have inherent meaning, making the code more understandable for both developers and search engines. Examples:

- `<article>`: Represents an independent and reusable content block, such as blog posts or news articles.
- `<section>`: Defines a section within a document, grouping related content.
- `<main>`: Contains the main content of the page, excluding headers, footers, and navigation menus.

### Accessibility
Web accessibility (A11Y) ensures that all users, including those with disabilities, can interact with web pages. Important practices include:

- **ARIA Attributes (Accessible Rich Internet Applications):** Improve accessibility for dynamic elements. Example:
  ```html
  <button aria-label="Close window">X</button>
  ```
- **Proper use of headings (`<h1>` to `<h6>`):** Following a logical hierarchy improves navigation for screen readers.
- **Alternative text (`alt`) for images:** Essential for visually impaired users:
  ```html
  <img src="image.jpg" alt="Description of the image">
  ```

### SEO (Search Engine Optimization)
SEO consists of strategies to improve a page's ranking in search engines. Essential practices include:

- **Proper use of HTML tags:**
  - `<title>`: Defines the page title displayed in search results.
  - `<meta name="description">`: Provides a brief description of the page.
  - `<header>`, `<nav>`, `<footer>`: Improve site structure for search engines.

- **User-friendly URLs:**
  - Prefer `/contact` over `/page?id=123`.

- **Image optimization:**
  - Use lightweight formats like WebP and define `alt` attributes correctly.

- **Use of structured tags (Schema Markup):**
  - Helps search engines better understand the page content.
  ```html
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "Article",
    "headline": "How to Improve Your Website's SEO",
    "author": "Your Name"
  }
  </script>
  ```

