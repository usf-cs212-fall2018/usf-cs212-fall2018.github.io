---
title: Final Code Review
navbar: Guides
layout: default
categories: project
label: New!
---

Here are some details regarding how your final project code reviews will be handled.

{% include section.html level="h3" name="Final Code Review Appointments" %}

Instead of a final exam, you will have your final project(s) evaluated in a code review appointment during finals week. This will be your last project code review for the semester. See below for eligibility, how to sign up, and how grading will be handled.

{% include section.html level="h4" name="Appointment Eligibility" %}

<p>The <a href="{{ "syllabus.html" | relative_url }}">syllabus</a> states the following <strong>Pass Requirements</strong> for this course:</p>

<blockquote>
<p>To ensure students are meeting the <a href="https://usf-cs212-fall2018.github.io/syllabus.html#learning-outcomes">learning outcomes</a> for this course, students <strong>must</strong> meet the following minimum requirements to receive a non-failing grade (D- or higher) in this course:</p>

<ul>
  <li><p><strong>Exam Pass Requirement:</strong> Students must receive a C letter grade or higher on at least one exam (including retakes).</p></li>

  <li><p><strong>Project Pass Requirement 1:</strong> Students must pass the functionality requirements for a minimum of 2 projects and the design requirements for at least 1 project by the <a href="https://usf-cs212-fall2018.github.io/syllabus.html#important-dates">project cutoff</a> deadline.</p></li>

  <li><p><strong>Project Pass Requirement 2:</strong> Students must pass the functionality requirements for a minimum of 3 projects and the design requirements for at least 2 projects by the end of the semester.</p></li>
</ul>

<p>Failure to meet 1 or more of the following requirements will result in an <strong>automatic F letter grade</strong> for this course, regardless of what your current letter grade is in Canvas.</p>
</blockquote>

<p>You must be passing both the <strong>Exam Pass Requirement</strong> and <strong>Project Pass Requirement 1</strong> to be eligible for a final code review appointment.</p>

{% include section.html level="h4" name="Appointment Signup" %}

<p>
  <i class="fas fa-fw fa-calendar-alt"></i> Fri Dec 7 &ndash; Thu Dec 13, 2018<br>
  <i class="fas fa-fw fa-clock"></i> 10:30am &ndash; 5:30pm<br>
  <i class="fas fa-fw fa-map-marker-alt"></i> <a href="https://www.usfca.edu/campus-buildings-services/main-campus/harney-science">Harney Science</a> 412B
</p>

