# Introduction to CSS

**CSS (Cascading Style Sheets)** is a stylesheet language used to describe the presentation of a document written in HTML or XML. CSS controls the layout, colors, fonts, and overall visual appearance of web pages.

- Though we can add few styles using html properties, it is best practices to use CSS for all the styling properties.

## Key Concepts

- **Selectors**: Patterns used to select elements you want to style.
  ```css
  /* Universal selector - selects all */
  * {
    margin: 0;
  }
  /* Example: Selects all '<p>' elements */
  p {
    color: blue;
  }
  /* Selects all the elements with class 'cards' */
  .cards {
    background-color: black;
  }
  /* Selects the element with id 'main' */
  #main {
    text: center;
  }
  ```
- **Responsive Design**: Techniques like media queries to ensure that websites work well on different devices and screen sizes.

  ```css
  @media (max-width: 600px) {
    .container {
      flex-direction: column;
    }
  }
  ```

# CSS: Inline Styles vs Internal Styles vs External Styles

## 1. Inline Styles

**Inline styles** are applied directly to HTML elements using the `style` attribute. They are useful for quick, one-time styling but can become cumbersome if overused.

### Example:

```html
<p style="color: blue; font-size: 16px;">
  This is a blue paragraph with inline styles.
</p>
```

## 2. Internal Styles

**Internal styles** are defined within the `<style>` tag inside the `<head>` section of an HTML document. These styles apply to the entire document and are useful when you want to style a single page.

```html
<head>
  <style>
    p {
      color: blue;
      font-size: 16px;
    }
  </style>
</head>
<body>
  <p>This is a blue paragraph with internal styles.</p>
</body>
```
## 3. External Styles

**External styles** are defined in a separate CSS file, which is linked to the HTML document using the `<link>` tag. This is the preferred method for larger projects.

```html
<head>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <p>This is a blue paragraph with external styles.</p>
</body>
```
```css
p {
  color: blue;
  font-size: 16px;
}
```
### Use cases
**Inline Styles**: 
- Best for quick, one-off styling; not scalable.

**Internal Styles**:
- Useful for single-page styling; not reusable across pages.

**External Styles**:
- Ideal for larger projects; promotes reuse and maintainability.