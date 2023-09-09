# Git Project
___

Git is an open source and free source distributed version control system designed to handle everything from small to large projects with speed and efficiency. With git, you can manage files over time and revert back to those changes.

For example, you want to make change to a website, you can make the chnange on a branch and merge the branch wiht the main branch. Basically, changes will be made to the website but with git you can revert back to previous versions of the website. Git can make comparisons between various codebases and have more information like who made those changes.

Throughout the implementation you will learn how to efficiently Initialize a Repository and Make Commits Work with Branches, Collaboration and Remote Repositories, and Tagging track changes, highlighting the significance of Git in modern software development workflows. The projects not only focuses on the technical aspects of Git but also emphasizes best practices for maintaining a clean commit history, optimizing workflows, and troubleshooting common issues.


## Initializing a Git Repository
Before initializing a git repo, ensure git has been installed in your computer. Now to initialize a git repository, follow these steps:

* Open a terminal on your computer, eg git bash or terminal.

* On your terminal create your working folder or directory, eg git_project using this command.

```bash
mkdir git_project
```

![mkdir git_project](./images/1.%20mkdir%20git_project.png)

* Change or move into your working directory or folder using this command.

```bash
cd git_project
```

![cd git_project](./images/1.%20cd%20git_project.png)

* While you are inside the folder, run this command.

```bash
git init
```

![git init](./images/1.%20git%20init.png)

## Making Your First Commit
In the previous section, the current working directory was initialized to a git repository. Commit in git means saving the changes made to your files. These changes can be adding, modifying or deleting files or text. When you make a commit, git takes a snapshot of the current state of your repository and saves a copy in the .git folder inside your working directory.

To make your first commit, the following steps are taken:

* Inside your working directory, create a file README.md using this command.

```bash
touch README.md
```

![touch README](./images/2.%20touch%20README.png)

* Write any sentence of your choice inside the text file.

```bash
echo "Git Project" >> README.md
```

![echo git_prjoect](./images/2.%20echo%20git%20project.png)

* Check the status of your repository, use the command below.

```bash
git status
```

![git status](./images/2.%20git%20status.png)

* Add your changes to git staging area using this command.

```bash
git add README.md
``` 

![git add README](./images/2.%20git%20add%20README.png)

* To commit your changes to git, run the command.

```bash
git commit -m "initial commit"
```

![git commit](./images/2.%20git%20commit.png)

## Working With Branches
Imagine you have a note book and you want to write a different story on different pages of your note book so you do not mess up your previous note. Git branch helps you create a different copy (page) of your source code. In your new branch you can make changes as you please and such can be added to the codebase of your application. Your change is independent of what is available in the main copy.

Git branch is commonly used to develop new feature of your application. You will agree with me that the initial code is untested and such can not be added to the code base of your live application. 

It is also an important tool for collaboration with remote teams (developers working from different locations). They can make seperate branches while working on same feature. And at the end of the day, coveerge their code to one branch.

### Making Your First Git Branch
To make a new branch run this command: `git checkout -b`. The -b flag helps you create and switch to the new branch.

 Having made your first commit in the previous section, the following steps are taken to create your first branch:

* Make a new branch by running this command:

```bash
git checkout -b my_new_branch
```

![git checkout1](./images/3.%20git%20checkout1.png)

### Listing  Your Git Branches
The git branch command is used to list all the branches on your local git repository as shown below:

```bash
git branch
```

![git branch](./images/3.%20git%20branch.png)

### Change Into An Old Branch
To change to an existing or old branch, use the command below:

```bash
git checkout <branch-name>
```

![git checkout2](./images/3%20git%20checkout2.png)

### Merging A Branch Into Another Branch
Lets say we two branches A and B. If you want to add the content of branch B into A. First we change into branch A and run the git command below:

```bash
git merge B
```

![git merge](./images/3%20git%20merge.png)

