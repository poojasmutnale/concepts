# Introduction to HTML

HTML is the foundation of web development. It provides the basic structure and content of a webpage, which can then be enhanced with CSS for styling and JavaScript for interactivity.

## What is HTML?

**HTML (HyperText Markup Language)**

- Is the standard language used to create and design webpages.
- It structures the content on the web, allowing browsers to interpret and display text, images, links, and other media.

## Basic Structure of an HTML Document

An HTML document typically starts with a `<!DOCTYPE html>` declaration, followed by the `<html>` tag which contains two main sections: `<head>` and `<body>`.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <h1>This is a Heading</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

- **`<!DOCTYPE html>`**: Defines the document type and version of HTML.
- **`<html>`**: The root element that encloses all the content on the page.
- **`<head>`**: Contains meta-information about the document, such as its title and linked resources (e.g., CSS files).
- **`<body>`**: Contains the visible content of the webpage, including text, images, links, and more.

# Semantic vs. Non-Semantic HTML Tags

## What Are Semantic Tags?

**Semantic HTML tags**

- Clearly describe their meaning in a way that both the browser and the developer can understand.
- These tags define the purpose of the content enclosed within them, making the structure of the webpage more meaningful and easier to read.

### Examples of Semantic Tags:

- **`<header>`**: Defines the header section of a webpage, often containing the site's logo, navigation, or title.
- **`<nav>`**: Represents a navigation section containing links to other parts of the site.
- **`<main>`**: Specifies the main content area of the document.
- **`<article>`**: Denotes self-contained content that could be distributed independently, like a blog post or news article.
- **`<section>`**: Defines a section of content, typically with a heading.
- **`<footer>`**: Specifies the footer of a document or section, often containing copyright information or links.

### Advantages of Semantic Tags:

- **Improved Accessibility**: Screen readers and other assistive technologies can better interpret and navigate the content.
- **SEO Benefits**: Search engines can better understand and index the content, which can improve ranking.
- **Better Code Readability**: Semantic tags make the HTML code easier to read and maintain for developers.

## What Are Non-Semantic Tags?

**Non-semantic HTML tags**

- Do not convey any information about the content they contain.
- These tags are primarily used to style or layout content without providing any context about its purpose or structure.

### Examples of Non-Semantic Tags:

**`<div>`**: A generic container for grouping content.

- It has no intrinsic meaning and is typically used for layout purposes.

**`<span>`**: An inline container for text or elements.

- Like `<div>`, it has no inherent meaning and is often used for styling purposes.

### Usage of Non-Semantic Tags:

- **Layout and Styling**: Non-semantic tags are often used with CSS to style or position content on the page.
- **Grouping Content**: They are useful for wrapping content when no specific semantic meaning is required.

### Drawbacks of Non-Semantic Tags:

- **Lack of Meaning**: Non-semantic tags don’t provide any context, making it harder for search engines and assistive technologies to understand the content.
- **Harder Maintenance**: Overusing non-semantic tags can make HTML documents less readable and harder to maintain.

## When to Use Which?

- **Use Semantic Tags**: When you want to define the structure and meaning of your content, improving accessibility, SEO, and maintainability.
- **Use Non-Semantic Tags**: When you need generic containers for layout purposes, or when no semantic tag fits the specific use case.
