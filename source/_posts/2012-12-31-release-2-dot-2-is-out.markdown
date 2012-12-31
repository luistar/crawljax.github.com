---
layout: post
title: "Release 2.2 is out"
date: 2012-12-31 12:43
comments: true
categories: [ releases ]
---
Release 2.2 contains bug fixes and several improvements:

* Switched to a new Logging framework for better log output. ([Issue #73](https://github.com/crawljax/crawljax/pull/73))
* The StateFlowGraph and other elements are now serializable ([Issue #52](https://github.com/crawljax/crawljax/issues/52), [Issue #53](https://github.com/crawljax/crawljax/issues/53), [Issue #77](https://github.com/crawljax/crawljax/issues/77)) 
* More HTML elements are predefined for crawling. This can lead to a higher crawl coverage.([Issue #72](https://github.com/crawljax/crawljax/issues/72)) 

You can find all closed issues [here](https://github.com/crawljax/crawljax/issues?milestone=2&state=closed) or look at the full diff [here](https://github.com/crawljax/crawljax/compare/crawljax-2.1...crawljax-2.2).

Crawljax 2.2 is avaiable through [Maven central](http://search.maven.org/#browse%7C462108398) and our [download section](/downloads).