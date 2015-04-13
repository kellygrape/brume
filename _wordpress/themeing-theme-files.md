---
layout: wordpress
title: Theme Development - Theme Files
---

###Theme Files

Wordpress has a number of standard theme files.  When you look at the source of a theme (by downloading it to your desktop and opening it in your code editor / file explorer), you will find differences from one theme to another.  As you start to look at more and more themes, you will begin to see patterns and similarly-named files.

###Minimum Needed Files

At the very minimum, your theme needs an **index.php** and a **style.css** file.

**File naming is very important in wordpress**.  Only by naming your files the correct thing will Wordpress be able to understand what your theme is for.  For example, if you decide to name your **style.css** something different (even just *styles.css*), your theme will not work.

###Template Hierarchy

As you add files to your theme, Wordpress will begin to utilize those files for different things - for example, if you add a **single.php**, Wordpress will know to use this template for your single blog posts.

[Understanding Wordpress Template Heirarchy](http://www.elegantthemes.com/blog/tips-tricks/understanding-the-wordpress-template-hierarchy)
[The Worpdress Template Heirarchy](http://www.sitepoint.com/the-wordpress-template-hierarchy/)

####Twenty Fifteen Template Hierarchy Example (from [Sitepoint]((http://www.sitepoint.com/the-wordpress-template-hierarchy/)))

Suppose you have activated the Twenty Fifteen theme and a user visits the page yoursite.com/author/tahir/. First, WordPress will search for the template labeled `author-tahir.php` but `author-tahir.php` is not available. WordPress will then look for `author.php`, if it also does not exist, it will look for `archive.php`. This file is available in Twenty Fifteen theme. If you delete or rename `archive.php` then WordPress will use `index.php` to render the page.

Each time a user visits your website, WordPress moves up the template hierarchy until it finds a template file that matches. This has everything to do with how these files are named.

###Read More

- http://www.smashingmagazine.com/2013/03/13/a-guide-to-wordpress-theme-options/
- https://yoast.com/wordpress-theme-anatomy/