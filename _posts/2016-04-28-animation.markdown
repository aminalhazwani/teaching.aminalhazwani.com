---
layout: post
title:  "Motion with Meaning: Semantic Animation in Interface Design"
day:    "Thu, April 28"
time:   "11 AM - 1 PM"
meta:   "Animation is fast becoming an essential part of interface design, and it’s easy to see why. It gives us a whole new dimension to play with—time. This creates opportunities to make our interfaces better at every level: it can make them easier to understand, more pleasant to use, and nicer to look at."
visible: true
---

_**DISCLAIMER** This article was originally published on A List Apart. Feel free to read it here or [there](http://alistapart.com/article/motion-with-meaning-semantic-animation-in-interface-design). If you are interested in the discussion [read the comments](http://alistapart.com/article/motion-with-meaning-semantic-animation-in-interface-design#comments) on their website._

For example, animation can help [offload some of the work (PDF)](https://www.cs.umd.edu/hcil/jazz/learn/papers/CS-TR-3964.pdf) of processing interface changes from our brains to the screen. It can also be used to explain the meaning and relationships of interface elements, and even teach users how to do things—all without making an interface more complex.

Sometimes all of these factors converge: when you minimize a window, would you be able to tell where it goes without the animation? How much longer would it take you to find the minimized window in the dock?

<figure>
<video width="" height="" controls="" poster="http://alistapart.com/d/440/fig-01-osx-minimize-696px.jpg">
<source src="http://alistapart.com/d/440/fig-01-osx-minimize-696px.mp4" type="video/mp4">
<source src="http://alistapart.com/d/440/fig-01-osx-minimize-696px.webm" type="video/webm">
</video>
<figcaption>Hard cuts make it difficult to understand state changes, because changing the entire page means you have to <a href="http://paulstamatiou.com/design-provide-meaning-with-motion/">rescan the entire thing to see what changed</a>.</figcaption>
</figure>

So far, so uncontroversial, right? Animation is _a good thing_—[when done well, at least](http://alistapart.com/article/designing-safer-web-animation-for-motion-sensitivity). But there's one aspect of animation that nobody ever seems to talk about. Some animation, while technically well executed, makes interfaces more confusing instead of less.

Consider the following process:

<figure>
<video width="240" height="" controls="" poster="http://alistapart.com/d/440/fig-02-ios-multitasking-first-part-696px.jpg">
<source src="http://alistapart.com/d/440/fig-02-ios-multitasking-first-part-696px.mp4" type="video/mp4">
<source src="http://alistapart.com/d/440/fig-02-ios-multitasking-first-part.webm" type="video/webm">
</video>
</figure>

When we tap the Overcast app icon on the homescreen, the icon zooms and morphs into the app. The other icons stay in place. They're still in their initial positions, laid out in a grid around the open app.

<figure>
<video width="240" height="" controls="" poster="http://alistapart.com/d/440/fig-03-ios-multitasking-second-part-696px.jpg">
<source src="http://alistapart.com/d/440/fig-03-ios-multitasking-second-part-696px.mp4" type="video/mp4">
<source src="http://alistapart.com/d/440/fig-03-ios-multitasking-second-part.webm" type="video/webm">
</video>
</figure>

We start multitasking. The app zooms out. We _should_ get back to the icons around the app on the homescreen, but instead we see a stack of other apps. Why is the icon above the app now? Where are all the other icons? And why does another homescreen appear next to the apps?

The app is both _inside_ its icon on the homescreen and _next_ to the homescreen. The two animations give us conflicting information about where the homescreen and the apps are located in space.

![Diagram showing the multitasking workflow](http://alistapart.com/d/440/fig-04-multitasking.svg)

These animations _might_ make sense if you designed the individual screens in a vacuum. It's only when they all try to play together as parts of a single experience that things get confusing. The problem isn't with any of the individual transitions, but with the fact that the animations contradict each other.

## History

How did we get here? Let's take a step back and quickly review the history leading up to this point.

Since their inception in the 1970s, graphical user interfaces were basically [a series of static screens (PDF)](https://faculty.washington.edu/aragon/classes/hcde411/w13/readings/Chang_AnimationInUI_UIST93.pdf) linked together without any transitions. Every state change was a hard cut.

Although there are some notable early examples of good interface animation that date [all the way back to the original Macintosh (PDF)](https://www.cs.umd.edu/hcil/jazz/learn/papers/CS-TR-3964.pdf), because of the limited graphical capabilities of computers back then, effective animation was the exception rather than the rule.

<figure>
<video width="400" height="" controls="" poster="http://alistapart.com/d/440/fig-05-osx-lisa-696px.jpg">
<source src="http://alistapart.com/d/440/fig-05-osx-lisa-696px.mp4" type="video/mp4">
<source src="http://alistapart.com/d/440/fig-05-osx-lisa-696px.webm" type="video/webm">
</video>
<figcaption>Example of a remarkably fluid animation in an early version of Mac OS.</figcaption>
</figure>

As computers got increasingly powerful, animation started to be used more frequently for things like maximizing windows or opening new tabs. It was still mostly pressed into service for small things, though, and rarely influenced the overall structure of interfaces.

Only now are we starting to get to a point where computing resources aren't holding interfaces back anymore. With [today's devices](http://www.technologytell.com/apple/files/2014/09/A8GPU.png), everything can be animated—and increasingly everything is. The problem is that the design process hasn't caught up to this change in technology. For the most part, interfaces are still conceived as separate, static screens and then [linked together with relatively crude animations](https://youtu.be/Vm1J2wUhNOk?t=3m40s).

This is probably how our multitasking example came to be; different parts of the experience were designed separately and then linked together without considering either the relationships between them or the consequences of arranging them this way. The problem is that if animation (and therefore the spatial structure of an interface) is an afterthought, it's all too easy to create contradictory behaviors.

Now that we've figured out how we got here, let's think about how we can avoid such pitfalls.

## A simple shift

Adding animation to interfaces fundamentally changes them, and necessitates a new way of thinking. We call this new approach _semantic animation_. It all starts with a simple conceptual shift:

> You can't treat individual screens as separate entities if the transitions between them are animated. To the user, the entire experience is one continuous space.

Similarly, two representations of the same element on different screens can't be seen as separate from each other. To the user, there is only one element—it simply changes form.

This means that when you add animations, an interface isn't a series of screens anymore, but a collection of semantic components inside a [single, continuous space](http://scottmccloud.com/4-inventions/canvas/). These self-contained components enclose everything associated with them, like meta information or interactive controls.

<figure>
<video width="400" height="" controls="" poster="http://alistapart.com/d/440/fig-06-dribbble-696px.jpg">
<source src="http://alistapart.com/d/440/fig-06-dribbble-696px.mp4" type="video/mp4">
<source src="http://alistapart.com/d/440/fig-06-dribbble-696px.webm" type="video/webm">
</video>
<figcaption>Example of how a post on <a href="https://dribbble.com">Dribbble</a> could work as a semantic component. The post always remains one cohesive element; it simply changes its representation over time.</figcaption>
</figure>

This may sound complicated, but in practice it's actually quite simple: instead of designing screens and then adding transitions between them, start by designing individual components and thinking about how they change and move in different contexts. With that in place, layout and animations will come together naturally, following the semantic structure of the content.

## Explain relationships between elements

Animations are most useful when they [reflect and reinforce the semantic relationships](http://alistapart.com/article/ui-animation-and-ux-a-not-so-secret-friendship#section4) between elements: for example, "this comment belongs to this article," or "these menu items are part of this menu."

Think of every element of your interface as a single, self-sufficient component with a specific meaning, state, and position in space. Then make sure your animations reflect this. If a popover belongs to a button, it shouldn't just fade in; it should emerge from that button. When opening an email, the full message should not just slide in from the side, but come from within the preview.

You get the idea, right? Once you're used to this way of thinking, it almost becomes second nature.

<figure>
<video width="" height="" controls="" poster="http://alistapart.com/d/440/fig-07-meteor-toys-696px.jpg">
<source src="http://alistapart.com/d/440/fig-07-meteor-toys-696px.mp4" type="video/mp4">
<source src="http://alistapart.com/d/440/fig-07-meteor-toys-696px.webm" type="video/webm">
</video>
<figcaption>The dialogs on <a href="https://meteor.toys">Meteor Toys</a> are a great example of semantic components.</figcaption>
</figure>

The following examples show two completely different approaches to the same problem: one is screen-based; the other takes semantic animation into account. When opening Launchpad on OS X, the app icons just fade in and the background is blurred. This doesn't tell the user anything about where the icons come from and what their relationship is with other parts of the interface.

<figure>
<video width="" height="" controls="" poster="http://alistapart.com/d/440/fig-08-osx-launchpad-696px.jpg">
<source src="http://alistapart.com/d/440/fig-08-osx-launchpad-696px.mp4" type="video/mp4">
<source src="http://alistapart.com/d/440/fig-08-osx-launchpad-696px.webm" type="video/webm">
</video>
<figcaption>OS X Launchpad.</figcaption>
</figure>

The app drawer in [GNOME](https://www.gnome.org/gnome-3) (a desktop environment for GNU/Linux), on the other hand, uses an animation that elegantly explains where the icons come from and where they are when they're not visible.

<figure>
<video width="" height="" controls="" poster="http://alistapart.com/d/440/fig-09-gnome-launchpad-696px.jpg">
<source src="http://alistapart.com/d/440/fig-09-gnome-launchpad-696px.mp4" type="video/mp4">
<source src="http://alistapart.com/d/440/fig-09-gnome-launchpad-696px.webm" type="video/webm">
</video>
<figcaption>GNOME application launcher.</figcaption>
</figure>

### Multiple representations

A common problem to look out for is different representations of a single element that are visible at the same time. This is bad, because it doesn't make sense from the user's point of view to see the same thing in more than one place simultaneously.

In the following example from Google's [Material Design Guidelines](https://www.google.com/design/spec/animation/meaningful-transitions.html), when you tap on an image in a list view, a bigger version of the image is shown. The bigger version slides in from the right on a separate layer. This is a textbook case of multiple representations: there's no connection between the two images.

<figure>
<video width="240" height="" controls="" poster="http://alistapart.com/d/440/fig-10-google-material-old-696px.jpg">
<source src="http://alistapart.com/d/440/fig-10-google-material-old-696px.mp4" type="video/mp4">
<source src="http://alistapart.com/d/440/fig-10-google-material-old-696px.webm" type="video/webm">
</video>
</figure>

Why is the image both in the list view _and_ on that other screen? Are all of the big versions of the images stacked to the right?

Google recently changed this example in their guidelines. Here's the updated version:

<figure>
<video width="240" height="" controls="" poster="http://alistapart.com/d/440/fig-11-google-material-new-696px.jpg">
<source src="http://alistapart.com/d/440/fig-11-google-material-new-696px.mp4" type="video/mp4">
<source src="http://alistapart.com/d/440/fig-11-google-material-new-696px.webm" type="video/webm">
</video>
</figure>

The new example is better because there are no multiple representations, but the animation fails to account for the interface elements on top, which change with no animation at all.

Now, here's an instance of something that checks all the boxes: Facebook Paper's timeline makes the relationship between thumbnail and detail view completely obvious. No multiple representations, no semantic loose ends. The transition is so smooth that you barely notice the state change.

<figure>
<video width="240" height="" controls="" poster="http://alistapart.com/d/440/fig-12-ios-facebook-paper-696px.jpg">
<source src="http://alistapart.com/d/440/fig-12-ios-facebook-paper-696px.mp4" type="video/mp4">
<source src="http://alistapart.com/d/440/fig-12-ios-facebook-paper-696px.webm" type="video/webm">
</video>
</figure>

See how the interface elements on the bottom of the detail view come from within the image? The image is a self-sufficient component, containing all of the information and actions associated with it.

Another example of how to do this well is Apple's Passbook app. It may seem unremarkable at first, but imagine if it behaved like the first Material example, with the full cards sliding in from the right when you tap a list item. That would be ridiculous, wouldn't it?

The transition between list and detail view is so fluid that you don't really think of it as a transition; the elements just naturally move in space. This is semantic animation at its best.

<figure>
<video width="240" height="" controls="" poster="http://alistapart.com/d/440//fig-13-ios-passbook-696px.jpg">
<source src="http://alistapart.com/d/440/fig-13-ios-passbook-696px.mp4" type="video/mp4">
<source src="http://alistapart.com/d/440/fig-13-ios-passbook-696px.webm" type="video/webm">
</video>
</figure>

## Keep space consistent

Animations create expectations about where the animated elements are in space. For example, if a sidebar slides out to the left, you intuitively know that it's somewhere left of the visible elements. Thus, when it comes back into view, you expect it to come in from the left, where you last saw it. How would you feel if it came back in from the right?

Lest they break the space established by earlier animations, animations should not communicate contradicting information. Our earlier iOS multitasking example shows exactly why this is problematic: two different transitions tell the user conflicting things, completely breaking their mental model of the interface.

<figure>
<video width="240" height="" controls="" poster="http://alistapart.com/d/440/fig-14-multitasking-696px.jpg">
<source src="http://alistapart.com/d/440/fig-14-multitasking-696px.mp4" type="video/mp4">
<source src="http://alistapart.com/d/440/fig-14-multitasking-696px.webm" type="video/webm">
</video>
</figure>

Interestingly, OS X does something similar, but handles it in a spatially consistent way. When you full-screen a window, it scales to fill the entire screen, similar to iOS. However, it also moves horizontally to a new workspace. The window isn't _inside_ the first workspace anymore; spatial consistency is thus preserved.

<figure>
<video width="" height="" controls="" poster="http://alistapart.com/d/440/fig-15-osx-fullscreen-696px.jpg">
<source src="http://alistapart.com/d/440/fig-15-osx-fullscreen-696px.mp4" type="video/mp4">
<source src="http://alistapart.com/d/440/fig-15-osx-fullscreen-696px.webm" type="video/webm">
</video>
</figure>

Remember: violating spatial consistency is the user interface equivalent of [an M.C. Escher painting](https://en.wikipedia.org/wiki/Relativity_(M._C._Escher)
). So unless your app is [Monument Valley](http://www.monumentvalleygame.com/), please make sure to keep your space simple and non-contradictory.

## Practical considerations

Right now you may be thinking, "But wait—there's no way to apply this to _everything_!" And yeah, you're probably right.

If you did manage to do that, you'd end up with something like a single, zoomable surface containing every possible state of the system. And although that's an [interesting idea](https://www.youtube.com/watch?v=G6yPQKt3mBA), "pure" [zoomable user interfaces](https://en.wikipedia.org/wiki/ZUI) tend to be problematic in practice, because they're [hard to navigate if they go beyond a certain level of complexity (PDF)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.147.6981&rep=rep1&type=pdf).

When designing real products, semantic animation needs to be balanced with other considerations like user experience and performance. Most of your interfaces are probably never going to be 100 percent correct from a semantic-animation perspective, but that's okay. Semantic animation is a way of thinking. Once you've adopted it, you'll be surprised how many things it applies to, and how much low-hanging fruit is out there. It forces you to think about hierarchy and semantics, which helps you find simpler solutions that make more sense to the people who use your products.

Note that we, the authors, are far from having figured all of this out yet. Our article doesn't touch on many important questions (which we're still exploring) related to the consequences of animating interfaces. Nevertheless, we're convinced that semantic animation is a promising idea with real potential for making digital interfaces more intuitive and comprehensible.
