---
title: html-lesson
nav_order: 1
has_children: false
parent: html
layout: page
header-includes:
- \pagenumbering{gobble}
---

## Introduction to HTML
HTML (HyperText Markup Language) defines the structure and content of webpages. We use HTML elements to create all of the paragraphs, headings, lists, images, and links that make up a typical webpage. In this lesson, we will explore all about HTML.


## Introduction to the HTML Boilerplate

All HTML documents have the same basic structure or boilerplate that needs to be in place before anything useful can be done. In this lesson, we will explore the different parts of this boilerplate and see how it all fits together.


### Creating an HTML file

To demonstrate an HTML boilerplate, we first need an HTML file to work with.

Create a new folder on your computer and name it `html-boilerplate`. Within that folder create a new file and name it `index.html`.

You're probably already familiar with a lot of different types of files, for example doc, pdf, and image files.

To let the computer know we want to create an HTML file, we need to append the filename with the `.html` extension, as we have done when creating the `index.html` file.

It is worth noting that we named our HTML file `index`. We should always name the HTML file that will contain the homepage of our website `index.html`. This is because web servers will by default look for an `index.html` page when users land on our websites -- and not having one will cause big problems.

### The DOCTYPE

Every HTML page starts with a doctype declaration. The doctype's purpose is to tell the browser what version of HTML it should use to render the document. The latest version of HTML is HTML5, and the doctype for that version is `<!DOCTYPE html>`.

The doctypes for older versions of HTML were a bit more complicated. For example, this is the doctype declaration for HTML4:

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
```

However, we probably won't ever want to be using an older version of HTML, so we'll always use `<!DOCTYPE html>`.

Open the `index.html` file created earlier in your text editor and add `<!DOCTYPE html>` to the very first line.

### HTML element

After we declare the doctype, we need to provide an `<html>` element. This is what's known as the root element of the document, meaning that every other element in the document will be a descendant of it.

This becomes more important later on when we learn about manipulating HTML with JavaScript. For now, just know that the `<html>` element should be included on every HTML document.

Back in the `index.html` file, let's add the `<html>` element by typing out its opening and closing tags, like so:

```html
<!DOCTYPE html>
<html lang="en">
</html>
```

Noticed the word `lang` here? It represents an HTML attribute which is associated with the given HTML tag i.e. `<html>` in this case. These attributes provide additional information about HTML elements. (More about `HTML attributes` in the following lesson.)

#### What is the lang attribute?

`lang` specifies the language of the text content in that element. This attribute is primarily used for improving accessibility of the webpage. It allows assistive technologies, for example screen readers, to adapt according to the language and invoke correct pronunciation.

### Head element

The `<head>` element is where we put important meta-information **about** our webpages, and stuff required for our webpages to render correctly in the browser.
Inside the `<head>`, we **should not** use any element that displays content on the webpage.

Back in our `index.html` file, let's add a `<head>` element with a `<meta>` element and a title within it. The `<head>` element goes within the `<html>` element and should always be the first element under the opening `<html>` tag:

```html
<!DOCTYPE html>

<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>My First Webpage</title>
  </head>
</html>
```

#### Meta element

We should always have the `<meta>` tag with the charset encoding of the webpage in the `<head>` element: `<meta charset="UTF-8">`.

Setting the encoding is very important because it ensures that the webpage will display special symbols and characters from different languages correctly in the browser.

#### Title element

Another element we should always include in the head of an HTML document is the `<title>` element:

 `<title>My First Webpage</title>`

The `<title>` element is used to give webpages a human-readable title, which is displayed in our webpage's browser tab. For example, if you look at the current tab's name of your browser, it will read "HTML Boilerplate &#124; The Odin Project"; this is the `<title>` of the current `.html` file.

If we didn't include a `<title>` element, the webpage's title would default to its file name. In our case that would be `index.html`, which isn't very meaningful for users; this would make it very difficult to find our webpage if the user has many browser tabs open.

There are many more elements that can go within the head of an HTML document. However, for now it's only crucial to know about the two elements we have covered here. We will introduce more elements that go into the head throughout the rest of the curriculum.

### Body element

The final element needed to complete the HTML boilerplate is the `<body>` element. This is where all the content that will be displayed to users will go - the text, images, lists, links, and so on.

To complete the boilerplate, add a `<body>` element to the `index.html` file. The `<body>` element also goes within the `<html>` element and is always below the `<head>` element, like so:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>My First Webpage</title>
  </head>

  <body>
  </body>
</html>
```

