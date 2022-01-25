# Remotes

- Remotes repositories (commonly just referred to as remotes) are a _remote_ place
  (i.e. not on your computer) where you can store the information about your git repository.
- A local repository can have **any number of remotes.** Examples:
  - GitHub (most popular, we'll be using this one)
  - GitLab
  - BitBucket

## Creating a Remote Repository (GitHub)

To create a new GitHub repository, go to https://github.com and log in. Then
click on the **new repository** button. It is highly recommended for the remote
repository to have the **same name** as the local repository.

## Adding the Remote to Your Local Repo

Now that the remote repository, we can _link_ it to our local repository using
the following command:

```sh
git remote add <remote-name> <remote-url>
```

Notice that two things are needed to add a remote to a repository:

- **Remote name:** every remote you add to your local repo must have a name. This is so that git can tell the difference between this remote and others. The most common name/alias for a remote repository is **origin.**
- **Remote URL:** every remote must also have a URL, so git knows exactly where on the internet this repo is. You can get the URL for a remote on GitHub by going to the remote repo, clicking the **code** button in the top right, clicking HTTPS, and copying the link.

## Pushing Commits to the Remote Repository

Once a remote repository has been added to your project, you can **push** your commits
to the remote repository using this command:

```sh
git push <remote-name> <branch>
```

This too needs a few arguments to work properly:

- **Remote name:** this is where the remote name we made earlier comes into play. If the remote you want to push to is `origin`, that is what you would put in the slot of the first argument.
- **Branch name:** just like local repositories, remote repositories have branches. However, by default, there are _no branches_ on a remote repository to begin with. A branch is only created when commits from a local branch are **pushed** to it. This second argument is the name of the branch you want to push to (which needs to be the **same as your local branch**); this branch will be created if it doesn't already exist.

## Pulling Commits from the Remote Repository

Sometimes (especially if there are other people working on one project), a branch on the remote repository might be _ahead_ of a branch on your machine. To pull the missing commits from the remote branch, you can use the following command:

```sh
git pull <remote-name> <branch>
```

The arguments are the **same** as the `push` command.

## Tracking a Remote Branch

Git offers a feature where you can set up a local branch to **track** a remote branch.
Essentially, if you track a remote branch from a local branch, the following things happen:

- Any pushing or pulling operations will **no longer need arguments**. In essence, you don't need to type `git push origin master`. Instead you can type `git push`.
- When you execute `git status`, the command will show you a comparison of how far ahead/behind you are with the remote branch you're tracking.

You can use this command to track a remote branch:

```
sh
git branch -u <remote-name>/<branch>
```

This takes the **same** arguments as `git push`, but in a different format.
For example, if you were on the local `master` branch, and you wanted to track
the `master` branch on the `origin` remote, you would execute:

```sh
git branch -u origin/master
```

In the same situation, you can also track automatically when pushing using:

```sh
git push -u origin master
```

The `-u` option on `git push` means that the local branch will start tracking
the remote branch being pushed to.
