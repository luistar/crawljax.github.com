---
layout: post
title: "Release 3.0 is out"
date: 2013-03-06 17:14
comments: true
categories: [ releases ]
---
Release 3.0 is out. This is our biggest release so far. The release contains [several bug fixes and loads of enhancements](https://github.com/crawljax/crawljax/issues?milestone=3&state=closed). The code base has been split up in modules, the API has changed a little and the crawl overview plugin has been completely renovated.

### New overview plug-in

Most notable in the new release is the new overview plugin. The plugin shows an interactive state graph of the crawl and some statistics. Make sure you check out [a demo](http://crawls.crawljax.com) or try one of our [examples](https://github.com/crawljax/crawljax/tree/master/examples) yourself.

{% img /images/new-overview-plugin.png  "The new overview plugin" %}

### New Features

* Crawljax is now configured using a configuration builder. You can start of you configuration using `CrawljaxConfiguration.builderFor("http://your.website.com");`.
* The project has been split up in three versions: *core*, *cli* and *examples*. The Command Line Interface (CLI) module is the simplest way to run Crawljax. You can just download the zip and run Crawljax on any site. The *core* module can be included in any project using Maven to extend Crawljax or to run in programmatically. The *examples* module is the easiest way to try out several configurations of Crawljax in your favorite IDE. Checkout our updated documentation for more details. 
* You can configure the crawler to crawl all found `href` attributes. Even if the elements are not visible because they only show up when the crawler hovers on another element.
* You can now specify  that the crawler doesn't click any children of a certain element using a short syntax like `dontClickChildrenOf("LI").withId("dontClickMe");`

You can [view all closed issues](https://github.com/crawljax/crawljax/issues?milestone=3&page=1&state=closed) or [the full diff](https://github.com/crawljax/crawljax/compare/crawljax-2.2...crawljax-3.0) on Github.