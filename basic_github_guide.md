# 💻 Basic introduction to Git and GitHub

_Written by [@pzuritas](https://github.com/pzuritas). Inspired by various GitHub tutorials, most notably its own [guides](https://guides.github.com/)._

This is a (very) basic introduction to Git and GitHub, made as a prologue for the second guide which outlines how to use GitHub for scientific project management.

## 🤔 What is Git and GitHub?

_Git_ is a version control system (VCS for short). It keeps track of the creation, deletion and changing of computer files, most importantly text files (code).

_GitHub_ is a hosting service for Git which provides free cloud storage and a ton of added structure which makes it great for collaboration and scientific production.

## 🧐 What do you need to use it?

You're going to need...

0. ... Git installed on your computer, available [here](https://git-scm.com/).

1. ... a GitHub account, which can be created for free in the GitHub [website](https://github.com/). PUC provides students with a "developer pack" which comes with professional licenses for a ton of useful stuff, so sign up with your @uc e-mail and follow instructions [here](https://education.github.com/pack) to access all of that.

2. ... to either **know how to use your command line** to navigate directories (`cd`, `ls` and the like) or to **learn how to use a GitHub GUI** (available, for example, in browser as the GitHub webpage, as a [desktop client](https://desktop.github.com/) or as a native integration in text editors like [VSCode](https://code.visualstudio.com/).) Windows users preferring to use the command line will have to install Git Bash when prompted during Git installation or use the Windows PowerShell, as the native Windows terminal is not a Unix shell.

3. You probably want a browser plugin like the [Chrome MathJax plugin](https://chrome.google.com/webstore/detail/mathjax-plugin-for-github/ioemnmodlmafdkllaclgeombjnmnbima?hl=en) to render LaTeX equations like this one $\Delta u = 0$ everywhere on GitHub (GitHub's Markdown doesn't render equations everywhere natively).

## ❗ Essential Git and GitHub concepts

Think of these as reserved keywords.

### 📁 Working directory

The _working directory_ is the **actual** directory of your files that you are working on. It is the fancy name for the folder in your computer which holds the files for your project.

### 🗂️ Repository (or repo for short)

The _repository_ is the most important Git unit. Roughly speaking, a repo is a storage unit for directories and files associated with a particular project, **along with their version history**. The repository, therefore, will hold all commited (see next section) **versions** of your working directory.

### 💾 Commit

Git doesn't automatically save all of your work. When you edit files in a working directory, you must `commit` your changes to the repo in order for them to be logged by Git. Commiting is therefore the act of telling Git that the changes you made are to be saved. A _commit_ (noun, not verb) is therefore a particular saved version of your repo's files, a snapshot. Commits should have a _commit message_ briefly describing what the commit changed.

### :octocat: Local repositories and remote repositories

Having Git installed on your computer allows you to commit your changes to a _local repo_, that is, a Git repository that is stored virtually in your computer. However, GitHub can store repos in the cloud for free and provides a friendly interface to engage with them. You therefore want to upload (or `push`) your local repo into GitHub's _remote repo_ so that the repository is stored in the GitHub service.

## 🌎 GitHub Hello World

This section shows **one** way to create a GitHub repo and store some changes in it.

### 1. Creating a repo directly on GitHub

On [github.com](https://github.com), sign in and find the "Repositories" side menu on the left. Select "New". In the "Create a new repository" page, write the repository's name, description and select some settings. Click "Create repository" when done.

### 2. _Cloning_ said repo into your computer

- GitHub Desktop users: on GitHub Desktop, select "File" -> "Clone repository". Select the repository and choose a path for your local working directory. Click "Clone".
- Command line users: on your command line interface, `cd` into the parent folder where you want to create your working directory. There, run `git clone [HTTPS]` where `[HTTPS]` is your repo's HTTPS URL, i.e. `https://github.com/user/repo-name.git`.

### 3. Creating and editing files in the working directory for said repo

After cloning, a new directory will have been created in your computer with the same name as the repository. Use it to work (create code files, subdirectories, etc).

### 4. _Staging_ the changes to commit them (only for command line users!)

If you want to save changes you made to your working directory, use the command `git add [file]` in your working directory where `[file]` is the file with changes that you want to save. The command is versatile, for example, using `*` instead of a file name will stage all changes made in the working directory. `add` is a command that _stages_ the changes you made so that they will be _commited_ all at once.

### 5. Commiting the changes to your local repo

- GitHub Desktop users: on GitHub Desktop, while in the relevant repository, select the changes to commit and write a commit message on the "Summary" text entry to the bottom left. When ready, select "Commit to *main*".
- Command line users: once your changes have been staged, run `git commit -m [message]` where `[message]` is a string that summarises the changes made. For example, `git commit -m "Added a new method"`. Note that quotation marks are needed.

### 6. Pushing the changes to the remote repo

- GitHub Desktop users: select "push" or "push origin" (the latter option will be available if you've never pushed or fetched from GitHub, as in, you've never connected your local repo to the GitHub repo).
- Command line users: run `git push` or `git push origin main` (the latter option is needed only for the first push of a repo).

### 7. Verifying that the remote repo on GitHub now has the previous commit

Go to the repo's website on GitHub and verify that your commit is there! Your changes should be visible, and the commit message should appear next to the relevant files.

### 8. Editing the files again and keeping up the good work

You can now continue to work on your working directory. Once you've made sufficient changes for a commit, repeat the process you've already done to push the changes to the GitHub repo.

### 10. Verifying that the remote repo has the entire commit history

Once you've made a few changes, go to the GitHub repo website and select the "N commits" text that appears right below the "Code" button. There you can see all the commits you've made to the repo as snapshots!

That's it! You now know the very basics of Git and GitHub. These services have a lot more to offer so be sure to check out other features when you're ready!

## 📚 Additional references

- [GitHub Guides](https://guides.github.com/): general GitHub and Markdown guides, very useful, but be sure to note that these are intended for collaboration on software.
- [Git and GitHub for poets](https://www.youtube.com/watch?v=BCQHnlnPusY): great tutorial that shows GitHub's usefulness beyond software engineering.
- [Make a README](https://www.makeareadme.com/): nice resource to make a good README file.
