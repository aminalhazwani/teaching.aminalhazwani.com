---
layout: post
title:  "CSS Typography - Part 2"
day:    "Tue, April 19"
time:   "10 AM - 12 PM"
meta:   "Once the typography is set in our designs how can we translate it in code? There are some helpful properties that allow us to define the text in webpages"
visible: true
---

In todays lecture we continue with some handful CSS properties and nice hacks that help us set beautiful typography on our website. We try to emulate the styles and the layout from an article published on [theatlatic.com](http://www.theatlantic.com/magazine/archive/2015/03/what-isis-really-wants/384980/).

You can [download the starting point (ZIP)](http://turbo.aminalhazwani.com.s3.amazonaws.com/uploads/teaching/unibz/web-design/css-typography-part-two-starting-point.zip) which is just the markup. If you are looking for the styled result scroll down at the end of this page.

## Dropcaps

Lets see for example how we can set a beautiful dropcap with CSS. The pseudo-class `::first-letter` allows us to select only the first character of a body text. By doing so we can style that specific letter. 

```css
.class::first-letter {
  float: left;
  font-size: 4.5rem;
  color: red;
}
```

## Aside

If we would like to add elements in our page that will tend to stay on the side, like a sidebar or a related post section we can use the semantic tag `aside`.

```html
<aside>
  <h4>Related Story</h4>
  <img src="path/toimage.jpg" alt="">
  <a href="#">Link content</a>
</aside>
```

## Font weight

We review how to use the `font-weight` property and what it means to set it to 300, 500, or 900. 

```css
h1 {
  font-weight: 300 // Equals to Light
}
```

For further specification I would suggest you to check the property on [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight).

## Font color

We also review the `color` property. We check which are the values that can be used like `rgb`, `rgba`, `hex`, or even HTML colors like in the example below. 

```css
a {
  color: cornflowerblue;
}
```

For a full list of all the HTML color check them on [w3schoools.com](http://www.w3schools.com/colors/colors_names.asp).

## Center things

We learn that HTML elements are displayed in a cascade-manner. So one after the other. But how can we for example place elements above other, or even more specifically how can we vertically and horizontally align a children element in a parent elements.

First we create the two containers, the parent element and the children element.

```html
<header class="header">
  <div class="header_content">
    <h1>Title</h1>
    <h2>Subtitle</h2>
  </div>
</header>
```

Secondly we set the position of the parent to `relative` and for the purpose of this exercise we make the `.header` fill the whole available viewport with the `vh` unit (which stands for viewport height). There are also other vieport units such as `vw`, `vmin`, and `vmax`. If you use this approach remember to check [browser support](http://caniuse.com/#search=vh).

```css
.header {
  position: relative;
  width: 100%;
  height: 100vh;
  background-image: url('path/toimage.jpg');
  background-position: center;
  background-size: cover;
}
```

Finally we set the child element to be absolutely positioned relative to the parent. We want to have it perfectly in the center and since we don't know its size we can use the `transform: translate();` property to move it. Remember that position of an element always starts from the top-left corner, that's why we have to move back and up by 50% our child element. Otherwise we would have the top-left corner at the center of our parent element. 

```css
.header_content {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

## BEM Methodology

We also talk about CSS naming methodologies. We introduce BEM which stands for Block Element Modifier. The convention follow this pattern:

```css
.block {}
.block__element {}
.block--modifier {}
```

With the words of [Harry Roberts](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/) we can explain it like this:

- `.block` represents the higher level of an abstraction or component.
- `.block__element` represents a descendent of `.block` that helps form `.block` as a whole.
- `.block--modifier` represents a different state or version of .block.

The reason for double rather than single hyphens and underscores is so that your block itself can be hyphen delimited, for example:

```css
.site-search {}         /* Block */
.site-search__field {}  /* Element */
.site-search--full {}   /* Modifier */
```

### Real world example

Imagine you have a header with a series of call to actions and you want to have all them look the same except the one for the log in that you want to set in green.

```css
.header {
  background-color: white;
}

.header__button {
  padding: 4px;
  border-radius: 2px;
  background-color: gray;
}

.header__button--theme {
  color: white;
  background-color: green;
}
```

[Download the ZIP](http://turbo.aminalhazwani.com.s3.amazonaws.com/uploads/teaching/unibz/web-design/css-typography-part-two-ending-point.zip) of the resulting code of this lecture.
