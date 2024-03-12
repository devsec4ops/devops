# Branching

Branching is a powerful feature of Git that allows you to work on new features or bug fixes without affecting the main project code. It enables you to create isolated branches, work on them independently, and then merge them back into the main branch when ready.

## Main/Master Branch

The `main` or `master` branch is the default branch in Git. It typically represents the main project code and is the branch that is deployed to production.

When working on new features or bug fixes, it's common practice to create separate branches from the `main` or `master` branch, work on them, and then merge them back into the `main` or `master` branch when ready.

## Branching Commands

### Listing Branches

To list all the branches in a repository, use the following command:

```bash
git branch
```

### Creating a Branch

To create a new branch, use the following command:

```bash
git branch <branch-name>
```

Replace `<branch-name>` with the name of the new branch.

For example, to create a branch named `feature-1`, you would use the following command:

```bash
git branch feature-1
```

### Switching Branches

To switch to a different branch, use the following command:

```bash
git checkout <branch-name>
```

Replace `<branch-name>` with the name of the branch you want to switch to.

For example, to switch to the `feature-1` branch, you would use the following command:

```bash
git checkout feature-1
```

### Creating and Switching Branches

To create and switch to a new branch in one step, use the following command:

```bash
git checkout -b <branch-name>
```

Replace `<branch-name>` with the name of the new branch.

For example, to create and switch to a branch named `feature-2`, you would use the following command:

```bash
git checkout -b feature-2
```

### Merging Branches

To merge changes from one branch into another, use the following command:

```bash
git merge <branch-name>
```

Replace `<branch-name>` with the name of the branch you want to merge into the current branch.

For example, to merge changes from the `feature-1` branch into the `master` branch, you would use the following command:

```bash
git checkout master
git merge feature-1
```

## Branching Workflow
 
> `HEAD` is a reference to the currently checked out commit or branch in Git. It is a pointer that points to the current branch or commit.

To See the visualization of the git branching workflow, click [here](https://git-school.github.io/visualizing-git/#free) and follow below sequence of events.


* Consider a repository with a `master` branch and one commit as the starting point of the project. `HEAD` points to the `master` branch.

* To work on a new feature, create a new branch `feature` from the `master` branch using the command `git branch feature`.

* Commits are made to the `feature` branch to implement the new feature as you progress with the development using the command `git commit -m "message"`.


* You found out that there is a bug in the `master` branch that needs to be fixed. In order not to mix the bug fix with the new feature, create a new branch `bug-fix` from the `master` branch.
  * Checkout the `master` branch using the command `git checkout master`.
  * Create a new branch `bug-fix` from the `master` branch and checkout using the command `git checkout -b bug-fix`.

* Commits are made to the `bug-fix` branch to fix the bug using the command `git commit -m "message"`.

* Once the bug is fixed, merge the `bug-fix` branch into the `master` branch.
  * Checkout the `master` branch using the command `git checkout master`.
  * Merge the `bug-fix` branch into the `master` branch using the command `git merge bug-fix`.
    
* At this stage if your feature changes are complete, to include the new feature in the `master` branch, merge the `feature` branch into the `master` branch
  * Checkout the `master` branch using the command `git checkout master`.
  * Merge the `feature` branch into the `master` branch using the command `git merge feature`.

* However, lets consider a case where you need to make more changes and also require bugfix changes in your feature branch to test the changes. In this case, merge the `master` branch into the `feature` branch.
  * Checkout the `feature` branch using the command `git checkout feature`.
  * Merge the `master` branch into the `feature` branch using the command `git merge master`. This will include the bug fix changes in the `feature` branch.

* Make further changes to the `feature` branch and commit the changes using the command `git commit -m "message"`.

* Once the feature is complete, merge the `feature` branch into the `master` branch.
  * Checkout the `master` branch using the command `git checkout master`.
  * Merge the `feature` branch into the `master` branch using the command `git merge feature`.

* Finally, delete the `feature` branch using the command `git branch -d feature`.

* The `master` branch now contains the new feature and the bug fix changes.

This is a basic branching workflow in Git. It allows you to work on new features and bug fixes independently, and then merge them back into the main branch when ready.
