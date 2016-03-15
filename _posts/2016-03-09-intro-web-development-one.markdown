---
layout: post
title:  "Intro to web development - Part 1"
day:    "Wed, March 9"
time:   "10 AM - 12 PM"
meta:   "If you design for the web it's good to know how the technology behind it works. In this lecture we setup of our machine for web development, we go through a first introduction to HTML documents together with the a small start of CSS"
visible: true
---

## Text editor

Get the _Sublime Text 3_ text editor here: [https://www.sublimetext.com/3](https://www.sublimetext.com/3)

### Install Package Control

The package control allows you to install handy packages for Sublime Text like themes, code linting, toolkits, etc.

The simplest method of installation is through the Sublime Text console. The console is accessed via `View > Show Console` menu. Once open, paste the appropriate Python code for your version of Sublime Text into the console. Go to [https://packagecontrol.io/installation](https://packagecontrol.io/installation) and copy and paste the appropriate Python code for your version of Sublime Text into the console.

## HTML (Content Structure)

Basic structure of a tag: `<tag attribute="value"> content </tag>`

### Page structure

```html
<!DOCTYPE html>
<html>
  <head>
    Meta information about the page
  </head>
  <body>
    Actual content page
  </body>
</html>
```

### Meta Tags

Tags used in the `<head>` containing meta information about the page.

- Title tag

```html
<title> My site's title </title>
```

- Link tag (for including external files like stylesheets and or scripts)

```html
<link rel="stylesheet" href="style.css">
```

- Meta tag (for including general information like special characters or description for SEO)

```html
<meta charset="UTF-8">
```

<!-- <meta name="viewport" content="width=device-width, initial-scale=1"> -->
<!-- Using the meta viewport value `width=device-width` instructs the page to match the screen’s width in device-independent pixels. This allows the page to reflow content to match different screen sizes, whether rendered on a small mobile phone or a large desktop monitor. [^1] -->

### Content Tags

Tags used in the `<body>` to describe the visible element of the page:

- Paragraph

```html
<p> text </p>
```

- Headline

```html
<h1> main headline </h1>
<h2> second-level headline </h2>
...
<h6> sixth-level headline </h6>
```

- Unordered list

```html
<ul>
  <li> list item 1 </li>
  <li> list item 2 </li>
  <li> list item 3 </li>
</ul>
```

- Ordered list

```html
<ol>
  <li> list item 1 </li>
  <li> list item 2 </li>
  <li> list item 3 </li>
</ol>
```

- Image `<img src="http://url.com/image.png" alt="Description of the image">`

### Hyperlinks

- Hyperlink to link from one page to another `<a href="http://url.com/page.html"> Visit the website! </a>`

### Phrase Tags

- Important text `<strong> Important text </strong>`
- Emphasized text `<em> Emphasized text </em>`

### Divider Tag

- Divider (container for other things)

```html
<div>
  ...
</div>
```

### Comments

To make HTML code disappear from the page, you can just add `<!--` and `-->` before and after it.

```html
<!--
  <p> This won't be on the page </p>
-->
<p> This will be! </p>
```

## CSS (Styles)

Basic structure of a stylesheet:

```css
selector {
  property: value;
  property: value;
  property: value;
}
```

And a real-world exmaple:

```css
h1 {
  font-size: 40px;
}

.button {
  padding: 10px;
  color: white;
  background-color: red;
}
```

### Basic visual style

- Color of text: `color: blue;`
- Color of background: `background-color: green;`
- Font family (usually defined as a comma separated list of fonts. If the first font is not installed, it will use the second and so on): `font-family: "Times New Roman", Georgia, serif;`
- Font size (set the font size): `font-size: 24px;`
- Font style (normal, italic or oblique): `font-style: italic;`
- Text align (left, right, center or justify): `text-align: center;`
- Text decoration (underline or strikethrough): `text-decoration: underline;`
- Opacity (0 is invisible, 1 is fully visible): `opacity: .7;`

### Box model

![Image that shows the box model](../uploads/2016/03/box-model.jpg)

To simplify working with the box model, include the following code at the beginning of your CSS. It makes the width and height properties work independently of padding and border.

```css
* {
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
}
```

### Units

- Pixels (pixel on the screen): `padding: 10px;`
- Percentage (usually the percentage of the width of the parent element but depends on the property): `width: 50%`
- Ems (x times the parent element's font size in pixels): `font-size: 1.25em` (equivalent to `font-size: 24px` if the parent's font size is 16px)
- Rems (x times the root `<html>` element's font size in pixels): `margin: 2rem` (equivalent to `margin: 32px` if the root's font size is 16px)

### Color formats

- Built-in-colors (browsers have a few basic colors built in, you can simply use them by name like red, green, blue, black, white, ...): `color: teal;`
- Hexadecimal (describes the RGB value as 3 consecutive hexadecimal numbers #rrggbb): `color: #ff00ba` In this case `ff` is the red value, `00` green, and `ba` blue
- RGB (a different way of writing RGB colors, with decimal numbers, from 0 to 255 for red, green and blue instead of hex numbers): `color: rgb(34, 12, 64);`
- RGBA (exactly the same as the previous, but additionally, the opacity of the color can be defined with the last parameter): `color: rgba(34, 12, 64, 0.3);`