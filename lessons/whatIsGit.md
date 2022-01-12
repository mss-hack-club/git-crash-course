# What is Git?

Git is what we call "version control system", or a "source control manager".

## What is a repository?

- Set of collection of a set of files related to one another.
  - All the code required to run a project
- In order to track history with git, you have to be in a git **repository**
- You can make any file a git repository using the command:

```sh
git init
```

When this command is run, a **.git** folder is created in your folder, marking
it as a repository. _Never touch the .git folder (there is no reason to)._ It is
hidden for a reason (a hidden file/folder starts with a dot)

## Checking Status of Repository

At any point, you can check the **status** of a repository using the following command:

```sh
git status
```
