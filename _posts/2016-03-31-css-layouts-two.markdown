---
layout: post
title:  "CSS Layouts - Part 2"
day:    "Thu, March 31"
time:   "2 PM - 4 PM"
meta:   "Do your remember how to create simple layouts in CSS? In this lecture we rock and we build much more complex grid systems. Fasten your seatbelt, we are gonna fly!"
visible: true
---

## Starting Point

The starting point of this lecture is the markup and the styles we wrote last class after the _establish design direction_ workshop. We translated the content we defined in the workshop in HTML tags and CSS properties. You can download the resulting code with [this .zip file](https://drive.google.com/open?id=0Bx1h0_Ovh8h2aTMzZUF3MU5rWEU).

The task for today is to add real content and learn new CSS properties to continue with the style definition. 

## New Meta Tags

### Charset

This attribute declares the character encoding used of the page.

```html
<meta charset="utf-8">
```

### Viewport

It gives hints about the size of the initial size of the `viewport`. This pragma is used by several mobile devices only.

```html
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1">
```

## New CSS

### Background image

```css
.class {
  background-image: url('http://url.com');
  background-position: center
  background-size: cover
  background-repeat: no-repeat
}
```

### Display

We review the `display` property and in particular the `inline-block` value. We learn that this property adds spaces in between the elements. To reset this space we simply add a negative margin:

```css
.class {
  display: inline-block;
  margin-right: -4px;
}
```

### Calc function

You can perform calculations to determine CSS property values:

```css
.class {
  width: calc(50% - 4px);
}
```

### Pseudo classes

We review what a pseudo-classe is and how we can use it:

```css
selector:pseudo-class {
  property: value;
}
```

For example, consider the following markup:

```html
<nav>
  <a class="nav_item" href="#">Menu item one</a>
  <a class="nav_item" href="#">Menu item two</a>
  <a class="nav_item" href="#">Menu item three</a>
</nav>
```

We want to add some distance between the navigation items. We could add some `padding` or `margin` between each of the item:

```css
.nav_item {
  padding: 0 16px; // Shorter form for "padding: 0 16px 0 16px;"
}
```

But the resulting space between the first and the second menu item and the second and the third menu item would be `32px` because the paddings are sum together. In order to address this issue we could simply apply the `padding` just to the second menu item with the help of the `:nth-child` pseudo-class:

```css
.nav_item:nth-child(2) {
  padding: 0 16px;
}
```

Many are the pseudo-classes available that you can use:

- `:hover`
- `:active`
- `:focus`
- `:first-child`
- `:last-child`
- `:nth-child`
- `:first-of-type`
- `:last-of-type`
- ...and many more!

For a full introduction to pseudo-classes I would suggest you to check the page on [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes).

### Media Queries

Media Queries is a module of CSS that defines expressions allowing to tailor presentations to a specific range of output devices without changing the content itself. We can set the media type and/or the a number of [media features](https://developer.mozilla.org/en-US/docs/Web/CSS/@media#Media_features) .

```css
@media screen and (min-width: 480px) {
  .class {
    ...
  }
}
```

### Position

Specifies the type of positioning method used for an element. It can be useful for scripted animation effects, for sticky navigation or to control the position element relatively to their parent container. 

- Static: `position: static`
- Relative: `position: relative;`
- Absolute: `position: absolute;`
- Fixed: `position: fixed;`

## Result

You can download the resulting code of this lecture with [this .zip file](https://drive.google.com/open?id=0Bx1h0_Ovh8h2X1AyRlVBX1Q2X0k).