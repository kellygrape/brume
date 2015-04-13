---
layout: post
title: April 13, 2015 - Wordpress, Page Templates, Basic Theme Development and Child Themes
assignmentlink: 2015-04-13-assignments
hasassignment: true
---


###Wordpress Reference

I've created a Wordpress Reference area for this class on our class website.  You can access this from the header of our website, or by clicking [here](/wordpress).  I will add to this as the class goes on.


##Basic Theme Development

###Huge Caveat

We will be editing an already created theme directly in this exercise.  **We are doing this for the purposes of learning.**  If you were to take this theme and re-sell it, claiming the work as your own without crediting the original theme author, **that would be stealing**.  There are already existing theme frameworks / base themes that allow you to create your own themes without having to start from scratch, so if you are interested in doing some serious theme development, I suggest you start with one of those themes.

- [_s](http://underscores.me/)

### Get Set Up

Let's talk about basic theme development.  Please follow along with this exercise.

- [Download this theme](/media/h5.zip).  Do not unzip it.
- Start your local server
- Open up your local Wordpress installation and Log In
- Go to the "Appearance" section.
- Add a new theme, and add the theme we just downloaded.  Do not activate it.

- In your file explorer (Finder or Explorer), navigate to your Document Root.  Inside your Document Root, navigate to your wordpress installation, and then to the folder `wp-content/themes`.
  - This is where your theme has been installed to.  See the h5 folder?  That is your new theme!
  - From the h5 folder, open the file `style.css` in your favorite code editor.

### Updating Style.CSS - give your theme a name!

- In `style.css`, update the info at the top of the page to reflect your new theme’s name, with you as the author.
- Not all of the variables are required for your theme to work properly.
- Save your `style.css`
- Go back to your browser, and in your Wordpress dashboard Appearance section, you should see that the H5 theme has changed its name to whatever you changed it to.  **Activate your theme**.
- View your website and see that it has changed.

### Changing Styles

- In `style.css`, add a background color to your theme's body.  Pick something light (but not white!).
- Save `style.css`, and reload your wordpress website to see that the background color has changed.


### Template Files

[About Theme Files on our Wordpress Reference](wordpress/themeing-theme-files.html)

As Wordpress generates your website, it will look at the content that you are requesting (via the URL), and look through the template files to find the correct template file to display your content.  There is a hierarchy to how this is done.  

- Static pages, such as About or Contact, are built using the `page.php` template.
- Page views which display a list of posts are built using the `index.php` template.
- Page views which display a single post are built using the `single.php` template.
- [Read more on our Wordpress Help section](/wordpress/themeing-theme-files.html)

Let's add something special to the header of all of our **pages**.  We are going to edit the `page.php` file.

- From the h5 folder, open the file `page.php` in your favorite code editor.
- There is a lot of strange code, but you should be able to recognize the HTML in this file.  Find the `<h1>` tag.
- After the `<h1>` tag, add an `<h2>` tag.  Inside this tag, write "This is a Wordpress Page"
- Save this file

Now, we need to add a page to our Wordpress installation in order to see this.

- Add a new Wordpress page.  The content can be whatever you would like.  Title it "Theme Test" (so you can delete it later!)
- Save the page, and view it in your browser.
- Do you see the `<h2>` that we added?

### Custom Page Templates

[Custom Page Templates on our Wordpress Reference](/wordpress/themeing-page-templates.html)

Now that we have edited our `page.php` template, we may decide that we want specific pages to have a different look - maybe we want a specific page to have our 'About Us' page to have different text in the `<h2>` tag that we created before.

We can create a custom page template based off of any of our template files.  The most logical one to use as a base is the `page.php` template.

- From the h5 folder, copy your `page.php`.  Name your newly created file `template-about.php`
  - for your custom templates, the name of the file doesn't matter.  As long as you don't use a reserved file name (something that would exist in the theme hierarchy), you can use whatever you would like as your name.
- Open your `template-about.php` file.
- Remember that H2 we created before?  Change the text that is inside of it.
- Save this file

Ok, now that we've made our change, we want the file to be useable by our Wordpress pages.  You can do this in a few different ways.  The first is to make it available via the template hierarchy.  So, if you knew that this special template would **always** be used **only** by your about page, you could rename the file `page-about.php`.  This structure tells wordpress to use this template for **Pages** with the slug **About**.

However, maybe we want this file to be selectable by one or many Wordpress pages.  To do this, you need to add a special comment section in the header of the file.

- Open your `template-about.php` file.
- Insert the following code at the top of the file.

```
<?php
/*
Template Name: My Awesome Custom Page
*/
```

- Save this file

Now that we've created a Custom Template, we can active it on any of our pages.  Go to your Wordpress Dashboard, and edit one of your pages.  On the side, under the "Publish" section, there is a section where you can choose a Custom Page template.  Your custom page should be listed here.

- [Great Video Tutorial on doing this](https://www.youtube.com/watch?v=9HCxKyj1SV0)
- [Creating Custom Page Templates in WordPress](http://premium.wpmudev.org/blog/creating-custom-page-templates-in-wordpress/)

### Child Themes

We have talked before in class about creating child themes.  I've pulled out that lesson and copied it here - [About Child Themes on our Wordpress Reference](/wordpress/themeing-child-theme.html)

Now that you know a little bit more about theme files in Wordpress, you can do more with your child theme than just change the stylesheet.

Any file that you put in your child theme will be used instead of the same-named file in the parent theme.  So, if you want to do something different with the `page.php` file, simply copy it from the parent theme into the child theme, and make your changes in the child theme.

You can also create your custom page templates inside of your child theme, so they don't get mixed up with your parent theme files.