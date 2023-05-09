---
title: "GitStudy"
author: "Ruby_Luo"
date: '2023-05-08'
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

# Step1: check git config environment
```{bash,warning=FALSE,echo=TRUE,eval=FALSE,message=FALSE}
#when you first use the git, you should config environment, the most important thing is the username and user email, it will be used to link to your github workplace later.
git config --global user.name "Lihua_Luo"
git config --global user.email imrubyluo@gmail.com
#check if it correct
git config --list
```

# Step2: submit files
```{bash,warning=FALSE,echo=TRUE,eval=FALSE,message=FALSE}
git init #初始化git仓库
git status
nano test1.txt
git add
git commit -m "first edit"
git log # check commit 
```

# Step3: Basic-1: Record changes
```{bash,warning=FALSE,echo=TRUE,eval=FALSE,message=FALSE}
#check the status of files
git status
#Add 1/2 onion to ingredients.txt and also the instruction to “enjoy!” to instructions.txt. Do not stage the changes yet (do not git add yet).
nano test1.txt # remember don't add it
git diff test1.txt # we can see the changes
```

# Step4: .gitignore
```{bash,warning=FALSE,echo=TRUE,eval=FALSE,message=FALSE}
vi .gitignore
ls -a 
```

# Step5: branch
```{bash,warning=FALSE,echo=TRUE,eval=FALSE,message=FALSE}
git branch experiment
git checkout experiment
git add ingredients.txt
git commit -m "hhh"
git log --oneline

nano ingredients.txt #add something inside
git add ingredients.txt
git commit -m "little change"
git log --oneline

#merge brunch 
git checkout master #before merge brunch, make sure you are in the master branch, and then merge
git merge experiment
git log --all --decorate --oneline --graph
```

# Step6: Tags
```{bash,warning=FALSE,echo=TRUE,eval=FALSE,message=FALSE}
git tag -a nobel-2021 -m "recipe I made for the 2021 Nobel banquet"
git show nobel-2021
```

# Step7: link git to github
```{bash,warning=FALSE,echo=TRUE,eval=FALSE,message=FALSE}
#creat a new repository named recipe first, and then
#or push an existing repository from the command line
git remote add origin git@github.com:Ruby-luo-0309/recipe.git
git branch -M main
git push -u origin main
#dd
```

