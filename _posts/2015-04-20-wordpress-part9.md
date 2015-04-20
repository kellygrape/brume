---
layout: post
title: April 20, 2015 - From Local to Live
assignmentlink: 2015-04-20-assignments
hasassignment: true
---


## Migrating to a Live Server

In this class we will be making the following assumptions:

1. You have a local server (everyone should have one for this class - this is your localhost).
2. You have a remote server (you should have signed up with an account with Reclaim Hosting at the beginning of the semester)
3. You are able to log in to your remote server
4. You have used FTP to upload the Wordpress files to your web server.

## Wordpress Local to Live

There are lots of different ways to move Wordpress from Local to Live.  Remember, Wordpress works from a combination of files and a database - so, you need to make sure that whatever migration method you choose, both are covered.

- http://www.wpexplorer.com/wordpress-local-to-live/
- http://www.elegantthemes.com/blog/tips-tricks/migrating-a-local-wordpress-installation-to-a-live-web-server
- http://www.themeskingdom.com/knowledge-base/how-to-migrate-wordpress-from-localhost-to-live-server

Be sure to read these tutorials all the way through!  Some of the steps are crucial to success, and if you just skim the articles you will miss important things!

There are some plugins that help with some of this work.

- https://wordpress.org/plugins/all-in-one-wp-migration/
- https://wordpress.org/plugins/wordpress-move/

## The Wordpress Database

We are going to migrate our Wordpress Databases from our Local installations to our Live installations.  First, I will show you an easy way to do it, using the Import / Export feature.

Then, we will discuss some downfalls of this method (if you're interested or need a refresher on our class discussion, check Method 1 in [Wordpress Local to Live](http://www.wpexplorer.com/wordpress-local-to-live/)

We will then do a full database migration - from our local databases to a database we create on our live servers.

### Create a New Database on Reclaim Hosting

1. Log into Reclaim Hosting
2. Go to your cPanel
3. Click on "MySQL Database Wizard".  The wizard will walk you through the process of creating a new database for your wordpress installation.  **Use strong usernames and passwords - this is a live installation**.  Make sure you write down your username and password, and your DB name - we will need them in just a minute.
4. After your user is created, you will get to a step where you can grant your user privileges to your database.  Check the box for "All Privileges"
5. Once you are done creating your database, click "Return Home".

### Make Your WP Installation on Reclaim Hosting Recognize Your New Database

We will be editing the `wp-config.php` file that you uploaded to your Reclaim Hosting.  We have to edit this file because it needs to have the correct database information in it.  We are going to edit it directly on the server using the File Manager, since your code editors are not hooked up to FTP.  

1. Log into Reclaim Hosting
2. Go to your cPanel
3. Click on "File Manager"
4. Choose "Document Root For [your domain]"
5. Find the `wp-config.php` file in your Reclaim Hosting folder.  It will be in whatever folder you uploaded it to.
6. Single-click on it, then at the top click "Code Editor".  This might give you some warning message, you can skip the warning.
7. Edit the database information in this file with the information that you just created.
8. Save the file.

### Export your WP Database from your Local Website

Follow the first steps of Method 2 from [this tutorial](http://www.wpexplorer.com/wordpress-local-to-live/)

### Modify File Paths

THIS IS VERY IMPORTANT.  It is described in greater detail in Method 2 from [this tutorial](http://www.wpexplorer.com/wordpress-local-to-live/)

### Upload your WP Database to your Reclaim Hosting Site

1. Log into Reclaim Hosting
2. Go to your cPanel
3. Click on "phpMyAdmin"
4. In the sidebar, click the name of the database you created.
5. In the top menu, click "Import"
6. Click "Browse your computer" and find the file you created when you exported your DB from your local site.
7. Click "Go"

### Log in to your WP site on Reclaim Hosting

Once you've done all these steps, you should be able to log in to your wordpress site on Reclaim Hosting.

## Wordpress Media

- [What is Media](http://www.wpbeginner.com/glossary/media/)
- [The Media Library](https://en.support.wordpress.com/media/)
- [Making the Wordpress Media Library your Friend](https://www.mattcromwell.com/wordpress-media-library-your-friend/)
- [The Media Library (from the Codex)](https://codex.wordpress.org/Media_Library_Screen)
- [How to Easily Embed Videos in Wordpress](http://www.wpbeginner.com/beginners-guide/how-to-easily-embed-videos-in-wordpress-blog-posts/)
- [YouTube and Wordpress](https://en.support.wordpress.com/videos/youtube/)
- [Wordpress Embeds (from the Codex)](https://codex.wordpress.org/Embeds)