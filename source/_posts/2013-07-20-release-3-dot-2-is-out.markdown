---
layout: post
title: "Release 3.2 is out"
date: 2013-07-20 13:35
comments: true
categories: [ releases ]
---
Release 3.2 is out. It's a small update with one API change and several bug fixes: 

### Metrics [#314](https://github.com/crawljax/crawljax/issues/314)
Implements statistics for Crawljax using [Codehale's metrics](http://metrics.codahale.com/manual/core/#man-core-reporters-slf4j). 

We have pre-loaded some metrics in core and you can extend the functionality yourself. We have created [an example](https://github.com/crawljax/crawljax/blob/master/examples/src/main/java/com/crawljax/examples/MetricPluginExample.java) that shows how you can print the already inserted metrics and add one of your own. 

The default counters that are included right now are:

- Crawler lost count
- Unfired actions count
- Invocations per plugin count.

The output of the example is the standard counters plus a histogram of the DOM-size: 
```
[main] INFO  - type=COUNTER, name=com.crawljax.crawlevents.crawler_lost, count=0
[main] INFO  - type=COUNTER, name=com.crawljax.crawlevents.unfired_actions, count=0
[main] INFO  - type=COUNTER, name=com.crawljax.crawlplugins.DomChangeNotifierPlugin.invocations, count=19
[main] INFO  - type=COUNTER, name=com.crawljax.crawlplugins.OnBrowserCreatedPlugin.invocations, count=1
[main] INFO  - type=COUNTER, name=com.crawljax.crawlplugins.OnFireEventFailedPlugin.invocations, count=0
[main] INFO  - type=COUNTER, name=com.crawljax.crawlplugins.OnInvariantViolationPlugin.invocations, count=0
[main] INFO  - type=COUNTER, name=com.crawljax.crawlplugins.OnNewStatePlugin.invocations, count=17
[main] INFO  - type=COUNTER, name=com.crawljax.crawlplugins.OnRevisitStatePlugin.invocations, count=1
[main] INFO  - type=COUNTER, name=com.crawljax.crawlplugins.OnUrlLoadPlugin.invocations, count=15
[main] INFO  - type=COUNTER, name=com.crawljax.crawlplugins.PostCrawlingPlugin.invocations, count=1
[main] INFO  - type=COUNTER, name=com.crawljax.crawlplugins.PreCrawlingPlugin.invocations, count=0
[main] INFO  - type=COUNTER, name=com.crawljax.crawlplugins.PreStateCrawlingPlugin.invocations, count=15
[main] INFO  - type=HISTOGRAM, name=com.crawljax.examples.MetricPluginExample.domsize, count=17, min=2, max=5, mean=3.4705882352941178, stddev=0.7998161553463027, median=4.0, p75=4.0, p95=5.0, p98=5.0, p99=5.0, p999=5.0
```
 

### Further more:

* Crawl configuration now has an option to set the output folder [#316](https://github.com/crawljax/crawljax/issues/316). This is useful for plugins that require an output folder.
* `Browser.getDom()` is deprecated. You can now choose between `getStrippedDom` and `getUnstrippedDom()` [#305](https://github.com/crawljax/crawljax/issues/305).
* __API Change__: Proxy plugin has been removed. It didn't work in 3.1 and 3.0 and is now replaced by the `PreCrawlPlugin`. [#286](https://github.com/crawljax/crawljax/issues/286)