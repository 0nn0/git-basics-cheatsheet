# Git Cheatsheet (Basics)

This cheatsheet is a list of our most used Git commands, and it countains useful information for those who are getting started.

It is available in the languages above. Since the translation rely on volunteers, the content between the available languages may vary.

- [English Version](#english-version)
- [Versão em Português](https://github.com/0nn0/git-basics-cheatsheet/tree/master/Português)

_In case you've missed, there's a list of our most used commands and shortcuts in the [Terminal for macOS](https://github.com/0nn0/terminal-mac-cheatsheet)._

## English Version

### Glossary

| Keywords                     | Description                                                                                                             |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| git                          | Open-source distributed version-control system, used to store code in repositories                                      |
| GitHub, GitLab and Bitbucket | Platform for hosting and collaborating on Git repositories                                                              |
| staging                      | Proposed files/directories that you'd like to commit                                                                    |
| commit                       | Saving all staged files/directories to your local repository                                                            |
| branch                       | An independent line of development, so you can develop features isolated from each other. Master branch is the default. |
| clone                        | Local version of a repository, including all commits and branches                                                       |
| remote                       | Common repository on eg. Github that all team members to keep that changes in sync with                                 |
| fork                         | Copy of a repository owned by a different user                                                                          |
| pull request                 | A method of submitting contributions to a repository                                                                    |
| HEAD                         | Represents your current working directory                                                                               |

### Configuration

| Key/Command                              | Description                                         |
| ---------------------------------------- | --------------------------------------------------- |
| `git config --global user.name [name]`   | Set author name to be used for all commits          |
| `git config --global user.email [email]` | Set author email to be used for all commits         |
| `git config color.ui true`               | Enables helpful colorization of command line output |

### Core Commands

| Key/Command                 | Description                                              |
| --------------------------- | -------------------------------------------------------- |
| `git init [directory]`      | Creates new local repository                             |
| `git clone [repo]`          | Creates local copy of remote repository                  |
| `git add [directory]`       | Stages specific [directory]                              |
| `git add [file]`            | Stages specific [file]                                   |
| `git add -A`                | Stages all changed files                                 |
| `git add .`                 | Stages new and changed files, NOT deleted files          |
| `git add -u`                | Stages changed and deleted files, NOT new files          |
| `git commit -m "[message]"` | Commit everything that is staged                         |
| `git status`                | Shows status of changes as untracked, modified or staged |

### Synchronization of Changes

| Key/Command   | Description                                                                           |
| ------------- | ------------------------------------------------------------------------------------- |
| `git fetch`   | Downloads all history from the remote branches                                        |
| `git merge`   | Merges remote branch into current local branch                                        |
| `git pull`    | Downloads all history from the remote branch and merges into the current local branch |
| `git push`    | Pushes all the commits from the current local branch to its remote equivalent         |

*Tip: `git pull` is the combination of `git fetch` and `git merge`*

### Undo Changes

| Key/Command                 | Description                                                                                 |
| --------------------------- | ------------------------------------------------------------------------------------------- |
| `git checkout -- [file]`    | Replace file with contents from HEAD                                                        |
| `git revert [commit]`       | Create new commit that undoes changes made in [commit], then apply it to the current branch |
| `git reset [file]`          | Remove [file] from staging area                                                             |
| `git reset --hard HEAD`     | Removes all local changes in working directory                                              |
| `git reset --hard [commit]` | Reset your HEAD pointer to previous commit and discard all changes since then               |

### Branches

| Key/Command                | Description                        |
| -------------------------- | ---------------------------------- |
| `git branch [branch]`      | Create a new branch                |
| `git checkout [branch]`    | Switch to that branch              |
| `git checkout [branch] -b` | Create and checkout new branch     |
| `git merge [branch]`       | Merge [branch] into current branch |
| `git branch -d [branch]`   | Deletes the [branch]               |
| `git push origin [branch]` | Push [branch] to remote            |
| `git branch`               | Lists local branches               |
| `git branch -r`            | Lists remote branches              |
| `git branch -a`            | Lists local and remote branches    |

### History

| Key/Command                | Description                                                      |
| -------------------------- | ---------------------------------------------------------------- |
| `git log`                  | Lists version history for the current branch                     |
| `git log --author=[name]`  | Lists version history for the current branch from certain author |
| `git log --oneline`        | Lists compressed version history for the current branch          |
| `git show [commit]`        | Outputs metadata and content changes of the specified commit     |
| `git blame [file]`         | Shows who changed what and when in file                          |

### Gitignore

You can list files/directories that you want to explicitely exclude from Git in a `.gitignore` file. This file should be placed at the root of your repository.

It is noted that people usually exclude dependency caches, such as `node_modules`, system files, such as `.DS_Store`, among others.

You can see the `.gitignore` file of [this repository](https://github.com/0nn0/git-basics-cheatsheet/blob/master/.gitignore) or [more examples](https://github.com/github/gitignore) provided by GitHub.

### Platforms

The following platforms can be used to host your repositories.

| Platform                           | Price |
| ---------------------------------- | ----- |
| [GitHub](https://github.com)       | Free  |
| [GitLab](https://gitlab.com)       | Free  |
| [Bitbucket](https://bitbucket.org) | Free  |

### Graphical User Interface (GUI)

Is the command-line interface not for you? Try one of the following clients.

| Clients                                      | Operational System | Price      |
| -------------------------------------------- | ------------------ | ---------- |
| [Github](https://desktop.github.com)         | Mac and Windows    | Free       |
| [Source Tree](https://www.sourcetreeapp.com) | Mac and Windows    | Free       |
| [Tower](https://www.git-tower.com)           | MacOS and Windows  | $69 to $99 |

### Resources
-   [Learn Git concepts, not commands](https://dev.to/unseenwizzard/learn-git-concepts-not-commands-4gjc)
-   [Syncing a Fork](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/syncing-a-fork)
-   [Flight rules for Git](https://github.com/k88hudson/git-flight-rules) - What to do when things go wrong...
-   [*Pro Git*](https://book.git-scm.com/book/en/v2)
-   [Git Flow](https://guides.github.com/introduction/flow/)
-   [Git and Github in Plain English](https://blog.red-badger.com/2016/11/29/gitgithub-in-plain-english)
-   [Learn Git Version Control using Interactive Browser-Based Scenarios](https://www.katacoda.com/courses/git)
