---
layout: default
navbar: Guides
title: Importing Eclipse Projects from Github
categories: general
---

**VIDEO AND SCREENSHOTS PENDING**

Follow these steps to import an Eclipse project from your Github repository. These steps assume you have already followed the <a href="{% post_url 2018-08-20-configuring-ssh-keys %}">Configuring SSH Keys</a> and <a href="{% post_url 2018-08-21-java-and-eclipse-setup %}">Java and Eclipse Setup</a> guides.

{% include section.html level="h2" name="Import Projects into Eclipse" %}

  1. Copy the SSH link to clone your repository in Github.

      {% include screenshot.html image="github-clone-or-download.png" zoom="50%" %}

  2. In Eclipse, select "Import..." from the "File" menu. Select "Projects from Git" in the dialog window and click the "Next" button.

  3. Select "Clone URI" and click the "Next" button. Copy the SSH link into the "URI" field.

    *The remaining fields will auto-populate based on your URI!* You do not need to change anything else. Keep in mind your values may differ from the image below.

  4. Make sure the "master" branch is selected and click the "Next" button.

  5. Modify the "Directory" field if you want (optional).

  6. Make sure "Import existing Eclipse projects" is selected and click the "Next" button.

  7. Make sure the projects you wish to import is selected and click the "Finish" button.

  8. Double-check the project setup and try running the code. If you see errors, use the troubleshooting steps below. Otherwise, your project is ready!

{% include section.html level="h2" name="Troubleshooting" %}

  1. If you notice several errors (similar to below), it is likely something isn't quite right with the build path setup for your Eclipse project. This happens when your setup is different from expected (either you have a different version of Eclipse, Java, or named your third-party libraries differently).

  2. To fix this, right-click your project folder and select "Build Path" and "Configure Build Path" from the menus. On the following window, click the "Libraries" tab. Remove everything that has a red "x" icon or is listed as "unbound" in the label.

  3. Now, we have to re-add the necessary libraries. Click the "Add Library..." button and follow these steps:

      - Select "JRE System Library" to re-add Java 10 (if necessary). I recommend you select "Workspace default JRE" unless the default is NOT Java 10.

      - Select "JUnit" to re-add JUnit 5 (if necessary). Make sure "JUnit 5" is selected in the dropdown, **not** JUnit 4.

      - Select "User Library" to add a third-party user library (if necessary). This could be log4j2, StringTemplate, Apache Commons, etc. depending on the assignment. See [Guides: Adding User Libraries in Eclipse](#) for more details on how to set those up.

  4. Click "Apply" and "OK" when done. You should see all of the scary red icons disappear. If not, ask on Piazza or during office hours for help!
