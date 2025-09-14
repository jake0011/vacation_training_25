---
title: css-projects
nav_order: 2
has_children: false
parent: css
layout: page
header-includes:
- \pagenumbering{gobble}
---


# CSS Projects
Now that you’ve learned the basics of CSS, it’s time to revisit your previous HTML projects and make them come alive with styling.  
These projects build *on top of* your HTML work (Projects 01–03), helping you master CSS step by step.  

---

### Project 04: Styling the Recipe Website (CSS Fundamentals)

Take your **HTML Recipe Website (Project 01)** and add CSS to make it visually appealing.

<div class="lesson-content__panel" markdown="1">

#### Iteration 1: link your stylesheet
1. In the root folder of your recipe project, create a file named `style.css`.
2. Link it to each HTML page:

```html
   <link rel="stylesheet" href="style.css">
````

#### Iteration 2: body and text styling

1. Set a light background color for the site.
2. Apply a readable font (`font-family`).
3. Change heading colors and style your links.

#### Iteration 3: recipe cards

1. Wrap each recipe preview on the index page in `<div class="card">`.
2. Style `.card` with:

   * Borders, padding, and margin.
   * Rounded corners.
   * A subtle box-shadow.

#### Iteration 4: hover effects

1. Make links change color on hover.
2. Add a hover effect on `.card` (background color change or shadow).

</div>

---

### Project 05: Styling the Blog Website (Flexbox Layouts)

Upgrade your **Blog Website (Project 02)** with layouts and flexbox.

<div class="lesson-content__panel" markdown="1">

#### Iteration 1: navigation bar

1. Use `display: flex` on `<nav>` to arrange links horizontally.
2. Add a background color.
3. Space out the links evenly.

#### Iteration 2: blog post layout

1. Wrap each blog post in `<div class="post">`.
2. Use fixed width + `margin: auto` to center posts.
3. Style headings with consistent spacing.

#### Iteration 3: sidebar

1. Add an `<aside>` for “About Me” or dummy links.
2. Use flexbox to place it beside posts.
3. Style with contrasting background and padding.

#### Iteration 4: responsive design

1. Add media queries so the sidebar stacks below posts on small screens.
2. Adjust fonts for readability on mobile.

</div>

---

### Project 06: Styling the Portfolio Website (Advanced CSS)

Polish your **Portfolio Website (Project 03)** with flexbox, animations, and responsive design.

<div class="lesson-content__panel" markdown="1">

#### Iteration 1: project cards

1. Wrap each project in `<div class="project-card">`.
2. Use flexbox to arrange cards in rows.
3. Add padding, background, and shadows.

#### Iteration 2: hover interactions

1. Use `transform: scale(1.05)` on hover.
2. Add smooth transitions with:

   ```css
   transition: all 0.3s ease;
   ```

#### Iteration 3: buttons

1. Style “View Project” buttons with:

   * Padding and rounded corners.
   * Gradient backgrounds.
   * Hover color/box-shadow effects.

#### Iteration 4: responsive layout

1. 3 cards per row on desktop.
2. 2 cards per row on tablet.
3. 1 card per row on mobile.
4. Adjust fonts for readability.

</div>

Some of the concepts may not be familiar to you, but I put them there to challenge you, so make sure to be challenged. By the time you complete the third project, you should have learned more than the training has taught you, simply by looking things up.

