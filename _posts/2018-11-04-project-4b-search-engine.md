---
title: Project 4b Search Engine
navbar: Guides
layout: default
categories: writeups
label: New!
---

For this project, you will extend your [previous project]({% post_url 2018-10-08-project-3 %}) to create a fully functional search engine. This project is split into two main components: (1) a [multithreaded web crawler]({% post_url 2018-11-04-project-4a-web-crawler %}) using a work queue to build the index from a seed URL, and (2) a [search engine web interface]({% post_url 2018-11-04-project-4b-search-engine %}) using [embedded Jetty](https://www.eclipse.org/jetty/) and servlets to search that index.

**This writeup is for the search engine functionality only.** See the general [Project 4 Writeup]({% post_url 2018-11-04-project-4 %}) for more details.

{% include section.html level="h2" name="Functionality" %}

Pending

{% include section.html level="h3" name="Search Engine Core Functionality" %}

Pending

{% include section.html level="h3" name="Search Engine Extra Functionality" %}

Pending

{% include section.html level="h3" name="Input" %}

Your main method must be placed in a class named `Driver`. The `Driver` class should accept the following **additional** command-line arguments:

  - Pending

The command-line flag/value pairs may be provided in any order, and the order provided is not the same as the order you should perform the operations (i.e. always build the index before performing search, even if the flags are provided in the other order).

Your code should support all of the command-line arguments from the [previous project]({% post_url 2018-10-08-project-3 %}) as well.

{% include section.html level="h3" name="Output" %}

The JSON output of your inverted index and search results should be the same from the [previous project]({% post_url 2018-10-08-project-3 %}). As before, you should **only generate output files if the necessary flags are provided**.

Pending

{% include section.html level="h3" name="Testing" %}

Pending
