<!-- Date 04-11-2021 -->
# <h1 style="text-align:center; font-size:360%; font-family:Game Of Squids;color:#4A3E76;"><em>Git & GitHub</em></h1>

##### These tutorials are watched from [**_Udemy_**](https://www.udemy.com/ "Click here to checkout Udemy Website") website from [**_The Git & Github Bootcamp_**](https://www.udemy.com/course/git-and-github-bootcamp/ "Click here to check out Course")

##### Note: This Readme only contains git cheat-sheet, practice of these commands are done on my [**_Second github account_**](https://github.com/aman0864 "Click to see my Second GitHub account")

---

---

---

---

---

<!-- Date 04-11-2021 -->

## Installation & Setup

#### Simple Git Commands

Use below command to check Git version:

```git
git --version
```

To configure the name that Git will associate with your work, run this command:

```git
git config --global user.name "Aman"
```

To configure the E-mail that Git will associate with your work, run this command:

```git
git config --global user.email "blablabla@gmail.com"
```

To open the current working directory in default file explorer of your machine:

```git
start .
```

To print the location of the current working directory:

```git
pwd
```

To create a new file in the current working directory:

```git
touch file_name.txt
```

To create a new folder in the current working directory:

```git
mkdir folder_name
```

To delete a file which is available in the current working directory:

```git
rm file_name.txt
```

To delete a folder which is available in the current working directory:

```git
rm -rf folder_name
```

To display all files **except hidden ones** in the current working directory:

```git
ls
```

To display all files **including hidden ones also** in the current working directory:

```git
ls -a
```

<!--
To see what changes you made in repository:

```git
git status
``` -->

> Note: `-` operator is used in git bash when we need to modify a command's behavior.

#### Simple Terminal Commands

-   Regarding Locations
    -   Use `cd` to change path(`cd` stands for **Change Directory**).
    -   Use `cd ..` to change path to the super-directory.
    -   Use `cls` to clear terminal commands.
    -   Use `start .` to open the current working directory in default file explorer of your machine.
    -   Use `dir .` to print a list of all the files available in the current working directory.
-   Regarding creation of files & folder
    -   Use `echo optional_text_you_need_in_your_file > file_name.txt` to create a file in the current working directory.
    -   Use `mkdir folder_name` to create a folder in the current working directory.
-   Regarding deletion of files & folder
    -   Use `del file_name.txt` to delete a file which is available in the current working directory.
    -   Use `rmdir folder_name` to delete a folder which is available in the current working directory and which **does not contains some other files and folders inside it**.
    -   Use `rmdir /S folder_name` to delete a folder which is available in the current working directory and **contains some other files and folders inside it**.

<!-- > Note: `-` is used when we need to modify a command's behavior. -->

---
<!-- Date 04-11-2021 -->

## The Very Basics Of Git Adding & Committing

To create a new git repository use below command this is something you do once per project.  Initialize the repo in the top-level folder containing your project:
```git
git init
```
Git status gives information on the current status of a git repository and its contents.
```git
git status
```
Use git add to add specific files to the staging area.  Separate files with spaces to add multiple at once. You can use `git add .` to stage all changes at once.
```git
git add file1 file2
```
Use below given command to commit changes on git. The -m flag allows us to pass in an inline commit message, rather than launching a text editor. We'll learn more about writing good commit messages later on.
```git
git commit -m "Your message which will be treated as a Git commit"
```
To see which user committed which thing when you can use the below command:
```git
git log
```

---
<!-- Date 05-11-2021 -->

## Commits In Detail (And Related Topics)

