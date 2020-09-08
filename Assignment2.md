
1. Describe what is the output of the following commands
    -  `git branch` 
    -  `git checkout BRANCH_NAME` (USE THE NAME OF AN EXISTING BRANCH)
    -  `git log --decorate`
````
git branch 

*master
  math

git checkout math
Switched to branch 'math'


get log --decorate

commit e3c629dd524712aedea96d7dbaad1c50d12b5b5e (HEAD -> math)
Author: Igor Steinmacher <igorsteinmacher@gmail.com>
Date:   Wed Aug 14 23:13:48 2019 -0700

    Adding some more knowledge to the function

commit 654b490a181dedf82dd6deda5f9848d6cca05918
Author: Igor Steinmacher <igorsteinmacher@gmail.com>
Date:   Wed Aug 14 23:12:14 2019 -0700

    Added a draft of A.py

commit 2dfb02c3f9383d6c3b2695c99e175d8b85f594a1
Author: Igor Steinmacher <igorsteinmacher@gmail.com>
Date:   Wed Aug 14 23:08:47 2019 -0700

     Creating all files (all empty)


````
2. Try `git log --graph --all`. What do you see?

````
 commit 18931d12a8be7cac049b73c6bc8136e9482f3371 (master)
| Author: Igor Steinmacher <igorsteinmacher@gmail.com>
| Date:   Wed Aug 14 23:15:28 2019 -0700
| 
|     Making a small change here
|   
| * commit e3c629dd524712aedea96d7dbaad1c50d12b5b5e (HEAD -> math)
|/  Author: Igor Steinmacher <igorsteinmacher@gmail.com>
|   Date:   Wed Aug 14 23:13:48 2019 -0700
|   
|       Adding some more knowledge to the function
| 
* commit 654b490a181dedf82dd6deda5f9848d6cca05918
| Author: Igor Steinmacher <igorsteinmacher@gmail.com>
| Date:   Wed Aug 14 23:12:14 2019 -0700
| 
|     Added a draft of A.py
| 
* commit 2dfb02c3f9383d6c3b2695c99e175d8b85f594a1
  Author: Igor Steinmacher <igorsteinmacher@gmail.com>
  Date:   Wed Aug 14 23:08:47 2019 -0700
  
       Creating all files (all empty)
````

3. Use `git diff BRANCH_NAME` to view the differences from a branch and the current branch.
   Summarize the difference from master to the other branch.

````
Math has an A.py file that contains 
-   if operator == 'sum':
-      print num1 + num2
-   ``   print 'That was easy buddy'
-   else:
-      if operator == 'subtraction':
-         print num1 - num2
-         print 'I could handle that...'
-      else:
-         print 'my knowledge is limited'

while Master has +   print 'my knowledge is limited'     


Master B.py has the extra line
+# Another file that will receive a line of code... at least.
````


4. Write a command sequence to merge the non-master branch into `master`

````
git commit -m "igor told me to"
git merge math

````

5. Write a command (or sequence) to (i) create a new branch called `math` (from the `master`) 
and (ii) change to this branch (yes, `math` is already there, just report what you've done, the error and the reason you got the error. If you deleted and recreated the branch, you are fine too)

````
git branch math
fatal: A branch named 'math' already exists.
git checkout math
````

7. Write a command (or sequence) to commit your changes

````
git commit B.py -m "learning math"

````

 Write a command sequence to merge the `math` branch into `master` and describe what happened

````
git merge math

My edits to B.py would be overwritten if I continued with the merge. 

error: Your local changes to the following files would be overwritten by merge:
	B.py
Please commit your changes or stash them before you merge.
Aborting
````
10. Write a set of commands to abort the merge
````
git merge --abort
git reset --hard
````
   
11. Now repeat item 9, but proceed with the manual merge (Editing B.py). All implemented functions are needed. Explain your procedure
````
Open the B.py in Nano 
Append the B.py fille so it doesnt have the =====head part , the ==== midddle part or the  ====base part.

````
12. Write a command (or set of commands) to proceed with the merge and make `master` branch up-to-date

````
 git add B.py
git commit -m "fixed?"
git merge math

````

Report your experience of making this submission, including the steps followed, commands used, and hurdles faced (within the file you created for the Part 1.
````
I created a forked version of Igor's repo.
Then I when to my fork/ students and created a new file called Herman_Chloe.md. 
I then Megered my File with my fork of igor's repo. 
Finally I requested a pull request with Igors repo so that my new file could be added. Hooray! 
````