# CSS Flexbox Exercise: Building a Flexible Layout System

## Introduction
Flexbox (Flexible Box Layout) is a powerful CSS layout model that helps you design complex layouts and align items within a container. This exercise will guide you through the fundamental concepts of Flexbox while building practical examples.

## Prerequisites
- Basic understanding of HTML and CSS
- Code editor
- Web browser

## Exercise Overview
You'll progressively build and modify a webpage layout using Flexbox, starting with simple concepts and moving to more complex arrangements.

## Part 1: Basic Flexbox Container
### Task 1.1: Create Your First Flex Container
1. Create an HTML file with this basic structure:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Flexbox Exercise</title>
    <style>
        /* Your CSS will go here */
    </style>
</head>
<body>
    <div class="container">
        <div class="box">1</div>
        <div class="box">2</div>
        <div class="box">3</div>
    </div>
</body>
</html>
```

2. Add this initial CSS:
```css
.container {
    display: flex;
    /* Try each property separately */
    /* justify-content: center; */
    /* align-items: center; */
    border: 2px solid #333;
    height: 200px;
}

.box {
    width: 100px;
    height: 100px;
    background-color: #3498db;
    margin: 10px;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 24px;
}
```

### Task 1.2: Experiment with Flex Direction
1. Add `flex-direction` to your container and try each value:
```css
.container {
    display: flex;
    flex-direction: row; /* Try: row, column, row-reverse, column-reverse */
}
```

2. Observe how the layout changes with each value

## Part 2: Alignment and Spacing
### Task 2.1: Justify Content
Modify your container to try each `justify-content` value:
```css
.container {
    display: flex;
    justify-content: flex-start; /* Try each: */
    /* flex-start | flex-end | center | space-between | space-around | space-evenly */
}
```

### Task 2.2: Align Items
Experiment with `align-items`:
```css
.container {
    display: flex;
    height: 300px;
    align-items: stretch; /* Try each: */
    /* stretch | flex-start | flex-end | center | baseline */
}
```

## Part 3: Flexible Items
### Task 3.1: Understanding Flex Grow
1. Add more boxes to your HTML (total of 5 boxes)
2. Modify your CSS to experiment with `flex-grow`:
```css
.box {
    /* Previous styles remain */
    flex-grow: 1; /* Try different numbers */
}

/* Make one box grow differently */
.box:nth-child(2) {
    flex-grow: 2;
}
```

### Task 3.2: Flex Basis and Shrink
Add these properties to your boxes:
```css
.box {
    /* Previous styles remain */
    flex-basis: 200px;
    flex-shrink: 1; /* Try 0 and 1 */
}
```

## Part 4: Real-World Layout Challenge
### Task 4.1: Create a Header Layout
Build a typical website header with logo and navigation:
```html
<header class="header">
    <div class="logo">Logo</div>
    <nav class="nav">
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Services</a>
        <a href="#">Contact</a>
    </nav>
</header>
```

```css
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px;
    background-color: #f8f9fa;
}

.logo {
    font-size: 24px;
    font-weight: bold;
}

.nav {
    display: flex;
    gap: 20px;
}

.nav a {
    text-decoration: none;
    color: #333;
}
```

### Task 4.2: Create a Card Layout
Build a responsive card container:
```html
<div class="card-container">
    <div class="card">
        <img src="placeholder.jpg" alt="Card 1">
        <h3>Card Title</h3>
        <p>Card description goes here</p>
        <button>Learn More</button>
    </div>
    <!-- Add more cards -->
</div>
```

```css
.card-container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    padding: 20px;
}

.card {
    flex: 1 1 300px;
    display: flex;
    flex-direction: column;
    padding: 15px;
    border: 1px solid #ddd;
    border-radius: 8px;
}

.card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
}

.card button {
    margin-top: auto;
}
```

## Common Mistakes to Watch For
1. Forgetting to set `display: flex` on the container
2. Confusing `justify-content` (main axis) with `align-items` (cross axis)
3. Not considering flex-direction when using justification properties
4. Forgetting to add height to container when using `align-items`

## Extension Challenges
1. Create a sticky footer that stays at the bottom
2. Build a holy grail layout (header, footer, main content, two sidebars)
3. Create a responsive navigation menu that switches to a column on mobile

## Tips for Success
- Use your browser's developer tools to inspect the flex containers
- Try resizing your browser to see how layouts respond
- Experiment with different values for each property
- Comment out properties one at a time to understand their effects

## Additional Resources
1. CSS Tricks Flexbox Guide: https://css-tricks.com/snippets/css/a-guide-to-flexbox/
2. MDN Flexbox Documentation: https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox

Remember: The best way to learn Flexbox is through experimentation. Don't be afraid to break things and try different combinations of properties!
