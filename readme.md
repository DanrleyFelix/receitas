# Recipe Page — README

## What I Learned (brief summary)

In this project I practiced fundamental concepts of HTML and CSS: semantic structure (`<main>`, `<section>`, `<footer>`), accessible images with `alt`, loading Google Fonts, applying typography, working with the CSS box model (`box-sizing`, `padding`, `margin`, `border-radius`), background images with `cover`, and several selector patterns such as type, ID, grouping, and the adjacent-sibling combinator (`+`). I also reinforced spacing systems, color usage, and how to center a fixed-width layout with `margin: 0 auto;`.

---

## Project Breakdown — What Was Used and Why

### HTML: structure and semantics

* `<!DOCTYPE html>`
  Enables standard mode (HTML5).
* `<html lang="pt-br">`
  Defines the document language for accessibility and SEO.
* `<head>` with `<meta charset="UTF-8">` and `<meta name="viewport">`
  Sets encoding and viewport for responsive behavior.
* Google Fonts (`<link rel="preconnect">` + `<link href="...fonts.googleapis.com">`)
  Loads external fonts “Alice” and “Open Sans”.
* `<link rel="stylesheet" href="style.css">`
  Separates content from presentation.
* `<body>`
  Holds visible content.
* `#page` (wrapper)
  Central container for fixed width, padding, background, and rounded corners.
* `<main>`
  Defines the primary content of the page.
* `<section>`
  Groups related thematic content such as about, ingredients, and preparation.
* Headings: `<h1>` (main title) and `<h2>` (subtitles)
  Creates semantic hierarchy.
* `<p>`
  Defines paragraphs of text.
* `<ul><li>`
  Displays ingredients as an unordered list.
* `<img src="..." alt="...">`
  Adds accessible images with descriptive text.
* `<footer>`
  Provides credits and closing content.

### CSS: concepts applied

* **Reset:**

  ```css
  * { margin: 0; padding: 0; }
  ```

  Removes default browser spacing.
* **Global typography in `:root`:**
  Defines `font-family`, `line-height`, and `color` for the entire document.
* **Background image with cover:**

  ```css
  body {
    background-image: url(assets/bg-image.jpg);
    background-size: cover;
  }
  ```
* **Box model and layout:**

  ```css
  #page {
    box-sizing: border-box;
    width: 800;
    padding: 24px;
    background-color: #F0E8C2;
    border-radius: 24px;
    margin: 48px auto 28px;
  }
  ```
* **Internal and external spacing:**
  `padding` adds inner spacing; `margin` separates elements.
* **Rounded corners:**
  `border-radius` applied to containers and images.
* **Typography hierarchy:**
  Different sizes for `h1` and `h2` to structure the text.
* **Indented list:**
  `ul { padding-left: 24px; }` for bullet alignment.
* **Footer alignment:**
  `text-align: center;` centers the text, `vertical-align: middle;` aligns the icon with text.

---

## Selectors and Combinations

### Basic selectors

* **Type selector:**
  `body`, `main`, `img`, `h1`, `h2`, `ul`, `footer`
* **ID selector:**
  `#page` targets a unique element.
* **Grouping:**

  ```css
  h1, h2 { ... }
  ```

### Combinators

* **Adjacent sibling (`+`):**

  ```css
  #about p + p { margin-top: 12px; }
  section + section { margin-top: 24px; }
  ```

  Styles only elements immediately following another.
* **Descendant (space):**
  Example: `#page img` selects any image inside `#page`.
* **Child (`>`):**
  Example: `main > section` selects direct children only.
* **General sibling (`~`):**
  Example: `h2 ~ p` selects all paragraphs after an `h2`.

### Other useful selectors

* **Class:** `.card`, `.title` for reusable styles.
* **Attribute:** `a[target="_blank"]` targets links with specific attributes.
* **Pseudo-classes:** `:hover`, `:focus`, `:first-child`.
* **Pseudo-elements:** `::before`, `::after`.

---

## Learning Checklist

* [x] Semantic tags: `main`, `section`, `footer`, `h1`/`h2`, `p`, `ul`/`li`, `img`
* [x] Selectors: type, ID, grouping, adjacent sibling (`+`)
* [x] Box model: `box-sizing`, `padding`, `margin`, `border-radius`
* [x] Typography and external fonts (Google Fonts)
* [x] Background with `cover`
* [x] Basic accessibility (`lang`, `alt`, heading hierarchy)
* [x] Initial responsiveness (`meta viewport`)
