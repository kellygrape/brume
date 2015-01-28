---
layout: post
title: Jan 28, 2015 - HTML and CSS Review
assignmentlink: 2015-01-28-assignments
hasassignment: true
---

##Class Goal

We will review HTML and CSS, plus review the information about CSS Selectors that we missed in the last class.

##Lesson Plan

### MAMP / XAMPP / Local Server Checkup

Everyone should have a functioning local server.  Launch your local server, and then open your index.php file in your code editor.  I will spend some time troubleshooting.  While I am troubleshooting, please quietly begin work on the readings for tonight, or catch up on homework that you have not yet completed.

### HTML Review

Review basic HTML structure
  - `<head>`
  - `<header>`
  - `<body>`
  - `<footer>`
  - HTML5 elements
  
#### Linking

  - Hyperlinks (the `<a>` tag) are used to link text on a page to other resources.  They appear within the `<body>` of your HTML document

#### Adding some style

There are four ways to add CSS to a page - using an **external stylesheet**, embedding the CSS directly into your HTML (using the `<style>` tag), importing CSS into other CSS (using `@import`), and using inline styles (something like `<p style="color:red">`).

You can read more about the first three on [HTMLDog](http://htmldog.com/guides/css/beginner/applyingcss/).

External stylesheets should be included in the `<head>` of your HTML document.  The order in which you include them will affect the way the styles are applied.  For example, we may have the following stylesheets applied to a page.

```
<link rel="stylesheet" href="style1.css" type="text/css" />
<link rel="stylesheet" href="style2.css" type="text/css" />
```

**style1.css** includes a rule that sets the background-color of `<body>` to red.  **style2.css** includes a rule that sets the background-color of `<body>` to blue.  Since **style2.css** is included AFTER **style1.css**, the rule in **style2.css** will override the first one.  The background of the page will be blue!

#### Layout and the Box Model

Let's review the **box model** of CSS.  You can read more about this on [Learn to Code HTML & CSS](http://learn.shayhowe.com/html-css/opening-the-box-model/).

The box model comes with some quirkiness.  A lot of modern web design frameworks have started to force the browser to use alternative (and more sensible, depending on who you ask) box-sizing.  You can read more about that here - [CSS Tricks box-sizing](http://css-tricks.com/box-sizing/).  I like to implement this by adding the following to my CSS:

```
html {
  box-sizing: border-box;
}
*, *:before, *:after {
  box-sizing: inherit;  
}
```

You can read more about this technique on Paul Irish's article ["* { Box-sizing: Border-box } FTW"](http://www.paulirish.com/2012/box-sizing-border-box-ftw/)


#### Inspecting Element

Let's open this template in Chrome and discover how we can explore and learn about the code by using Chrome's Inspect Element tool.

[Boxify](http://tympanus.net/Freebies/Boxify/)

## Resources for Class

[HTML Dog's Beginner Guide for HTML](http://htmldog.com/guides/html/beginner/)
[Web Validator](http://validator.w3.org/) - a great tool for finding errors in your code!
