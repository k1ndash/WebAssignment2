# Assignment 2 — Advanced CSS (Flexbox & Grid)

**Name:** Meiirzhan Tolendi
**Group:** SE-2539

---


## Part 1. Flexbox

### Task 0. Navigation Bar

The header is a flex container (`display: flex`) with `justify-content: space-between` to push the logo left and the links right, and `align-items: center` to keep them on the same vertical line. Spacing between the links uses `gap` instead of margins.

*Screenshot:*
`![Task 0 — Navigation bar](screenshots/task0-navbar.png)`

### Task 1. Card Row

The card container is a flex row (`flex-wrap: wrap`, `gap`). Each individual card is a column flexbox (`flex-direction: column`), which keeps the button pinned to the bottom of the card no matter how much text is above it — this is what makes all three cards line up at equal height. Hovering a card lifts it with `transform: translateY()` and adds a soft shadow.

*Screenshot:*
`![Task 1 — Card row](screenshots/task1-cards.png)`

---

## Part 2. Grid System

### Task 2. Page Layout with Grid Areas

The page wrapper is a grid container with named `grid-template-areas`: header and footer each span both columns, while the sidebar and main content share the middle row. Each child element is placed with the matching `grid-area` name.

*Screenshot:*
`![Task 2 — Grid layout](screenshots/task2-grid-layout.png)`

### Task 3. Image Gallery

Nine images sit inside a `grid-template-columns: repeat(3, 1fr)` container with a fixed `grid-auto-rows` and a consistent `gap`. Each image's caption is absolutely positioned at the bottom of its `<figure>` and slides into view on hover using `transform: translateY()`.

*Screenshot:*
`![Task 3 — Image gallery](screenshots/task3-gallery.png)`

---

## Part 3. Combining Flexbox & Grid

### Task 4. Portfolio Page

The overall page skeleton (header, projects column, sidebar, footer) is laid out with **Grid** — a two-column `grid-template-columns: 2fr 1fr` for the main section. Inside that skeleton, **Flexbox** handles the smaller pieces: the header nav is a flex row, and each project card arranges its thumbnail, title, description and button with `display: flex`. The footer sits outside the grid's two columns and spans the full page width.

*Screenshot:*
`![Task 4 — Portfolio page](screenshots/task4-portfolio.png)`

---

## Summary of work process

I built one shared `css/style.css` file with the color/typography variables, reset rules and all task-specific styles, and every page links to it. I started with Flexbox for the simpler one-dimensional layouts (navbar, card row), then moved to Grid once I needed to control both rows and columns at the same time (the page-area layout and the gallery). For the portfolio task I combined both: Grid for the page's big regions, Flexbox for the content inside each region. The trickiest part was making the cards equal height — the fix was making each card itself a column flex container so `flex: 1` on the paragraph pushes the button down to the same spot in every card.

---

## Resources used

- Abitova G.A. *Web Technologies Front-End Development*, Part 1 (2022)
- https://www.w3schools.com/css/css3_flexbox.asp
- https://www.w3schools.com/css/css_grid.asp
- https://www.w3schools.com/css/css3_box-sizing.asp
