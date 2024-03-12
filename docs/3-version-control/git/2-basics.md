# Basics

## Creating a Repository

To create a new Git repository, navigate to the project directory and run the following command:

```bash
git init
```

This command initializes a new Git repository in the current directory.

## Cloning a Repository

To clone an existing Git repository, use the following command:

```bash
git clone <repository-url>
```

Replace `<repository-url>` with the URL of the repository you want to clone.

## Checking the Status

To check the status of your repository, use the following command:

```bash
git status
```

This command shows you the current status of your repository, including any changes that need to be committed or staged.

## Staging Changes

To stage changes for a commit, use the following command:

```bash
git add <file-name>
```

To stage all changes, use the following command:

```bash
git add .
```

## Unstaging Changes

To unstage changes, use the following command:

```bash
git restore --staged <file>
```

To unstage all changes, use the following command:

```bash
git reset HEAD .
```

## Discarding Changes

To discard changes in your working directory, use the following command:

```bash
git restore <file>
```

## Viewing Changes

To view the changes that have been staged, use the following command:

```bash
git diff --staged
```

To view the changes that have not been staged, use the following command:

```bash
git diff
```

## Committing Changes

To commit staged changes, use the following command:

```bash
git commit -m "commit message"
```

Replace `"commit message"` with a brief description of the changes you are committing.

## Viewing Commit History

To view the commit history, use the following command:

```bash
git log
```

To view a summarized version of the commit history, use the following command:

```bash
git log --oneline
```

## Ignoring Files

To ignore files in your repository, create a file named `.gitignore` in the root directory of your project and add the names of the files or directories you want to ignore. For example:

```plaintext
# Ignore .DS_Store files
.DS_Store

# Ignore log files
*.log

# Ignore node_modules directory
node_modules/
```

This file tells Git which files or directories to ignore when tracking changes.