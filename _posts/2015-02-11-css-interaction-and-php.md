---
layout: post
title: February 11, 2015 - CSS Interactions
assignmentlink: 2015-02-11-assignments
hasassignment: true
---

##Class Goal

We will be working with CSS animations in this class (hover states, transforms, and transitions.)

For most of this class we will be working through Shay Howe's excellent guides to CSS Transforms and Transitions.  So, rather than notes specific this this lesson, I will be providing links to those guides, plus other resources you may find useful.  We will be doing some in-class examples and experimentations.


##Lesson Plan

### MAMP / XAMPP / Local Server Checkup

Everyone should have a functioning local server.  Launch your local server.  Your document root should look something like this:

<img src="../media/0204/directory-structure.png" alt="directory-structure" />


###Core Concept Check

An HTML Element is written like this:

```
<div class="awesome-div">
  This is my div!
</div>
```

Some CSS that could target that element could be written like this:

```
div {
  background-color: green;
  width: 200px;
  height: 200px;
}
```

OR like this:

```
.awesome-div {
  background-color: green;
  width: 200px;
  height: 200px;
}
```

We can use pseudo-classes to change the styling of almost any HTML element.  One of the most common ways to alter CSS is when **hovering** on that element.

```
.awesome-div:hover{
  background-color: blue;
  width: 300px;
  height: 300px;
}
```

Let's play around with this on CodePen.

[See this example on CodePen](http://codepen.io/kellygrape/pen/LEemKV?editors=110)

###CSS Transforms

[CSS Transforms Guide](http://learn.shayhowe.com/advanced-html-css/css-transforms/)

###CSS Transitions and Animations

[CSS Transitions and Animations Guide](http://learn.shayhowe.com/advanced-html-css/transitions-animations/)

###CodePen, SASS, Jade/HAML

CodePen allows you to write shorthand CSS and HTML.  Let's talk about these options!

[Example pen using these options](http://codepen.io/sforsparky/pen/HoLcy)

### Free Coding Time

- Play around with CSS Transitions and Transforms!
- Start working on Project #1 (linked from today's Assignments)
  
###Cool Examples

[Rotating Text](http://codepen.io/kellygrape/pen/GgydqJ)

  - Forked from [Liz](http://codepen.io/lizink/)'s Pen [Rotating Words](http://codepen.io/lizink/pen/EkAdH/).
  - [Original tutorial found here](http://tympanus.net/codrops/2012/04/17/rotating-words-with-css-animations/)
