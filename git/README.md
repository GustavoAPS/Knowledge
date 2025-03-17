# Git

Git is a free and open source distributed version controll system.

---

## Setup Git

Set a name that is identifiable for credit when review version history

```git
git config --global user.name “[firstname lastname]”
```


Set an email address that will be associated with each history marker

```git
git config --global user.email “[valid-email]”
```


Set automatic command line coloring for Git for easy reviewing

```git
git config --global color.ui auto
```

## Setup Respository and Init

initialize an existing directory as a Git repository

```git
git init
```

retrieve an entire repository from a hosted location via URL

```git
git clone [url]
```

## Stage & Snapshot

show modified files in working directory, staged for your next commit

```git
git status
```

Add a file as it looks now to your next commit (stage)

```git
git add [file]
```

Unstage a file while retaining the changes in working directory

```git
git reset [file]
```

Diff of what is changed but not staged

```git
git diff
```

Diff of what is staged but not yet commited

```git
git diff --staged
```

Commit your staged content as a new commit snapshot

```git
git commit -m “[descriptive message]”
```

## Branch & Merge


list your branches. a * will appear next to the currently active branch

```git
git branch
```

create a new branch at the current commit

```git
git branch [branch-name]
```

switch to another branch and check it out into your working directory

```git
git checkout
```

merge the specified branch’s history into the current one

```git
git merge [branch]
```

show all commits in the current branch’s history

```git
git log
```

## Inspect & Compare

show the commit history for the currently active branch
```git
git log
```
show the commits on branchA that are not on branchB
```git
git log branchB..branchA
```

show the commits that changed file, even across renames
```git
git log --follow [file]
```

show the diff of what is in branchA that is not in branchB
```git
git diff branchB...branchA
```

show any object in Git in human-readable format
```git
git show [SHA]
```


## Tracking Path Changes

delete the file from project and stage the removal for commit
```git
git rm [file]
```

change an existing file path and stage the move
```git
git mv [existing-path] [new-path]
```

show all commit logs with indication of any paths that moved
```git
git log --stat -M
```

## Ignoring Patterns

Save a file with desired paterns as .gitignore with either direct string
matches or wildcard globs.

```git
logs/
*.notes
pattern*/
```

System wide ignore patern for all local repositories

```
git config --global core.excludesfile [file]
```

## Share & Update


Add a git URL as an alias
```git
git remote add [alias] [url]
```

Fetch down all the branches from that Git remote
```git
git fetch [alias]
```

Merge a remote branch into your current branch to bring it up to date
```git
git merge [alias]/[branch]
```

Transmit local branch commits to the remote repository branch
```git
git push [alias] [branch]
```

Fetch and merge any commits from the tracking remote branch
```git
git pull
```

---

## Rewrite History

apply any commits of current branch ahead of specified one
```git
git rebase [branch]
```

clear staging area, rewrite working tree from specified commit
```git
git reset --hard [commit]
```

## Temporary commits

Save modified and staged changes
```git
git stash
```

list stack-order of stashed file changes
```git
git stash list
```

write working from top of stash stack
```git
git stash pop
```

discard the changes from top of stash stack
```git
git stash drop
```