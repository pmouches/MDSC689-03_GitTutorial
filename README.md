# MDSC689-03_GitTutorial

**Why git?**
Git is a version control system, it is used to:
1. Follow the history of a source code
2. Work in collaboration on a programming project

Github is a website hosting git repositositories.

**How to use Github?**

1. [Install](https://help.github.com/en/github/getting-started-with-github/set-up-git) git on your computer, and create a Github account (use ucalgary email to create private repositories).
2. Create a new repository or clone an existing repository.
* Create new: go inside your folder, open the terminal and use the command *git init*.
* Clone existing: go to the GitHub webpage of the repository, click on clone and copy the URL. Go inside the folder wher you want to clone, open the terminal and use the command *git clone myURL*.
3. Add new files to your repository: create your file, open the terminal and use the command *git add myNewFile*.
4. Modify your files: once your modifications are relevant (e.g. you implemented a new feature that works), use the command *git commit myModifiedFile -m"my message"* to commit your changes.
5. Once your done working for the day, send all your commits to the server using the command *git push*. /!\ Your collegues might have modified the code while you were working! Before pushing your modifications, use the command *git pull* to fetch their modification. If they modified the same files as you git will automatically merge both your modifications. If you modified the same line of code, git will ask you to manually merge the files.

![Alt text](/images/gitimage.png?raw=true "Optional Title")

**About the commits**

* Commiting your modifications is important as you can easily cancel your last commits *git reset --hard HEAD^*.
* Use explicit messages for each commit to keep your repository clean (option *-m "message"*).
* You can come back to a previous version of your code using *git checkout myFile commitHash*. Use *HEAD* as *commitHash* to undo all the non commited changes (i.e. go back to your last commited version).

**Other usefull commands**
* *git diff myFile*: Show the local differences between your file and the last commited version
* *git status*: Shows the status of your working directory.

**Branches in git**

Branches allow to work in parallel on other features. It's like creating a copy of your code, while you your collegues are still  working and commiting on the main feature. The main branch is called *master*.
* *git branch myNewBranch*: Creates a new branch.
* *git checkout myNewBranch*: Moves you to the branch *myNewBranch*
* *git branch*: Lists all the existing branches.
* Merge two branches: If you want to merge *myNewBranch* with the master branch, go to the master branch with *git checkout master* and merge *myNewBranch* with *git merge myNewBranch*.
