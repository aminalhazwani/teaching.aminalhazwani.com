---
layout: post
title:  "Intro to web development - Part 2"
day:    "Tue, March 16"
time:   "10 AM - 12 PM"
meta:   "So, do you remember how to set a heading in HTML? And how to style a paragraph? Sure you do! During this lecture we review our HTML knowledge and we introduce new HTML tags and CSS properties"
current: true
visible: true
---

## Customize Sublime Text 3

### Install a theme to the text editor

1. Press `cmd` + `shift` + `P` or `ctrl` + `shift` + `P` (on Windows/Linux) to access the Package Control
2. Type "install"
3. Search for "Material Theme"
4. Press `enter`

A new tab should open with the confermation of the just installed theme.

1. Press `cmd` + `,` or `Preferences > Settings - User` (on Win/Linux) which opens the user settings
2. Copy and paste `"theme": "Material-Theme.sublime-theme", "color_scheme": "Packages/Material Theme/schemes/Material-Theme.tmTheme"` (pay attention to the commas)

You should now have your brand new Sublime Text theme. If you notice some graphical problems simply restart Sublime.

## Starting point

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Name Surname, Designer</title>
    <meta description="Write here a nice description about your practise and persona. Between 150 and 160 characters">
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <h1>Name Surname</h1>
    <img src="http://placekitten.com/400/300" alt="A brief description of the picture for screenreaders of if the load fails">
    <p>
      A short description about your practice, your knowledge, clients you worked for, your skills, etc.
    </p>
  </body>
</html>
```

## New HTML Tags

- **Header**<br>It represents a group of introductory or navigational aids. It may contain some heading elements but also other elements like a logo, wrapped section's header, a search form, and so on.

```html
<header>
  <img src="logo.gif" alt="Brand's logo">
  <h1>Brand's name</h1>
</header>
```

- **Navigation**<br>It represents a section of a page that links to other pages or to parts within the page: a section with navigation links.

```html
<nav>
  <a href="/about/">About</a>
  <a href="/work/">Work</a>
  <a href="/contact/">Contact</a>
  <a href="/blog/">Blog</a>
</nav>
```

- **Footer**<br>It typically contains information about the author of the section, copyright data or links to related documents.

```html
<footer>
  <p>© 2016 Name Surname, unless otherwise noted.</p>
  <p>Write me: <a href="mailto:someone@example.com">someone@example.com</a></p>
</footer>
```

- **Section**<br>It represents a generic section of a document, i.e., a thematic grouping of content, typically with a heading. Each `<section>` should be identified, typically by including a heading (`<h1>-<h6>` element) as a child of the `<section>` element.

```html
<section>
  <h1>WWF</h1>
  <p>The World Wide Fund for Nature (WWF) is....</p>
</section>
```

- **Article**<br>It represents a self-contained composition in a document, page, application, or site, which is intended to be independently distributable or reusable (e.g., in syndication). This could be a forum post, a magazine or newspaper article, a blog entry, an object, or any other independent item of content. Each `<article>` should be identified, typically by including a heading (`<h1>-<h6>` element) as a child of the `<article>` element.

```html
<article>
  <h1>Google Chrome</h1>
  <p>Google Chrome is a free, open-source web browser developed by Google, released in 2008.</p>
</article>
```

- **Main**<br>It represents the main content of the `<body>` of a document or application. The main content area consists of content that is directly related to, or expands upon the central topic of a document or the central functionality of an application. This content should be unique to the document, excluding any content that is repeated across a set of documents such as sidebars, navigation links, copyright information, site logos, and search forms (unless the document's main function is as a search form).

```html
<main>
  <section>
    <h1>Tagline</h1>
    <p>Description</p>
  </section>
  <section>
    <article>
      <h2>Title</h2>
      <p>Excerpt</p>
    </article>
    <article>
      <h2>Title</h2>
      <p>Excerpt</p>
    </article>
    <article>
      <h2>Title</h2>
      <p>Excerpt</p>
    </article>
  </section>
</main>
```

The HTML Tags descriptions are from the [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

## New CSS

### Classes

Classes are identifiers which can be manually added to HTML in order to make it easier to style. Classes are generally used when many elements share the same styles.

```html
<div class="class1 class2 class3">
  ...
</div>
```

### Pseudo-classes

Pseudo-classes specify a state of an element.

```css
selector:pseudo-class {
  property: value;
}
```

For example:

```css
p em:last-of-type {
  color: lime;
}
```

```html
<p>
  <em>I'm not lime :(</em>
  <strong>I'm not lime :(</strong>
  <em>I'm lime :D</em>
  <strong>I'm also not lime :(</strong>
</p>

<p>
  <em>I'm not lime :(</em>
  <span><em>I am lime!</em></span>
  <strong>I'm not lime :(</strong>
  <em>I'm lime :D</em>
  <span><em>I am also lime!</em> <strike> I'm not lime </strike></span>
  <strong>I'm also not lime :(</strong>
</p>
```

There are many pseudo-classes avaiable like:

- `:hover`
- `:active`
- `:focus`
- `:first-child`
- `:last-child`
- `:nth-child`
- `:first-of-type`
- `:last-of-type`
- ...and many more!

For a full introduction on pseudo-classes I would suggest you to check the page on [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes).

## Advanced selectors

Style everything on the page: `* {...}`

Style all the children of elements with class `.header`: `.header > * {...}`

Style all the children of elements with class `.header` that are `a` tags: `.header > a {...}`

Style all the descendants (children, children of children and so on) of elements with class `.header` that are `a` tags: `.header a {...}`

## CSS Layouts

### Centering elements

There are two ways of centering elements depending on their context:

**Text elements** (e.g. paragraphs, titles)

```css
text-align: center;
```

**Block elements** (e.g. containers)

```css
margin-left: auto;
margin-right: auto;
```