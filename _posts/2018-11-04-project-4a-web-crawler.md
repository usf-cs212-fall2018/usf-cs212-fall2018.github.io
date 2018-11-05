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

  - Add support to build the inverted index from a seed URL instead of a directory using a web crawler. The web crawler must be multithreaded using a work queue such that each URL that must be crawled is handled by a single worker thread. See the [Input](#input) section for specifics.

  - To avoid a infinite crawl, the web crawler should parse up to a fixed limit of unique URLs as specified by a command-line argument. If the argument is missing, the crawler should parse up to a maximum of 50 links by default (including the seed URL). See the [Input](#input) section for specifics.

  - The web crawler must use sockets to download webpages over HTTP or HTTPS when crawling. It is acceptable to read the entire web page into memory at once. Do *not* add HTML from web pages unless the HTTP response status code was `200 OK` and the content type is HTML.

      If the HTTP response status was a redirect, follow the redirect up to a limit of 3 redirects (to avoid an infinite redirect loop). The content at the end of this process will be assigned to the original URL. For example, the URL [~cs212/redirect/one](https://www.cs.usfca.edu/~cs212/redirect/one) eventually redirects to [~cs212/simple/hello.html](https://www.cs.usfca.edu/~cs212/simple/hello.html). However, the web crawler will associate the content of [~cs212/simple/hello.html](https://www.cs.usfca.edu/~cs212/simple/hello.html) with the original link [~cs212/redirect/one](https://www.cs.usfca.edu/~cs212/redirect/one) instead.

      You may NOT use the URL class to download the HTML, but you may use this class to parse and clean URLs (see the Relative URLs and Unique URLs sections below). Instead, see the [HttpsFetcher](https://github.com/usf-cs212-fall2018/lectures/blob/master/Sockets/src/HttpsFetcher.java) lecture code for a starting point using sockets.

  - Convert all processed URLs to a consistent absolute form (remove fragments, convert relative URLs to absolute URLs, etc.) and do not process the same URL more than once. For example, if you already processed <https://www.cs.usfca.edu/~cs212/gutenberg/1228.htm> and encounter <https://www.cs.usfca.edu/~cs212/gutenberg/1228.htm#link2H_4_0006>, you should not re-process this URL and it should not count towards the total.

      See the [LinkParser](https://github.com/usf-cs212-fall2018/template-linkparser) homework assignment for more specifics.

  - Use a breadth-first approach to crawling URLs. For example, suppose the seed URL has 49 or more URLs on the page. The first 49 URLs on the seed page (plus the seed URL itself) should be a part of the crawl.

      If you use the work queue correctly, then crawling will automatically be breadth-first.

  - For each cleaned, unique URL that must be crawled (i.e. haven't hit the maximum number of links and this is a unique link):

    - Each worker thread should be responsible for parsing a single link.

    - Parse all of the URLs on the page, and add to the queue of URLs to process as appropriate. (You must do this before you remove the HTML tags.)

    - Remove any style and script segments and remove all of the HTML tags and entities. See the [HTMLCleaner](https://github.com/usf-cs212-fall2018/template-htmlcleaner) homework assignment for more specifics.

    - Clean, parse, and stem the resulting text to populate the inverted index in the same way plain text files were handled in previous projects.  

  - Support the same JSON output capability as before. See the [Output](#output) section for specifics.

The functionality of your project will be evaluated with various JUnit tests. Please see the [Testing](#testing) section for specifics.

{% include section.html level="h2" name="Input" %}

Your main method must be placed in a class named `Driver`. The `Driver` class should accept the following **additional** command-line arguments:

  - `-url seed` where `-url` indicates the next argument `seed` is the seed URL your web crawler should initially crawl to build the inverted index.

      If the `-url` flag is provided, your code should **enable multithreading** with the default number of worker threads even if the `-threads` flag is not provided.

  - `-limit total` where `-limit` is an *optional* flag that indicates the next argument `total` is the total number of URLs to crawl (including the seed URL) when building the index. Use `50` as the default value if this flag is not properly provided.

The command-line flag/value pairs may be provided in any order, and the order provided is not the same as the order you should perform the operations (i.e. always build the index before performing search, even if the flags are provided in the other order).

Your code should support all of the command-line arguments from the [previous project]({% post_url 2018-10-08-project-3 %}) as well.

{% include section.html level="h2" name="Output" %}

The JSON output of your inverted index and search results should be the same from the [previous project]({% post_url 2018-10-08-project-3 %}). As before, you should **only generate output files if the necessary flags are provided**.

{% include section.html level="h2" name="Testing" %}

You must pass 100% of the tests in the [`Project4Test.java`](https://github.com/usf-cs212-fall2018/project-tests/blob/master/src/Project4Test.java) group of JUnit tests to satisfy the web crawler functionality requirements. See the [project testing]({% post_url 2018-08-25-project-testing %}) guide for details.

<article class="message is-info">
  <div class="message-body">
    <i class="fas fa-info-circle"></i>&nbsp;These tests are only for the web crawler functionality. The search engine functionality will be verified during the final code review appointment, not via automated system tests.
  </div>
</article>

{% include section.html level="h2" name="Hints" %}

It is important to develop the project iteratively. Some hints related to this project are:

  - Use the relevant homework and lecture code, including the [HTMLCleaner](https://github.com/usf-cs212-fall2018/template-htmlcleaner), [LinkParser](https://github.com/usf-cs212-fall2018/template-linkparser), and [HttpsFetcher](https://github.com/usf-cs212-fall2018/lectures/blob/master/Sockets/src/HttpsFetcher.java) classes.

  - Create helper methods to parse the HTTP response status line into a status code, to test whether status codes represent a redirect, and whether the content type of the HTTP response is HTML.

  - Outside of the relevant homework and lecture classes, there is likely only one new class (a web crawler class) required for this project. However, you must be careful to properly multithread and synchronize in this class!

The important part will be to test your code as you go. The JUnit tests provided only test the entire project as a whole, not the individual parts. You are responsible for testing the individual parts themselves.

<article class="message is-info">
  <div class="message-body">
    <i class="fas fa-info-circle"></i>&nbsp;These hints may or may not be useful depending on your approach. Do not be overly concerned if you do not find these hints helpful for your approach for this project.
  </div>
</article>
