# Git Basics Cheatsheet

This cheatsheet is a list of our most used Git commands and useful information for those who are getting started.

It is available in a few languages. Since the translation rely on volunteers, the content between the available languages may vary. Choose one below:

-   [English Version](#english-version)
-   [Versão em Português](https://github.com/0nn0/git-basics-cheatsheet/tree/master/Português)

_In case you've missed, there's a list of our most used commands and shortcuts in the [Terminal for Mac](https://github.com/0nn0/terminal-mac-cheatsheet)._

## English Version

### GLOSSARY

| Keywords                | Description                                                                                                             |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| git                     | Open-source distributed version-control system, used to store code in repositories                                      |
| GitHub/Gitlab/Bitbucket | Platform for hosting and collaborating on Git repositories                                                              |
| staging                 | Proposed files/directories that you'd like to commit                                                                    |
| commit                  | Saving all staged files/directories to your local repository                                                            |
| branch                  | An independent line of development, so you can develop features isolated from each other. Master branch is the default. |
| clone                   | Local version of a repository, including all commits and branches                                                       |
| remote                  | Common repository on eg. Github that all team members to keep that changes in sync with                                 |
| fork                    | Copy of a repository owned by a different user                                                                          |
| pull request            | A method of submitting contributions to a repository                                                                    |
| HEAD                    | Representing your current working directory                                                                             |

### CONFIGURE

| Key/Command                            | Description                                         |
| -------------------------------------- | --------------------------------------------------- |
| git config --global user.name [name]   | Set author name to be used for all commits          |
| git config --global user.email [email] | Set author email to be used for all commits         |
| git config color.ui true               | Enables helpful colorization of command line output |

### CORE COMMANDS

| Key/Command               | Description                                              |
| ------------------------- | -------------------------------------------------------- |
| git init [directory]      | Creates new local repository                             |
| git clone [repo]          | Creates local copy of remote repository                  |
| git add [directory]       | Stages specific [directory]                              |
| git add [file]            | Stages specific [file]                                   |
| git add -A                | Stages all changed files                                 |
| git add .                 | Stages new and changed files, NOT deleted files          |
| git add -u                | Stages changed and deleted files, NOT new files          |
| git commit -m "[message]" | Commit everything that is staged                         |
| git status                | Shows status of changes as untracked, modified or staged |

### SYNCHRONIZE CHANGES

| Key/Command | Description                                                                                                                                        |
| ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| git fetch   | Downloads all history from the remote branches                                                                                                     |
| git merge   | Merges remote branch into current local branch                                                                                                     |
| git pull    | Updates local working branch with all new commits from the corresponding remote branch. `git pull` is a combination of `git fetch` and `git merge` |
| git push    | Pushes all local branch commits to remote repository                                                                                               |

### UNDO CHANGES

| Key/Command               | Description                                                                                 |
| ------------------------- | ------------------------------------------------------------------------------------------- |
| git checkout -- [file]    | Replace file with contents from HEAD                                                        |
| git revert [commit]       | Create new commit that undoes changes made in [commit], then apply it to the current branch |
| git reset [file]          | Remove [file] from staging area                                                             |
| git reset --hard HEAD     | Removes all local changes in working directory                                              |
| git reset --hard [commit] | Reset your HEAD pointer to previous commit and discard all changes since then               |

### BRANCHES

| Key/Command              | Description                        |
| ------------------------ | ---------------------------------- |
| git branch [branch]      | Create a new branch                |
| git checkout [branch]    | Switch to that branch              |
| git checkout [branch] -b | Create and checkout new branch     |
| git merge [branch]       | Merge [branch] into current branch |
| git branch -d [branch]   | Deletes the [branch]               |
| git push origin [branch] | Push [branch] to remote            |

### REMOTE REPOSITORIES

| Key/Command                | Description                        |
| -------------------------- | ---------------------------------- |
| git remote add [name][url] | Switch to that branch              |
| git fetch [remote][branch] | Merge [branch] into current branch |
| git pull [remote]          | Switch to that branch              |
| git push [remote][branch]  | Create and checkout new branch     |

### HISTORY

| Key/Command              | Description                                                      |
| ------------------------ | ---------------------------------------------------------------- |
| git log                  | Lists version history for the current branch                     |
| git log --author=[name]  | Lists version history for the current branch from certain author |
| git log --pretty=oneline | Lists compressed version history for the current branch          |
| git show [commit]        | Outputs metadata and content changes of the specified commit     |
| git blame [file]         | Shows who changed what and when in file                          |

### THE .gitignore FILE

You can list files/directories that you want to explicitely exclude from Git in a `.gitignore` file. This file should be placed at the root of your repository.

You might want to exclude:

-   Dependency caches such as /node_modules
-   Build output directories such as /build
-   Hidden system files such as .DS_Store
-   Personal IDE config files

Example `.gitignore` file:

```
# Comment in gitignore
node_modules/
.cache/
dist/
```

See [more examples](https://github.com/github/gitignore)

### PLATFORMS

The following platforms can be used to host your Git repositories.

| NAME                               | PRICE |
| ---------------------------------- | ----- |
| [Github](https://github.com)       | Free  |
| [Gitlab](https://gitlab.com)       | Free  |
| [Bitbucket](https://bitbucket.org) | Free  |

### GRAPHICAL USER INTERFACE (GUI) CLIENTS

Is the command-line not for you? Try one of the following GUIs.

| NAME                                         | OS                | PRICE           |
| -------------------------------------------- | ----------------- | --------------- |
| [Github](https://desktop.github.com)         | Mac and Windows   | Free            |
| [Source Tree](https://www.sourcetreeapp.com) | Mac and Windows   | Free            |
| [Tower](https://www.git-tower.com)           | MacOS and Windows | 59 USD per year |

### RESOURCES

-   [Flight rules for Git](https://github.com/k88hudson/git-flight-rules) - What to do when things go wrong...
-   [GitBook](https://book.git-scm.com)
-   [Git Flow](https://guides.github.com/introduction/flow/)
