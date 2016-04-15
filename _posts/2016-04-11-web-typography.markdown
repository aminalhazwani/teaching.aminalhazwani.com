---
layout: post
title:  "Web Typography"
day:    "Tue, April 12"
time:   "10 AM - 12 PM"
meta:   "Websites are 90% typography and 90% white space. We see how to set the typography for our product in order to get the best reading experience possible"
current: true
visible: true
---

Before getting into the world of web typography I would like to show you how are eyes move across websites and we try to understand how we read webpages and we can optimize our content and text to pleased our visitors eyes.

## How we read

Back in 2006 the Nielsen Norman group did a research and analyzed how people read. At the end of their analysis they released images of heat maps from eye-tracking studies. The areas where people looked the most while reading are red, fewer views yellow and least viewed areas are blue.[^1]

![Eye-tracking device](../uploads/2016/04/eye-tracking-device.jpg)

As you can see below we can identify a F-shaped pattern. Thanks to this research the study was able to define three different ways on how people read. Laura Franz on [Smashing Magazine](https://www.smashingmagazine.com/2014/09/balancing-line-length-font-size-responsive-web-design/) described them like this:

### Casually

People read casually, skimming over text, reading words and sentences here and there to get a sense of the content.

![Heat maps from eye-tracking studies of casual reading](../uploads/2016/04/casual-reading-preview.jpg)

### Scan with purpose

People also scan with purpose, jumping from section to section, looking for a particular piece of information.

![Heat maps from eye-tracking studies of scan with purpose reading](../uploads/2016/04/scanning-with-purpose.jpg)

### Engaged manner

Finally, people read in an engaged manner. When they find an article or blog post they are interested in, they will slow down and read the whole text, perhaps even going into a trance-like state.

![Heat maps from eye-tracking studies of engaged manner reading](../uploads/2016/04/reading-preview.jpg)

But how the F-shaped patterns are formed? As Laura states we know that people don't read each individual word instead they they use their central vision to focus on a word while using their peripheral vision to find the next spot on which to focus.

![Peripheral vision example](../uploads/2016/04/peripheral-vision.jpg)

We also know that readers anticipate the next line while moving their eyes horizontally along the line; so, their eyes are drawn down the left edge of the text.

## Size and alignment

In the book "On Web Typography" Jason Santa Maria writes that in 1928, Jan Tschicold dismissed centered text and advocated for left-aligned text. Tschicold argued that this would assist readers by providing a consistent left (vertical) edge for the eye to return to after finishing each (horizontal) line.

### Line Length (Measure)

Having the right amount of characters on each line is key to the readability of your text. It shouldn't merely be your design that dictates the width of your text, it should also be a matter of legibility. The optimal line length for your body text is considered to be 50-60 characters per line, including spaces ("Typographie", E. Ruder).[^2] On the web I say that up to 75 characters is acceptable.

### Leading

A simple rule is that your leading should be wider than your word spacing. This is because when the balance is correct, your eye will move along the line instead of down the lines. If your measure is wider than the guidelines for optimum legibility then increase the leading. Your leading should increase proportionally to your Measure. **Small Measure, less leading. Wide Measure, more leading.**[^3]

A good starting point with `line-height` is between 120% and 150% of the `font-size` that can be translated into 1.2–1.5.

### Font Size

Jason Santa Maria says that the best way to approach sizing is to consider the reader and the reading distance. Most people sit about 45–60 centimeters (18–24 inches) away from their screens when it comes to a desktop; for mobile devices, it's a bit less. Considering the typical distance and common text sizes in printed matter–about 10 points or roughly 13 pixels–I tend to make my base type size 16 or 18 pixels, or 1–1.2 ems.

In general, he says that he would rather err on the side of making something too large than risk it being too small. From my experience it often happens to notice a person use the zoom-in function of their browser than seeing them using the zoom-out. 

## Contrast

The _contrast_ of a typeface refers to the differences in the thick and thin strokes of its characters. A monoline typeface has the absolute least amount of contrast. For instance, Helvetica features consistent stroke widths. Compare that to a high-contrast typeface like Bodoni, whose strokes vary form beefy to delicate, all in one letter.[^4]

![Bodoni vs Helvetica](../uploads/2016/04/type-contrast.jpg)

Higher contrast typefaces tend to be useful in small bursts of headlines, because the extreme variation in stroke width in burdensome in long text. 

![Headline with high contrast typeface](../uploads/2016/04/high-contrast-typeface-1.jpg)

Our eyes are attracted to the exceptions—the stuff that looks different form everything else.

![Headline with high contrast typeface exceptions](../uploads/2016/04/high-contrast-typeface-2.jpg)

You're more likely to stop or slow down and notice the letters, rather than read, when in my eye encounters that kind of modulation. 

![Headline with high contrast letters](../uploads/2016/04/high-contrast-typeface-3.jpg)

A typeface with less contrast can create a smooth, welcoming rhythm for reading. Most typefaces intended for long-form text have medium to low contrast, which creates less interplay between the individual letters and words.

![Screenshot from kindle ebook read with the typography set in Bookerly](../uploads/2016/04/bookerly.jpg)

This gives text a steadier visual rhythm as your eyes move across a line, which in turn aids readability. When we aren't distracted by the exceptions, we can focus on the act of reading itself.

### Display faces vs. Text faces

Typefaces have inherit roles. And we are talking about basically to kind of typefaces: 

- Display faces: which are typefaces meant to be used large sizes. They have a lot more contrast and are a little more decorative.
- Text faces: are supposed to be used in running text, they generally have a higher x-height and a lower contrast. The focus is on legibility.[^5]

![Screenshot that shows the difference between a display typeface and a text typeface](../uploads/2016/04/display-vs-text.jpg)

### Color contrast

Text exists to be read. Make sure your type has enough contrast with the background. You can easily test if your text has enough contrast by simply taking a screenshot of your website and than transform it in grayscale your preferred image editor. Or even better, you can test if the contrast ratio is accessible for color blind people with tools like [Contrast Ratio](http://leaverou.github.io/contrast-ratio/) by Lea Vereou. 

## Hierarchy

Always form the book of Santa Maria we understand that _hierarcy_ helps us prioritize content based on individual elements and relationships between them. It helps our readers easily scan chunks of information and understand what they're looking at. When done right, a typographic system feels intuitive, like an unspoken set of instructions. Without any internal logic in place, our content may look like a monolithic block.

![New York Times website](../uploads/2016/04/nyt.jpg) 

In order to achieve that we can take advantage of some basic but powerful tools like: size, space, color and proximity.

Hierarchy applies a systematic approach to grouping similar items and distinguishing dissimilar ones. We express hierarchy both semantically (in the underlying HTML markup) and visually (in our design).

## Space and composition

### Baseline grids

A _baseline grid_ is a series of rows spunt out of the spacing between baselines in text, or the invisible line that letters sit on. In practice, we often visualize the baseline in print design by overlaying our page with a baseline grid as shown below:

![Baseline in print design](../uploads/2016/04/baseline-print.jpg)

Unlike the physical page, the web is a fluid medium and baseline grids on the web are slightly different because of the way the line-height property works. We often see a baseline grid that looks like this instead:

![Baseline in web design](../uploads/2016/04/baseline-web.jpg)

But don't worry. We can easily work and create good vertival rhythm also with such a baseline.

### Vertical Rhythm

In design, vertical rhythm is the structure that guides a reader’s eye through the content. Good vertical rhythm makes a layout more balanced and beautiful and its content more readable.[^6] The goal is to try to keep vertical spaces between elements on a page consistent with each other.[^7] Implementing vertical rhythm is quite simple:

1. Set the vertical white space between elements to a multiple of your line-height
2. Set the line-height of all text elements to a multiple of your base line-height

```css
h1 {
  line-height: 48px;
  margin: 32px 0; 
}

p {
  line-height: 24px;
  margin: 24px 0;
}
```

From the blog of Zell Liew we learn that one important principle of vertical rhythm is repetition. **Repetition breeds familiarity**. It has the ability to make things feel as if they belong together. It gives the feeling that someone has thought it all out, like it's part of the plan.

### Whitespace

Back to the book of Santa Maria we read that whitespace frames the content and provides structure to the page. And when it comes to articles, whitespace is an indispensable factor not only in giving the eye room to read, but also creating a welcoming environment.

![Smart use of white space on a working library website](../uploads/2016/04/white-space.jpg)

If your pages are too cluttered, you're inviting the reader to head elsewhere.

## Methods for choosing a typeface

The last pill from the bible "On Web Typography" is a method that can help you choose the best typeface for your porject. First: be ready to abandon your favorite typeface. It doesn't matter if it's the loveliest hairline or the most elegant serif. If it doesn't serve your design, it doesn't serve the reader.

### Word association

Ask yourself: what do I want my design to convey? Think of words that describe a website for a social cooperative. You may think of descriptive words like accessible, open, welcoming, and more. 

![List of words associations from early plans for the Mighty website design from Jason Santa Maria](../uploads/2016/04/word-associations.jpg)

Scribble down any words that come to mind. You're brainstorming, so there are no wrong answers. The important thing is to write as many ideas as you can. After you've done that, start sorting similar words together into groups.

![Shortlist of typefaces fro the Mighty website design from Jason Santa Maria](../uploads/2016/04/comparison-real-text.jpg)

### Comparison of real text

The most useful thing you can do when deciding wheter to use a typeface is to try it out in a situation as close to the real thing as possible. 

> Typefaces are the clothes that words wear<br>–Tobias Frere-Jones

You can do this so quickly that you have no reason not to. Simply drop blocks of the same text into a HTML document, se each paragraph to a different typeface, and open in a browser.

If you're being lazy designer Richard Rutter made a template system for this express purpose called [Body Text Tester](http://blog.fontdeck.com/post/23601339698/body-text-tester). Or you can also try the web service [Typecast](https://typecast.com/).

## From discussion in class

- [Google Fonts](https://www.google.com/fonts)
- [Typekit](https://typekit.com/fonts)
- [Webtype](http://www.webtype.com/)
- [FontFont](https://www.fontfont.com/)
- [MyFonts](http://www.myfonts.com/)
- [Grilli Type](https://www.grillitype.com/)
- [Klim Type Foundry](https://klim.co.nz/)
- [Village](http://vllg.com/fonts/name)
- [Bold Monday](https://www.boldmonday.com/)
- [Commercial Type](https://commercialtype.com/)
- [Colophon Foundry](http://www.colophon-foundry.org/)
- [Commercial Type](https://commercialtype.com/)
- [Production Type](https://www.productiontype.com/)
- [Open Foundry](http://open-foundry.com/hot30)

[^1]: [Balancing Line Length and Font-size in Responsive Web Design](https://www.smashingmagazine.com/2014/09/balancing-line-length-font-size-responsive-web-design/)
[^2]: [Line Lenght and Readability](http://baymard.com/blog/line-length-readability)
[^3]: [Five Simple Steps to Better Typography](http://www.markboulton.co.uk/journal/five-simple-steps-to-better-typography)
[^4]: [On Web Typography](https://abookapart.com/products/on-web-typography)
[^5]: [Jason Santa Maria speaking at Build Conference](https://vimeo.com/34178417)
[^6]: [4 Simple Steps to Vertical Rhythm](http://typecast.com/blog/4-simple-steps-to-vertical-rhythm)
[^7]: [Why is Vertical Rhythm an Important Typography Practice?](http://zellwk.com/blog/why-vertical-rhythms/)