---
title: Project Testing
navbar: Guides
layout: default
categories: project
---

You must use the [JUnit 5](https://junit.org/junit5/) tests provided with the [project-tests](https://github.com/usf-cs212-fall2018/project-tests) repository to determine if your project is meeting the required functionality. The suite of tests for each project are given by the `Project#Test.java` files in the [src](https://github.com/usf-cs212-fall2018/project-tests/tree/master/src) subdirectory. For example, the tests for [Project 1]({% post_url 2018-08-27-project-1 %}) are provided by the [Project1Test.java](https://github.com/usf-cs212-fall2018/project-tests/blob/master/src/Project1Test.java) file.

Your code must pass these tests (using the [remote testing](#testing-remotely) procedure below) both to earn credit for the functionality portion of the project grade, and before every subsequent code review required after that point. For example, you will earn a grade for [Project 1a (Functionality)](https://usfca.instructure.com/courses/1579367/assignments/6779382) for the first code release that passes the tests. However, to earn a grade for [Project 1b (Design)](https://usfca.instructure.com/courses/1579367/assignments/6779384), your code will need to pass the tests again before every code review until you pass the design requirements.

Each project also includes **additional** tests on top of the previous tests. For example, the project 3 tests still require that your code passes the project 1 and project 2 tests.

The provided tests only examine the final output of your code---you are still responsible for writing your own test code while developing and debugging your project.

<article class="message is-warning">
  <div class="message-body">
    <i class="fas fa-exclamation-triangle"></i>&nbsp;You should place your test code in your own project repository, not the <a href="https://github.com/usf-cs212-fall2018/project-tests">project-tests</a> repository. <strong>You do not have access to commit and push to the test repository!</strong>
  </div>
</article>

{% include section.html level="h2" name="Run Configurations" %}

It is possible to run `Driver.java` directly with your own command-line arguments using "[Run Configurations](http://help.eclipse.org/photon/topic/org.eclipse.jdt.doc.user/tasks/tasks-java-local-configuration.htm)" in Eclipse. This is useful for your own debugging, and testing out individual tests.

The tricky part is getting the paths right, since the test files are not in the same project as your code. On a Mac or Linux system, assuming your project repository and the [project-tests](https://github.com/usf-cs212-fall2018/project-tests) repository are in the same parent folder, you can add the following command-line arguments:

```
-path "../project-tests/text/simple/hello.txt" -index hello.json
```

{% include screenshot.html image="project-eclipse-run-configuration.png" zoom="50%" %}

The quotation marks are required if there is a space in the path, otherwise they can be omitted. This should generate a file `hello.json` in the Eclipse project for your project repository (not the [project-tests](https://github.com/usf-cs212-fall2018/project-tests) repository). Right-click and select "Refresh" if you do not see the file at first.

On a Windows system, the path separators `/` should be `\` instead.

{% include section.html level="h2" name="Testing Locally" %}

You should make sure you are passing the [JUnit 5](https://junit.org/junit5/) tests locally before testing your code remotely. I also recommend you run only one test at a time at first, then groups of tests, and then the entire suite of tests only after you know you are passing each group individually. You can do this by right-clicking a test name or test class, and selecting "Run As" &raquo; "JUnit Test" from the menu. You can also manually configure the run configuration as well:

{% include screenshot.html image="project-eclipse-junit-run-configuration.png" zoom="50%" %}

The output of each test provides additional information useful for debugging. For example:

{% include screenshot.html image="project-eclipse-junit-output.png" zoom="50%" %}

The full output, which can be copied to the console for easy copying/pasting using the <img src="{{ "eclipse-copy-junit-output-to-console.png" | prepend: "/images/" | relative_url }}" style="height: 16px; vertical-align: middle;"> button, includes the following text:

```
Actual File:
    out/index-text-simple-hello.json
Expected File:
    expected/index-text/index-text-simple-hello.json
Arguments:
    -path text/simple/hello.txt -index out/index-text-simple-hello.json
Message:
    Difference detected on line: 2.
```

This gives the actual arguments passed to `Driver` by the test, the actual and expected files being compared, and where the first difference was detected. You can use the [Compare Editor](http://help.eclipse.org/photon/topic/org.eclipse.platform.doc.user/reference/ref-25.htm?cp=0_4_4_1_2) in Eclipse to compare the files side-by-side for debugging, or use the [Run Configurations](#-run-configurations) in Eclipse to enter the same arguments manually. Just keep in mind the paths need to be updated slightly since your `Driver` class is in a different folder than the project test code. So, for the above example, the appropriate command-line arguments to enter into the `Driver` run configuration would be:

```
-path ../project-tests/text/simple/hello.txt -index out/index-text-simple-hello.json
```

Then, the `index-text-simple-hello.json` will (hopefully) show up in the `out` subdirectory of your project repository.

<article class="message is-warning">
  <div class="message-body">
    <i class="fas fa-exclamation-triangle"></i>&nbsp;To save space, the tests automatically delete your output files if they match the expected output. Only output files for failing tests will be kept.
  </div>
</article>

{% include section.html level="h2" name="Testing Remotely" %}

Pending

{% include section.html level="h2" name="Video Walkthrough" %}

<p>This video walkthrough will illustrate this entire process on a Mac OSX system.</p>

<div>
  <iframe width="560" height="315" src="https://www.youtube.com/embed/n3159AmZV2M?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
  <br/>
  <small><a href="https://youtu.be/n3159AmZV2M"><i class="fab fa-youtube"></i> https://youtu.be/n3159AmZV2M</a></small>
</div>

<p>Please note this video was recorded for a previous semester. The Github organization and teacher assistants have changed since then.</p>
