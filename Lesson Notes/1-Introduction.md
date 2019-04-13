# Introduction to HTML and CSS
## The Internet

- A bunch of computers
- Each are communicating with each others
- Sending data (or files) between them

> We do this with **CODE**

## The Tools

We'll be making use of the following tools in this class just so that everyone is on the same page

1. Visual Studio Code - Text Editor - Like Word or Notes
2. Google Chrome - Web Browser - Like Safari for the Apple People
3. Git and GitHub - Version Control and Code Sharing - Like Google Drive for code
4. Live Server Extension - Don't worry about this now

> Overview of tools

Our Code will be made of three different parts

1. HTML for content
2. CSS for style
3. JS for the fun stuff

## HTML - Intro to Tags

> Short for HyperText Markup Language

- An HTML file is sent by the server when we go to a specific website
- Browser then displays that file to us
- Uses **Tags** to display content

An HTML Tag tells the browser where certain information/content starts and ends

For example, an HTML file starts and ends  with the `html` tag

```html
<html> Opening HTML Tag
    ...
    Your Website Code
    ...
</html> Closing HTML Tag
```

### A Basic HTML File

The minimum requirements for an HTML file are just the following

```html
<html>
<head>
    <title>Title for your website</title>
</head>
<body>
    Hello, World!, <br>
    code that is not in the body will not be visible on the page, such as the title
</body>
<html>
```

> Now follow along

### Adding Content

An HTML File makes use of a lot of different types of tags, but a typical HTML File will consist of the following

```html
<html>
<head>
    <title>IT Class, Lesson 1</title>
</head>
<body>
    <h1>Heading 1</h1>

    <h2>Heading 2</h2>

    <p>This is a paragraph of text. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam lobortis turpis vulputate hendrerit tincidunt. Nunc vitae commodo orci, a bibendum odio. Morbi quis sapien pulvinar nunc molestie iaculis. Vivamus sit amet lacinia ex. Sed bibendum turpis nec cursus tincidunt.</p>

    <p>This is another paragraph<br>But with a line break</p>

    <p id="Bob">And this paragraph has a ID. His name is Bob</p>

    <div>This is just a general block, it can be anything you want, even just a line like the next tag.</div>

    <hr/>

    <p>Some tags can be inline like the <span>Span Tag (Which is like the div of inline tags</span> or even the <b>Bold Tag</b></p>

    <li>We even get list tags</li>
    <li>Like these</li>

    <ol>
        <li>Which can work differently</li>
        <li>When inside of other tags</li>
        <li>Like an Numbered List</li>
    </ol>

    <h2>Tags can be <b>ANYTHING</b> you want them to be, even an image or link to another website</h2>

    <p><a href="https://giphy.com">I am a link to Giphy3</a> Links make use of an "href" attribute, which we'll discuss later</p>
    
    <img src="https://media.giphy.com/media/jquDWJfPUMCiI/200w.webp" width="500px">
</body>
</html>
```

### 'Invisible' Tags

However, not all tags can be seen, such as `style` and `script` tags, as well as any `comments`

```html
<style>
    /* This is where we write the code
    that makes our website look good */
</style>

<script>
    // This is where we write the code
    // that makes our website do things
</script>

<!-- <h1>My Name is Nabeel</h2> -->
```

> Code can be commented out for us to come back to later or to provide information to anyone reading our code


Tags can even be used to get files from other websites, like the `link` tag below, which will get a font and allow us to use it on our website

```html
<link href="https://fonts.googleapis.com/css?family=Heebo|Open+Sans" rel="stylesheet">
```

We can put things like links to other files we want to use in our `head` or `body` depending on what we need to do

### Project Overview

We'll be making a simple To-Do list website that will let you add items and remove items, and you know - do all the to-do-ing that you need to do

To get started let's add the following to our HTML

1. The `html`, `head`, and `body` tags
2. `title` tag inside the `head` with the name of your website
3. `h1` tag inside the `body` with a heading for your website
4. An Ordered List with some to-do items using the `ol` tag for your overall list and the `li` tag for each item

> Now that everyone has done that, we can move on to CSS

## CSS - Intro to Styles

> Short for Cascading Style Sheets

- CSS is the language used to make our websites look good
- It makes use of `selectors` to say what elements to change
- And `properties` and `values` to say how to change them
- Written inside of an HTML element or a `style` tag (We'll cover both of these)

A `style` in its simplest form consists of a `property` and `value`. For example:

```css
color: red;
```

### Style Attribute

If we are only going to be using a specific style on a single element, we can make use of Inline CSS

HTML Elements have `attributes`, these allow us to give more information to an element, such as the `href` and `src` attributes from before

When adding a **inline** style we can use the `style` attribute, such as

```html
<h1 style="color: red;">Hello World</h1>
```

An element can have multiple styles as well, separated by a semicolon '`;`'

```html
<h1 style="border-color: red; border-width: 5px; border-style: solid;">Hello, World!</h1>
``` 

> Try to change the style of one of your elements

### Style Tag

The style tag, unlinke the method above, allows us to change the style of multiple elements at a time. We can do this using **selectors**

Selectors can be

1. Element Types
2. ID's
3. Element *Classes*
4. Any Combination of the Above

We can style all elements of a specific type based on their Element type as follows. This is done in a `style` tag, and makes use of the following structure

![W3 Schools CSS Selectors](https://www.w3schools.com/css/selector.gif)

#### Element Selectors

```css
<style>
    h1 {
        color: red;
    }

    p {
        border-color: blue;
        border-width: 5px;
        border-style: solid;
    }
</style>
```

> Let's try to use the above method to style out Headings and List Items using a Font from Google Fonts

We can add the font to our `head` tag

```html
<head>
    <link href="https://fonts.googleapis.com/css?family=Heebo|Open+Sans" rel="stylesheet">
    ...
</head>
```

And then use it in our CSS like so:

```html
<style>
    h1 {
        font-family: 'Heebo', sans-serif;
    }

    p {
        font-family: 'Open Sans', sans-serif;
    }
</style>
```

#### ID's

We can select based on an ID for a specific element with the `id` attribute

```html
<h1 id="Bob">My Name is Bob</h1>

<style>
    #Bob {
        color: green;
    }
</style>
```

#### Classes

We can also define classes, the difference between a class and an ID is that **ID's should only be used once** in a website, we can use classes **As many times as we want**

1. A class can be added the element in the `class` attribute
2. An element can have one class, or many classes

```html
<h1 class="green">I am Green</h1>

<h2 class="green underline">I am Grunderline</h2>

<style>
    .green {
        color: green;
    }

    .underline {
        text-decoration: underline;
    }
</style>
```

> Themes give us styles that can be used with `class` names