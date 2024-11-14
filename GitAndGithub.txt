# Starting with Git and Github

**Steps :-**

1.  To Check if git is there in your m/c or not ==> git --version
2.  If not present ==> download git using link("https://git-scm.com/downloads")
3.  Install the downloaded "**.exe" file and restart the terminal
4.  To check if git has any registered user ==> git config --global --list
5.  Irrespective of user found or not, if want to register as an user follow these commands ==> 
    i)  ==> git config --global user.name <username>
    ii) ==> git config --global user.email <user_email_id> 
    ...
    registered user should have minimum of two attributes atleast, so using only two as of now
6.  Git only tracks the files which are there in "Staging Area / Git repository" and not just in 
    "Working Directory". 
    To create Git repository use command ==> git intit / git init -b <branch_name>(optional), 
    It will create .git folder in your project folder which represents the "Staging Area or Git repository".
7.  To Check if the files have been added to the Git repository or not ==> git status
8.  To add any/all file to the Staging area from the working directory ==> 
    git add <file_name_with_extention> / git add .
9.  To unstage any file if required from Staging area ==> git rm --cached <file_name_with_extention>
10. Commiting(Saving) any file can only be done if the file exist in Staging area and for Committing all the staged 
    files will use ==>  git commit -m <logical_message>
11. To check all the logs of current branch commits ==> git log / git log --pretty=oneline
12. If want to skip the staging area and directly commit the changes ==> git commit -a -m <logical_message>
13. To discard all the changes in working directory after previous commit ==> git restore <file>
14. To check the difference between Staged and Unstaged files ==> git diff
15. To check the difference between Staged and Committed files ==> git diff --staged
16. To remove a file if committed bymistake ==> git rm --cached <file_name>
17. Now Create Account on either of the remote services e.g - Github, gitlab, Bitbucket, etc 
    Here we are using Github as the remote service ....
18. After creating account on Github create a repository
19. To Connect your local Git repository to remote one, it requires a ssh-key to be generated from your local 
    m/c and set it to the remote account --->
    i)   To generate ssh-key ==>  ssh-keygen -o (It will create public key at the location you will specify)
    ii)  Once the public key is generated, copy and paste this public key on the location -  open Github -> 
         Settings -> SSH and GPG keys -> New SSH key -> paste the key and save.
    iii) Now run this command on your terminal ==> git remote add git@github:<user_name>/<remote_repository_name>
20. Now, Once remote and local repositories are connected and can communicate, we can perform required operations
21. To push any changes to remote ==> git push origin <branch_name>
22. To pull the latest Code from remote ==> git pull origin <branch_name>
23. To Check "origin" reference repositories for fetch and push ==> git remote -v
24. To Show tags/versions if any in the project ==> git tag
25. To show the details of any particular tag/version ==> git show <tag_name>
26. To add tag/version into the project ==> git tag <tag_name> -m <meassage> //e.g - git tag v1.0 -m "first release"
27. To push tag/version to the remote repository ==> git push origin <tag_name>
28. To get any project from github ==> git clone <project_url>
29. To see the branches existing in the project either remote or local ==> git branch / git branch --all
30. To Create a new branch ==> git branch <new_branch_name>
31. To Switch from branch1 to branch2 (be in branch1) ==> git checkout branch2 / git switch branch2
32. To move back to the just previous branch ==> git switch -
33. To delete an existing branch if not required furthur ==> git branch -d <branch_name>
34. To merge a branch branch2 into branch1 (be in branch1) ==> git merge branch2 but before merging make sure 
    to have the latest code from remote repos
35. While merging if found with conflicts then resolve them manualy and then commit and push the merged code.
    If can not resolve the conflicts then to stop merging use ==> git merge --abort
36. If you want to ignore some files and folders in the project to be tracked by git then mention their names
    or patterns of them in .gitignore file. e.g - Main.class, *.class, *.log, Dir/, Static/Dir, etc



### **Git Commands ===>>>>**

1.  git --version
2.  git config --global user.name <username>
3.  git config --global user.email <user_email_id> 
4.  git config --global --list
5.  git intit / git init -b <branch_name>(optional)
6.  git status
7.  git add <file_name_with_extention> / git add .
8.  git rm --cached <file_name_with_extention>
9.  git commit -m <logical_message>
10. git log / git log --pretty=oneline
11. git commit -a -m <logical_message> 
12. git restore <file>
13. git diff 
14. git diff --staged
15. git rm --cached <file_name>
16. ssh-keygen -o
17. git remote add git@github:<user_name>/<remote_repository_name>
18. git push origin main
19. git pull origin main
20. git remote -v
21. git tag
22. git tag <tag_name> -m <meassage> //e.g - git tag v1.0 -m "first release"
23. git push origin <tag_name>
24. git show <tag_name>
25. git clone <project_url>
26. git branch / git branch --all
27. git branch <new_branch_name>
28. git checkout branch2 / git switch branch2
29. git switch -
30. git branch -d <branch_name>
31. (be in branch1) ==> git merge branch2
32. git merge --abort