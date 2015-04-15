---
layout: post
title: April 15, 2015 - From Local to Live
assignmentlink: 2015-04-15-assignments
hasassignment: true
---


## Migrating to a Live Server

In this class we will be making the following assumptions:

1. You have a local server (everyone should have one for this class - this is your localhost).
2. You have a remote server (you should have signed up with an account with Reclaim Hosting at the beginning of the semester)
3. You are able to log in to your remote server

## URL and Folder Structure Review

We will quickly refresh this.

## Using FTP to upload files to your web server

FTP stands for File Transfer Protocol.  It's a way that you are able to transfer files from one area to another.  We will be using FTP to load our files from our local server to our remote server.  [There's a great guide by Reclaim Hosting for this](http://docs.reclaimhosting.com/Getting-Started-with-Reclaim-Hosting/Uploading-Files-to-your-Reclaim-Hosting-Account/#ftp)

## Cyberduck

Everyone should download and install the program [Cyberduck](https://cyberduck.io/?l=en).  If you have another FTP program you would like to use, that is fine.  Another option is [Filezilla](https://filezilla-project.org/).  There are many, many more options.

## Setting up FTP for Reclaim Hosting and Cyberduck

First, open Reclaim Hosting and log in.  Click on the link in the menu for "cPanel".

In cPanel, find the area for FTP Accounts.

Create a new account.  This can be whatever you would like it to be - I suggest picking a username and password that you will remember.  **This is a live server that other people can access.  Pick a secure username and password (not <em>admin</em> and <em>password</em>)**  When you create your new account, set the Directory (right before the 'Quota' select boxes) to be `public_html/` (so, where it autofills with your username, just delete the part that is your username)

Now that you have that set up, open Cyberduck.  Click 'Open Connection'.  Use the following details.
- **Server** : your domain name
- **Username** : the FULL username you just created.  It likely looks like an email address - username@mydomain.com.  Use the entire thing.
- **Password**: the password you just created

Once you have filled this out, hit 'Submit' (or 'Connect').  You may get an alert about connecting over an Unsecured FTP Connection.  Click Continue.

If it authenticates, make this a bookmark so that you can easily connect again in the future.  Click "Bookmarks" in the menu and click "Add Bookmark".

## Using FTP

If you drag and drop files from your computer to your FTP window, those files will be uploaded to your server.

**You should be putting files in your public_html folder**.  If you open your FTP Program and you see options like `public_ftp` and other things, you need to choose the `public_html` folder before you continue.

## Wordpress Local to Live

There are lots of different ways to move Wordpress from Local to Live.  Remember, Wordpress works from a combination of files and a database - so, you need to make sure that whatever migration method you choose, both are covered.

- http://www.wpexplorer.com/wordpress-local-to-live/
- http://www.elegantthemes.com/blog/tips-tricks/migrating-a-local-wordpress-installation-to-a-live-web-server
- http://www.themeskingdom.com/knowledge-base/how-to-migrate-wordpress-from-localhost-to-live-server

Be sure to read these tutorials all the way through!  Some of the steps are crucial to success, and if you just skim the articles you will miss important things!

There are some plugins that help with some of this work.

- https://wordpress.org/plugins/all-in-one-wp-migration/
- https://wordpress.org/plugins/wordpress-move/