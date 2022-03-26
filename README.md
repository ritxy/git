# Download git

https://git-scm.com/downloads

# What is Git

Git is an open source distributed version control system designed by Linux Torvalds to handle code projects.

Git is decentralized control version in opposition to SVN.
Each user have a complete copy of the repository with the full history in each machine.

# Concepts in Git

When you use Git you have a copy of all the repository files and the full history of the repository.

When you add or modify a file in your hard disk in your Git folder Git doesn't know anything about them.

First you have to add this files to an area called "staging area" and Git knows that the files are ready to be commited in the repository.

The next step is do a commit to make the changes be written in the repository.

If we have downloaded the code from a repository that is in a server we can upload our changes to make them available for the rest of the people doing a "push".

Areas:
* working directory -> The directory where are our files
* stage -> Is a place where the files are stored before do the commit
* repository -> Is where the files are placer after do a commit
    * The name of main branch of the repository is "main". You can have another branches for the modifications that you are doing for the project

# Note
Since some version now in Git the default branch has been renamed to main so in older projects your default branch will be named master and in the new projects will be main.

# Book about Git
You can read a free book about Git in their webpage in this address:
* https://git-scm.com/book/

# GIT COMMANDS

## Check git version

>git version

## Configure git

Configuration for all projects
>git config --global user.name "Developers name"

>git config --global user.mail "Developer@dev.com" 

Configuration just for one project
>git config user.name "Developers name"

>git config user.mail "Developer@dev.com"

The changes thar we are going to do in the repository will be doing with this credetentials and they will identify us.

When we create the repository we can create a file with the name **.gitignore**, inside of this file you can add what files or type of files that you don't want to have under control of git.

## Check git configutation

>git config --list

## Create a new repository, do it from the folder where you have your code

>git init

This commad will create a directory with the .git where is all the information of the repository.
Delete this folder if you don't want to have the code under control of git

## Clone a repository

>git clone https://github.com/ritxy/git.git
>>We clone the repository from one server to our local machine so we have all the repository in our local machine

## Check status of the repository

>git status

This command will tell us the status of the files inside the repository.
If there are files in the staged area, files that must be commited ...

## Stage a file

>git add README.md --> Put file README.md in the stating area
>git add -A --> Put all the files in the working directory in the stating area

## Unstage a file

>git restore --staged README.md

## Recover a file that has been modified but not has been staged yet

>git checkout file_modified
This will recover file from the last commit
The file must be tracked by Git

## Commit a file

>git commit README.md
>git commit README.md -m "Description of the commit"

With this command we add files in the repository and we can add a comment  describing the changes

## Add file to the latest commit

>git commit --ammend
>>This will add the latest files in the stage area and modify the comment of the commit. If there is any file to commit will let you change the message of the latest commit.

## Make an add and commit with message at the same time

>git commit -am "Message of the commit"
>>This command works with files that are tracking with Git

## Go back files since the last commit

>git checkout -- .
>>This will recover the files since the last commit. If some files are in the staging area they will not be recovered

## Show the log of the commits in the repository

>git log

## Clone a repository

>git clone <https://github.com/ritxy/git.git>

Download the code from a repository to our local machine. We will have all the history log.

## Show the differences between one local file and the file in the repository

>git diff name_of_the_file_to_diff

## Download the latest version of the code in the repository

>git pull origin main

## Upload code to the repository

>git push origin main

## Create a new branch

>git branch name_of_the_branch

> git checkout name_of_the_branch 
>>We must do this to start working with the new branch

We create a branch with the code of the main to work with it.
Later we will merge our branch with the main to put our changes available for the rest of the people.

## Upload a file inside the branch we are working

>git push -u origin name_of_the_branch_we_are_working

## Upload files from our branch to to main repository

>git checkout main
>>We change to the main branch

>git pull origin main
>>We download the latest changes in the main branch if our repository is shared in a network. If you are working in a project just in your computer this is not necessary.

>git branch --merged
>>Show the branches we have merged before

>git merge name_of_the_branch_we_are_working
>>Put the changes of the branch in the main branch

>git push origin main
>>We upload the code to the repository to make it available to the rest of the people

## Delete a branch we don't need anymore

>git push origin --delete name_of_the_branch_we_want_to_delete
>>Delete the branch from the repository from where we downloaded the code

>git push origin --delete name_of_the_branch_we_want_to_delete
>>With this we delete the branch from my local repository

## Git show branches

>git branch

>git branch -A
>>Show all the branches, branches in local and branches remotely



