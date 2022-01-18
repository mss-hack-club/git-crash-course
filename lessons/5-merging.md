# Merging

Merging is a key functionality of Git that allows you to combine commits
from different branches (i.e. merge them).

## Merge Command

To merge a certain branch into another, first **switch to the branch you want to merge into** (not from).

For example, if you wanted to merge branch `B` _into_ branch `A`, you would first switch to A:

```sh
git checkout A
```

Then, you can use the merge command:

```sh
git merge B
```

## Merge Conflicts

Sometimes, you will run into **merge conflicts.** This normally happens when
the branch you're trying to merge has conflicting changes in specific sections
of some files.

For example, if you added a name to a file on line 8 and the branch you're merging in
(the incoming changes) try to add a different name to the _same_ line, you
would encounter a merge conflict.

### Merge Conflict Markers

When you encounter a merge conflict, Git inserts **merge conflict markers** into
your file.

Assume you are attempting to merge `incoming-branch` _into_ `master`. You checkout `master`
and attempt to merge, but there is a conflict.

A section of a file with merge conflicts has this setup with merge conflict markers:

- `<<<<<<< HEAD`: this is an **opening** merge conflict marker. It marks the _beginning_ of the conflicting section. This means: "from this point to the separator is how things **currently** are on the **current branch** (or the branch you're merging _into_, in this case `master`)"
- `=======`: this symbol marks the separating the HEAD section from the changes on the incoming branch. In essence, this means: "everything from here to the closing merge conflict marker are **incoming changes** (or how things are on the branch you're merging _from_, in this case `incoming-branch`)"
- `>>>>>>> incoming-branch`: this is a **closing** merge conflict marker. It marks the _end_ of the conflicting section

A file can have multiple of these conflicting sections. It is up to the user to resolve them (see below).

#### Resolving Merge Conflicts

Resolving merge conflicts are done by essentially keeping the changes you want from the options Git has given you.

- In the above example if you want to keep the changes coming in from `incoming-branch`, you would simply remove the merge conflict markers and the content on `master`, and keep the changes on `incoming-branch`.
- You would do the same if you wanted to keep the changes from `master`.
- If you want to keep **both**, simply remove all merge conflict markers and keep the conent from both sections.

##### Using the Editor for Merge Conflict Resolution

Many editors offer a functionality to make resolving the merge conflict easier.

For example, in **VSCode**, if you open a file with merge conflicts in it, you will
have the following options:

- **Accept Current Changes:** keeps the changes on HEAD (your current branch, in the example above `master`)
- **Accept Incoming Changes:** keeps the incoming changes (from the branch you're merging from, in the example above `incoming-branch`)
- **Accept Both Changes**: keeps all the changes from both branches
- **Compare Changes:** provides a comparison of both branches in question

Though it may seem complicated at first, all VSCode is really doing here is removing the merge
conflict markers for you.
