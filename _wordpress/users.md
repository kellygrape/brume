---
layout: wordpress
title: User Management
---

##Wordpress Configuration - User Administration

When you first install WP, you will set up an administrator username and password.  This is your default user for the site.  The administrator username and password that you choose is specific to that installation - if you want to use the same username and password for multiple installations, you may, but it is not always advisable for security reasons (if someone is able to hack your account for one site, they can do it for other sites).

###Don't use Admin as your username!

It is advisable not to use **admin** or **administrator** as your username for live installations.  Having your administrator username be **admin** can leave your site open to hacking (at the very least, it makes it easier for hackers to attack your site!).

- Did you already set your admin username?  You can change it in the database.  [Follow these instructions](https://www.siteground.com/tutorials/wordpress/change-wordpress-username.htm)

###Logging In 

By now you should be familiar with the process of logging in to the administrative dashboard.  On WP sites, there are two URLs that you can use to get to the admin login screen:

- http://[www.example.com]/wp-login.php
- http://[www.example.com]/wp-admin

There are ways that you can change this, but for the vast majority of installations, this is where you will find the admin login.

###User Registration

User registration is turned off on Wordpress by default.  If you would like to allow users to register for your website, you can do so in the Settings->General section of the dashboard, by clicking the box next to "Anyone Can Register".  You will also want to set the default user role at this time.  [Learn more about this here](http://www.wpbeginner.com/beginners-guide/how-to-allow-user-registration-on-your-wordpress-site/)

###Creating New Users

Since user registration is turned off, anyone new users you would like to be able to access your website need to be created manually.  You can do this by going to the Users->Add New section of the dashboard.  [Read more about this here](http://www.wpbeginner.com/beginners-guide/how-to-add-new-users-and-authors-to-your-wordpress-blog/)



