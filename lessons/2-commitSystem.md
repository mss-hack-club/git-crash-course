# The Commit System

Git keeps track of commits using a mechanism called **commits.**

## What is a commit?

A commit is a **set of related changes** all bundled up together.

### Parts of a Commit

- Hash: a random sequence of auto-generated characters that Git uses to identify the commit
- Message: a human readable message (written by the person that commits) to say what took place in that commit

## The Types of Git Files

- Untracked files: files that Git is not currently tracking (normally means **new files**)
- Unstaged files: files that Git is tracking and have been modified
- Staged files: files that Git is tracking, have been changed, and have been marked for committing
- Ignored files: files and folders that Git has been explicitly told to ignore

### Staging Files

Staging files (marking them as "ready to commit") is done with the following command:

```sh
git add <file/folder>
```

Note: do not actually use the `<>`; simply put the name of the file or folder you want to stage.

To stage all the files in your repository (tracked and untracked) use:

```sh
git add .
```

### Committing Files

You can **commit** (bundle) all staged files using:

```
git commit -m "your message here"
```

Ensure you put your commit message (should be descriptive) in the quotes.
