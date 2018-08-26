---
title: Lab Submission
navbar: Guides
layout: default
categories: labs
---

To receive credit for your coding hour, you must follow the steps below:

  1. If you are attending the lab session in person, sign in with the teacher assistant and submit the date in the appropriate "Lab Attendance" assignment in Canvas to earn participation credit.

  2. Decide whether you are going to spend an hour on your homework or project, and open that assignment in Eclipse. (You may not switch later, so choose wisely!)

  3. In Eclipse, [create a branch](http://wiki.eclipse.org/EGit/User_Guide#Creating_a_New_Local_Branch) named `lab##` where `##` is the 2 digit week number. For example, name the branch `lab02` if this is your first lab session during week 2.

  4. Create a "trivial" commit to mark the start of lab in this new branch. You can do this by adding a comment to the code like `// Start of lab` and then [committing the change](http://wiki.eclipse.org/EGit/User_Guide#Committing_Changes).

  5. Work on your code. Make sure you **commit often**, as you need at *least* 3 non-trivial commits to earn lab credit. This works out to 1 commit every 20 minutes---set a timer if you think that will help. Once you are used to `git`, it is likely you will have more than 3 commits by the end of the hour.

  6. When you are done, make sure to [push your changes](http://wiki.eclipse.org/EGit/User_Guide#Pushing_to_other_Repositories) to Github if you have not already.

  7. Now, it is time to combine your `lab##` branch back into the `master` branch. Open a browser and navigate to your Github repository. Click on the "branches" link, and make sure you should see your lab branch and commits.

  8. Click the "[New pull request](https://help.github.com/articles/creating-a-pull-request/)" button next to your lab branch. The base branch should be `master` and your `lab##` branch should be in the "compare" dropdown. Enter "End of lab" as the message and click the "Create pull request" button when done.

  9. If all went well, you should now see a "Merge pull request" button. Click that button to finalize the merge of your lab changes into your `master` branch. It will also give you the option of deleting the `lab02` branch. That is up to you---we will still see the commits you made on the pull request even after your branch is deleted.

  10. Copy and paste the link to your pull request into Canvas to earn lab credit. From here, we'll be able to see all of your lab-related commits.

  11. **You are not done yet!** Go back to Eclipse, and switch back to the `master` branch. Make sure you [pull your changes](#) that you made on Github back into your local repository. You are successful if you see your lab changes show up in Eclipse.

These steps are not designed just to annoy you. It is forcing you to get used to several core `git` and Github operations that you are likely to encounter in industry. So, even though it is 10+ steps to submit a lab, it can all be summarized as "use `git` normally for an hour" once you are used to this ecosystem.

If you do not follow these steps, we may not be able to verify your lab submission! If something goes wrong, you can try submitting a different hour of work (remember, you should be spending at least 8 hours a week on this class outside of lecture).
