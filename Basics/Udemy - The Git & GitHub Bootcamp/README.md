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