Use below command to configure git with [VS Code](https://code.visualstudio.com/) text editor:
```git
git config --global core.editor "code --wait"
```

Use below command to print all the commits in oneline(with short explanation):
```git
git log --oneline
```

Use below command to edit stuff in a git commit which is just made now, It will not work if you made a mistake or want to edit on a commit which is been made before 1 commit:
```git
git commit --amend
```

Use below command instead of using `git add .` and `git commit`, the below will automatically commit all your stuff at once:
```git
git commit -a
```

Use below command to create a `.gitignore` file, which is used to ignore some of the files or folders:
```git
touch .gitignore
```

---
<!-- Date 05-11-2021 -->

## Working With Branches

Use below command to see all branches of your the repository:
```git
git branch
```

Use below command to create a branch in your repository, note that **branch name should not include any spaces**:
```git
git branch branch_name
```

Use below command to switch branches in your repository:
```git
git switch branch_name
```

Use below command to switch and create branch in single line of code in your repository:
```git
git switch -c branch_name
```

Use below command to delete a branch in your repository:
```git
git branch -D branch_name
```

Use below command to rename a branch in your repository. Make sure that you are in the branch you want to rename:
```git
git branch -m new_name_of_branch
```

---

<!-- Date 05-11-2021 -->

## Merging Branches

#### Fast-Forward Branching

Use below command to merge another branch into the current branch:

```git
git merge name_of_branch_to_merge_in
```

> Note: Not all merges are **fast-forward** merges, The branches which does not conflict with each other at all can easily preform **fast-forward**. There are several [different types of commits](https://www.geeksforgeeks.org/merge-strategies-in-git/) like Recursive Merge etc. 

#### Resolving Conflicts

Whenever you encounter merge conflicts, follow the following to encounter them:
- Open up the file(s) with merge conflicts
- Edit the file(s) to remove the conflicts. Decide which branch's content you want to keep in each conflict.  Or keep -the content from both.
- Remove the conflict "markers" in the document
- Add your changes and then make a commit!

---
<!-- Date 07-11-2021 -->

## Comparing Changes With Git Diff

Use below command to check the difference since the last commit and the current **un-staged** changes:

```git
git diff
```

Use below command to check the difference since the last commit and the current **staged and un-staged** changes:

```git
git diff HEAD
```

Use below command to check the difference since the last commit and the current **staged** changes:

```git
git diff --staged
```
> Note: You can also use `git diff --cached` instead of `git diff --staged`, but `--staged` looks more sensible.

Use below command to check the difference **within a particular file** since the last commit and the current data:

```git
git diff file_name
```

Use below command to check the difference **between two different branches** since the last commit and the current data:

```git
git diff branch_1..branch_2
```
> Note: You can also use `git diff branch_1 branch_2` instead of `git diff branch_1..branch_2` they both mean ~same.

Use below command to check the difference **between two different commits**(by using commit hashes) since the last commit and the current data:

```git
git diff 19264c5..482df4a
```
> Note: You can also use `git diff 19264c5 482df4a` instead of `git diff 19264c5..482df4a` they both mean ~same.
>> Note: `19264c5` and `482df4a` are the commit's hash number.


---

<!-- Date 07-11-2021 -->

## The Ins and Outs of Stashing

Use below command to stash changes of your repository:

```git
git stash
```
>Note : You can also use `git stash save` instead of using `git stash`, as it may be an [Aliases](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases) of `git stash save`.

Use below command to get back the stash changes of your repository:

```git
git stash pop
```

Use below command to get back the stash changes of your repository, but note that the **stash will not become clean and you can still use it in another branches of your repository**:

```git
git stash apply
```

You can add multiple stashes in your repository and the will be in same order as the are stashed to view all stashes use below command:

```git
git stash list
```


If you have untracked files (files that you have never checked in to Git), they will not be included in the stash. Fortunately, you can use the `-u` option to tell git stash to include those untracked files:

```git
git stash -u
```

You can access any particular stash from your stashes by using the below command:

```git
git stash stash@{2}
```
> Note: in `git stash stash@{2}` *2* is the stash number.

When you use multiple stashes in your repository you need to clear the stashes at some point before you mix-up all your stuff and to clear a stash from a stash list use the below command:

```git
git stash drop stash@{1}
```
> Note: in `git stash stash@{1}` *1* is the stash number.

If you want to clear-up everything in your stashes use the below command:

```git
git stash clear
```

---

<!-- Date 08-11-2021 -->

## Undoing Changes & Time Traveling

#### Git Checkout
Use  the below command to travel back to a specific commit of your repository:
```git
git checkout 03f3a63
```
> Note: In `git checkout 03f3a63`, `03f3a63` is the **hash number** of the commit.

Use  the below stated command to travel back to a particular number of commits back in your repository:
```git
git checkout Head~1
```
> Note: In `git checkout Head~1`, `1` is the number of how many commits you need to go back to.

Use the below mentioned command to go to the head of your repository where you edited last commit:
```git
git switch -
```

Use the below mentioned command revert changes of a specific file of your branch from a specific commit:
```git
git checkout c57e697 file_name
```
> Note: In `git checkout c57e697 file_name`, `c57e697` is the **commit hash** you can also use `Head~3` instead of it 
>> To revert the changes according to your last commit of branch you can us `--` instead of `c57e697` or `Head~3`.

#### Git Restore
To restore the file to the contents as they are in the HEAD, use below given command:
```git
git restore file_name
```
> **_Note: If you use `git restore file_name` the content of file specified is totally gone it cannot be back again._**

To restore the file to the contents as they are in a specific commit, use below given command:
```git
git restore --source c57e697 file_name
```
> **_Note: If you use `git restore file_name` the content of file specified is totally gone it cannot be back again._**
>> Note: In `git restore --source c57e697 file_name`, `c57e697` is the **commit hash** you can also use `Head~3` instead of it. 

If you accidentally staged a file with sensitive information the to make it ub-staged, use below given command:
```git
git restore --staged file_name
```

#### Git Reset
If you accidentally messed up the with your branch you can take back whole repo. back to a specific commit you made in past but, the commits made by you are gone, use below given command to do so:
```git
git reset c57e697
```
> Note: **Changes will not lose**, `git reset` will just delete the commits not change the file.
>> You can branch make a branch and take changes with you.
>>> In `git reset c57e697`, `c57e697` is the **commit hash** you can also use `Head~3` instead of it. 

In order to change the file as well as delete the commits, use below given command:
```git
git reset --hard c57e697
```
> Note: _**You will lose changes**_, `git reset --hard` will delete the commits as well as change the file.
>> In `git reset --hard c57e697`, `c57e697` is the **commit hash** you can also use `Head~3` instead of it. 

#### Git Revert
If you are collaborating on a project and if you want to continue your work from a previously made commits you can not use `git reset` or `git restore` to do so, as it can raise some serious problems/issues. So instead of using `git reset` or `git restore` you have to use the below command:
```git
git revert c57e697
```
> Note: In `git revert` will make another commit which will be the copy of commit `c57e697`, it will not delete the commits or there changes.
>> In `git revert c57e697`, `c57e697` is the **commit hash** you can also use `Head~3` instead of it.

---

<!-- Date 08-11-2021 -->

## Github The Basics

You can clone any repository whether or not it is on [GitHub](https://github.com/), by using th below command:
```git
git clone https://github.com/AmanRathoreM/Git-Github
```
> Note: In `git clone https://github.com/AmanRathoreM/Git-Github`, `https://github.com/AmanRathoreM/Git-Github` is a [url of a repository](https://github.com/AmanRathoreM/Git-Github) I need to clone.

> Note: You can setup your local machine for coloration on [GitHub](https://github.com/) by seeing [GitHub docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

Use below command to view the existing remote repositories in your local git repository:
```git
git remote
```

Use below command to view the existing remote repositories info **in detail** :
```git
git remote -v
```

Use below command to view the existing remote repositories info **in detail** :
```git
git remote add name_of_remote_repository url_of_remote_repository
```
> Note: According to the git conventions name of the remote repository should be **origin**, but it is not necessary.

Use below command to push your  code to a remote repository:
```git
git push name_of_remote_repository branch_name_you_want_to_push
```
> Note: You can also use just `git push` to push your current working branch to a remote repository.

---

<!-- Date 09-11-2021 -->

## Fetching & Pulling

#### Fetching

Use the following command to fetch data from a remote repository:
```git
git fetch remote_repo_name branch_name_you_want_to_fetch
```
> Note: If you did not specify name of the remote repo the its default name will be taken as `origin`.

#### Pulling

You can also use below command to retrieve changes from a remote repository. Unlike `git fetch`, pull actually updates our HEAD branch with whatever changes are retrieved from the remote.
```git
git pull remote_repo_name branch_name_you_want_to_pull
```
> Note: If you did not specify name of the remote repo and name of the branch you want to pull from, their's default name will be taken as `origin` and _**name of the branch you are working**_ respectively.
>> `git pull` can also result in [merge conflicts](https://git-scm.com/docs/git-merge#_how_to_resolve_conflicts).

---

<!-- Date 09-11-2021 -->

## Github Grab Bag Odds & Ends

> There is not much in this section but the point should be noted that you can also [host your website on GitHub](https://pages.github.com/) for free.

---

<!-- Date 09-11-2021 -->

## The Power of Reflogs - Retrieving Lost Work

In case you want to view full history of commits, merges, checkouts etc. of your repository you can use the following command:
```git
git reflog show HEAD
```
> Note: Logs file are stored only for 90 days by default, however you can change that period globally or locally.
>> `HEAD` in `git reflog show HEAD` is just a reference to the command you can also use a branch name etc. to check it's logs.

If you want to go back in the history not only of commits but also of merges, checkouts etc. of your repository you can use the following command:
```git
git checkout HEAD@{2}
```
> Note: You can get `HEAD@{2}` type of id when you run `git reflog show HEAD` which displays multiple `HEAD@{...}` with each having a unique information.
>> You can also use `git reflog master@{one.week.ago}`, `git checkout bugfix@{2.days.ago}`, or `git diff main@{0} main@{yesterday}` to play with your stuff.

Suppose you had hard rested an important work than by using the below command you can get your work back:
```git
git reset --hard master@{1}
```
> Note: `master@{1}` is just a reference to some commit, merge, checkout etc. happened in past in your repository.

---

<!-- Date 09-11-2021 -->

## Writing Custom Git Aliases

You can make your own custom git aliases by adding the following syntax in `.git/config` file:
```git
[alias]
    s = status
    l = log
```

You can also add a custom git alias from command-line by using the below syntax:
```git
git config --global alias.sb branch
``` 
> Note: in `git config --global alias.sb branch`, `sb` and `branch` are respectively the name of the alias and the command that alias will run.
>> It is recommend to add alias from file as it is easier in making complex alias.

> You can get more [pre-made aliases](https://github.com/GitAlias/gitalias) from internet.
