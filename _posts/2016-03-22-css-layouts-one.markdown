---
layout: post
title:  "CSS Layouts - Part 1"
day:    "Tue, March 22"
time:   "2 PM - 4 PM"
meta:   "We continue to learn how CSS can help us style our project but we also introduce how to layout things in our canvas with the help of some handy CSS properties like flexbox"
---

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

## CSS Layouts

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