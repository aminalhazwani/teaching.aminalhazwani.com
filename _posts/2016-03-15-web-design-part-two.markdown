---
layout: post
title:  "Web Design 101 - Part 2"
day:    "Tue, March 16"
time:   "2 PM - 4 PM"
meta:   "In this lecture we consolidate our web design basis while talking about common practises such as progressive enhancement, mobile first and content first"
current: true
---

In the [previous lecture](http://teaching.aminalhazwani.com/web-design-part-one/) we learned what it means to design for the web today and how [responsive web design](http://teaching.aminalhazwani.com/web-design-part-one/#responsive-web-design) can help us serve the current web context of numerous devices and scenarios. And how by being responsive we can embrace unpredictability.

In this lecture we are going to see other approaches that help up design and develop accessible and future-friendly web experiences.

## Mobile first

Already back in 2009 Luke Wroblewski soon realized that designers should have a new focus. He saw a trend of ever-increasing numbers for mobile web usage. He saw that the omnipresent web was being utilized on much more than just desktops and those larger displays. The numbers for mobile Web usage were growing by leaps and bounds. This was what gave way to the fundamental focus of _Mobile First_.[^1]

Luke’s definition of mobile first consists of three core components:

- The _growth_ of mobile is a huge _opportunity_ to reach more people than ever
- The _constraints_ of the mobile medium force us to _focus_ on what really matters
- The _capabilities_ of mobile create opportunities to _innovate_

In the last years there has been a lot of discussion about the different approaches to deliver mobile web experiences. Responsive web design vs. adaptive design vs. device agnostic design (which is the one you notice when in front of the url you see and `m.` like `m.url.com`). But at the end the user doesn't really care about the design approach you use.

> End-users don’t care about your responsive web or your separate sites, they just want to be able to get stuff done.[^2]

The mobile first design allows us designers to do just that, it allows the end-users to get stuff done, regardless of the generation of their device.

### Graceful degradation (old top-down approach)

![Image that shows practically how graceful degradation works](../uploads/2016/03/graceful-degradation.jpg)

In the mix of this de-evolving process, most of the time, you are overloading the smaller devices with far too information causing the smaller devices to lag at excruciatingly low speeds.

A recent survey of 2300 CIOs in the States showed some dramatics and some valuable statistics[^3]:

- more than 1.2 billion people worldwide use the web via mobile devices
- mobile sales are growing three times faster than overall ecommerce
- mobile users expect pages to load as fast as, if not faster than, pages on desktop computers (40% will abandon a page that takes longer than 3 seconds to load)
- up to 97% of mobile shopping carts are abandoned
- when pages are slow, user frustation increases and engagment decreases

One of the most embraced method in order to address these problems is progressive enhancement. 

### Progressive enhancement (new bottom-up approach)

![Image that shows the benefits of progressive enhanceme
nt](../uploads/2016/03/progressive-enhancement.jpg)

This progressive enhancement helps in keeping the content and media featured on a site from being far too heavy for the lowest-tech phones to handle.

Progressive enhancement uses web technologies in a layered fashion that allows everyone to access the basic content and functionality of a web page, using any browser or Internet connection, while also providing an enhanced version of the page to those with more advanced browser software or greater bandwidth.[^4]

By first creating an experience that prioritizes a worst-case mobile scenario, you ensure that your users will be able to accomplish their goals despite a lot of factors working against them.

### Force designers to focus on core content and functionality

With, roughly, 80% of the screen size taken away when you start with mobile first design, you have to think about how to utilize your space in a much more conservative manner.

Mobile forces you to focus on only the most important data and actions in an application or website. You have to prioritize.[^5]

> Mobile users will do anything and everything desktop users will do, provided it's presented in a usable way.

All this approaches lead to just one conclusion: devices will come and go and technological trends will wax and wane, but content, business goals and user goals remain. [^6]

If you take the time to figure out the right way to get your content out there, you’ll have the freedom (and the flexibility) to get it everywhere. You can go back to thinking about the right design and development approaches for each platform, because you’ll already have a reusable base of content to work from.[^7]

## Content first

The device landscape is constanslty changing. Capabilities are constantly changing. _Properly structured content_ is portable to future platforms.[^8] 

As it happens with the mobile first methodology structuring content first creates content focus and hierarchy. We should not assume that users want different content simply because of the platform they're using. And this approach helps us do just that: same content is delivered to all users no matter the device they are using to access it. 

> Knowing the type of device the user is holding doesn't tell you anything about the user's intent. 

### Linear content

The great thing about this approach is it forces you into a content hierarchy. The most important piece of content is on top, followed by the next, followed by the next. Unlike a desktop approach where you can put two pieces of content side by side for equal footing, a mobile approach means one is above the other.[^9]

We have gone through many different useful practices that help use craft a flexible and accessible web. And as we saw previously by being able to design fluid products we embrace and acknowledge the _unpredictability_ of the web. All these approaches can summarized with the [future-friendly web manifesto](#) signed by many important web figures such as [Brad Frost](#), [Jonathan Stark](#), and many [more](#)

- The web is not one-dimensional
- The power of the web is its ubiquitousness
- We need to reconsider the content we create and the context in which people interact with our content
- We need to respect people's time and give them relevant, purposeful content without the extra cruft
- Content like water. Think of your core content as a fluid thing that gets poured into a huge number of containers 
- Mobile is more than just a smaller screen
- The combination of mobile-first and responsive web design is a good idea
- Progressive enhancement plays an essential role in future-friendly design
- Design for touch (http://bradfrost.com/blog/web/for-a-future-friendly-web/)

## Workshop #2

...

## From discussion in class

...

[^1]: http://zurb.com/word/mobile-first
[^2]: https://www.youtube.com/watch?feature=player_embedded&v=SVPJcw5-WNc
[^3]: https://blog.radware.com/applicationdelivery/applicationaccelerationoptimization/2015/02/why-you-should-care-about-mobile-web-performance/
[^4]: https://en.wikipedia.org/wiki/Progressive_enhancement
[^5]: http://www.lukew.com/ff/entry.asp?933
[^6]: http://bradfrost.com/blog/web/mobile-first-responsive-web-design/
[^7]: http://alistapart.com/article/your-content-now-mobile
[^8]: http://www.slideshare.net/stephenhay/structured-content-first/28-THANK_YOUtwittercomstephenhayslidesharenetstephenhaystructuredcontentrst
[^9]: https://responsivedesign.is/strategy/page-layout/mobile-first

- https://twitter.com/wilto/status/63284673723375616
- http://www.slideshare.net/stephenhay/structured-content-first/23-Thinking_about_creating_anddesigning_structured
- http://info.cern.ch/hypertext/WWW/TheProject.html and http://line-mode.cern.ch/www/hypertext/WWW/TheProject.html
- http://bradfrost.com/wp-content/uploads/2011/06/progressive_enhancement.jpg


