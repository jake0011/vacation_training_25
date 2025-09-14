---
title: css
nav_order: 6
has_children: true
parent: Web Development
layout: page
header-includes:
- \pagenumbering{gobble}
---

### Introduction

In the previous lesson, you learned how to write the HTML that determines how a web page is structured. The next step is to make that structure look good with some *style*, which is exactly what CSS is for. In the next few lessons, we're going to focus on what we believe are some foundational CSS concepts, things that everyone should know from the beginning — whether they are just starting out or need a refresher.

### Lesson overview

This section contains a general overview of topics that you will learn in this lesson.

- Add styles to HTML with CSS.
- Understand how to use the class and ID attributes.
- Add styles to specific elements using the correct selectors.


## Before that;
Being able to inspect and debug your HTML and CSS is critical for frontend development. This lesson will take us through the Chrome Dev Tools, which allow you to see detailed information about your elements and CSS rules, as well as assist you in finding and fixing problems in your code.

### The inspector

To open up the inspector, you can right-click on any element of a webpage and click "Inspect" or press F12. Go ahead and do that right now to see the HTML and CSS used on this page.

Don't get overwhelmed with all the tools you're now seeing! For this lesson, we want to focus on the Elements and Styles panels.

### Inspecting elements

In the Elements panel, you can see the entire HTML structure of your page. You can click on any of the elements in this panel to select that specific element. Alternatively, you can click the blue-highlighted icon shown below on the left, and hover over any element on the page.

![Inspector Icon](https://cdn.statically.io/gh/TheOdinProject/curriculum/594984d7c9f9e744577f19ea475b3864e8cc7c91/html_css/v2/foundations/inspecting-html-and-css/imgs/01.png)

<span id="strikethrough">When an element is selected, the Styles tab will show all the currently applied styles, as well as any styles that are being overwritten (indicated by a strikethrough of the text).</span> For example, if you use the inspector to click on the "Your Career in Web Development Starts Here" header on the [TOP homepage](https://www.theodinproject.com/home), on the right-hand side you'll see all the styles that are currently affecting the element, as seen below:

![Overwritten style](https://cdn.statically.io/gh/TheOdinProject/curriculum/f8fd38fc62578d8e8368f5303126215a492847f0/foundations/html_css/inspecting-html-and-css/imgs/03.png)

### Testing styles in the inspector

The Styles panel also allows you to edit styles directly in the browser. You can click inside of any individual selector to add a new rule or click on an existing attribute or value to alter it. When doing so, the webpage responds with the changes in real-time. This won’t affect the source code in your text editor, but it is extremely useful for quickly testing out various attributes and values without needing to reload the page over and over again.

