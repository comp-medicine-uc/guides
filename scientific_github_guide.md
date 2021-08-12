# 👨‍🔬👩‍🔬 GitHub guide for scientific projects

_Written by @pzuritas for @comp-medicine-uc. Inspired by [Ryan Abernathey's guide](https://rabernat.medium.com/scientific-collaboration-and-project-management-in-github-d74f2255ae5f) and various GitHub tutorials, most notably its own [guides](https://guides.github.com/)._

This guide assumes you have basic familiarity with Git and GitHub.

## 🤔 Why GitHub for scientific project management?

GitHub is perfect for **version control** and **collaboration** on the cloud, which makes it ideal for scientific projects. It also provides a nice interface through which to **track tasks** and various other quality of life features, such as native support for Jupyter Notebook displays.

## 📝 Some more GitHub concepts

GitHub provides more structure and features than Git alone to work. In particular, to manage a scientific project we have _issues_ and _projects_ in our _organization_.

### 🥼 Organization and teams

GitHub organizations provide a way for groups to organize their. The @comp-medicine-uc organization houses our work and repositories. Teams are subgroups of organizations which can be assigned to a specific project or repo, to stratify access.

### 🔬 Projects

GitHub projects are ways to keep track of work surrounding a large-scale endeavour (for example, a particular research line in the group encompassing several papers). They provide a kanban board for task management which is automatically connected to related issues (in other words, a cool to-do list).

### ✅ Issues

GitHub _issues_ are ways to keep track of tasks to be done in general, whether they be features to be implemented in code, bugs to be fixed, papers to be read, etc. Issues can be created in repos and assigned to one or more people with access to it. Issues can be _closed_ when they are resolved (i.e. when the task is done).

## 👨‍💻👩‍💻 Our workflow

The following lists a typical workflow for a scientific project with GitHub.

1. @dehurtado creates a project in the @comp-medicine-uc organization for your research project.

The project overview will be visible in [this webpage](https://github.com/orgs/comp-medicine-uc/projects). This page is good for a general overview, actual task management should be done through issues. It will update automatically.

2. @dehurtado creates a repo in the organization for your future paper.

3. Create an issue with a task and assing it to someone (yourself, probably).

Go to the repo's GitHub webpage, select the "Issues" tab and select the "New Issue" button. Write the task to be done as the issue title, and maybe a short description. On the sections to the right, asign the issue to the person responsible (probably yourself) and select the project it belongs to. Fianlly, select the "Submit new issue" button.

4. Work on the repo with Git and GitHub.

Work on the task assigned as normal, using typical GitHub commands, commiting and pushing your work regularly if necessary. You can comment observations and other things in the issue page that was created.

5. When a task is completed, close the issue.

Go to the "Issues" tab of your repo once again and select the issue corresponding to the completed task. Write an optional descriptive comment and select "Close issue". In the comment, you can optionally reference a commit by copying and pasting the commit's hash (its long code, something like `62efbb0f064d8645ffe86740edb8c5dde599f7d9`).

You can also close an issue _through_ a commit. If you commit something that closes an issue (completes a task), you can write `Closes [tag]` in the commit message to automatically close the issue when the commit is pushed, where `[tag]` is the issue's tag. For example, `"Added a new feature. Closes #3"` as a commit message will close issue #3.

6. Repeat 3-4-5-6 until paper is completed.


With this workflow, the repo stands as a nice snapshot of work done until now, with the commit history recording steady progress. Additionally, issues allow one to keep track of different tasks, and maybe work on many at a time without losing track of them.

## Some typical conventions and good practices

- Use English whenever possible as a universal language.
- Commit messages should be descriptive, not just `"Made some changes"`.
- Issue titles should be short, use the description and comment section for a longer discussion.
- Name repos and folders with kebab-case (e.g. `this-is-a-folder`) and files with snake_case (e.g. `this-is-a-folder/this_is_a_file.py`).
- Write code following style rules. A complete guide for Python can be seen [here](https://www.python.org/dev/peps/pep-0008/).
- Always write `README` files, remember they guide users that didn't work on the project.
- General good practices for scientific computing can be seen [here](https://swcarpentry.github.io/good-enough-practices-in-scientific-computing/).

> Personal comment: I like to start my commit messages with emoji when I can as an added tag. [Here's](https://gitmoji.dev/) a guide to doing so usefully.

## 📝 Collaborating with GitHub

You can use Git and GitHub with basically just four or five commands: `clone`, `commit`, `add`, `push` and maybe `pull`. However it has a ton more to offer which makes work easier. In particular, branches can be used for collaboration between two or more people.

### Branches

Branches are independent timelines of commits in a repo. Say two people are working on the same repo, but on different features of code. They can create a branch for each feature, work on it, and then merge the branch onto the main branch. The process of _merging_ allows collaborators to check for possible conflicts between their respective work, and resolve them before updating the repository. After merging, all commits in the branch are recorded in the main branch.

### Pull requests

When collaborating, you often want people to review your work. This can be done via _pull requests_. When working on your own branch, when you feel it is ready to be merged onto the main brach, you can open a pull request and asign reviewers. A pull request is a request for your branch to be merged onto the main branch (or pulled into it, hence the name). A pull request opens a special page for reviewing and commenting your work. When the reviewers approve of your work (maybe after a few more commits and discussion), you can close the pull request and merge onto the main branch.
