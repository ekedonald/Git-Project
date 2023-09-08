# Git Project
Git is an open source and free source distributed version control system designed to handle everything from small to large projects with speed and efficiency. With git, you can manage files over time and revert back to those changes.

For example, you want to make change to a website, you can make the chnange on a branch and merge the branch wiht the main branch. Basically, changes will be made to the website but with git you can revert back to previous versions of the website.

With git, you can make comparisons between various and have more information like who made those changes.

Throughout the implementation you will learn how to efficiently Initialize a Repository and Make Commits Work with Branches, Collaboration and Remote Repositories, and Tagging track changes, highlighting the significance of Git in modern software development workflows. The projects not only focuses on the technical aspects of Git but also emphasizes best practices for maintaining a clean commit history, optimizing workflows, and troubleshooting common issues.


## Initializing a Git Repository
Before initializing a git repo, ensure git has been installed in your computer. Now to initialize a git repo follow these steps:
* Open a terminal on your computer, eg git bash or terminal
* On your terminal create your working folder or directory, eg git_project using this command:
```bash
mkdir git_project
```
* Change or move into your working directory or folder using this command:
```bash
cd git_project
```
* While you are inside the folder, run this command:
```bash
git init
```

## Making Your First Commit
In the previous section, the current working directory was initialized to a git repository. Commit in git means saving the changes made to your files. These changes can be adding, modifying or deleting files or text. When you make a commit, git takes a snapshot of the current state of your repository and saves a copy in the .git folder inside your working directory.

To make your first commit, the following steps are taken:
* Inside your working directory, create a file README.md using this command:
```bash
touch README.md
```
* Write any sentence of your choice inside the text file.
```bash
echo "Git Project" >> README.md
```
* Add your changes to git staging area using this command:
```bash
git add README.md
``` 
* To commit your changes to git, run the command:
```bash
git commit -m "initial commit"
```

## Working with Branches
Imagine you have a note book and you want to write a different story on different pages of your note book so you do not mess up your previous note. Git branch helps you create a different copy (page) of your source code. In your new branch you can make changes as you please and such can be added to the code base of your application. Your change is independent of what is available in the main copy.

Git branch is commonly used to develop new feature of your application. You will agree with me that the initial code is untested and such can not be added to the code base of your live application. 

It is also an important tool for collaboration with remote teams (developers working from different locations). They can make seperate branches while working on same feature. And at the end of the day, coveerge their code to one branch.

### Making Your First Git Branch
To make a new branch run this command: `git checkout -b`. The -b flag helps you create and switch to the new branch.

 Having made your first commit in the previous section, the following steps are taken to create your first branch:

* Make a new branch by running this command:
```bash
git checkout -b my_new_branch
```

### Listing  Your Git Branches
The git branch command is used to list all the branches on your local git repository as shown below:

```bash
git branch
```

### Change Into An Old Branch
To change to an existing or old branch, use the command below:

```bash
git checkout <branch-name>
```

### Merging A Branch Into Another Branch
Lets say we two branches A and B. If you want to add the content of branch B into A. First we change into branch A and run the git command below:

```bash
git merge B
```

### Deleting A Git Branch
When a new feature is added to an applicatiom, it is done in a feature branch. Usually this feature branch is deleted when the code must have tested and merged into a staging or dev environment depending on the branch strategy of the team. Git branch can be deleted using the command shown below:

```bash
git branch -d <branch_name>
```
This by no means all that you can do with branches in git. To learn more type command `git branch --help` on your terminal.

## Collaboration & Remote Repositories
### Pushing Your Local Git Repository To Your Remote Github Repository
In previous sections, you have written your story in your local repository and your friend is interested in contributing to your story but he is unable to do so because the story is currently stored locally in your macine.

Having created a github account and github repository in earlier steps, lets send a copy to our repository in github. This can be achieved by taking the following steps below:

* Add a remote repository to the local repository using the command below:

```bash
git remote add origin <link_to_our_github_repo>
```

* To get the remote link click on he green button code, copy the https link. A screenshot is shown below:

* After commiting your chages in your local repo. You can push the content to the remote repo using the command below:

```bash
git push origin <branch name>
```

The word origin refers to your remote link, it evaluates to the repo url. It can be any word you choose.

### Cloning Remote Git Repository
In the previous section, you successfully added a remote git repositroy and pushed your story in the local repository. Now your friend can make contributions to your story. Give it a thought, will he be working on your story on github directly on make a local copy ?

Best practice dictates that he makes a copy of your story in his local machine, creates a branch where he can make all the modifications he sees fit. But how is he going to make a local copy of our story in the local machine ? Git clone command to the rescue.

The git clone command helps to make a copy of remote repository in your local machine. See it as a git tool for downloading remote repository into your local machine. The command is as follows:

```md
git clone <link to your remote repository>
```

## Branch Management and Tagging
### Introduction To Mardown Syntax
Markdown syntax is a lightweight markuo language that is we=idely used for formatting plain text. It allows you to add formatting elements to your text without using complex HTML or other formatting languages. Markdown is commonly used for creating documents, README files, forum posts and even web pages.

Here are the most commonly used markdown syntax elements:

1. Headings: To create heading, use the hash symbol at the beginning of the line. The number of hash symbol indicates the level of the heading.

``` md
# Heading
## Heading 2
### Heading 3
```

2. Empashis: asterisks or underscore is used to emphasize text.

```md
*italic* or _italic_
**bold** or __bold__
```

3. List: markdown has support for both ordered abd unordered list.

* Unordered List Example:

```md
- Item 1
- Item 2
- Item 3
```

* Ordered List Example:

```md
1. First Item
2. Second Item
3. Third Item
```

4. Links: To create a hyperlink, use square brackets for the link text followed by parentheses containing the URL. For example:

```md
[visit twitter.com](https://twitter.com)
```

5. Images: To display an image, use an exclamation mark followed by square brackets for the the alt text and parentheses containing the URL.

```md
![Alt Text](https://example.com/image.jpg)
```

6. Code: To display code or code snippets, use backticks (`) to enclose the code as shown below:

```md
`console.log('Welcome to google.com)`
```

Like I earleir mentioned these are the most commonly used markdown syntax elements. 