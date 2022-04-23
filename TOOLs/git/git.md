# git



## Git intro

### make a git repo

- To make a directory a git repo, we should use `git init` command. And `.git` file' existence is the criteria to test whether we have change a directory into a git repo.  

  ![Screen Shot 2022-04-23 at 13.27.59](git.assets/Screen%20Shot%202022-04-23%20at%2013.27.59.png)

- Using `git status` we could know all the status information of our cuurent branch, like how many files have been modified, how many new files have been added, which file has been delete, whether we have uncommitted files, etc. 

  ![Screen Shot 2022-04-23 at 13.28.12](git.assets/Screen%20Shot%202022-04-23%20at%2013.28.12-0699664.png)

  You will better comprehension on the `git status`, when seeing this snapshot.

  ![Screen Shot 2022-04-23 at 13.32.25](git.assets/Screen%20Shot%202022-04-23%20at%2013.32.25.png)

   ![Screen Shot 2022-04-23 at 13.32.53](git.assets/Screen%20Shot%202022-04-23%20at%2013.32.53.png)

- If we want to use the full function of the git, we could use git configure to configure some of our personal informations. See the document for more information.

  

### Working directory

Before add or commit every thing, we are work in the working directory. And by `git add . `or`git add *`command, we put our change into the stage area. And then by commit we put our change into the Repository(may be a repo hosted on the GitHub, normally)

![IMG_1507](git.assets/IMG_1507.JPG)

### Stageing area

![IMG_1509](git.assets/IMG_1509.JPG)

### Commit area

<img src="git.assets/IMG_1508.JPG" alt="IMG_1508" style="zoom: 50%;" />

So one theory of git is: Git = Tracking changes - Not storing files again and again.



### branches & commits

If we have an idea on our project, but we don't really sure whethre we can make it or not. Then we could use`git branch new_branch_namw `git checkour -b new_branch_name` to create a whole new copy of our `main` branch (or in some situation we call it `master branch), and then we add new feature into this branch, therefore any changes we make will not make a impact on the original branch. And by using `git branch` we can simply find we are now on which branch.

<img src="git.assets/Screen%20Shot%202022-04-23%20at%2013.42.27.png" alt="Screen Shot 2022-04-23 at 13.42.27" style="zoom:150%;" />

![Screen Shot 2022-04-23 at 13.42.51](git.assets/Screen%20Shot%202022-04-23%20at%2013.42.51.png)

<img src="git.assets/Screen%20Shot%202022-04-23%20at%2013.43.40.png" alt="Screen Shot 2022-04-23 at 13.43.40" style="zoom:150%;" />



### Delete data

####  Working dir



#### Unstaged changes



#### Staged changes



#### Lasted commits



#### Branches





`git ls-files`