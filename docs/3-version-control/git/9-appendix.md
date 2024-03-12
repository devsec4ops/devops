# GIT Commands

## Basic Commands
| Command                       | Description                                               |
| ----------------------------- | --------------------------------------------------------- |
| `git init`                    | Initializes a new Git repository in the current directory |
| `git clone <repository-url>`  | Clones an existing Git repository.                        |
| `git status`                  | Shows the current status of the repository.               |
| `git add <file-name>`         | Stages changes for a commit.                              |
| `git add .`                   | Stages all changes for a commit.                          |
| `git restore --staged <file>` | Unstages changes.                                         |
| `git reset HEAD .`            | Unstages all changes.                                     |
| `git restore <file>`          | Discards changes in the working directory.                |
| `git diff --staged`           | Shows the changes that have been staged.                  |
| `git diff`                    | Shows the changes that have not been staged.              |
| `git commit -m "message"`     | Commits staged changes with a message.                    |
| `git log`                     | Shows the commit history.                                 |
| `git log --oneline`           | Shows a summarized version of the commit history.         |

## Remote Commands
| Command                       | Description                                   |
| ----------------------------- | --------------------------------------------- |
| `git remote`                  | Lists the remotes for the current repository. |
| `git remote add <name> <url>` | Adds a new remote to the current repository.  |
| `git pull <remote> <branch>`  | Pulls changes from a remote repository.       |
| `git push <remote> <branch>`  | Pushes changes to a remote repository.        |

## Branching Commands
| Command                         | Description                                  |
| ------------------------------- | -------------------------------------------- |
| `git branch`                    | Lists all the branches in the repository.    |
| `git branch <branch-name>`      | Creates a new branch.                        |
| `git checkout <branch-name>`    | Switches to a different branch.              |
| `git checkout -b <branch-name>` | Creates and switches to a new branch.        |
| `git merge <branch-name>`       | Merges changes from one branch into another. |