### Deleting A Git Branch
When a new feature is added to an applicatiom, it is done in a feature branch. Usually this feature branch is deleted when the code must have tested and merged into a staging or dev environment depending on the branch strategy of the team. Git branch can be deleted using the command shown below:

```bash
git branch -d <branch_name>
```

![git branch -d](./images/3%20git%20branch%20-d.png)

This by no means all that you can do with branches in git. To learn more type command `git branch --help` on your terminal.

## Collaboration & Remote Repositories
Git is used for collaboration among remote teams (developers residing in different countries). But come to think of it, how can developers working remotely collaborate seamlessly on the same codebase since you currently have your codebase on your computer.

This is where **github** comes in. Github is a web based platform where git repositories are hosted. By hosting our local git repository on github, it becomes available to the public and repostiories can also be made private. Anyone can access public repositories while people with special privileges can access the public repository.

Hence, remote teams can now view, update and make changes to the same repository.

### Creating A Github Account
The following steps are taken to create a github account:

 1. Head over to [sign up on github.com](https://github.com/signup)

 2. Enter your username, password and email.

 ![create account1](./images/5.%20create%20account1.png)

 3. Verify your account by solving the puzzle.

 ![create account2](./images/5.%20create%20account2.png)

 4. Click on the Create Button to create your account.

 ![create account3](./images/5.%20create%20account3.png)

 5. An activation code will be sent to your email, enter the code in the textboxes provided below and a Github account will be created.

 ![create account4](./images/5.%20create%20account4.png)

 ### Creating Your First Repository
 1. Click on the plus sign beside the search bar, a drop menu will appear. Select **New Repository**.

 ![new repo1](./images/5.%20new%20repo1.png)

 2. Fill out the form by adding a unique repository name, description, ticking the box to add a README.md file and clicking the green button to create your repository.

 ![new repo2](./images/5.%20new%20repo2.png)

### Pushing Your Local Git Repository To Your Remote Github Repository
In previous sections, you have written your story in your local repository and your friend is interested in contributing to your story but he is unable to do so because the story is currently stored locally in your macine.

Having created a github account and github repository in earlier steps, lets send a copy to our repository in github. This can be achieved by taking the following steps below:

* Add a remote repository to the local repository using the command below:

```bash
git remote add origin <link_to_our_github_repo>
```

![git remote add](./images/4.%20git%20remote%20add.png)

* To get the remote link click on he green button code, copy the https link. A screenshot is shown below:

![git remote link](./images/4.%20git%20remote%20link.png)

* After commiting your chages in your local repo. You can push the content to the remote repo using the command below:

```bash
git push origin <branch name>
```

![git push](./images/4.%20git%20push.png)

The word origin refers to your remote link, it evaluates to the repo url. It can be any word you choose.

### Cloning Remote Git Repository
In the previous section, you successfully added a remote git repository and pushed your story in the local repository. Now your friend can make contributions to your story. Give it a thought, will he be working on your story on github directly on make a local copy?

Best practice dictates that he makes a copy of your story in his local machine, creates a branch where he can make all the modifications he sees fit. But how is he going to make a local copy of our story in the local machine? Git clone command to the rescue.

The git clone command helps to make a copy of remote repository in your local machine. See it as a git tool for downloading remote repository into your local machine. The command is as follows:

```md
git clone <link to your remote repository>
```

![git clone](./images/4.%20git%20clone.png)

## Branch Management and Tagging
### Introduction To Mardown Syntax
Markdown syntax is a lightweight markup language that is widely used for formatting plain text. It allows you to add formatting elements to your text without using complex HTML or other formatting languages. Markdown is commonly used for creating documents, README files, forum posts and even web pages.

Here are the most commonly used markdown syntax elements:

1. Headings: To create heading, use the hash symbol at the beginning of the line. The number of hash symbols indicates the level of the heading.

``` md
# Heading
## Heading 2
### Heading 3
```

2. Empashis: Asterisks or Underscores are used to emphasize text.

```md
*italic* or _italic_
**bold** or __bold__
```

3. List: Markdown has support for both ordered abd unordered list.

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