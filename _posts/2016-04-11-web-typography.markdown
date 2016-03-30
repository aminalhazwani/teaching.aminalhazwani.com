---
layout: post
title:  "Web Typography"
day:    "Tue, April 12"
time:   "10 AM - 12 PM"
meta:   "Websites are 90% typography and 90% white space. We see how to set the typography for our product in order to get the best reading experience possible"
---

(https://twitter.com/zeldman/status/679727437198929921)

Just the right typefaces that support the art direction
(https://24ways.org/2009/type-inspired-interfaces)

We must prioritise the text over the font, or semantics over style

Something peculiar happened when typography became entwined with the web though, since there was now a colossal number of systems that could render that text. Unfortunately however these systems couldn’t agree with one another about anything, especially when it came to typography.
(https://www.robinrendle.com/essays/new-web-typography/)

As it happens, most fonts are not supported consistently.
(http://fontfamily.io/)

Easy fix is font stack, fallback declaration.

```css
p {
  font-family: "Tiempos Text", Georgia, serif;
}
```

It’s tough for a typographer like me to admit it, but on the web we have to prioritise the text, and the font, independently.
(http://kennethormandy.com/journal/efficient-web-type-circa-1556)

"centered on the principle of progressive enhancement—that a text itself is fundamentally more important than our suggestions about how it should be typeset."
(http://nicewebtype.com/)

The term readability doesn't ask simply “Can you read it?” or “How fast can you read it?” 

It also asks “Do you want to read it?"
(https://twitter.com/typographica/status/268091875746009088)

### Display faces vs. Text faces

Typefaces have inherit roles. On the wen we are talking about basically to kind of typefaces: 

- Display faces: which are typefaces meant to be used large sizes. A lot more contrast. A little more decorative.
- Text faces: supposed to be used in running text. They generally have a higher x-height and a lower contrast. The focus is on legibility.
(https://vimeo.com/34178417)

Typography in practice is not choosing fonts or making fonts, it’s about shaping text for optimal user experience.
(https://ia.net/know-how/the-web-is-all-about-typography-period)

### Contrast

Text exists to be read. Make sure your type has enough contrast with the background. You can easily test if your text has enough contrast by simply taking a screenshot of your website and than transform it in grayscale your prefered image editor. Or even better, you can test if the contrast ratio is accessible for clor blind people with tools like [Contrast Ratio](http://leaverou.github.io/contrast-ratio/) by Lea Vereou. 

### Size

### Hierarchy

### Space

- http://tbrown.org/
- http://nicewebtype.com/
- http://ilovetypography.com/2008/02/28/a-guide-to-web-typography/
- http://kennethormandy.com/journal/efficient-web-type-circa-1556
- http://ilovetypography.com/2008/02/28/a-guide-to-web-typography/
- https://www.smashingmagazine.com/2015/11/using-system-ui-fonts-practical-guide/
- https://www.smashingmagazine.com/2012/07/one-more-time-typography-is-the-foundation-of-web-design/
- http://betterwebtype.com/
- http://zellwk.com/blog/why-vertical-rhythms/
- http://www.studiothick.com/essays/web-typography-is-broken/
- http://www.imaginarycloud.com/blog/a-typography-workshop/
