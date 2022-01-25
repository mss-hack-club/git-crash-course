# Pull Requests

Pull requests are possibly one of the most powerful features offered by remote
repository services such as GitHub. A pull request essentially allows you to request
to merge changes from a certain branch in one repository into a certain branch
on another repository. You can make pull requests on your own repository or even
across forks. Pull requests also give the capability for people to discuss and review
changes.

Here is how they work.

## The Contributing Workflow

Assume that there is an open source project you really want to contribute to.
Here is how you would go about doing that using the skills you have learned in this
Git and GitHub course.

1. Make a fork of the repository.
   a. This is to ensure you can make changes on the codebase and push them back to the cloud
2. Clone your new fork.
3. Make a new branch on your local clone of the fork.
   a. You almost never want to work on the `master` branch of your own repositories (even if it is a copy). It is best practice to make a new branch and merge.
4. Add and commit your changes.
5. Push the changes back to the remote branch (same branch name as the branch you made).
6. Create a pull request:
   a. Go to your fork on GitHub and go to the 'Pull Requests' tab.
   b. Select the repo and branch you want to merge _into_ on the _left._ E.g. if you want to merge your changes back in to the **base repo's master branch**, you would choose the base repo from the list and the master branch from that repo in the next box.
   c. Select the repo and the branch you want to merge _from_ on the _right_. Normally, you want to merge changes from your fork, so that is the repo you would choose. The branch should be the branch you pushed your changes to.
7. Wait for an **administrator** (someone with write access to the base repo) to accept your contribution.

### Notes

- You can make PRs on your own projects (this is advisable when your project grows bigger)
- Most projects have **contributing guidelines**, which you should make sure to read before contributing (there is normally useful information there).
  - Some projects have something called **Continuous Integration**, which is a series of tests that a PR must pass before being merged. The contributing guidelines are the place to understand how to make your code pass these tests.
- The workflow described above is exactly the way software development works in the real world, be it within a company or on an open source project. Therefore, learning this process early and practicing contributing will prove to be extremely beneficial.