### Viewing HTML files in the browser

The HTML boilerplate in the `index.html` file is complete at this point, but how do you view it in the browser? There are a couple of different options:

<div class="lesson-note lesson-note--warning" markdown="1">

#### Use Google Chrome

In order to avoid branching our lesson's instructions to accommodate for all of the differences between browsers, we are going to be using Google Chrome as our primary browser for the remainder of this course. All references to the browser will pertain specifically to Google Chrome. We **strongly** suggest that you use Google Chrome for all of your testing going forward.

</div>

1. You can drag and drop an HTML file from your text editor into the address bar of your browser.

1. You can find the HTML file in your file system and then double click it. This will open up the file in the default browser your system uses.

1. You can use the terminal to open the file in your browser:
   - Ubuntu: Navigate to the directory containing the file and type `google-chrome index.html`
   - macOS: Navigate to the directory containing the file and type `open ./index.html`
   - WSL: Navigate to the directory containing the file and type `explorer.exe index.html`. Note, this will open up the file in the default browser your system uses.

Using one of the methods above, open up the `index.html` file we have been working on. You'll notice the screen is blank. This is because we don't have anything in our body to display.

Back in the `index.html` file, let's add a heading (more on these later) to the body, and save the file:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>My First Webpage</title>
  </head>

  <body>
    <h1>Hello World!</h1>
  </body>
</html>
```

Now, if you refresh the page in the browser, you should see the changes take effect, and the heading "Hello World!" will be displayed.

### VSCode shortcut

VSCode has a built-in shortcut you can use for generating all the boilerplate in one go. Please note that this shortcut only works while editing a file with the `.html` extension or a text file with the HTML language already selected. To trigger the shortcut, delete everything in the `index.html` file and just enter `!` on the first line. This will bring up a couple of options. Press the <kbd>Enter</kbd> key to choose the first one, and voila, you should have all the boilerplate populated for you.

You may notice that the boilerplate produced by this shortcut includes a line we have not yet mentioned:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

This is not something we need to know about until we discuss responsive design, an advanced topic involving different screen sizes which we will cover much later in the curriculum. For now, you can leave that line as it is.

It's still good to know how to write the boilerplate yourself in case you find yourself using a text editor like notepad (heaven forbid), which doesn't have this shortcut. Try not to use the shortcut in your first few HTML projects, so you can build some muscle memory for writing the boilerplate code.

## Elements and tags

Almost all elements on an HTML page are just pieces of content wrapped in opening and closing HTML tags.

HTML tags are essential building blocks that define the structure and content of a webpage.

Opening tags tell the browser that this is the start of an HTML element. They are comprised of a keyword enclosed in angle brackets `<>`. For example, an opening paragraph tag looks like this: `<p>`.

Closing tags tell the browser where an element ends. They are almost the same as opening tags; the only difference is that they have a forward slash before the keyword. For example, a closing paragraph tag looks like this: `</p>`.

A full paragraph element looks like this:

```html
<p>some text content</p>
```

Let's break this down:

- `<p>` is the opening tag.
- `some text content` represents content wrapped within the opening and closing tags.
- `</p>` is the closing tag.

You can think of elements as containers for content. The opening and closing tags tell the browser what content the element contains. The browser can then use that information to determine how it should interpret and format the content.

HTML has a [vast list of predefined tags](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) that you can use to create all kinds of different elements. It is important to use the correct tags for content. Using the correct tags can have a big impact on two aspects of your sites: how they are ranked in search engines; and how accessible they are to users who rely on assistive technologies, like screen readers, to use the internet.

Using the correct elements for content is called semantic HTML. We will explore this in much more depth later on in the curriculum.

### Void Elements

Some HTML elements do not have a closing tag. These elements just have a single tag, like: `<br>` or `<img>`. They are known as void elements because they are void of any content, there is nothing inside of them. No closing tag means they can't wrap content like other tags do.

You might also see these referred to as self-closing tags. But those are just void elements with a forward slash(/) at the end like: `<br />` or `<img />`. You're likely to see self-closing tags used often for historical reasons. Browsers will be able to render them just fine, but the latest version of the HTML specification discourages their use and considers them invalid.

---

## Popular Text Elements 
Most content on the web is text-based, so you will find yourself needing to work with HTML text elements quite a bit, so we will look at some of the popular text elements in HTML that you might be using often.

### Paragraphs
What would you expect the following text to output on an HTML page?

```html
<body>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
  incididunt ut labore et dolore magna aliqua.

  Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris
  nisi ut aliquip ex ea commodo consequat.
