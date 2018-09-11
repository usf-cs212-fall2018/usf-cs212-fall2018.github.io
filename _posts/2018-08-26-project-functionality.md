---
title: Project Functionality
navbar: Guides
layout: default
categories: project
label: Updated 9/10
---

Each project grade is split into two components: functionality and design. This guide details the process for verifying and grading the functionality of your projects. You should only go through this process if:

  1. You are [passing all of the project tests locally]({% post_url 2018-08-25-project-testing %}#testing-locally) on your system.

  2. You are [passing all of the project tests remotely]({% post_url 2018-08-25-project-testing %}#testing-locally) on your system.

      <p><article class="message is-warning">
        <div class="message-body">
          <i class="fas fa-exclamation-triangle"></i>&nbsp;You may want to consider making a new release with a cleaned-up version of your code before requesting verification! This means making sure your code is properly formatted and has Javadoc comments for all classes, members, and methods. You will not pass code review until your code is formatted and commented, and code review is much faster when your code is readable.
        </div>
      </article></p>

  3. For projects 2 through 4, you have already had the functionality of the previous project verified and your grade is updated in Canvas.

  4. You do not already have an open verification request.

Functionality must be verified sequentially and you may only have one open request at any time. Therefore, you cannot pass the functionality of project 2 until you have the functionality of project 1 verified. You cannot pass the functionality of project 3 until you have the functionality of project 1 verified. And finally, you cannot pass the functionality of project 4 until you have the functionality of project 3 verified.

{% include section.html level="h2" name="Project Verification" %}

If all of the above is true, then you can request verification from a teacher assistant. The steps are:

  1. In Github, [create an issue](https://guides.github.com/features/issues/) in your project repository.

      <p><article class="message is-warning">
        <div class="message-body">
          <i class="fas fa-exclamation-triangle"></i>&nbsp;Issues can be edited but not deleted. Please be careful to follow these steps exactly!
        </div>
      </article></p>

  2. Enter the title `Project v#` where `v#` is the release number to verify. This is the only way we can tell which release you want verified and code reviewed.

  3. If this is the first time you have passed the tests remotely, ask for your functionality grade in Canvas to be updated in the issue description.

  4. On the side under "Assignees", add the teacher assistant Olivia Kumar (`oliviakumar` is her username). She will process your verification requests.

  5. On the side under "Milestone", add the issue to the `Project #` milestone where `#` is the project number (1, 2, 3, or 4). Create the milestone if necessary.

  6. Click the "Submit new issue" and wait for a response from the teacher assistant. You can see a [sample issue](https://github.com/usf-cs212-fall2018/template-project/issues/1) on the project template repository.

The teacher assistant will respond with instructions on how to sign up for code review if your project passes the tests remotely and created the issue properly.

If you are signing up for a code review, be wary of making many changes in your `master` branch before your code review appointment. The instructor will review the version associated with the passing release, so if you continue working on your code you may have a difficult time merging the changes afterward.

{% include section.html level="h2" name="Functionality Grading" %}

Your functionality grade will be based on the **date you created the issue** that passed verification. If the issue date is before the checkpoint deadline, you will earn 100% on the project functionality. If the issue date is after the checkpoint deadline, your grade will be deducted 10% (up to a maximum of 30%) per week.

The functionality deadline schedule is below (assume all deadlines are at 11:59pm):

| Grade | Project 1  | Project 2  | Project 3  | Project 4  | Description   |
|------:|:----------:|:----------:|:----------:|:----------:|:--------------|
|  110% | N/A        | &le; 10/02 | &le; 10/23 | &le; 11/13 | Extra Credit<sup><em>*See Below</em></sup> |
|  100% | &le; 09/18 | &le; 10/09 | &le; 10/30 | &le; 11/20 | Checkpoint |
|   90% | &le; 09/25 | &le; 10/16 | &le; 11/06 | &le; 11/27 | 1 Week Late |
|   80% | &le; 10/02 | &le; 10/23 | &le; 11/13 | &le; 12/04 | 2 Weeks Late |
|   70% | &le; 10/09 | &le; 10/30 | &le; 11/20 | &gt; 12/04 | 3 Weeks Late |
|    0% | &gt; 11/01 | &gt; 11/01 | &gt; 12/04 |            | Project Cutoff |

Keep in mind the [project pass requirements]({{ "/syllabus.html" | relative_url }}#pass-requirements) for projects 1 and 2. All of your grades default to 0% if you do not pass the functionality of projects 1 and 2 by the project cutoff deadline on Thursday November 11, 2018. You must also pass the functionality of project 3 by the last day of class on Tuesday December 4, 2018.

**The deadline extra credit can only be used to make up for late submissions in earlier projects.** For example, if you submitted project 1 late, you can regain some of those points by submitting project 2 early. There may be other extra credit opportunities associated with each project that are not subject to that constraint.

{% include section.html level="h2" name="Working Ahead" %}

Worried about the deadline schedule and how slow code reviews progress?

You *can* work ahead on the functionality of the next project after passing verification, just **not in the `master` branch** used for the current project and code reviews. If you want to work ahead, create a separate branch for the next project. You can even create releases from that branch, allowing you to pass functionality for the next project while still undergoing code review for the current project.

However, you have to be comfortable with branching and merging in `git` if you choose this route. It is very easy to cause merge conflicts that can be difficult to resolve, and we can only provide so much assistance.

You **cannot** work two projects ahead than the project currently under code review.

<p><article class="message is-danger">
  <div class="message-body">
    <i class="fas fa-exclamation-triangle"></i>&nbsp;If your <code>master</code> branch includes functionality for the next project, you'll be asked to remove it and reschedule the code review. This could cost you a week, and undo your efforts to work ahead!
  </div>
</article></p>
