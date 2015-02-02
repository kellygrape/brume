---
layout: post
title: Jan 26, 2015 - CSS Selectors
assignmentlink: 2015-01-26-assignments
hasassignment: true
---

##Lesson Plan

Review types of selectors in CSS.  Understanding CSS selectors is really important, and will help us when we start using jQuery.

### Type selector
  The most basic kind of selector, using just the name of the HTML element as the selector.
  
  ```css
  li{
    /* this will select all li on the page */
    color: red;
  }
  ```

### Class / ID selector
  The second-most basic kind of selectors, allows you to select elements that have attributes of either class or ID.
  
  ```html
  <div id="main-content">
    <p class="intro">This is my intro text</p>
    <p>This is the regular text</p>
  </div>
  ```
  
  ```css
  #main-content{
    /* we select the things within the div with the main-content 
        ID by using #main-content */
    font-size: 14px;
  }
  
  .intro{
    /* we select the things within the p with the intro class by using .intro */
    color: red;
  }
  ```

### Universal selector 
  The Universal Selector is the * in CSS (the asterix character). It is essentially a type selector that matches any type. (From [CSS Tricks]((http://css-tricks.com/almanac/selectors/u/universal/)).  This isn't frequently used (you may use it once or twice in your projects), but important to know.
  
  - [What is the difference between using * or using `body` as a selector?](http://programmers.stackexchange.com/questions/178049/css-use-universal-selector-vs-html-or-body-selector) - the first two answers here are really good explanations of the difference.
  - [Things it might be fun to try the universal selector on](http://css-tricks.com/things-it-might-be-funuseful-to-try-the-universal-selector-on/)

### Descendant

  The descendant selector allows you to more **more specific** with what you apply your CSS to.  For example, you might only want your list items inside your menu to be red; list items elsewhere on the page should be their regular color!
  
  You can stack these however you like - the example below is a **type** selector as a descendant of a **class** selector.  You could also have two type selectors (`ul li`), a class and a class (`.menu .active`), etc.

  Note the SPACE here between the selectors.  You could write something like `li.active` - this would select all `li`'s that have the class of `active`.  This is not an example of a descendant selector.
  
  ```css
  .menu li{
    /* this will select all li within the element (div, ul, whatever) 
        with the class 'menu' */
    color: red;
  }
  ```
  
  - [CSS Tricks on Descendant Selectors](http://css-tricks.com/almanac/selectors/d/descendant/)
  
### Child Selector

This is very similar to the descendant selector.  It can get a bit confusing, so some examples might help.  Basically, whereas a **descendant selector** (`.main li`) will select all of the things (`li`) anywhere inside of the other thing (`.main`), a **child selector** (`.main > li`) will only select when the things (`li`) are  **direct children** of the other thing (`.main`).

You can see a visual of this on [CSS Tricks](http://css-tricks.com/almanac/selectors/c/child/).

This is really helpful when styling lists.

- [A good explanation and visualization](http://css-tricks.com/child-and-sibling-selectors/)

## Selectors that you should read about

### Attribute selector 

  - [Read on CSS Tricks](http://css-tricks.com/almanac/selectors/a/attribute/)

  One thing a bit confusing about this article is that it limits the examples to the 'rel' attribute.
  
  Remember, an attribute is something that you add to your HTML tag.  `class` is a type of an attribute in this example, as is `href`.
  
  ```html
  <a href="mailto:kpipe@sju.edu" class="email-link">Email Me!</a>
  ```
  
  We can't always depend that people will remember to add the class to their email links, so we could create a style using the attribute HREF, so that if the HREF **begins with** mailto, we want to make it bold and underline it.
  
  ```css
  a[href^="mailto"] { color: red; }
  ```
  
  The `^=` in that selector means 'begins with'.  All email links always begin with 'mailto', so I know this will correctly target the email links on my website!
  
### Pseudo-class

- [Read on CSS Tricks](http://css-tricks.com/pseudo-class-selectors/)

These are super useful!  You can use a pseudo-class to highlight only the last item of a list, for example.

```css
li:last-child{
  color: red;  
}
```

Or to add an underline when you hover on a link!

```css
a:hover{
  text-decoration: underline;  
}
```

### Pseudo-element

- [Read on CSS Tricks](http://css-tricks.com/pseudo-element-roundup/)

A little more complex, but there are some interesting use-cases here.

**A note about pseudo-classes and pseudo-elements** - you'll often see these with : or a :: between the selector.  There is no real difference - if you need to support IE8, make sure you use a single :.  More on this on [CSS Tricks](http://css-tricks.com/almanac/selectors/a/after-and-before/)

## Extra Bonus Selectors

It's good to know that these exist.  I don't frequently use them, and would probably need to look them up to remember what they did.  But they can certainly be useful in some circumstances.

- [General Sibling](http://css-tricks.com/almanac/selectors/g/general-sibling/)
- [Adjacent sibling](http://css-tricks.com/almanac/selectors/a/adjacent-sibling/)

## I hate CSS Tricks and want other resources for learning about this

Not sure why you hate CSS Tricks, but here is another run-down of selectors from [Shay Howe](http://learn.shayhowe.com/advanced-html-css/complex-selectors/).


## Resources

- [Crazy-Town Selectors](http://css-tricks.com/crazy-town-selectors/)
- [Little CSS Stuff Newcomers Get Confused About](http://css-tricks.com/little-css-stuff-newcomers-get-confused-about/)
- [Interactive Specificity Calculator](http://specificity.keegan.st/)