</body>
```

It looks like two paragraphs of text, so you might expect it to display in that way. However, that is not the case.

When the browser encounters new lines like this in your HTML, it will compress them down into one single space. The result of this compression is that all of the text is clumped together into one long line.

If we want to create paragraphs in HTML, <span id='create-paragraph-element'> we need to use the paragraph element</span>, which will add a new line after each of our paragraphs. A paragraph element is defined by wrapping text content with a `<p>` tag.

Changing our example from before to use paragraph elements fixes the issue.

### Headings

Headings are different from other HTML text elements: they are displayed larger and bolder than other text to signify that they are headings.

<span id='different-heading-levels'>There are 6 different levels of headings starting from `<h1>` to `<h6>`. The number within a heading tag represents that heading's level. The largest and most important heading is h1, while h6 is the tiniest heading at the lowest level.</span>

Headings are defined much like paragraphs. For example, to create an h1 heading, we wrap our heading text in an `<h1>` tag.

Using the correct level of heading is important as levels provide a hierarchy to the content. An h1 heading should always be used for the heading of the overall page, and the lower level headings should be used as the headings for content in smaller sections of the page.

### Strong element

The `<strong>` element makes text bold. It also semantically marks text as important; this affects tools, like screen readers, that users with visual impairments will rely on to use your website. The tone of voice on some screen readers will change to communicate the importance of the text within a strong element. To define a strong element, we wrap text content in a `<strong>` tag.

But you will probably find yourself using the strong element much more in combination with other text elements.

Sometimes you will want to make text bold without giving it an important meaning. You'll learn how to do that in the CSS lessons later in the curriculum.

### Em element

The `<em>` element makes text italic. It also semantically places emphasis on the text, which again may affect things like screen readers. To define an emphasised element, wrap the text content in an `<em>` tag.

Again, like the strong element, you will find yourself mostly using the `<em>` element with other text elements:


### Nesting and indentation

You may have noticed that in all the examples in this lesson we indent any elements that are within other elements. This is known as nesting elements.

<span id='nested-relationship'>When we nest elements within other elements, we create a parent and child relationship between them. The nested elements are the children and the element they are nested within is the parent.</span>

Just as in human relationships, HTML parent elements can have many children.  <span id='elements-same-level'>Elements at the same level of nesting are considered to be siblings.</span>

We use indentation to make the level of nesting clear and readable for ourselves and other developers who will work with our HTML in the future. In our examples, we have indented any child elements by two spaces per nesting level.

The parent, child, and sibling relationships between elements will become much more important later when we start styling our HTML with CSS and adding behavior with JavaScript. For now, however, it is just important to know the distinction between how elements are related and the terminology used to describe their relationships.

### HTML comments

HTML comments are not visible to the browser; they allow us to *comment* on our code so that other developers or our future selves can read them and get some context about something that might not be clear in the code.

In order to write an HTML comment, we just enclose the comment with `<!--` and `-->` tags. 

---

## Links and Images

Links are one of the key features of HTML. They allow us to link to other HTML pages on the web. In fact, this is why it's called the web.

### Preparation

To get some practice using links and images throughout this lesson we need an HTML project to work with.

1. Create a new directory/folder named `vacation-training_25`.
1. Within that directory, create a new file named `index.html`.
1. Open the file in VS Code and fill in the usual HTML boilerplate.
1. Finally, add the following h1 to the body:

```html
<h1>Homepage</h1>
```

### Anchor elements

To create a link in HTML, we use the anchor element. An anchor element is defined by wrapping the text or another HTML element we want to be a link with an `<a>` tag.

Add the following to the body of the `index.html` page we created and open it in the browser:

```html
<a>About The Odin Project</a>
```

You may have noticed that clicking this link doesn't do anything. This is because an anchor tag on its own won't know where we want to link to. We have to tell it a destination to go to. We do this by using an HTML attribute.

<span id="attribute"></span>An HTML attribute gives additional information to an HTML element and always goes in the element's opening tag. An attribute is usually made up of two parts: a name, and a value; however, not all attributes require a value. <span id="where-to-go"></span>In our case, we need to add an `href` (hypertext reference) attribute to the opening anchor tag. The value of the href attribute is the destination we want our link to go to.

Add the following `href` attribute to the anchor element we created previously and try clicking it again, don't forget to refresh the browser so the new changes can be applied.

```html
<a href="https://www.theodinproject.com/about">About The Odin Project</a>
```

By default, any text wrapped with an anchor tag without an `href` attribute will look like plain text. If the `href` attribute is present, the browser will give the text a blue color and underline it to signify it is a link.

It's worth noting you can use anchor tags to link to any kind of resource on the internet, not just other HTML documents. You can link to videos, pdf files, images, and so on, but for the most part, you will be linking to other HTML documents.

### Opening links in a new tab

The method shown above opens links in the same tab as the webpage containing them. This is the default behaviour of most browsers and it can be changed relatively easily. All we need is another attribute: the `target` attribute.

While `href` specifies the destination link, `target` specifies where the linked resource will be opened. If it is not present, then, by default, it will take on the `_self` value which opens the link in the current tab. To open the link in a new tab or window (depends on browser settings) you can set it to `_blank` as follows:

```html
<a href="https://www.theodinproject.com/about" target="_blank" rel="noopener noreferrer">About The Odin Project</a>
```

<span id="target-security"></span>You may have noticed that we snuck in the `rel` attribute above. This attribute is used to describe the relation between the current page and the linked document.

`noopener`: The `noopener` value of the `rel` attribute ensures that a link opened in a new tab or window cannot interact with or access the original page. Without it, the new page can use JavaScript to manipulate the original page, which poses a security risk.

For example:

```html
<a href="https://example.com" target="_blank" rel="noopener">Open Example</a>
```

In this code:
target="_blank": opens the link in a new tab.
rel="noopener": prevents the new tab from accessing the original page, ensuring security. Without `noopener`, the new tab could use JavaScript to interact with the original page, which is unsafe.

`noreferrer`: The `noreferrer` value of the `rel` attribute provides both privacy and security. It prevents the new page from knowing where the user came from (hiding the referrer) and also includes the behavior of `noopener`, preventing the new page from accessing the original page.

For example:

```html
<a href="https://example.com" target="_blank" rel="noreferrer">Visit Example</a>
```

In this example:
target="_blank": opens the link in a new tab.
rel="noreferrer": ensures the new page cannot see the referring page’s address (privacy) and prevents it from accessing the original page (security).

By using rel="noreferrer", you automatically get the benefits of both privacy and security.

Why do we need this added behaviour for opening links in new tabs? Security reasons. The prevention of access that is caused by `noopener` prevents [phishing attacks](https://www.ibm.com/topics/phishing) where the opened link may change the original webpage to a different one to trick users. This is referred to as [tabnabbing](https://owasp.org/www-community/attacks/Reverse_Tabnabbing). Adding the `noreferrer` value can be done if you wish to not let the opened link know that your webpage links to it.

Note that you may be fine if you forget to add `rel="noopener noreferrer"` since more recent versions of browsers [provide security](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a#security_and_privacy) if only `target="_blank"` is present. Nevertheless, in line with good coding practices and to err on the side of caution, it is recommended to always pair a `target="_blank"` with a `rel="noopener noreferrer"`.

### Absolute and relative links

Generally, there are two kinds of links we will create:

- Links to pages on other websites on the internet.
- Links to pages located on our own websites.

#### Absolute links

Links to pages on other websites on the internet are called absolute links. A typical absolute link will be made up of the following parts: `scheme://domain/path`. An absolute link will always contain the [scheme and domain](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL#basics_anatomy_of_a_url) of the destination.

