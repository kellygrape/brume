---
layout: post
title: February 2, 2015 - CSS Layout & Responsive Design
assignmentlink: 2015-02-02-assignments
hasassignment: true
---

##Class Goal

We will discuss CSS for layout, plus discuss responsive design.  We will have time in class to work on our own layouts.

##Lesson Plan

### MAMP / XAMPP / Local Server Checkup

Everyone should have a functioning local server.  Launch your local server, and then open your index.php file in your code editor.  I will spend some time troubleshooting.  While I am troubleshooting, please quietly begin work on the readings for tonight, or catch up on homework that you have not yet completed.

### CSS Layout

- Utilizing floats
- Clearfix - I like to use [Nicholas Gallagher's Micro-clearfix](http://nicolasgallagher.com/micro-clearfix-hack/).  Copy and paste the following code into your CSS file.

```
/**
 * For modern browsers
 * 1. The space content is one way to avoid an Opera bug when the
 *    contenteditable attribute is included anywhere else in the document.
 *    Otherwise it causes space to appear at the top and bottom of elements
 *    that are clearfixed.
 * 2. The use of `table` rather than `block` is only necessary if using
 *    `:before` to contain the top-margins of child elements.
 */
.cf:before,
.cf:after {
    content: " "; /* 1 */
    display: table; /* 2 */
}

.cf:after {
    clear: both;
}

/**
 * For IE 6/7 only
 * Include this rule to trigger hasLayout and contain floats.
 */
.cf {
    *zoom: 1;
}
```

### Responsive Design

- What is responsive design?
- What are some common design patterns?
- How can we accomplish responsive layouts?
  - think of everything as blocks
  - responsive design patterns

### Coding Work

- Choose one of the mockups and replicate it using HTML and CSS.  Your design doesn't have to be perfectly responsive, but you should not have any fixed-width elements.  Note - these are just simple mock-ups.  Colors, text, and fonts used are just for demonstration purposed - you can choose your own colors and fonts.  Pay attention to white space!

- <a href="../media/0202/layout1.png">Layout #1</a> (note - the round things on this should be social media icons.  You don't have to make them circular.)
- <a href="../media/0202/layout2.png">Layout #2</a>  (note - the round things on this should be social media icons.  You don't have to make them circular.)
- <a href="../media/0202/layout3.png">Layout #3</a>

## Resources

- [Google Web Basics about Responsive Design](https://developers.google.com/web/fundamentals/layouts/rwd-fundamentals/set-the-viewport)
- [A Different Way to consider responsiveness](http://webdesign.maratz.com/lab/responsivetypography/realtime/) (turn on camera and demonstrate responsive text!)