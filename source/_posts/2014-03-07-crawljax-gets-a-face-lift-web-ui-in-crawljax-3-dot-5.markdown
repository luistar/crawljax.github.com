---
layout: post
title: "Crawljax gets a face lift. Web UI in Crawljax 3.5"
date: 2014-03-07 11:36
comments: true
categories: [ features ]
---
Latest feature that will be available with Crawljax 3.5 is a Web front end for Crawljax. It supports all the major functionality of crawljax such as adding/editing crawl configurations, installing plugins, viewing crawl logs in real time and displaying plugin output. This is implemented using [the common java web application stack](http://blog.palominolabs.com/2011/08/15/a-simple-java-web-stack-with-guice-jetty-jersey-and-jackson/) and [ember.js](http://emberjs.com/) MVC framework. Kudos to the developers, [@jeremyhewett](https://github.com/jeremyhewett) and [@ryansolid](https://github.com/ryansolid).
To run it, simply unzip the web distribution archive and run the command `java -jar crawljax-web-3.5-SNAPSHOT.jar`. You can customize the port and output directory using `-p` and `-o` arguments. Here are some screen-shots of the web interface in action. More usage tutorials will follow.

{% img /images/webui1.jpg  "Crawljax Web UI Home" %}
Crawljax Web UI Home - You can start by adding a 'New Configuration' as shown

{% img /images/webui2.jpg  "Edit Configuration Page" %}
'Edit Configuration' Page

{% img /images/webui3.jpg  "Add Plugin Page" %}
'Add Plugin' Page

{% img /images/webui4.jpg  "Crawl Status Log" %}
Crawl status log with real-time updates

{% img /images/webui5.jpg  "Crawl Overview Output" %}
Output of the Crawl Overview plugin