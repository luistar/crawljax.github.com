---
layout: post
title: "Crawljax gets a face lift. Web UI in 3.5"
date: 2014-03-07 11:36
comments: true
categories: [ features ]
---
We just released Crawljax 3.5 and with it comes a web interface for Crawljax. It supports all the major functionality of crawljax such as adding/editing crawl configurations, installing plugins, viewing crawl logs in real time and displaying plugin output. Kudos to the developers, [@jeremyhewett](https://github.com/jeremyhewett) and [@ryansolid](https://github.com/ryansolid).
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

Also in release 3.5:

* Deprecated the malfunctioning DomChangeNotifierPlugin. Introuced StateVertexFactoryl. [#347](https://github.com/crawljax/crawljax/issues/347)
* Better PhantomJS support. Tests run on PhantomJS by default.
* Switched from URL's to URI's for better performance. [#322](https://github.com/crawljax/crawljax/issues/322)

[You can download the release from our GitHub project site.](https://github.com/crawljax/crawljax/releases)