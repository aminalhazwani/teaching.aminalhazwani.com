---
layout: post
title:  "Intro to web development - Part 2"
day:    "Tue, March 16"
time:   "10 AM - 12 PM"
meta:   "So, do you remember how to set a heading in HTML? And how to style a paragrpah? Sure you do! During this lecture we review our HTML knowledge and we introduce new HTML tags and CSS properties"
current: true
visible: true
---

## Customize Sublime Text 3

### Install a theme to the text editor

1. Press `cmd` + `shift` + `P` or `ctrl` + `shift` + `P` (on Windows/Linux) to access the Package Control
2. Type "install"
3. Search for "Material Theme"
4. Press `enter`

If the theme doesn't load:

1. Press `cmd` + `,` which opens the user settings
2. Copy and paste `"theme": "Material-Theme.sublime-theme", "color_scheme": "Packages/Material Theme/schemes/Material-Theme.tmTheme"`

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

- Header

```html
<header>
  <img src="logo.gif" alt="Brand's logo">
  <p>Tagline</p>
</header>
```

- Navigation

```html
<nav>
  <a href="/about/">About</a> |
  <a href="/work/">Work</a> |
  <a href="/contact/">Contact</a> |
  <a href="/blog/">Blog</a>
</nav>
```

- Footer

```html
<footer>
  <p>© 2016 Name Surname, unless otherwise noted.</p>
  <p>Write me: <a href="mailto:someone@example.com">someone@example.com</a></p>
</footer>
```

- Section

```html
<section>
  <h1>WWF</h1>
  <p>The World Wide Fund for Nature (WWF) is....</p>
</section>
```

- Article

```html
<article>
  <h1>Google Chrome</h1>
  <p>Google Chrome is a free, open-source web browser developed by Google, released in 2008.</p>
</article>
```

- Main

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

## New CSS

### Classes and Ids

Classes and ids are identifiers which can be manually added to HTML in order to make it easier to style. Classes are generally used when many elements share the same styles, while ids should only be used for one element.

```html
<div class="class1 class2 class3">
  ...
</div>

<div id="id">
  ...
</div>
```

**Note**: It's good practice not to use ids to style elements because they have a higher precedence than other selectors, which means overriding them can get messy.

### Pseudo-classes

Pseudo-classes specify a state of an element.

```css
selector:pseudo-class {
  property: value;
}
```

For example:

```css
a:hover {
  color: green;
}

.widget:last-of-type {
  margin-right: 0;
}

.container:nth-child {
  margin-right: 0;
}
```

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

### Display

Defines the type of a box element:

- Hide an element from the page: `display: none;`
- Flow elements like a word in a paragraph (width, height and vertical margins cannot be set): `display: inline;`
- Element does not flow (width, height and margins can be set freely): `display: block;`
- Flow elements like a word in a paragraph (width, height and vertical margins can be set freely): `display: inline-block;`
- Magic rainbow unicorns (more about it later): `display: flex;`

### Position

Specifies the type of positioning method used for an element:

- Static: `position: static`
- Relative: `position: relative;`
- Absolute: `position: absolute;`
- Fixed: `position: fixed;`