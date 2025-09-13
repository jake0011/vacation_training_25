---
title: HTML Projects
nav_order: 2
has_children: false
parent: Web Development
layout: page
header-includes:
- \pagenumbering{gobble}
---

# Projects.
It's time to practice all of the HTML knowledge you have acquired. There will be about 3 projects you are going to build with only HTML.

### Setting up your project's GitHub repository

As mentioned in the introduction lesson, you'll want to organize all your projects like a portfolio and link them to GitHub so it can be seen by others.

<div class="lesson-note lesson-note--warning" markdown="1">

#### Be careful about creating files on GitHub

GitHub allows us to make changes directly on its site. If you do this after you have cloned the repository to your machine, it will cause your local code to be a version behind the remote, creating extra challenges when you push your work. Most of the time, you should be creating files locally.

 As you progress in the course, you'll learn how to handle these situations, but for now, it's important to follow the instructions carefully to stay on the simple path.

</div>

If you do not know how to set up a repository, follow instructions found in the introduction to learn how, before carrying on with these steps:

1. Create a new repo for this project on GitHub.com and call it `vacation_training_25`, leave this step if you already have the repo setup. Make sure to choose the `public` option instead of the default private.

1. Clone that repository onto your local machine, inside the vacation_training directory/folder that you previously created. The command should look like `git clone git@github.com:username/vacation_training_25.git` (use SSH).

1. Now `cd` into the `vacation_training_25` project directory that is now on your local machine.

1. Set up your `README.md` file and write a brief introduction describing what the current project is and what skills you will have demonstrated once you have completed it. (You can also do this as a self-reflection at the end of the project, which is a good way to review what you have learned.)

If you are having trouble:

- All Git commands need to be run from inside your project's folder (did you forget to `cd` into the `vacation_training_25` folder?).

#### Tips on when to commit

When you're building your project, you will probably end up doing several `git add` + `git commit` cycles before being ready to push it up to GitHub with `git push origin main`.

When writing code, it's considered best practice to commit early and often. Commit every time you have a meaningful change in the code. This will create a timeline of your progress and show that your finished code didn't appear out of nowhere.

After you have entered `git push origin main`, switch over to your browser and open your repository on GitHub. You should now see all the files you just pushed.

Okay, that's enough Git for the moment -- time to actually build stuff!

---

### Project 01
In this project, you are going to build a basic recipe website.

The website will consist of a main index page which will have links to a few recipes. The website won't look very pretty by the time you've finished but it's important to keep in mind that the purpose of this project is to build your HTML chops; we will revisit this project in the future to style it up with CSS.

<div class="lesson-content__panel" markdown="1">

#### Iteration 1: initial structure

1. Within the `vacation_training_25` directory, create an `index.html` file.
1. Fill it out with the usual boilerplate HTML and add an `h1` heading "William's Recipes" to the body.

#### Iteration 2:  recipe page

