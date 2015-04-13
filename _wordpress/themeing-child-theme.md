---
layout: wordpress
title: Theme Development - Child Themes
---

###Wordpress Child Themes

- http://codex.wordpress.org/Child_Themes
- http://www.hongkiat.com/blog/wordpress-child-themes-dev/
- http://themeshaper.com/modify-wordpress-themes/


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