We've already seen an absolute link in action. The link we created to The Odin Project's About page earlier was an absolute link as it contains the scheme and domain.

`https://www.theodinproject.com/about`

#### Relative links

Links to other pages within our own website are called relative links. Relative links do not include the domain name, since it is another page on the same site, it assumes the domain name will be the same as the page we created the link on.

Relative links only include the file path to the other page, *relative* to the page you are creating the link on. This is quite abstract, let's see this in action using an example.

Within the `odin-links-and-images` directory, create another HTML file named `about.html` and paste the following code into it:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Odin Links and Images</title>
  </head>

  <body>
    <h1>About Page</h1>
  </body>
</html>
```

Back in the index page, add the following anchor element to create a link to the about page:

```html
<body>
  <h1>Homepage</h1>
  <a href="https://www.theodinproject.com/about">About The Odin Project</a>

  <a href="about.html">About</a>
</body>
```

Open the index file in a browser and click on the about link to make sure it is all wired together correctly. Clicking the link should go to the about page we just created.

This works because the index and about page are in the same directory. That means we can use its name (`about.html`) as the link's `href` value.

But we will usually want to organize our website directories a little better. Normally we would only have the `index.html` at the root directory and all other HTML files in their own directory.

Create a directory named `pages` within the `odin-links-and-images` directory and move the `about.html` file into this new directory.

Refresh the index page in the browser and then click on the about link. It will now be broken. This is because the location of the about page file has changed.

To fix this, we just need to update the about link `href` value to include the `pages/` directory since that is the new location of the about file *relative* to the index file.

```html
<body>
  <h1>Homepage</h1>
  <a href="pages/about.html">About</a>
