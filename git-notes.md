# git diff-tree

## List of all files changed in a commit

```bash
git diff-tree --no-commit-id --name-only -r <commit-ish>
```

# git stash

https://git-scm.com/book/en/v2/Git-Tools-Stashing-and-Cleaning

## Saving current state of unstaged changes to tracked files

```bash
git stash -k
```

## Saving current state including untracked files

```bash
git stash -u
```

## Delete all stored stashes

```bash
git stash clear
```

## Show list of all saved stashes

```bash
git stash list
```

## Show the contents of any stash in patch form

```bash
git stash show -p <stash@{n}>
```


## Apply any stash without deleting from the stashed list

```bash
git stash apply <stash@{n}>
```

## Apply last stashed state and delete it from stashed list

```bash
git stash pop
```

## Apply last stashed state and stage it

```bash
git stash apply --index
```

## Saving current state interactively - only some chunks

```bash
git stash --patch
```

# git clean

## Before deleting untracked files/directory, do a dry run to get the list of these files/directories

```bash
git clean -n
```

## Forcefully remove untracked files

```bash
git clean -f
```

# git branch

## Rename a branch

```bash
git branch -m <new-branch-name>
```

# git rebase

## Stash changes before rebasing

```bash
git rebase --autostash
```

# git update-index

## Don’t consider changes for tracked file.

```bash
git update-index --assume-unchanged <file_name>
```

## Undo assume-unchanged

```bash
git update-index --no-assume-unchanged <file_name>
```

## Ignore one file on commit (e.g. Changelog).

```bash
git update-index --assume-unchanged Changelog;
```

```bash
git commit -a
```

```bash
git update-index --no-assume-unchanged Changelog
```

# git fixup

## Marks your commit as a fix of a previous commit.

```bash
git commit --fixup <SHA-1>
```

## Squash fixup commits normal commits.

```bash
git rebase -i --autosquash
```

# git add

## Interactive staging.

https://git-scm.com/book/en/v2/Git-Tools-Interactive-Staging

```bash
git add -i
```

# misc

## Always rebase instead of merge on pull.

```bash
git config --global pull.rebase true
```

## List all the alias and configs.

```bash
git config --list
```

## Dry run. (any command that supports dry-run flag should do.)

```bash
git clean -fd --dry-run
```

## stage git changes

```bash
git status | grep modified | awk '{ print $2 }' | fzf --multi | xargs git add
```

# clean git branches

## only list 'date(last commited) - branch name'
```bash
git for-each-ref --sort=committerdate refs/heads/ --format='%(committerdate:short) %(refname:short)' | grep -vE "main|master|develop"
```

## safe select branches to delete
```bash
git for-each-ref --sort=committerdate refs/heads/ --format='%(committerdate:short) %(refname:short)' | \
grep -vE "main|master|develop" | \
fzf --multi --header="Select branches to DELETE (Tab to mark, Enter to confirm)" | \
awk '{print $2}' | xargs git branch -d
```

## !!! select branches to FORCE delete !!!
```bash
git for-each-ref --sort=committerdate refs/heads/ --format='%(committerdate:short) %(refname:short)' | \
grep -vE "main|master|develop" | \
fzf --multi --header="Select branches to DELETE (Tab to mark, Enter to confirm)" | \
awk '{print $2}' | xargs git branch -D
```
