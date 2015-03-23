---
layout: post
title: March 23, 2015 - Wordpress - Functions and Theming
assignmentlink: 2015-03-23-assignments
hasassignment: true
---

##Class Goal

Today we will be talking about our experiences using Layers, the Wordpress site builder.  We will also be looking at the basics of Wordpress theming, get an understanding of how to use a child theme to customize a theme, and gain some basic knowledge of PHP - the programming language is used to build Wordpress.

##Recap

What has everyone's thoughts been so far on using Layers to create your websites?

##Wordpress Theming

As you have seen, Wordpress themes can range from very simple to incredibly complex.  Themes can come with lots of baked-in functionality that you won't necessarily find in another theme.  The best themes (and Layers is not actually included in this generalization) will allow the end user to change their theme (change the look of their website) without dramatically losing functionality.

Themes can be found in lots of different places - the theme directory, online companies such as WooThemes and Elegant Themes, and large paid theme repositories such as ThemeForest.

###How to Choose a Theme

Choosing a theme can be a very personal and project specific process.  In general, good themes will allow you to build your website and display your content in an engaging way without getting in your way.

One thing that beginners get caught up on is overlooking themes just because they feature the wrong kind of photography or color scheme.  As web designers, **you know** that these kinds of things can be changed.  It can be especially helpful when meeting with clients to download some sample themes and do some basic customizations to help the client envision what their site might look like.  This will also give you the opportunity to try the theme out and see if it will actually meet your needs.

##What is a theme?

Wordpress themes are built using code - HTML, CSS, Javascript, and PHP.  At the bare minimum, a wordpress theme needs two files - a **style.css** and an **index.php**.  The index.php file should feature the [Wordpress Loop](https://codex.wordpress.org/The_Loop).

- [What is: Loop](http://www.wpbeginner.com/glossary/loop/)
- [The WordPress Loop Explained For Beginners](http://www.elegantthemes.com/blog/tips-tricks/the-wordpress-loop-explained-for-beginners)

The **style.css** file will need to have some comments at the beginning that tell Wordpress about your theme.

```css
/*   
Theme Name: Basic Minimum Theme
Description: Just the bare minimum to make this work
Author: My Name
Version: 1.0
*/
```

Let's take a look at a basic theme.  [Download this theme](../media/0323/basic.zip) and install it in your local wordpress installation to work along with me.

###PHP

Wordpress themes are built using PHP.  PHP mixes nicely with the HTML and CSS you already know.  PHP can act kind of like a variable for your page - you can use different functions in the language / built into Wordpress core that will help you display different values in different places.  Let's look at how we can mix HTML and PHP to give some separation to our theme.

###Building a Child Theme

A really good way to customize an already built theme is to create a **child theme**.  A child theme allows you to leverage all of the functionality of a theme, with your own customizations.  You won't be editing the pre-built theme directly; instead, you'll be creating a new theme based on the original theme.

There are some great tutorials out there for creating child themes, and a [couple different methods](http://www.drmagu.com/creating-a-child-theme-in-wordpress-alternate-methods-1331.htm) for doing so (including a plugin!).  Let's create our first child theme.

1. On your computer, go to your document root, then go to wordpress -> wp-content -> themes
2. Create a new folder.  Name it (ALL LOWERCASE) **2015child**
3. Inside this **2015child** folder, create a **style.css** file.  At the top of your style.css file, put the following code

```
/*
Theme Name: Example Twenty Fifteen
Version: 1.0
Description: A child theme of Twenty Fifteen
Template: twentyfifteen
*/
 
@import url("../twentyfifteen/style.css");
```

Now, you should be able to go to your Wordpress installation and activate this theme.  Now that we've done that, we can add our customizations.  Let's change the background color.

```
/*
Theme Name: Example Twenty Fifteen
Version: 1.0
Description: A child theme of Twenty Fifteen
Template: twentyfifteen
*/
 
@import url("../twentyfifteen/style.css");

body{
  background-color: blue;
}
```

Now, try to make all the post titles a different color.  You will probably have to go into Chrome's **inspect element** to discover what the correct selector you need to use is. 