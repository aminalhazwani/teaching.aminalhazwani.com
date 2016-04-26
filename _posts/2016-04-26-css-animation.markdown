---
layout: post
title:  "CSS animantion and transition"
day:    "Tue, April 26"
time:   "10 AM - 12 PM"
meta:   "The Level 3 CSS specifications give us some dope super powers. Now we can smoothly animate and transition elements in our page delivering a better experience"
current: true
visible: true
---

The first CSS property that allows us to add effects to the change of state of an element is `transition`.

## Transition

In order to add a transition to your element you have first to specify which are the properties that are addressed by the transition and how low the transition is going to last. Secondly you specify how these properties are going to change:

```css
.box {
  width: 100px;
  height: 100px;
  background-color: blue;
  transition: width 2s, height 2s, background-color 2s, transform 2s;
}

.box:hover {
  background-color: red;
  width: 200px;
  height: 200px;
  transform: rotate(180deg);
}
```

Remember to always check the browser support of your CSS properties. You may need some prefixes here and there to make transition work in older browsers.

### Transition timing function

You can also specify the transition timing function. The timing function is basically sets the intermediate values of the CSS property. It address the acceleration curve which translates into different speed over the transition duration;

```css
.box {
  transition-timing-function: ease;
}
```

I would suggest you to check [easigns.net](http://easings.net/) to see a brief catalogue of timing function. Moreover most of the browsers now let you play with this function. For example in Google Chrome it looks like this:

![Google Chrome Dev tools Cubic bezier Editor](../uploads/2016/04/devtools-cubicbezier-editor.jpg)

### Transition delay

You can also set a delay to your transition:

```css
.box {
  transition-delay: 2s;
}
```

Again, remember to always check the browser support of your CSS transition properties. 

## Animation

Another way to change the state of things in CSS are animation. You may ask what's the difference between a transition and an animation? Transition require a trigger to run like a mouse over while animation don't need a trigger (they can be trigger) but by default they run automatically on page load. Transitions can't change CSS properties and you cannot specify the start and end value while animations can do both. Finally transitions can't loop.

In order to apply an animation to your element you have to specify the duration and the name. Right after you define the `@keyframe` for such animation. You can set two keyframe with the `from`-`to` property or use percentage values that identify the progress of the animation from 0 to 100%.

```css
p {
  animation-duration: 3s;
  animation-name: slidein;
}

@keyframes slidein {
  from {
    margin-left: 100%;
    width: 300%;
  }

  to {
    margin-left: 0%;
    width: 100%;
  }
}
```

### Animation iteration count

Another animation property can set the number of times that the animation plays:

```css
p {
  animation-iteration-count: infinite;
}
```

### Animation direction

Or you can even set the animation duration: 

```css
p {
  animation-direction: alternate;
}
```

For more animation and ready-made examples I would suggest you to look into the amazing [animate.css](https://daneden.github.io/animate.css/) by Daniel Eden, designer at Dropbox. Remember to [check the code on GitHub](https://github.com/daneden/animate.css/tree/master/source) in order to understand how the library is built.

## More HTML and CSS

During this lecture we also continue our work on the Atlantic article.

### Blockquotes

We introduce the `blockquote` tag and we do some basic styles to make them more visible and well identifiable.

```css
blockquote {
  position: relative;
  margin-left: calc(1.625rem * 2);
}

blockquote::before {
  content: "\201C";
  display: block;
  float: left;
  font-size: 4.5rem;
  line-height: .8;
  color: red;
}
```

### Figure and figcaption

We also introduce tags such as `figure` and `figcaption`:

```html
<figure>
  <img src="http://url.com" alt="...">
  <figcaption>Caption of the image</figcaption>
</figure>
```

### Video

We also learn how we can add videos to our website. It's very similar to the `img` tag but we have some more convenient attributes like the poster image, controls and autoplay.

```html
<video src="vid/interview.mp4" controls autoplay poster="img/interview-poster.jpg"></video>
```

### Responsive iframe

Another way to add videos to our website is via the `iframe` tag. While this tag makes it easy to embed videos from different sources like YouTube or Vimeo it doesn't keep the ratio on resize because the `width` and the `height` are fixed and come directly from the provider servers.

Luckily we can hack this behavior via HTML and CSS. First we wrap the `iframe` in a container:

```html
<div class="embed">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/5x3vuslV2ZU" frameborder="0" allowfullscreen></iframe>
</div>
```

and we apply this CSS to `.embed`:

```css
.embed {
  display: block;
  position: relative;
  overflow: hidden;
  height: 0;
}
```

then the hack comes! We create a new class which sets the `padding-bottom` of the container based on the ratio of our video (in this case 16 to 9):

```css
.embed-16-9 {
  padding-bottom: calc((9 / 16) * 100%);
}
```

we add the class `.embed-16-9` to the parent container `.embed` and finally we position the `iframe` in the parent container and make it fill the whole space:

```css
.embed > iframe {
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
```

Pretty cool, huh? 

### Utility CSS

We also introduce the concept of utility classes. An utility class applies a single rule to an element. They're often called "helpers" and they are simple, componsable, and most importantly reusable. During the lecture we create an utility class for the `margin-bottom` in order to easily create vertical rhythm or reset the margin of certain elements:

```css
.mb0 {
  margin-bottom: 0;
}

.mb-xs {
  margin-bottom: 8px;
}

.mb-s {
  margin-bottom: 16px;
}

.mb {
  margin-bottom: 24px;
}

.mb-m {
  margin-bottom: 32px;
}

.mb-l {
  margin-bottom: 48px;
}

.mb-xl {
  margin-bottom: 96px;
}
```


