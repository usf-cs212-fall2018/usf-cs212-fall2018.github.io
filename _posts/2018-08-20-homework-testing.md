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

Once you are passing all of the tests locally, it is time to test your homework remotely. There are two primary steps to this process: [committing and pushing](http://wiki.eclipse.org/EGit/User_Guide#Committing_Changes) your changes to Github, and then logging into a CS Lab computer and running the `homework` script.

After you have updated your remote Github repository, [login to a CS lab computer]({% post_url 2018-08-18-using-cs-lab-computers %}) and run the following command from a terminal:

```
/home/public/cs212/homework GitUser HomeworkName
```

Replace `GitUser` with your GitHub username and `HomeworkName` with the name of the homework you want to test. For example:

```
/home/public/cs212/homework sjengle ArgumentMap
```

This script will clone your remote Github repository, fetch fresh test code (in case you changed anything) from the template repository, compile the Java code, and then run all of the JUnit tests and report how many tests passed or failed. This script is used for grading homework.

If you want the detailed output of running the tests, you can add the `-r` flag to the command. This will generate a file in your home directory named `cs212-GitUser-HomeworkName.txt` when any tests fail. You can [download the file](https://www.cs.usfca.edu/support.html#ftp) to your own system if you do not want to try and read the file on the lab computers.

{% include section.html level="h2" name="Bonus: Aliases" %}

You will be doing this quite a bit, so I recommend making an alias. To do this, open the `~/.bashrc` file on a lab computer and add the following line:

```
alias hw="/home/public/cs212/homework GitUser"
```

Replace `GitUser` with your GitHub username. Run `source ~/.bashrc` for the command to take affect.

If you are uncomfortable with editing a file via the command line, you can run this command on a lab computer to do it for you:

```
echo 'alias hw="/home/public/cs212/homework GitUser"' >> ~/.bashrc; source ~/.bashrc
```

Then, you can test homework using the following command on the lab computers:

```
hw HomeworkName
```

Replace `HomeworkName` with the name of the homework you want to test. The alias will still work with the `-r` flag as well!

You only need to set the alias once. Every time you login again, the `.bashrc` file will re-add that alias for you.

{% include section.html level="h2" name="Video Walkthrough" %}

<p>This video walkthrough will illustrate this entire process on a Mac OSX system.</p>

<div>
  <iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/QSC1gK6TtSk?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
  <br/>
  <small><a href="https://youtu.be/QSC1gK6TtSk"><i class="fab fa-youtube"></i> https://youtu.be/QSC1gK6TtSk</a></small>
</div>