1. Create a new directory within the `vacation_training_25` directory and name it `recipes`.
1. Create a new HTML file within the  `recipes` directory and name it after the recipe it will contain. For example `lasagna.html`. You can use the name of your favorite dish or, if you need some inspiration, you can find a recipe to use at [Allrecipes](https://www.allrecipes.com/). Be sure to include the usual boilerplate HTML. This boilerplate code should be in every `.html` file you create.
1. For now, just include an `h1` heading with the recipe's name as its content.
1. Back in the `index.html` file, add a link to the recipe page you just created. Example: Under the `<h1>Odin Recipes</h1>` heading, write out the link like so: `<a href="recipes/recipename.html">Recipe Title</a>`. The text of the link should again be the recipe name.
1. **Add a link back to the index page** on your recipe page for easier navigation. You can place this link at the top or bottom of your recipe page (e.g., `lasagna.html`). Here's an example:

   ```html
   <a href="../index.html">Home</a>
   ```

   This allows users to quickly return to the home page after viewing the recipe.

#### Iteration 3:  recipe page content

Your new recipe page should have the following content:

1. A free image of the finished dish under the h1 heading that you added earlier.

1. Under the image, it should have an appropriately sized "Description" heading followed by a paragraph or two describing the recipe.

1. Under the description, add an "Ingredients" heading followed by an **unordered list** of the ingredients needed for the recipe.

1. Finally, under the ingredients list, add a "Steps" heading followed by an **ordered list** of the steps needed for making the dish.

#### Iteration 4: add more recipes

1. Add two more recipes with identical page structures to the recipe page you've already created.
1. Don't forget to link to the new recipes on the index page. Also, consider putting all the links in an unordered list so they aren't all on one line.

Example:

```html
 <ul>
    <li><a href="recipes/yourrecipe.html">Recipe Title 1</a></li>
    <li><a href="recipes/yourrecipe.html">Recipe Title 2</a></li>
    <li><a href="recipes/yourrecipe.html">Recipe Title 3</a></li>
  </ul>
```
  
Your links won't be flashy, but for now, just focus on building them out.

</div>

### Viewing your project on the web

If you want to show your work (the project) to others, or submit a solution below, you will need to publish your site so that others can access it from the web, rather than just on your local machine. The good news is that if you have your project on GitHub (as described above), doing this is straightforward.

GitHub allows you to publish web projects directly from a GitHub repository. Doing this will allow you to access your project from `your-github-username.github.io/your-github-repo-name`.

<div class="lesson-note">

A GitHub paid account is required to publish web projects from a private repository. Free accounts can only publish from public repositories. This training website was created using Github pages.

</div>

There are a couple of ways to go about doing this, but the simplest is this:

1. Make sure that the main HTML file of your project is called `index.html`. If it is not, you will need to rename it.
1. Go to your GitHub repo on the web and click the **Settings** button as shown in the screenshot below.
    ![Screenshot pointing to the Settings located in an example repository](https://cdn.statically.io/gh/TheOdinProject/curriculum/90b1a362af0bb8635af9593cd8911c9aefb68569/foundations/html_css/html-foundations/imgs/01.png)
1. Click on **Pages** on the left side bar.
1. Change the **Branch** from *none* to *main branch* and click **Save**.
1. It may take a few minutes (The GitHub website says up to 10, but we've seen it take up to an hour. Do not add a "theme" to your project, or you may have git conflicts, instead, be patient.) but your project should be accessible over the web from `your-github-username.github.io/your-github-repo-name` (obviously substituting your own details in the link).
1. If your project does not publish after 1 hour, ensure that you have a file called `index.html` in the root of your repository and all the settings have been set correctly.  Go to your repo on GitHub and click on Actions, if there are no entries, then go back to the settings, change the **Branch** from *main branch* to *none* and click **Save**, then change the **Branch** from *none* to *main branch* and click **Save**.

---

### Project 02
In this project, you are going to build a **personal portfolio webpage**.  
This will help you practice organizing multiple sections, linking pages together, and structuring content in a way that feels like a real-world project.

<div class="lesson-content__panel" markdown="1">

#### Iteration 1: basic structure

1. Inside your `vacation_training_25` directory, create a new folder called `portfolio`.
1. Inside it, create an `index.html` file with the boilerplate HTML.
1. Add an `<h1>` heading with your name, e.g. “Hi, I’m William!”

#### Iteration 2: About Me section

1. Below the heading, create an “About Me” section with an `<h2>` tag.
1. Add a short paragraph describing yourself (pretend it’s for a real employer).
1. Include a small profile image of yourself or a placeholder image.

#### Iteration 3: Projects section

1. Create a new `<h2>` heading called “Projects.”
1. Add an **unordered list** with 3 list items, each linking to a placeholder project page (e.g., `project1.html`, `project2.html`, etc.).
1. Create those new HTML files (`project1.html`, etc.) inside the same folder. For now, just give each file a heading like “Project 1 Coming Soon!”

#### Iteration 4: Contact section

1. Add another `<h2>` heading called “Contact Me.”
1. Include a small paragraph encouraging visitors to reach out.
1. Add links using the `<a>` tag to a fake email (e.g., `mailto:you@example.com`) and your GitHub profile.

#### Iteration 5: Navigation

1. Add a simple navigation bar at the top of the page (just a `<nav>` with links to “About,” “Projects,” and “Contact”).
1. Make the links anchor tags that scroll the page (use `href="#about"`, `href="#projects"`, `href="#contact"` and add the corresponding `id` attributes to your sections).

</div>

This project helps you think about **page layout, sections, navigation, and linking multiple pages together**.

---

### Project 03
In this project, you are going to build a **blog website**.  
This will challenge you to work with multiple posts, semantic HTML, and richer structures like articles and footers.

<div class="lesson-content__panel" markdown="1">

#### Iteration 1: blog homepage

1. Inside `vacation_training_25`, create a folder called `blog`.
1. Add an `index.html` file. Give it a heading “My Blog.”
1. Below the heading, create a navigation menu with links to `about.html` and `contact.html`.

#### Iteration 2: blog posts list

1. On the homepage, create a section titled “Recent Posts.”
1. Inside, create 3 blog post previews.  
   - Each should be inside an `<article>` tag.  
   - Include a post title (`<h2>`), a short paragraph summary, and a “Read more” link.  
   - Each link should go to its own HTML file (e.g., `post1.html`, `post2.html`, `post3.html`).

#### Iteration 3: individual blog post pages

1. Create `post1.html`, `post2.html`, and `post3.html`.  
2. Inside each, include:
   - A main title (`<h1>`) for the post.  
   - The date (`<time>`) of the post.  
   - Several paragraphs of placeholder content.  
   - An image inside the article (you can use a free stock image or placeholder).  
   - A link back to the homepage.

#### Iteration 4: footer

1. On each page (homepage and post pages), add a `<footer>` with your name and a copyright symbol.  
2. Also add links to your GitHub and email here as well.

#### Iteration 5: extra credit (optional)

1. Add a sidebar (`<aside>`) on your homepage with a list of categories or tags.  
2. Add a simple “Subscribe” form using a text input and a submit button (it won’t work yet, but we’ll wire things up later).

</div>

This project helps you learn **semantic HTML tags, structuring multiple pages into a website, and creating reusable sections (like navigation and footers)**.

