# Cloning and Forking

## Cloning

Cloning is the process of copying a remote repository (and all of the information
that comes with it, such as commits) on to your local machine. To clone a repository
on to your local machine, open a terminal in the folder you want the cloned repo
to be in and use the following command:

```sh
git clone <repo-url>
```

You must supply the **repo url** to this command so it knows which repo to clone.
Refer to the section on remotes to learn how to get the URL of a repository.

Some things to note:

- Cloning will make a **new folder** to store the repo in. For example, if you are cloning a project called `discord-bot`, a folder with the same name will be created in the folder where the terminal is open. The folder will contain the code from the latest commit from the master/main branch (or whatever is the default branch) on the remote repository.
- Cloning will **automatically add a remote** to the new local repository. This remote, by convention, will be called `origin`, and the URL is the URL of the repo you cloned from.
- Unless you have **write permissions** to the remote repository, **you will not be able to push any changes you make on the cloned code.** To make and push changes (i.e. contribute) see _forking_ below and the section on _pull requests._

## Forking

If you intend to contribute to a project (make and push changes on the code of the project),
you need to have **write permissons** on the repository you want to push to. If the project
is someone else's (more often than not), this is not the case. If you want to make and push
changes to such a project, you must make a **fork.**

### What is a fork?

A fork is essentially a **copy** of a repository and all its information (contributors, commits
, etc.).

### Creating a Fork

Creating a fork of any project is as simple of going to the project you want to fork
and clicking the **Fork** button in the top right corner. This will create a copy of
the selected repository on your account (provided you are signed in to GitHub).

### Working With Forks

After you have created a fork, you can work with it as if you would work with
a regular remote repository.

- Start by **cloning** it.
- Then, make a **new branch** to develop a feature.
- Finally, **push** back to your fork.

You can then request to merge your changes from a branch on your fork into the
main project using a **pull request** (see section on Pull Requests).

### Notes on Forks

- You can update a branch of your fork with the `master` branch of the base repository by visiting the page of the branch on the fork and pressing the _Fetch Upstream_ button.
- Forks are not only used for the PR workflow (see section on Pull Requests). If the license of a project allows it, you can even fork a repo to change it completely and market it as a new project. An example of this is the **Neovim** text editor, which is originally a **fork** of the older text editor **Vim.** Even though Neovim is forked from Vim, Neovim is now completely its own project.

# When to Clone vs. Fork

To put it simply:

- Clone the base repository directly when you have **write access** to that repository (i.e. you own the project or are a collaborator)
- Fork the repository when you do **not** have write access; forks can be independently maintained or used to merge changes back in to the base repo via a Pull Request.
