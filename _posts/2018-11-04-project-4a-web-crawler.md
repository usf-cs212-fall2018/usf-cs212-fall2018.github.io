---
title: Project 4a Web Crawler
navbar: Guides
layout: default
categories: writeups
label: New!
---

For this project, you will extend your [previous project]({% post_url 2018-10-08-project-3 %}) to create a fully functional search engine. This project is split into two main components: (1) a [multithreaded web crawler]({% post_url 2018-11-04-project-4a-web-crawler %}) using a work queue to build the index from a seed URL, and (2) a [search engine web interface]({% post_url 2018-11-04-project-4b-search-engine %}) using [embedded Jetty](https://www.eclipse.org/jetty/) and servlets to search that index.

**This writeup is for the web crawler functionality only.** See the general [Project 4 Writeup]({% post_url 2018-11-04-project-4 %}) for more details.

{% include section.html level="h2" name="Functionality" %}

The core functionality of the web crawler must satisfy the following requirements:

  - Maintain the functionality of the [previous project]({% post_url 2018-10-08-project-3 %}).

  - Process additional command-line parameters to [PENDING]. See the [Input](#input) section for specifics.

  - Support the same JSON output capability as before. See the [Output](#output) section for specifics.

  - Pending

The functionality of your project will be evaluated with various JUnit tests. Please see the [Testing](#testing) section for specifics.

{% include section.html level="h2" name="Input" %}

Your main method must be placed in a class named `Driver`. The `Driver` class should accept the following **additional** command-line arguments:

  - Pending

The command-line flag/value pairs may be provided in any order, and the order provided is not the same as the order you should perform the operations (i.e. always build the index before performing search, even if the flags are provided in the other order).

Your code should support all of the command-line arguments from the [previous project]({% post_url 2018-10-08-project-3 %}) as well.

{% include section.html level="h2" name="Output" %}

The JSON output of your inverted index and search results should be the same from the [previous project]({% post_url 2018-10-08-project-3 %}). As before, you should **only generate output files if the necessary flags are provided**.

Pending

{% include section.html level="h2" name="Testing" %}

Pending

{% include section.html level="h2" name="Hints" %}

It is important to develop the project iteratively. One possible breakdown of tasks are:

  - Pending

The important part will be to test your code as you go. The JUnit tests provided only test the entire project as a whole, not the individual parts. You are responsible for testing the individual parts themselves.

<article class="message is-info">
  <div class="message-body">
    <i class="fas fa-info-circle"></i>&nbsp;These hints may or may not be useful depending on your approach. Do not be overly concerned if you do not find these hints helpful for your approach for this project.
  </div>
</article>
