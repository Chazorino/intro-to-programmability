# Introduction to Git

Whether you come from a coding background or not, chances are, you have run into the need for a Version Control System (VCS).

Ever had any of these questions?
How do I make incremental changes and share my work with others?
How do I go back to the version of this file from (yesterday, last week, last year, ...)?
What changed between version X and version Y of a file?
People have been making changes to the same file (or set of files)... How do I reconcile and merge all these changes?

If you have ever asked yourself any of these questions, you have a need for a Version Control System.

Version Control Systems address problems like those described above and others that you probably haven't thought of yet (and we aren't including here!). They are powerful tools that help you share files, track changes to those files, and manage changes and contributions from authors and contributors.

Today, we are going to use Git and GitHub to:
Download a copy of the Sample Code you are going to work with to your laptop.
Get you started with a basic Git workflow.

Git is an open source (git-scm.com) Distributed Version Control System, while GitHub is a commercial company that runs GitHub.com, based on Git VCS tech.

Git is the underlying VCS technology and utility that is tracking changes and providing the tools to work with the files under "version control." GitHub is the cloud service we have chosen to host our sample code repository. GitHub enables content authors and contributors with both a place to host their version controlled files and powerful collaboration tools that support the content development and maintenance processes. GitHub also enables sharing and distribution of your version controlled files including mechanisms and tools for formal release versioning, content documentation and even static web hosting for your project.

## Basic Terminology

### Repository (Repo) 
A repository is essentially what its name describes: a vault (or repository) for storing the version-controlled files and data. On your computer a Git repository will look like a regular folder or directory, with one important difference: the repository directory will have a hidden .git/ subdirectory. This subdirectory is where Git stores the committed version controlled files and other repository data. You don't have to worry about or work with this hidden subdirectory, but now you know where the magic ✨ is!

### Working Directory
This is what you see on your computer when you look in the repository directory on your computer - the visible directory and its contents - these are your version-controlled and un-versioned files and folders.

### Versioned Files
Files that you have asked git to track.

### Un-Versioned Files
Files in your working directory that you haven't asked git to track.

### Commit
A commit is a snapshot in time of your version controlled files. Once committed, this snapshot is (almost) indelibly locked into the repository - always available for future retrieval and comparison.

### Branches
Branches enable parallel work within a repository. We create new branches to split-off work done by different people, to experiment with changes we might want to back out later, or to develop new features. Git provides tools to help visualize, reconcile and merge together changes made in different branches.

## Under the Hood
When you commit changes to version controlled files, Git stores full copies of all the changed files. It also stores a tree which contains links to all the changed files and previously-committed-unchanged-files in the current commit. Git computes a SHA1 hash of all stored files, trees and commits, and then uses the commit hashes to uniquely refer to individual commits. By computing and storing these hashes, git can detect changes to files and assure that the files retrieved from the repository are exactly as they were when committed to the repository.

"It's impossible to get anything out of Git other than the exact bits you put in." git-scm.com - Data Assurance

## Useful Git Commands
### Commit Authors - Telling Git Who You Are (one-time setup)
When you make a commit to a Git repository, Git automatically includes (in the indelibly hashed and stored commit) the name and e-mail address of the person that made the commit.
You need to tell git who you are before you can commit any changes to a repository.


### Cloning a Repository
When you want to work with someone else's code, you first have to get it on your machine. We do this with the git clone command. Please clone this repository with the command _git clone_ https://github.com/Chazorino/intro-to-programmability.git

Note: Please don't do it more than once. Having multiple copies of the code samples on your computer can cause confusion as to which one you are working with.

When you ran this command, the git client on your laptop connected to the URL provided and cloned a full copy of the repository to your machine. By the way, when we say "clone," we mean it. When you clone a repo you are indeed getting a complete copy of the repository and all of its contents. From the first commit to the last, you now have locally on your computer all of the files that have ever been committed to the repository. Don't believe me? Try running git log sometime (note if you do this in a repo with many commits, you can press space to page through the commits and q to quit).

Now that you have our repo on your computer, let's get it ready for you to edit and commit your changes.

### Prepare the Repo for Your Changes (Creating a Branch)
When you first clone a repository, you should be viewing and working on the ”main" branch, which just by convention of naming is the default branch for a repository.
You can verify what branch you are working on, and the current status of your working tree with the git status command.

If you started editing files on the master branch and committing your changes, your local repository would immediately be out of sync with the remote server, which isn't a problem... until it is. If someone else commits some changes to the master branch, and pushes their changes to the server before you push yours... You will have to merge (reconcile) their changes with your own before you can push your changes to the server. In fact, you cannot even get updates from the server on this branch until you reconcile the discrepancy. Sigh.

Wait... I thought this whole version control things was supposed to make collaborating on files easier!?! It does, but you need to create a branch!

You use the git checkout command to switch between branches, and adding the -b option to the checkout command causes Git to create a new branch - and then switch to it.
When you create a branch on your local repository, you are creating a safe place for you to make changes to the repo. Any changes you make and commit are committed locally to this new branch. Since you aren't making any commits to the branches that are synced with the remote server, any updates made to these other branches ("master" or otherwise) on the remote server, can easily be pulled down to your computer.


### Making a Commit
Committing your changes to a repository is a two-step process:

### Add - Stage files to be added to the commit with git add.
Commit - Commit the files to the repository with a commit message git commit.

The -m option lets you supply a short commit message right there on the command line. Without the -m option, Git would open your environment's default text editor (which on many systems is vim) so that you can enter a detailed and potentially lengthy commit message.

You should make it a personal practice to "commit often." Creating a commit is simple for you and a lightweight task for your computer. Committing often means that you are capturing more of the history of your code. You can go back and view commits and past changes anytime.

Yeah! My code (or some portion of it) is working!! Commit.

### Reverting Changes in Your Working Directory

Need: I made changes to a file, and now I want to revert those changes and get the original (last committed version) of the file back.
Solution: You can "checkout" the last version of the file to overwrite the changes you have made and restore the file to its last committed version.

Solution: You can "checkout" the last version of the file to overwrite the changes you have made and restore the file to its last committed version.


<div align="right">
   
   [Prev](README.md) - [Next](python_one_tasks.md)
</div>