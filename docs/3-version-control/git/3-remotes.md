# Working with Remotes

## What are Remotes?

In Git, a remote is a common repository that is hosted on a server. It can be accessed by multiple developers, allowing them to collaborate on a project. Remotes are typically used to share code, track changes, and synchronize work between team members.

When you clone a repository, Git automatically creates a remote called `origin` that points to the original repository. This allows you to fetch, pull, and push changes to and from the remote repository.

## Adding a Remote

To add a remote to your local repository, use the following command:

```bash
git remote add <name> <url>
```

Replace `<name>` with a name for the remote (e.g., `origin`, `upstream`, `myfork`) and `<url>` with the URL of the remote repository.

For example, to add a remote named `upstream` that points to a repository on GitHub, you would use the following command:

```bash
git remote add upstream
```

## Pulling from Remotes

To pull changes from a remote repository, use the following command:

```bash
git pull <remote> <branch>
```

Replace `<remote>` with the name of the remote repository (e.g., `origin`, `upstream`) and `<branch>` with the name of the branch you want to pull from.

For example, to pull changes from the `master` branch of the `origin` remote, you would use the following command:

```bash
git pull origin master
```

You can just use `git pull` to pull changes from the remote repository that your current branch is tracking.

## Pushing to Remotes

To push changes to a remote repository, use the following command:

```bash
git push <remote> <branch>
```

Replace `<remote>` with the name of the remote repository (e.g., `origin`, `upstream`) and `<branch>` with the name of the branch you want to push to.

For example, to push changes to the `master` branch of the `origin` remote, you would use the following command:

```bash
git push origin master
```

You can just use `git push` to push changes to the remote repository that your current branch is tracking.