Final code reviews are conducted during finals week. Each final code review appointment is 30 minutes each. You may sign up for an appointment on Canvas at:

  - [Final Code Review Signup](https://usfca.instructure.com/calendar2#view_name=agenda&view_start=2018-12-07&find_appointment=course_1579367)

Each eligible student must sign up for exactly 1 final code review appointment. Make sure to sign up early to avoid any conflicts with holiday travel or other final exams. **You must be on-time to your appointment.**

<article class="message is-danger">
  <div class="message-body"><i class="far fa-exclamation-triangle"></i>&nbsp;Treat your appointment like a final exam; if you miss it you do not get another opportunity and receive a 0 for any outstanding project grades.</div>
</article>

{% include section.html level="h3" name="Cutoff Deadlines" %}

Which projects you have graded during your final code review appointment depend on how many projects you have passed before the end of the semester. There are slightly different cutoff deadlines for passing design versus functionality at the end of the semester. See below for details.

{% include section.html level="h4" name="Design Cutoff" %}

The last date you can have a normal code review appointment is:

> **Wednesday, December 5, 2018**

If you have an issue created on Github for project verification by <strong class="has-text-danger">11:59pm on Tuesday, December 4, 2018</strong> and the associated release passes the tests, I will guarantee you an appointment on Wednesday. However, it may be in the evening. Please plan accordingly.

For fairness, the design of any outstanding projects after this point will be evaluated in your final code review appointment. If you submit a request for code review *after* this point, it will not be graded until your final code review appointment.

{% include section.html level="h4" name="Functionality Cutoff" %}

The last day to have project functionality verified before your final code review appointment is:

> **Thursday, December 6, 2018**

Specifically, you must have a release that passes the functionality tests and an issue *properly* created on Github asking for verification by 11:59pm on this date. (The issue does not need to be closed by this date.)

For fairness, the functionality of any outstanding projects after this point will be evaluated in your final code review appointment. If you submit an issue for project verification *after* this point, it will not be graded until your final code review appointment.

{% include section.html level="h3" name="Final Project Grading" %}

The project(s) you have graded during this appointment depends on what you have passed before your appointment (see design and functionality cutoff dates above). You can have the functionality of 1 project and the design of 1 project evaluated during your final code review appointment. These must be consecutive projects. You can earn a partial grade on these projects, but will earn a 0% on any other outstanding projects. Specifically:

<table class="table is-hoverable">

<thead>
<tr>
  <th colspan="2" class="has-text-centered">Project 1</th>
  <th colspan="2" class="has-text-centered">Project 2</th>
  <th colspan="2" class="has-text-centered">Project 3</th>
  <th colspan="2" class="has-text-centered">Project 4</th>
</tr>

<tr>
  <th class="has-text-centered is-size-7">Tests</th>
  <th class="has-text-centered is-size-7">Review</th>

  <th class="has-text-centered is-size-7">Tests</th>
  <th class="has-text-centered is-size-7">Review</th>

  <th class="has-text-centered is-size-7">Tests</th>
  <th class="has-text-centered is-size-7">Review</th>

  <th class="has-text-centered is-size-7">Crawler</th>
  <th class="has-text-centered is-size-7">Search</th>
</tr>
</thead>

<tbody>
<tr>
  <td class="has-text-centered">Pass</td>
  <td class="has-text-centered">Pass</td>

  <td class="has-text-centered">Pass</td>
  <td class="has-text-centered"><strong class="has-text-primary">Graded</strong></td>

  <td class="has-text-centered"><strong class="has-text-primary">Graded</strong></td>
  <td class="has-text-centered">0%</td>

  <td class="has-text-centered">0%</td>
  <td class="has-text-centered">0%</td>
</tr>

<tr>
  <td class="has-text-centered">Pass</td>
  <td class="has-text-centered">Pass</td>

  <td class="has-text-centered">Pass</td>
  <td class="has-text-centered">Pass</td>

  <td class="has-text-centered"><strong class="has-text-primary">Graded</strong></td>
  <td class="has-text-centered"><strong class="has-text-primary">Graded</strong></td>

  <td class="has-text-centered">0%</td>
  <td class="has-text-centered">0%</td>
</tr>

<tr>
  <td class="has-text-centered">Pass</td>
  <td class="has-text-centered">Pass</td>

  <td class="has-text-centered">Pass</td>
  <td class="has-text-centered">Pass</td>

  <td class="has-text-centered">Pass</td>
  <td class="has-text-centered"><strong class="has-text-primary">Graded</strong></td>

  <td class="has-text-centered"><strong class="has-text-primary">Graded</strong></td>
  <td class="has-text-centered">0%</td>
</tr>

<tr>
  <td class="has-text-centered">Pass</td>
  <td class="has-text-centered">Pass</td>

  <td class="has-text-centered">Pass</td>
  <td class="has-text-centered">Pass</td>

  <td class="has-text-centered">Pass</td>
  <td class="has-text-centered">Pass</td>

  <td class="has-text-centered"><strong class="has-text-primary">Graded</strong></td>
  <td class="has-text-centered"><strong class="has-text-primary">Graded</strong></td>
</tr>
</tbody>

</table>

For example, if you have passed the tests for project 1 functionality, code review for project 1 design, and the tests for project 2 functionality by the cutoff, then you will have the design of project 2 reviewed and the functionality of project 3 verified during your final code review appointment. You may earn a partial grade for both those projects. However, you will receive a 0% for project 3 design, and all of project 4.

You can use the [What-If Grades](https://guides.instructure.com/m/4212/l/55065-how-do-i-approximate-my-assignment-scores-using-the-what-if-grades-feature) feature in Canvas to estimate the impact this will have on your final letter grade for the course.

You will receive your final grade for the course at the end of your final code review appointment.
