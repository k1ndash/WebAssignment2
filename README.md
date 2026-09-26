# Assignment 2 — Advanced CSS (Flexbox & Grid)

**Name:** Meiirzhan Tolendi
**Group:** SE-2539

---


Part 1. Flexbox

Task 0. Navigation Bar

The header is a flex container (display: flex) with justify-content: space-between, pushing the logo left and the links right, and align-items: center, keeping them on one vertical line. Gap is used for spacing instead of margins.

Task 1. Card Row

The card container is a flex row (flex-wrap: wrap, gap). Each card is a column flexbox (flex-direction: column), which keeps the button at the bottom no matter how much text is above it — this makes all three cards equal in height. On hover, a card lifts with transform: translateY() and gets a soft shadow.

Part 2. Grid System

Task 2. Page Layout with Grid Areas

The page wrapper is a grid container with named grid-template-areas: header and footer span both columns, while the sidebar and main content share the middle row. Each child is placed with its matching grid-area name.

Screenshot: screenshots/task2-grid-layout.png

Task 3. Image Gallery

Nine images sit in a grid-template-columns: repeat(3, 1fr) container with fixed grid-auto-rows and a consistent gap. Each caption is absolutely positioned at the bottom of its <figure> and slides in on hover using transform: translateY().

Screenshot: screenshots/task3-gallery.png

Part 3. Combining Flexbox & Grid

Task 4. Portfolio Page

The page skeleton (header, projects column, sidebar, footer) uses Grid — a two-column grid-template-columns: 2fr 1fr for the main section. Inside it, Flexbox handles the smaller parts: the header nav is a flex row, and each project card lays out its thumbnail, title, description and button with display: flex. The footer sits outside the two columns and spans the full page width.

Screenshot: screenshots/task4-portfolio.png

Summary of work process

I built one shared css/style.css file with variables, reset rules and all task styles, and every page links to it. I started with Flexbox for simple one-dimensional layouts (navbar, card row), then moved to Grid when I needed to control rows and columns at once (page areas, gallery). For the portfolio I combined both: Grid for big regions, Flexbox for content inside them. The trickiest part was equal-height cards — the fix was making each card a column flex container so flex: 1 on the paragraph pushes the button to the same spot in every card.

Resources used

Abitova G.A. Web Technologies Front-End Development, Part 1 (2022)
https://www.w3schools.com/css/css3_flexbox.asp
https://www.w3schools.com/css/css_grid.asp
https://www.w3schools.com/css/css3_box-sizing.asp
