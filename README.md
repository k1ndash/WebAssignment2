# Assignment 2 — Advanced CSS (Flexbox & Grid)

**Name:** Meiirzhan Tolendi
**Group:** SE-2539

---

### Part 1. Flexbox

## Task 0. Navigation Bar

The header uses display: flex with justify-content: space-between, so the logo goes left and the links go right. align-items: center keeps everything on one line, and I used gap instead of margins for spacing.

## Task 1. Card Row

The card container is a flex row with flex-wrap: wrap and gap. Each card is a column flexbox (flex-direction: column), so the button always stays at the bottom no matter how long the text is. That's how all three cards end up the same height. On hover, a card moves up with transform: translateY() and gets a shadow.

### Part 2. Grid System

## Task 2. Page Layout with Grid Areas

The page wrapper is a grid with named grid-template-areas. The header and footer take both columns, and the sidebar and main content share the middle row. Each element just gets its grid-area name.

## Task 3. Image Gallery

Nine images in a grid with grid-template-columns: repeat(3, 1fr), fixed grid-auto-rows and a gap. Each caption is absolutely positioned at the bottom of its figure and slides up on hover with transform: translateY().

### Part 3. Combining Flexbox & Grid

## Task 4. Portfolio Page

The page skeleton (header, projects, sidebar, footer) is built with Grid — two columns, grid-template-columns: 2fr 1fr for the main part. Inside that, Flexbox does the small stuff: the nav is a flex row, and each project card uses flex to line up the image, title, text and button. The footer is outside the two columns and spans the whole width.

### Summary of work process

I made one shared css/style.css with variables, reset rules and all the styles, and linked it on every page. I started with Flexbox for the simple one-direction layouts (navbar, cards), then switched to Grid when I needed rows and columns together (page layout, gallery). For the portfolio I used both — Grid for the big sections, Flexbox inside them. The hardest part was equal-height cards. I fixed it by making each card a column flex container, so flex: 1 on the paragraph pushes the button to the same place in every card.

### Resources used

Abitova G.A. Web Technologies Front-End Development, Part 1 (2022)
https://www.w3schools.com/css/css3_flexbox.asp
https://www.w3schools.com/css/css_grid.asp
https://www.w3schools.com/css/css3_box-sizing.asp
