---
layout: post
title:  "CSS Typography"
day:    "Tue, April 12"
time:   "2 PM - 4 PM"
meta:   "Once the typography is set in our designs how can we translate it in code? There are some helpful properties that allow us to define the text in webpages"
visible: true
---

As we saw in the previous lecture there are several foundries and services where you can get fonts from. For the purpose of todays exercise we are going to use [Google Fonts](https://www.google.com/fonts).

On Google Fonts you have three options to import the fonts in your website. You can point to the Google servers via the `link` tag, you can use the `@import` CSS property or you can load the font with JavaScript. Another option, which I prefer, is to download the fonts and self-host them. In the case of Google Fonts you simply add the fonts of your choice to the collection (with the big blue button):

![Add fonts to the collection on Google Fonts](../uploads/2016/04/google-fonts-1.jpg)

and then you download the zip:

![Download Google Fonts as zip file](../uploads/2016/04/google-fonts-2.jpg)

Once you unzip the file you notice that the fonts are in `.ttf` format. The format that we need is `.woff` which stands for web open font format. It is well supported by most browser and as long as you don't need to support IE < 8 or Opera Mini is the only file you will need. 

Talking about support I would like to show you [caniuse.com](http://caniuse.com) which is a website where you can check the support of all CSS properties.

![Screenshot of can I use interface](../uploads/2016/04/can-i-use.jpg)

Now that you have your `.ttf` file you need to convert it in `.woof`. In order to do just that you can use on-line services like [web-font-generator.com](https://www.web-font-generator.com/) or [fontsquirrel.com](https://www.fontsquirrel.com/tools/webfont-generator).

## Import font in CSS

Once you have your `.woff` files it's time to import them with the `@font-face` property, just like this:

```css
@font-face {
  font-family: "Font Name";
  src: url('path/fontname.woff') format('woff');
  font-weight: normal;
  font-style: normal;
}
```

After you declare where the CSS should look for your fonts you can add them to your selectors:

```css
.class {
  font-family: "Font Name", Helvetica, Arial, sans-serif;
}
```

## Vertical Rhythm

Now we are going to see how to create and maintain vertical rhythm in our website. As we saw in the previous lecture vertical rhythm is all about making a layout more balanced and  readable. The main purpose is to keep vertical spaces between elements on a page consistent with each other. We could set the spaces manually for each of our elements but luckily there handful tools like [gridlover.net](http://www.gridlover.net/try)

![Screenshot of gridlover.net](../uploads/2016/04/grid-lover.jpg)

With Gridlover we can tweak the base font size, the base line height and set the scale factor. Then it will automatically create all the styles for our typography elements.

Moreover you can add the embed code of the font provider in the `<head>`. In our case, with Google Fonts, we simply add the `<link>` that we find the collection view:

```html
<link href='https://fonts.googleapis.com/css?family=Fira+Mono:400,700' rel='stylesheet' type='text/css'>
```

In this way we can effectively set spacing and rhythm base on the font of our choice. Then all we have to do is to copy and paste the code in our `style.css` and update the margins and the paddings of our already existing elements with a multiplier of our just set base line height. 