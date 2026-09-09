# COSI 116A Assignment 1 Writeup: Introduction to Web Development

**Student:** Miles Laker  
**GitHub Repository:** [https://github.com/MilesLaker/Cosi116AHW1](https://github.com/MilesLaker/Cosi116AHW1)  

---

## 1. Commit History Summary

The repository was built step-by-step in exact accordance with the assignment specifications and git commit guidelines:

1. **Commit 1: HTML Basics** (`6eeef09`)
   - Constructed standard HTML5 document structure in `index.html`.
   - Included headings (`<h1>`), image (`<img>`), unordered list (`<ul>`), paragraphs (`<p>`), link (`<a>`), and action button (`<button>`).

2. **Commit 2: CSS Basics** (`d9871cf`)
   - Styled page layout in `styles/style.css` following the MDN tutorial guidelines.
   - Added Open Sans Google Font, centered orange content container (`width: 600px`), blue background, heading text-shadow, and image centering.

3. **Commit 3: JavaScript basics** (`c929f37`)
   - Implemented interactive logic in `scripts/main.js`.
   - Image switcher: toggles image source between `images/firefox-icon.png` and `images/firefox2.png` on click.
   - User prompt greeting: prompts user for name using `localStorage`, displaying custom welcome header.
   - Included script tag immediately before closing `</body>` tag.

4. **Commit 4: Build a basic bar chart** (`10b381c`)
   - Added SVG canvas element (`<svg id='cosi116a-svg' width="250" height="250">`) to `index.html`.
   - Styled SVG with `background: white;` and `rect { fill: blue; }` in `styles/style.css`.
   - Created three manually written `<rect>` elements encoding values **3**, **12**, and **42**.

---

## 2. Basic Bar Chart Implementation Details

The SVG bar chart encodes three data values (3, 12, and 42) inside a 250×250 white canvas. 

Because SVG origin `(0,0)` starts at the top-left corner, y-coordinates were calculated from the baseline (`y = 250`) using `y = 250 - height` to ensure bars grow right-side up:

- **Bar 1 (Value 3):**
  - `x = 40`, `y = 238`, `width = 30`, `height = 12`
- **Bar 2 (Value 12):**
  - `x = 95`, `y = 202`, `width = 30`, `height = 48`
- **Bar 3 (Value 42):**
  - `x = 150`, `y = 82`, `width = 30`, `height = 168`

> **Note:** The rendered page was verified running on local python web server (`python3 -m http.server 8000`). The screenshot below shows 3 manually written rectangles in a simple bar chart right-side up.

---

## 3. Verification

The web application was verified locally using `python3 -m http.server 8000` and renders cleanly in up-to-date Chrome and Firefox browsers.