</body>
```

Refresh the index page in the browser and try clicking the about link again, it should now be back in working order.

In many cases, this will work just fine; however, you can still run into unexpected issues with this approach. Prepending `./` before the link will in most cases prevent such issues. By adding  `./` you are specifying to your code that it should start looking for the file/directory *relative* to the `current` directory.

```html
<body>
  <h1>Homepage</h1>
  <a href="./pages/about.html">About</a>
</body>
```

#### A metaphor

Absolute and relative links are a tricky concept to build a good mental model of, a metaphor may help:

Think of your domain name (`town.com`) as a town, the directory in which your website is located (`/museum`) as a museum, and each page on your website as a room in the museum (`/museum/movie_room.html` and `/museum/shops/coffee_shop.html`). Relative links like `./shops/coffee_shop.html` are directions from the current room (the museum movie room `/museum/movie_room.html`) to another room (the museum shop). Absolute links, on the other hand, are full directions including the protocol (`https`), domain name (`town.com`) and the path from that domain name (`/museum/shops/coffee_shop.html`): `https://town.com/museum/shops/coffee_shop.html`.

## Images

Websites would be fairly boring if they could only display text. Luckily HTML provides a wide variety of elements for displaying all sorts of different media. The most widely used of these is the image element.

To display an image in HTML we use the `<img>` element. Unlike the other elements we have encountered, the `<img>` element is a void element. As we have seen earlier in the course, void elements do not need a closing tag because they are naturally empty and do not contain any content.

Instead of wrapping content with an opening and closing tag, it embeds an image into the page using a `src` attribute which tells the browser where the image file is located. The `src` attribute works much like the `href` attribute for anchor tags. It can embed an image using both absolute and relative paths.

For example, using an absolute path we can display an image located on The Odin Project site.

To display images on your website that are hosted on your own web server, you can use a relative path.

<details markdown="block">

<summary class="dropDown-header">Linux, macOS, ChromeOS</summary>

