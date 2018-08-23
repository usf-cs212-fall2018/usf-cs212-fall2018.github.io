---
layout: default
navbar: Guides
title: Homework Testing
categories: homework
---

Every homework comes with a `test` directory with JUnit 5 test code. You must pass all of these tests using the `homework` script on the lab computers as part of the [homework requirements]({% post_url 2018-08-21-homework-requirements %}).

{% include section.html level="h2" name="Local Testing" %}

You should try passing the tests locally before you try passing them remotely. Before you can do that, you need to follow the [homework setup]({% post_url 2018-08-19-homework-setup %}) guide to setup the your repository using Github classroom and then import that repository as a Java Project in Eclipse.

To run the JUnit tests provided with the homework template, follow these steps:

  1. Open up the `test` subfolder in the Eclipse project.

  2. Open up the class containing the same name as the homework assignment plus the suffix `Test` at the end. For example, for the `ArgumentMap` homework assignment, `ArgumentMapTest` is the associated test class.

  3. From the "Run" menu, select "Run As" &raquo; "JUnit Test" from the menu. If prompted which tests to run, select the one with the same name as the class. For example, for the `ArgumentMap` homework assignment, `ArgumentMapTest` is the associated test class. This will be the set of tests run by the `homework` script on the lab computers.

      *Note: You can run just the nested tests or one test at a time if you want. This can help you focus on a small number of tests at a time as you develop the code. To do this, right-click the test method or nested test class, and select "Run As" &raquo; "JUnit Test" from the popup menu.*

  4. Running the tests should open the "JUnit" view. You can use that view to see which tests you are passing and which you are not. See the [Eclipse User Guide](http://help.eclipse.org/photon/topic/org.eclipse.jdt.doc.user/reference/views/ref-view-junit.htm) for what each of the buttons mean in this view.

  5. After making changes to your code, you can re-run the tests by following the same steps or clicking the <img alt="Rerun Test" src="http://help.eclipse.org/photon/topic/org.eclipse.jdt.doc.user/images/org.eclipse.jdt.junit/elcl16/relaunch.png"> Rerun Test button.

It is important you only try to pass one test at a time, because the changes you make may affect other tests. You should `git commit` your changes every time you start passing a new test at a minimum, and `git push` your changes at the end of every coding session.

{% include section.html level="h2" name="Remote Testing" %}

Pending.
