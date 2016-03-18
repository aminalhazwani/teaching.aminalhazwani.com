---
layout:  post
title:   "Web Design 101 - Part 1"
day:     "Tue, March 8"
time:    "2 PM - 4 PM"
meta:    "Let's dive in the magical world of web design. We set the initial basis for the course with an introduction on the subject followed by policies and information"
visible: true
---

## What it means to design for the web today?

In order to understand how to design for the web we could look at how everything started back in the day. In 1989, Sir. [Tim Berners-Lee](https://www.w3.org/People/Berners-Lee/) proposed to create a global hypertext project, which later became known as the World Wide Web.[^1]
The web is an open source information space where documents and other web resources are identified by URLs, interlinked by hypertext links, and can be accessed via the [Internet](https://en.wikipedia.org/wiki/Internet).

At the beginning the web was composed by _text-only pages_ that could be viewed using a simple line-mode browser. As designers I think it's crucial to focus on the idea of text-only pages; to the browser every website is a unique file of text. 

This is how the very first website looked:

![The look of the very first website](../uploads/2016/03/first-website.jpg)

And this is how it looks today (yes, it's still on-line and yes, it's almost mobile ready!)

![The look of the first website today](../uploads/2016/03/first-website-today.jpg)

So, the web is pretty young. It's still a fairly new medium, that has emerged from the medium of printing, whose skills, design language and conventions strongly influence it. But in the words of John Allsopp we need to understand which of these lessons are appropriate for the web, and which mere rituals.

> We are not designing pages but systems of components

This is often seen as a limitation. It is the nature of the web to be _flexible_, and it should be our role as designers and developers to embrace this flexibility, and produce pages which, by being flexible, are _accessible_ to all.[^2]

So how can we be flexible? Well, first of all we must forget about pixel-perfection. 

![An undecided designer moving up and down by 1px his or her design](../uploads/2016/03/pixel-perfect.gif)

Designers usually want to control everything but we need to rethink this role, to abandon control, and seek a new relationship with the page.

> Make pages which are _accessible_, regardless of the browser, platform or screen that your _reader_ chooses or must use to access your pages.

How can we be accessible? By embracing flexibility: the web wasn't design to be constrained by a single context.

So, using some explanatory images from [Brad Frost](http://bradfrost.com/blog/web/for-a-future-friendly-web/) we could say that this is how the old contexts looked:

![Old context and usage of the web representation](../uploads/2016/03/old-context.jpg)

And this is how the new(actual) context looks:

![New context and usage of the web representation](../uploads/2016/03/new-context.jpg)

It can look scary but actually the power of the web is its _ubiquity_. But how can we respond and design to such different scenarios?

## Responsive Web Design

One of the best practices to overcome all these different contexts is responsive web design. This methodology was first defined by Ethan Marcotte with an article on [A List Apart](http://alistapart.com/article/responsive-web-design). The approach is describe by these three rules:

- _Fluid grids_ that ebb and flow with a devices’ screen size
- _Flexible images_ and media that keep content intact on any resolution
- Media queries allowing designs to _adapt_ by establishing dimension breakpoints

### Fluid grids

Fluids grids are a grid system that change and morph across different screen size. For example if a grid system is composed by 8 columns on a large screen will collapse to a 4 columns system on a smaller display.

### Flexible images

Flexible images and media are assets that adapt to the resolution of the device delivering the optimal source for every situation. For example when you access the contents from a smaller device the images are not cut out.

### Media queries

A media query is an expression that limits the scope of your styles sheets. Breakpoints help you define where a media query starts and where it ends. For example you could say how big an image can be above or below a certain breakpoint scoping its size within certain resolutions. 

> Responsive web design is the approach that suggests that design and development should respond to the user's behavior and environment based on the screen size, platform and orientation.

Summarizing, this is how the web looked: 

![Image that shows an old PC](../uploads/2016/03/this-is-not-the-web.jpg)

This is how it looks:

![Image that shows multiple device like smartphones, tablets and laptops](../uploads/2016/03/this-is-the-web.jpg)

And this how it will look:

![Image that shows multiple device like smartphones, tablets, laptops, smartwatch, cars, fridges, and many more](../uploads/2016/03/this-will-be-the-web.jpg)

As designers we must acknowledge and embrace _unpredictability_ because nobody knows where the device landscape is going to be. By being _responsive_ we not only serve the current range of devices but we work for also the unforeseen contexts. 

![Sergey Brin wearing a pair of google glasses](../uploads/2016/03/google-glasses.jpg)

## Workshop #1 

Let's try to identify the three criteria that define a responsive project. Choose a website of your preference. Look at it not as a reader but as a designer. Identify breakpoints, media queries and fluid grids. Make a screenshot of each media query and make the grid structure visible.

![A gif that shows breakpoints and media queries of bostonglobe.com](../uploads/2016/03/boston-globe-responsive.gif)

## From discussion in class

- [Spiegel.de](http://www.spiegel.de/)
- [Apple.com](http://www.apple.com/)
- [WTF Mobile Web](http://wtfmobileweb.com/)
- [Why Japanese Web Design Is So… Different](http://randomwire.com/why-japanese-web-design-is-so-different/)
- [Way Back Machine](http://archive.org/web/)
- [Awesome Screenshot Chrome Extension](https://www.awesomescreenshot.com/)
- [Flashes - Il Post](http://flashes.ilpost.it/)
- [Fatherly.com](http://wordisborn.fatherly.com/)
- [Bostonglobe.com](http://www.bostonglobe.com/)
- [Sublime Text 3](https://www.sublimetext.com/3)

[^1]: [https://en.wikipedia.org/wiki/World_Wide_Web](https://en.wikipedia.org/wiki/World_Wide_Web)
[^2]: [http://alistapart.com/article/dao](http://alistapart.com/article/dao)
