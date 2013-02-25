---
layout: post
title: "Release 2.3 is out"
date: 2013-02-24 17:14
comments: true
categories: 
---
Release 2.3 is out. This is our biggest release so far. The release contains [5 bug fixes and 9 enhancements](https://github.com/crawljax/crawljax/issues?milestone=3&state=closed). The code base has been split up in modules, the API has changed a little and the crawl overview plugin has been completely renovated.

### New Features

* The crawler now by default follows all found `href` elements. Even if the elements are not visible because they only show up when the crawler hovers on another element. This option can be disabled in the `CrawlSpecification`.
* You can now specify  that the crawler doesn't click any children of a certain element in the `CrawlSpecification`.
* The crawler doesn't get stuck anymore when a browser still has a dialog window open like a download dialog.
* The project has been split up in three versions: *core*, *cli* and *examples*. The Command Line Interface (CLI) module is the simplest way to run Crawljax. You can just download the zip and run Crawljax on any site. The *core* module can be included in any project using Maven to extend Crawljax or to run in programmatically. The *examples* module is the easiest way to try out several configurations of Crawljax in your favorite IDE. Checkout our updated documentation for more details. 

### New overview plug-in

Screenshot, demo, example. Epic.

### API Changes
We have made some changes to the Crawl configurations.

* The `CrawlSpecification` now also accepts `URL`'s.
* All time parameters now make use of the `TimeUnit` class. 