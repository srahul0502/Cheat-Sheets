# ![Logo](https://github.com/srahul0502/Cheat-Sheets/blob/main/Git/logo.png) Ultimate Git Cheat Sheet 🚀

## Create Git Repository

### Remote Update
```bash
git remote update
```

## Branching

### List Branches
```bash
git branch
```

### Switch To Branch
```bash
git checkout branch
```

### Create New Branch
```bash
git branch new
```

### Create Branch From Existing
```bash
git branch new existing
```

### Delete Branch
```bash
git branch -D branch
```

### Tag Current Commit
```bash
git tag tag-name
```

### Create Branch and Switch
```bash
git checkout -b branch
```

## 🛠️ Local Changes

### Changed in Working Directory
```bash
git status
```

### Tracked File Changes
```bash
git diff
```

### Add Changed Files
```bash
git add file1 file2 file3
```

### Remove File
```bash
git rm file
```

### Remove Directory (Recursive)
```bash
git rm dir/ -r
```

### Move File
```bash
git mv [existing-path] [new-path]
```

### See Files Ready for Commit
```bash
git status
git diff --cached
```

### Commit Changes
```bash
git commit
```

### Commit Changes with Message
```bash
git commit -m "My Message"
```

### Commit All Tracked Files with Message
```bash
git commit -a -m "Message"
```

### Change Last Commit
```bash
git commit --amend
```

### Revert Changes To File
```bash
git revert HEAD
```

### Return To Last Committed State
```bash
git reset --hard HEAD
```

## 🏁 Starting a New Repository

### From Existing Directory
```bash
cd proj_dir
git init
git add .
```

### From Other Repository
```bash
git clone existing_dir new_dir
git clone [git repo url]
```

## 🌐 Managing Remotes

### List Remotes
```bash
git remote -v
```

### Show Information
```bash
git remote show remote
```

### Add Remote
```bash
git remote add path/url
```

### Fetch Changes
```bash
git fetch remote
```

### Fetch and Merge
```bash
git pull remote branch
```

### Publish Local to Remote
```bash
git push remote branch
```

### Delete Remote Branch
```bash
git push origin -d branch-name
```

### Publish Tags
```bash
git push origin/upstream --tags
```

## 🚀 Power Tips

### Show Distribution Info
```bash
head -n1 /etc/issue
```

### Explore Mounted File Systems
```bash
mount
```

### Display System Date
```bash
date
```

### Check System Uptime
```bash
uptime
```

### Reveal Your Identity
```bash
whoami
```

### Get Help with a Command
```bash
man command
```

## 🔄 Merge and Rebase

### Rewrite History
```bash
git rebase [branch]
```

### Merge Branch Into Current
```bash
git merge branch
```

### Rebase Into Branch
```bash
git rebase branch
```

### Rebase Into Branch from Master
```bash
git rebase master branch
```

### Abort Rebase
```bash
git rebase --abort
```

### Merge Tool to Resolve Conflicts
```bash
git mergetool
```

### View Merge Conflicts
```bash
git diff
```

### View Complete Conflict Diff
```bash
git diff --base $file
```

### Against Your Changes
```bash
git diff --ours $file
```

### Against Others' Changes
```bash
git diff --theirs $file
```

### Discard Conflicting Patch
```bash
git reset --hard
git rebase --skip
```

### After Resolving Conflicts
```bash
git add $conflicting_file
git rebase --continue
```

