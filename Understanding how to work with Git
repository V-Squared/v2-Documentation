![](http://www.ghislainproulx.net/content/images/2014/GitHub101.jpg)


# Motivation
## We want:

- Collaborate with close friends efficiently
- Allow strangers to offer us project improvements easy to merge in
- Work fast even when working offline or with unreliable internet
- Have a working standard so we do not step on each others toes

This Articles provides the foundation to do all that.

## How we get it

**Workflow with strangers:**
Check out the diagram at the top. Say you are a stranger who wants to contribute to our project. You fork our project on GitHub, cloning our repo, but it now resides on your account and you have full access to it. You then clone onto your PC, which is where you work fast as all files are local. You create change and commit them to your repo. When you are satisfied with your improvements you upload them to your repo on GitHub and create a pull request with us. After some discussion we include your improvements into our development branch and eventually into our master branch.

**Workflow with core members:**
It works exactly the same, except that we do not fork but branch to begin with. Each new feature or each bug fix is a branch, that we work on exactly same way as describe above. Once the feature branch has been merged into the development branch it will be deleted.

## This article explains all that in more detail
Now that we are motivated and know what we want we are ready to dive into the details on how to get it:

# Table of Content

[TOC]



# Understanding how Git works is important

## Git is not GitHub
![](http://1.bp.blogspot.com/-WY2YpNr3W6g/UY6tZAc-H3I/AAAAAAAABLY/xJ9x3wIY8V8/s800/Github2.png)

- **GitHub:** Social Coding Collaboration Site on top of Git
- **Git:** Distributed Version Control System running on your Computer



## What Git is
![Git-Logo](https://git-scm.com/images/logo.png)

→ git►home-page](https://git-scm.com/)

Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

In plain English: Git manages your files, so that you can travel back in time to find older version (that still work) or it prevents your coworker to over write your changes when they work on the same files as you do. 



## What GitHub is
![GitHub Logo](http://doc.rultor.com/images/github-logo.png)

→ [GitHub►home-page](https://github.com/)

GitHub is a very nice, simple to use yet powerful web interface that sits on top of Git and adds a lot of collaborative features. Most important features from an open source standpoint are:

- Integrated issue tracking
- Pull requests with collaborative code review
- Text editor focused on collaboration
- Diff-Viewer for many file types, including code, .psd, .svg, .stl



## Why understanding how Git and GitHub work is important

In the beginning you will spend most of your time to learn and practice workflows. That is how to do things that move your project forward. Since Git is so flexible to support any workflow, it is hard to find documentation on a workflow that is best for you.

This leads to some experimentation and debugging. Such will fail if you do not have a very clear idea on how Git and GitHub work in the first place.

This Article focus on the principle ideas and concept how Git works, so you can master the subsequent learning of workflows without frustration, such as wondering why the hell Git did that or the opposite, how to get Git to do something, which it does not want to do as the designer of Git made it hard to do on purpose, as they decided what you want to do is is a stupid idea in the first place.



# Git Data Areas & Git Data Transport

## A definition of Git useful for this Chapter
The purpose of Git is to manage a project that is made of a set of files. Each set of files is a Version. The following chart shows you how the project is moving forward from Version 1 to V2 to V3 and so worth. It shows that in each version-bump some files are modified while others are not:

![](https://git-scm.com/book/en/v2/book/01-introduction/images/snapshots.png)

Git excels at coordinating and documenting changes done to the set of files for each version. This job is known as Version Control or Revision Management. 

Each Version is saved in the Git Repository in a compressed form. Each change is entered into the repository with a commit. 

Each commit creates a new snapshot of the set of files, also known as a version. If a version is released, it is called a release.

Git has different data areas to contain your set of files. When moving your project forward you will transport data between different data areas by means of git commands. Git tracks and archives this movement.

Tracking data transports between area sounds very boring. Instead very exciting is what this will allow you to do: Work with many people on the same set of files without stepping on each others toes as in overwriting each others work.

## What is a data area
You can have the same file in many different places. These places could be folders on your PC, could the staging area, the local repository or the remote repository. Within the repository there could be even different branches. All these places have different functions and may be of different types. But you will move your data from one place to another by means of got commands. In this Article we refer to the these places as "data area".

## What is data transport
When you transport your data from one data area to another. You will use data transport to get ready to work by getting the data you want to work on from your repository to your workspace (checking out) and you will finish your work by transporting your work (data) to the repository / repositories. (add / commit / push)

## Tracking data transport
Git is all about tracking data transport, labeling the data transport and tracking the data transport in the history or giving you change logs of what transport happens when you were not looking or which were so long ago that you forgot.

## Putting it together
![3 Git Areas with 3 transports](https://git-scm.com/book/en/v2/book/01-introduction/images/areas.png)
3 Git Areas with 3 transports

Above you see the 3 main Git Areas on your local computer: 1) Working Directory  2) Staging Area and 3) Local Repo. To get started you first check out a version from the repository by the checkout command. Git extracts the files and places them into the working directory. This is where you work on them, such as editing adding or deleting your files. When you are satisfied with one file, you stage it and move on to the next. Once you staged all files, you commit the new version back to the local repository. In case you wonder, to make this change public, you will still need to push it to the public repository. We will come to that.

## Files in Git Repository are compressed
![](https://software-carpentry.org/v5/novice/git/img/git-staging-area.svg)

This has two consequences:

1. A Git repository is very space efficient
2. If you want to access files, you need to get them out of the repository into the Working Area. See above.



# Git Data Areas

## ![Fork-Icon](https://cdn0.iconfinder.com/data/icons/octicons/1024/repo-forked-20.png) Fork
A fork is a consistent project with a distinct team of developers that move the project forward by committing to a set of repositories that differs from the original set of repositories from which the project was cloned to build the fork. 

**Forking a project is a good thing on GitHub:** If you want to contribute to an existing project to which you don’t have push access, you can “fork” the project. What this means is that GitHub will make a copy of the project that is entirely yours; it lives in your user’s namespace, and you can push to it.

This way, projects don’t have to worry about adding users as collaborators to give them push access. People can fork a project, push to it, and contribute their changes back to the original repository by creating what’s called a Pull Request, which we’ll cover next. This opens up a discussion thread with code review, and the owner and the contributor can then communicate about the change until the owner is happy with it, at which point the owner can merge it in.

In essence it means the original project is moving faster, as people who fork and offer pull request add development resources to the core team.

To fork a project, visit the project page and click the “Fork” button at the top-right of the page.


**Traditionally a fork was a bad thing:** In essence it meant that the developer community split into two independent development teams that from now on have different design goals. As such development speed would be reduced due to split resources.

## ![Branch-Icon](https://cdn0.iconfinder.com/data/icons/octicons/1024/git-branch-20.png) Branch 

A branch represents an independent line of development. The entire workflow of using a branch is exactly as with a fork described above, with the one important difference that a branch resides within the original repository, whereas a fork creates a new repository.

![GitHub-Branch](https://guides.github.com/activities/hello-world/branching.png)


## ![Git-Icon](https://cdn1.iconfinder.com/data/icons/Keyamoon-IcoMoon--limited/32/git.png) Git Repository

Your entire project resides in the git repository. Typically your project has many branches, such as the Master-Branch, Development-Branch, Feature1-Branch, Feature2-Branch, etc ... All these branches are stored 


## Git Areas on your Computer

## Branches



# Putting Git Areas on a map
![](http://www.intertech.com/PostingIMages/f05c4ce327e8_E7D5/IntroToGitConcepts_thumb.png)

## Local Git Areas on your Computer
- **Version Area aka Committed Files:** Each commit creates a new Version of the current branch in your repository
- **Staging Area aka Staged Files:** Collection of files ready to be committed
- **Working Area aka Development Workspace:** This is where you develop. Once a file is ready, you add it to the staging Area to compile the set of the new Version. Once the new Version is ready, you commit it into the current branch into the repository

## Remote Git Areas connected through the Internet
Your local repository can exchange data with many remote repositories which contain branches of the same project. Each Branch contains versions.


# How you tell Git to transport Data
![](https://git-scm.com/book/en/v2/book/01-introduction/images/areas.png)



# Git Data Transport handles conflicts


## Why Git needs Data Transport

## How you tell Git to transport Data

## Why conflicts are inevitable

## How Git detects conflicts

## How Git resolves conflicts





## Stash
A place to hide modifications while you work on something else

## Workspace / Working Tree
The place where you work on your files

## Staging / Index / cache:
The index (or "staging area") holds a snapshot of the content of the working tree. This snapshot is taken as the contents of the next commit.


## Committed files / Local repository

## Questions I still have on Git Areas on the computer

## Visible Files versus Repository
![](https://software-carpentry.org/v5/novice/git/img/git-staging-area.svg)

If you want to work or even see the files, you need to get them out of the repository and into the File System into your Working Files Directory:

![](http://marklodato.github.io/visual-git-guide/basic-usage-2.svg)



# Repositories

## Local Repository
A subdirectory named .git that contains all of your necessary repository files — a Git repository skeleton. Typical branches: master, feature-x, bugfix-y

## Upstream Repository
Version(s) of your project that are hosted on the Internet or network, ensuring all your changes are available for other developers. Default is "origin". Typical branches here: master, shared-feature-x, release-y


# Git Data Transport

## Git Data Transport Overview


## Git Data Transport Commands Overview
![Git Data Transport Overview](http://assets.osteele.com/images/2008/git-transport.png)


## Git Data Transport Commands Details

Git Cheatsheet ← Great!
- http://ndpsoftware.com/git-cheatsheet.html#loc=stash;



# The GitHub flow

## Lightweight: Master and Topic Branches
![The GitHub Flow](https://guides.github.com/activities/hello-world/branching.png)

GitHub is designed around a particular collaboration workflow, centered on branching with subsequent merging after a Pull Requests. This flow works the same whether you’re collaborating with a small team in a single shared repository, or network of strangers contributing to a project through dozens of forks. 

The only difference is that in the small team everyone has push access rights, whereas stranger will fork your repository, work on it and then ask you with a pull request to merge back their work into your repository

**For more details:**
→ [GitHub►Guides►Understanding the GitHub Flow](https://guides.github.com/introduction/flow/index.html)
→ [GitHub►Guides►Hello World](https://guides.github.com/activities/hello-world/)
→ [GitHub►Guides►Contributing by Forking](https://guides.github.com/activities/forking/)

Here’s is the rough overview:

1. Create a topic branch (or fork) from master.
2. Commit changes
3. Submit Pull Request 
4. Discuss, and optionally continue committing until integration master is satisfied
6. The integration master merges or closes the Pull Request.


**For more details on merging:**
Integrating Pull requests is the work of the [Integration Manager Workflow](https://git-scm.com/book/en/v2/Distributed-Git-Distributed-Workflows#_integration_manager). 

![Integration-manager workflow](https://git-scm.com/book/en/v2/book/05-distributed-git/images/integration-manager.png)

**Full Single Main Line Git Workflow**
![Single Main Line Git Flow](http://fbrnc.net/images/5/1/2/e/8/512e884650404668e1acd977e9355df42576fb0b-git.jpeg)

For more information → [Fabrizio Branca►Keeping it Simple: A Git Workflow](http://fbrnc.net/blog/2014/12/keeping-it-simple-git-workflow)

The essence of this simple workflow:

- Only one long lived branch: Master
- Stable Releases are on the Master Branch. They are marked by name.
- Development is going on also on the Master Branch, ahead of the last stable release
- No push is done to the Master Branch, only merges.
- Avoid merging a 2nd branch until testing of the last merge is complete. This is acceptable for small teams and short lived topic branches.

We will try this workflow first, as it promises to be simple yet powerful enough. A feature branch could still be worked upon by several developer who would push to the feature branch and collaborate on it until it is done. Only then it is merged into the Master Branch.



## Middleweight: Master, Develop and Topic Branches

Having only one Master Branch is simple, but it may lead to problems. It is common that during development you not only committed features but bugs as well. This becomes a problem on bigger projects where finding bugs in the Master could take days or weeks. To ensure the master branch only contains a stable release, the next best thing is to have three type of Branches:

![](https://git-scm.com/book/en/v2/book/03-git-branching/images/lr-branches-2.png)

- **Master Branch:** Stable and tested release
- **Development Branch:** The Branch into which all developments are merged from the topic branched
- **Topic Branches:** One Branch per topic. It is common that several topic branches are active the same time. A topic is either a new feature or a bug fix. Once development on the topic has been concluded the branch is merged into development and disappears. 

**Master** and **Development Branches live very *long* wheres **Topic** Branches are *short lived*. 

## Heavyweight: Powerful standardized branching
![](http://lanziani.com/slides/gitflow/images/gitflow_1.png)

This is a very well written Article → [Vincent Driessen►A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/)

It is a model well suited for larger projects. It is worth reading even if we first implement the simpler workflow!

## How Merging looks in SmartGitHg client
![](http://www.syntevo.com/smartgit/img/galery/hg-log.png)

We currently plan to use the Local Git Client SmartGitHg versus the Web Client of GitHub. Reasons are that we can work offline or we can work smoothly even considering the intermittent connection of the Chinese Internet.

Please notice the powerful diff view in the bottom and the visualization of the branches and their connection with merges.

## More reading on Git Workflow Options
- [Atlassian►Tutorials►Comparing Git Workflows](https://www.atlassian.com/git/tutorials/comparing-workflows)



# How Git stores Files in a repository
