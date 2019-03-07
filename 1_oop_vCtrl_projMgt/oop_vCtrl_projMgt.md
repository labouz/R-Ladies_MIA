---
title: "oop_vCtrl_prjMgt"
subtitle: "R-Ladies Miami"
author: "LB"
date: "February 28, 2019"
output: 
  html_document:
    keep_md: yes
    toc: yes
---



## Version Control
Version control is a crucial consideration, espectially when working with collaborators. We will try and collaborate on this project so, we will learn how to set up git on your machine and integrated into RStudio. Jenny Bryan also has a wonderful book online that provides an in-depth step-by-step on how to truly get git working smoothly, check it out here <https://happygitwithr.com>.  
  
  Overview:  

1. Install Windows: [Git](https://git-scm.com/) / macOS: Xcode
2. Register a [GitHub](https://github.com) account
3. Get your GitHub known to RStudio

```r
library(usethis)
use_git_config(user.name = "labouz", user.email = "lab218@miami.edu")
```
4. Make a test repo on GitHub.com
5. Connect RStudio to Git and GitHub
6. Create project with verison control
7. Make changes, commit, and push
8. Pulling changes
9. Issues

### What is Git and GitHub?
#### 1. Git
Git is a version control system. Simply, it allows you to capture "screenshots" of changes made and combines them automatically. This way, you and others can work on the same files at the same time and see each other's changes. If there are conflicts or ambiguity, Git will show you those too.  
There is a "parent" or "master" branch that can feed several "children" branches. 

#### 2. GitHub
GitHub is a website that allows you to share your projects on code with collaborators/the world. In conjuction with Git, it is one of the more user-friendly systems out there.  

#### 4. Create a test repo on GitHub.com
Go to <https://github.com>. Go to your repositories page and click "New".  
  Fill in info:  
  
* name: testRepo
* description: "testing the setup of first repo"
* private
* initialize with README
* click create
* copy HTTPS URL  
  
  
  
  ![click on the green clone button](/Users/Layla/Documents/GitHub/lootedart/images/1_https.jpg)
  
  
We can use the shell (see Happy Git for more details) to clone the repo to our 
local machines or we can do so from RStudio.

###Version Control Projects in RStudio

####5./6. Connect RStudio to Git and GitHub and Create a Version Control Project
If it's your first time using version control within RStudio, most likely you will
have to help RStudio find Git on your machine.  

From RStudio, *Tools > Global Options > Git/SVN* and direct RStudio to your Git 
executable file. Restart RStudio.  
  

![Set the path to where the .exe file is stored locally](/Users/Layla/Documents/GitHub/lootedart/images/1_gitexe.jpg)
  
  
Additional instructions for connecting Git/GitHub to RStudio:  <https://support.rstudio.com/hc/en-us/articles/200532077?version=1.1.463&mode=desktop>

Now that RStudio can detect Git, let's make a project! Once you've restarted RStudio, click on 
*File > New Project*. Select the "Version Control" option and then select "Git". Here, you will paste the HTTPS URL of the repo we just created on GitHub.com. The name of the repo should auto-complete.
Make sure the directory of the project is pointing to where you would like to store this project.

![Paste the URL of the repo into a new RStudio Version Control project](/Users/Layla/Documents/GitHub/lootedart/images/1_newproj.jpg)
  
  You've successfully created a version control project! The repo you created on
  GitHub will now be cloned to your local machine. 


####7. Let's Make Some Changes!

Let's open the README file and modify it. Add a line like "I'm going to push a change from RStudio"
and hit save.   
  
  To commit these changes:  
  
  * Click the Git tab in the upper right corner
  * Check the "Staged" box next to the README file.
  * Press "Commit"
  * Leave a "meaningful" commit message and press "Push"
  
  ![Commit the changes to the README file](/Users/Layla/Documents/GitHub/lootedart/images/1_commit.jpg)

  ![Leave a commit message and push the changes](/Users/Layla/Documents/GitHub/lootedart/images/1_push.jpg)

####8. Pulling

  Let's modify the README of your test repo on GitHub. Leave a new line like, 
  "This is a line from GitHub", leave a commit message, and  press commit.
    
  This should commit your change to the master branch but you will not see that
  change reflected in your project in RStudio. To see the change, go into the Git
  tab in the top right corner and press the blue "Pull" arrow. This will pull any 
  changes to the master remotely, locally.  
    
    *Tip: when working with collaborators, it's a good idea to pull changes first, 
    before pushing your local changes. Pull > Modify > Commit > Push

### Issues
  
#####Creating and Assigning Issues



## Project Management in RStudio

RStudio makes it easy organize and manage your project. Built-in functions, like "New Project" or "Import Data" aim to make your life a little easier. Let's start with creating a self-contained, reproducible project. It's a good idea to create a new project before starting a new script - that way, all data and code within that project can be easily picked back up after a break.

 How to create a project:

1. Click "File", "New Project"
2. Click "New Directory"
3. Click "New Project"
4. Name your project

