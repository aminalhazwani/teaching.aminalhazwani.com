---
layout: post
title:  "CSS Layouts - Part 1"
day:    "Tue, March 22"
time:   "2 PM - 4 PM"
meta:   "We continue to learn how CSS can help us style our project but we also introduce how to layout things in our canvas with the help of some handy CSS properties like <code>display</code>"
visible: true
---

In this lecture we write the markup for the content that we defined in the [previous workshop](http://teaching.aminalhazwani.com/design-strategy/#workshop-2---part-two). And we start to style it respecting the defined user feelings.

## Starting point

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Name Surname</title>
    <meta description="Write here a nice description about your practise and persona. Between 150 and 160 characters">
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
  </body>
</html>
```

### Add header content

As discussed in the workshop we decide that is important for us to display our logo and name on the porfolio site. For this kind of content the `<header>` tag suits perfectly our need.

```html
<body>
  <header>
    <img src="#" alt="Description of the picture">
    <h1>Name Surname</h1>
  </header>
</body>
```

### Add menu

In order to add a menu to our portfolio website we could use the `<nav>` tag to list all the avaiable pages.

```html
<body>
  <header>...</header>
  <nav>
    <a href="#">Menu item one</a>
    <a href="#">Menu item two</a>
    <a href="#">Menu item three</a>
  </nav>
</body>
```

### Add main content

It's important for our porfolio to diplays our projects with related pictures. So we could wrap them all in a `<section>` and then each singular project could use the `<article>` tag.

```html
<body>
  <header>...</header>
  <nav>...</nav>
  <main>
    <section>
      <h1>Projects</h1>
      <article>
        <img src="#" alt="Description of the project picture">
        <h2>Project title</h2>
        <p>Project description</p>
      </article>
    </section>
  </main>
</body>
```

### Add contacts

In order to add the contact to our page we can user the `<footer>` tag.

```html
<body>
  <header>...</header>
  <nav>...</nav>
  <main>...</main>
  <footer>
    <h3>Contacts</h3>
    <ul>
      <li><a href="#">Mail</a></li>
      <li><a href="#">Facebook</a></li>
      <li><a href="#">Twitter</a></li>
      <li><a href="#">Instagram</a></li>
    </ul>
  </footer>
</body>
```

## New CSS

### Ids

Ids are identifiers which can be manually added to HTML in order to make it easier to style. Ids should only be used for one element.

```html
<div id="id">
  ...
</div>
```

**Note**: It's good practice not to use ids to style elements because they have a higher precedence than other selectors, which means overriding them can get messy.

We can also use ids to create links to specific section of a page.

```html
<nav>
  <a href="#">...</a>
  <a href="#">...</a>
  <a href="#section">Go to section</a>
</nav>
...
<section id="section">
  ...
</section>
```

## CSS Layouts

### Display

Defines the type of a box element:

- Hide an element from the page: `display: none;`
- Flow elements like a word in a paragraph (width, height and vertical margins cannot be set): `display: inline;`
- Element does not flow (width, height and margins can be set freely): `display: block;`
- Flow elements like a word in a paragraph (width, height and vertical margins can be set freely): `display: inline-block;`
- Magic rainbow unicorns (more about it later): `display: flex;`