1. Create a new directory named `images` within the `odin-links-and-images` project.
1. Next, [download our practice image](https://unsplash.com/photos/Mv9hjnEUHR4/download?force=true&w=640) and move it into the images directory we just created.
1. Rename the image to `dog.jpg`.

</details>

<details markdown="block">

<summary class="dropDown-header">WSL2</summary>

When you download a file from the internet, Windows has a security feature that creates a hidden `Zone.Identifier` file with the same name as your downloaded file and it looks like `mypicture.jpg:Zone.Identifier` This file is harmless, but we'd like to avoid copying it over and cluttering up our directories.

1. Create a new directory named `images` within the `odin-links-and-images` project.

1. Next, [download the stock dog image](https://unsplash.com/photos/Mv9hjnEUHR4/download?force=true&w=640).

1. Right click on the new download at the bottom of the chrome window and select "Show in folder".

   1. Alternatively, if you do not see anything at the bottom of the chrome window, open the "Customize and control Google Chrome kebab menu and select the "Downloads" item. This will show all of your downloads, each with its own "Show in folder" button.

1. Rename the image to `dog.jpg`.

1. Drag the file from your downloads folder to VSCode's file browser into your new `images` directory.

   1. Alternatively, using your Ubuntu terminal, navigate to the folder you want to copy the image to (`cd ~/odin-links-and-images` for example)

   1. Type `cp <space>`

   1. Drag the `dog.jpg` image from a Windows Explorer window and drop it onto the terminal window, it should appear as `"/mnt/c/users/username/Downloads/dog.jpg"`

   1. Type `<space> .` to tell cp that you want to copy the file to your current working directory. The full command will look something like:

   ```bash
   cp "/mnt/c/users/username/Downloads/dog.jpg" .
   ```

   1. Hit <kbd>Enter</kbd> to complete the command, and use `ls` to confirm the file now exists.

Dragging files from Windows into the VSCode file browser prevents the `Zone.Identifier` files from being copied over. From now on, any time you need to copy pictures or other downloaded files like this into WSL2, you can do it in this way. If you ever accidentally copy these `Zone.Identifier` files into WSL2, you can safely delete them without any issue.

</details>

Finally add the image to the `index.html` file:

```html
<body>
  <h1>Homepage</h1>
  <a href="https://www.theodinproject.com/about">About The Odin Project</a>

  <a href="./pages/about.html">About</a>

  <img src="./images/dog.jpg">
</body>
```

Save the `index.html` file and open it in a browser to view Charles in all his glory.

<div class="lesson-note lesson-note--warning" markdown="1">

#### Images you use should be free for your intended purpose

There are many free images available but make sure to give credit to the creator of the image in your project.

An easy way to provide credit is to include the creator's name and contact info in a README file in your repository, or give [attribution](https://support.freepik.com/s/article/Attribution-How-when-and-where?language=en_US).

To find them - Google images and in image results -> Tools -> Usage rights -> "Creative Commons". Choose & click on a image and click license details.

We recommend that you always review the license requirements of any images you want to use.

</div>

### Parent directories

What if we want to use the dog image in the about page? We would first have to go up one level out of the pages directory into its parent directory so we could then access the images directory.

<span id="parent-filepath"></span>To go to the parent directory we need to use two dots in the relative filepath like this: `../`. Let's see this in action, within the body of the `about.html` file, add the following image below the heading we added earlier:

```html
<img src="../images/dog.jpg">
```

To break this down:

1. First, we are going to the parent directory of the `pages` directory which is `odin-links-and-images`.
1. Then, from the parent directory, we can go into the `images` directory.
1. Finally, we can access the `dog.jpg` file.

Using the metaphor we used earlier, using `../` in a filepath is kind of like stepping out from the room you are currently in to the main hallway so you can go to another room.

### Alt attribute

<span id="two-attributes"></span>Besides the `src` attribute, every image element should also have an `alt` (alternative text) attribute.

The `alt` attribute is used to describe an image. It will be used in place of the image if it cannot be loaded. It is also used with screen readers to describe what the image is to visually impaired users.

As a bit of practice, add an `alt` attribute to the dog image we added to the `odin-links-and-images` project.

### Image size attributes

While not strictly required, specifying height and width
attributes in image tags helps the browser layout the page without causing the page to jump and flash.

It is a good habit to always specify these attributes on every image, even when the image is the correct size or you are using CSS to modify it.


Go ahead and update the `odin-links-and-images` project with width and height attributes on the dog image.

### Lists

Whether it be IMDB's top 250 movies or the FBI's most wanted, lists are everywhere on the web and you are going to need one eventually in your webpages.

Luckily, with HTML there are a couple of different types of lists at your disposal.


### Unordered lists

If you want to have a list of items where the order doesn't matter, like a shopping list of items that can be bought in any order, then you can use an unordered list.

Unordered lists are created using the `<ul>` element, and <span id="li"></span>each item within the list is created using the list item element `<li>`.

Each list item in an unordered list begins with a bullet point.

### Ordered lists

If you instead want to create a list of items where the order *does* matter, like step-by-step instructions for a recipe, or your top 10 favorite TV shows, then you can use an ordered list.

Ordered lists are created using the `<ol>` element. Each individual item in them is again created using the list item element `<li>`. However, each list item in an ordered list begins with a number instead.


That should wrap up the basics of HTML needed to complete some wild wild projects.

Visit the next sub-page to start your projects.

