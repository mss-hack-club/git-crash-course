# Branches

Branches are one of the most important concepts in git. A branch is a stream of
commits that diverges from a given root (much like a regular tree). For a visual
representation of Git branches, see [this picture.](https://img.search.brave.com/vxR__UqTnx0rZ9P3XDRX9BpZtLe_-AMPPAVRL9pia78/fit/1200/1200/ce/1/aHR0cHM6Ly9taXJv/Lm1lZGl1bS5jb20v/bWF4LzQ2NjQvMSpN/emR6WjFLeGZvbHdN/ZkxTRkN6Ull3LnBu/Zw)

## Purpose

Branches are a useful utility in that they allow you to continue development of
a given feature in an isolated environment where you don't affect the main line.

## The Master Branch

The `master` branch (sometimes called `main`) is normally the default branch in
a repository which contains a usable product. You typically don't want to develop
on the master branch; instead, develop on another branch and merge that branch
into `master` (see merging below).

## Creating a Branch

To create a branch, you can use the following command:

```sh
git branch <name of new branch> # note: do not include the <>
```

This will create a new branch **from the branch you are currently on.** If you were
on `master`, the new branch would have _all of master's commits_, but any new ones
you make would only be on the new branch.

### Specifying Base Branch

If you want to create a new branch from a certain _other_ branch, use:

```sh
git branch <name of new branch> <name of old branch> # again, don't include the <>
```

Example usage:

```sh
git branch new-branch master # creates a new branch based off the master branch
```

## Viewing Branches

To list all your branches, you can use:

```sh
git branch -a
```

## Switching to a Branch

To switch to a new branch, you can use the `checkout` command.

```sh
git checkout <branch-name>
```

### Create and Checkout Command

If you want to create a new branch _and_ check it out in one command, you can use:

```sh
git checkout -b <new-branch-name>
```

### Finding the Current Branch

At any point, you can view which branch you are currently on by using:

```sh
git status
```

## Deleting Branches

To delete a branch, you can use:

```sh
git branch -d <name-of-branch>
```

**Note:** you must be on a _different_ branch than the one you intend to delete,
or this will not work.

### Force Deleting

Sometimes, you may have changes on the branch you want to delete. In this case,
git will not allow you to delete the branch using `-d`. You can force Git to delete
the branch using:

```sh
git branch -D <name-of-branch>
```
