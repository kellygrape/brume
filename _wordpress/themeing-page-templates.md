---
layout: wordpress
title: Theme Development - Custom Page Templates
---

###Custom Page Templates

Custom page templates are very useful for creating special features on your website.  You may find that your theme has come installed with a number of special page templates.  Experiment with these and see what they can do!

- [Changing page attributes](https://en.support.wordpress.com/pages/page-attributes/)
- [Wordpress Codex on Custom Page Templates](https://codex.wordpress.org/Page_Templates)

### Class Exercise Related to Page Templates
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