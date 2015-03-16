---
layout: post
title: March 16, 2015 - Wordpress
assignmentlink: 2015-03-16-assignments
hasassignment: true
---

##Class Goal

We will be working with Wordpress over the next few classes.

##Lesson Plan

### What is Wordpress?

Wordpress is a **content management system** (CMS).  It is free, open-source, and very powerful.  Originally built as a blogging software, Wordpress has now grown to be utilized for everything from small blogs all the way to full corporate websites.  Millions of companies use Wordpress to help them communicate.

There are lots of different kinds of CMS available - some are complicated, some are easy.  Some are free, some are very expensive.  As you grow to be more familiar with Wordpress, you might want to check out other types of popular CMS, such as Drupal or Joomla.

**Is Wordpress the best CMS?**  Absolutely not.  Wordpress is fantastic - it is very popular, flexible, and easy to learn.  The BEST CMS is the one that works best for whatever project you are working on.  Every CMS has flaws.

We will **not** be purchasing a book about Wordpress; however, if you are interested in learning more, there are some wonderful inexpensive guides available online.  I highly recommend the Wordpress books available at [Perishable Press](http://wp-tao.com/store/#combos) - I've purchased the combo of **Digging into Wordpress** and **The Tao of Wordpress**.  The nice thing about these guides is that you will receive free updates as Wordpress changes, and you will also get some themes to use.

### Wordpress.com or Wordpress.org

When you first decide to set up a site using Wordpress, you will need to make a decision - use **Wordpress.com** or **Wordpress.org**.  Wordpress.com allows you to set up a free Wordpress account and a website. Wordpress.org allows you to download the Wordpress software, install it on hosting of your choice, and run your own Wordpress website.  Both are run by the same parent company, Automattic.

**Wordpress.com**

- Web-based service
- Free, but limits on space and customization options
- You may have ads on your site that you can't control.
- Limited storage
- Your url will be somethingsomething.wordpress.com (although you can pay to customize)
- No access to the files and the database
- Updates are managed by the Wordpress team

This version is good for small websites, or for just getting your feet wet with Wordpress.

**Wordpress.org**

- Set up Wordpress on your own server
- No ads (unless you want them!)
- Storage limited only by your web host
- Unlimited customization
- Your URL will be whatever you choose, but you have to register it (usually part of your hosting)
- Full access to files and database
- You need to manage your updates to plugins, themes, and files

This version is good for designers, developers, and larger sites.  We will be using this version throughout this course, and the things we learn in the next few weeks will mostly be applicable to the self-hosted version of Wordpress.  Some of the knowledge you will gain might be used for Wordpress.com sites, but a lot of the customization options are only available for self-hosted sites.

**[Read more about Wordpress.com vs Wordpress.org](http://premium.wpmudev.org/blog/wordpress-org-vs-wordpress-com-a-definitive-guide-for-2014/)**

### Getting Started with Wordpress

To get started with WP, you will need a few things.

- A host
- A domain name
- Software
  - a web browser
  - a text / code editor
  - an FTP program (I recommend [Cyberduck](http://cyberduck.ch/) or [FileZilla](http://filezilla-project.org/).  Both are available for Mac and PC)
  - for local development, you will need something like MAMP to run a local server
  
**Choosing a host**

Choosing a web host is based on a number of important factors, more than we can cover in any single class.  Many hosts are available for $10 a month or less, and offer great features like one-click Wordpress installation.  At minimum, your host should support the technology that Wordpress is run on - Apache, MySQL, and PHP.  I recommend reading the following articles.  

- [How do you choose a WordPress host?](http://chrislema.com/choose-a-wordpress-host/)
- [The Ultimate Guide To Choosing A WordPress Host](http://www.smashingmagazine.com/2014/09/25/the-ultimate-guide-to-choosing-a-wordpress-host/)
- [How to choose the right WordPress hosting plan](https://themesurgeons.com/how-choose-right-wordpress-hosting-plan/)

### Understanding Wordpress

Unlike our previous web projects, where we coded our content directly into the page, Wordpress works by storing your content in a database and using special scripts that read the data and display it.

When you download Wordpress, you are downloading what is referred to as **Wordpress core**.  These are the base files needed to make the software work, and when paired with a database and correctly configured, are the base of what will make your website.  You will **never touch** the vast majority of these files, and that is by design.  In order to keep Wordpress functioning, and not lose your changes when the software is updated, it is very important to **not hack core**.

Any changes you want to make, such as plugins or themeing, will be done in the wp-content file.  The wp-config.php file and the .htaccess file are the only files outside of the wp-content folder that you will likely need to edit.


### Anatomy of a page visit, the Wordpress Version

1. A visitor requests a web page by typing a domain name into their browser (or clicking a link).
2. The requested domain is checked at the domain registrar to see where the server that manages that domain is.  The registrar will return with an address.
3. The request follows to that address, finding your server.
4. Your server, based on how it is configured, will server up the requested files.
  - If your files are HTML, CSS, and JS (a static website), they will be served up and rendered by the browser (we are familiar with this process).
  - If your website is managed by a database (a dynamic website, like Wordpress), the software will use files and database to generate the requested page (normally generated as HTML and CSS and JS) and send it to the browser. After the visitor requests a web page, the requested domain name is checked at the registrar to determine the correct server location.


### Initial Wordpress Setup - The Admin Side

- Logging in
- The Toolbar
  - this is customizable
  - quick way to get to different sections of your site
  - you may see different things here depending on what plugins you have active
- Main Menu
  - allow you to access different features of the backend
  - may look different depending on what theme and plugins you have (may have different options)
- Screen Options
  - things like to hide - checking the screen options is a great way to customize what panels you can see and what you don’t want to see
- Help Message & Feature Pointers
  - these are mostly callouts and can be dismissed, if you have read and understand what they do.
- The Dashboard
  - the Dashboard is what you see when you first log in.  
  - you will see messages here if your site has been automatically updated. you can also do some actions from this screen.
  - You can customize what you see on the dashboard - either through the [screen options](https://www.siteground.com/tutorials/wordpress/customize-dashboard.htm), through plugins ([list of plugins](http://mediatemple.net/blog/news/customizing-the-wordpress-admin-experience-for-clients/) and [another example](https://wordpress.org/plugins/ag-custom-admin/)) or by editing code ([example one](http://code.tutsplus.com/articles/customizing-the-wordpress-admin-the-dashboard--wp-33110) and [example two](http://premium.wpmudev.org/blog/adding-custom-widgets-to-the-wordpress-admin-dashboard/))

### Keeping Your Site Up to Date

An important part of managing a Wordpress site is keeping it updated.  Wordpress will trying to keep itself updated by pushing automatic updates.  Sometimes this might not be what you want to happen, and you can disable this feature in code, but generally it is good to allow Wordpress to keep itself updated.

You will find that WP will not update itself for major version releases - but you will have the ability to update it yourself.  Generally this is a simple process - Wordpress likes to make it easy to keep things up-to-date.

Your plugins will **not** be automatically updated, nor will your themes - you will often log in and see that there are updates to be installed.  It is important to keep your site up to date to ensure that your site is secure

### Content Management - Basic Content

Wordpress allows you to manage your content using two different content types - Pages and Posts.   Posts are the most common type of content in the Wordpress world - they are great for things like blog posts, news, and other frequently updating content.

Pages are used for more static content, such as your "About Us" page or Privacy Policies.

There are key differences in the way that Wordpress handles Pages and Posts, but there are also many similarities.  It's important as a Wordpress professional to have an understanding of what the best type for your content is, and use them each appropriately.

The editing for Posts and Pages is very similar.

**Read More about Posts vs Pages**

- [Pages vs Posts](https://en.support.wordpress.com/post-vs-page/)
- [What is the Difference Between Posts vs. Pages in WordPress](http://www.wpbeginner.com/beginners-guide/what-is-the-difference-between-posts-vs-pages-in-wordpress/)


### Categories?  Tags?  Both / neither?

Categories and tags are both types of taxonomy that can be used to help you organize your content.  [Read more about Categories and Tags](https://en.support.wordpress.com/posts/categories-vs-tags/)

### The reading experience

[Using Wordpress's "Front Page" feature](https://en.support.wordpress.com/pages/front-page/)
Setting up a home page
Setting up a posts page

