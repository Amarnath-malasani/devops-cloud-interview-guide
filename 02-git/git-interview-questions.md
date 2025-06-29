
# 📘 Git Interview Questions and Answers

## 🟢 Beginner Level

### Q1: What is Git?
**A1:**  
Git is a distributed version control system that helps developers manage and track changes to their codebase. It allows collaboration with features like branching, merging, and conflict resolution.

### Q2: What is a repository in Git?
**A2:**  
A Git repository (or "repo") is a storage location for a project that includes all files, directories, and history of changes.

### Q3: How do you create a new Git repository?
```bash
git init
```

### Q4: What is the difference between Git and GitHub?
**A4:**  
- **Git** is a version control system.  
- **GitHub** is a platform to host and collaborate on Git repositories.

### Q5: What is the purpose of the `git clone` command?
```bash
git clone <repo-url>
```

### Q6: How do you commit changes in Git?
```bash
git add <filename>
git commit -m "Your message"
```

### Q7: Difference between `git pull` and `git fetch`?
- `git pull` = `git fetch` + `git merge`  
- `git fetch` only downloads updates without merging

### Q8: How do you resolve merge conflicts?
Edit the files manually, then:
```bash
git add <file>
git commit
```

### Q9: How do you revert a commit?
```bash
git revert <commit-hash>
```

### Q10: How do you push changes?
```bash
git push origin main
```

## 🟡 Intermediate Level

### Q1: Branch vs Tag?
- **Branch**: Movable pointer to a commit  
- **Tag**: Fixed reference to a commit, used for releases

### Q2: Merge branches
```bash
git checkout target-branch
git merge source-branch
```

### Q3: Purpose of `git rebase`?
For cleaner, linear history without merge commits.

### Q4: Undo last commit
```bash
git reset HEAD~1
# or
git revert HEAD
```

### Q5: Use of `git stash`
Temporarily save uncommitted changes:
```bash
git stash
git stash pop
```

### Q6: Revert file to previous commit
```bash
git checkout <commit-hash> -- <file>
```

### Q7: Use `git cherry-pick`
Apply a specific commit to a different branch:
```bash
git cherry-pick <commit-hash>
```

### Q8: Delete a branch
```bash
git branch -d <branch>            # Local
git push origin --delete <branch> # Remote
```

### Q9: View commit history
```bash
git log
```

## 🔴 Advanced Level

### Q1: When to use Git rebase?
- Linear commit history  
- Squash multiple commits  
- Clean up before merging

### Q2: `git pull` vs `git pull --rebase`
- `git pull`: Merge remote changes
- `git pull --rebase`: Reapply your commits on top of latest remote

### Q3: Squash commits
```bash
git rebase -i HEAD~n
```

### Q4: What is `git reflog`?
Shows history of all branch changes — useful to recover lost commits:
```bash
git reflog
```

### Q5: Set up Git hooks
Go to `.git/hooks/`, rename a `.sample` file, edit and make executable.

### Q6: Use `git bisect`
To find the commit that introduced a bug:
```bash
git bisect start
```

### Q7: Sign commits/tags
```bash
git commit -S -m "msg"
git tag -s v1.0 -m "Signed tag"
```

### Q8: Git submodules
```bash
git submodule add <repo-url>
```

### Q9: Set up Git server
Use platforms like GitLab CE, Gitea, or Gitolite.

### Q10: Recover deleted commit
```bash
git reflog
git cherry-pick <commit>
```

## 📚 Scenario-Based Q&A

### Scenario 1: Pull latest changes from team
```bash
git pull
```

### Scenario 2: Undo last commit, keep changes
```bash
git reset HEAD~1
```

### Scenario 3: Switch branches safely
```bash
git stash
git checkout <branch>
git stash pop
```

### Scenario 4: View file history
```bash
git log <file>
```

### Scenario 5: Discard changes in file
```bash
git checkout -- <file>
```

### Scenario 6: Remove specific commits
```bash
git rebase -i <commit>
```

### Scenario 7: Push only selected commits
```bash
git cherry-pick <commit>
```

### Scenario 8: Pull remote without losing local
```bash
git stash
git pull
git stash pop
```

### Scenario 9: Remove secrets from history
```bash
git filter-branch --force --index-filter "git rm --cached --ignore-unmatch <file>" --prune-empty --tag-name-filter cat -- --all
```

### Scenario 10: Change last commit message
```bash
git commit --amend
```

### Scenario 11: Split commit into two
1. `git rebase -i HEAD~n`
2. Mark commit as `edit`
3. `git reset HEAD^`
4. `git add` and `git commit` separately

### Scenario 12: Remove sensitive file completely
```bash
git filter-branch --tree-filter 'rm -f path/to/file' -- --all
```

### Scenario 13: Setup collaborative workflow
- `git clone <repo-url>`
- `git checkout -b feature`
- Work, push, create PR

### Scenario 14: Commit in wrong branch
```bash
git cherry-pick <commit>
git revert <commit>
```

### Scenario 15: Undo bad merge
```bash
git revert -m 1 <merge-commit>
```

### Scenario 16: Merge `main` into feature
```bash
git checkout main
git pull
git checkout feature
git merge main
```

## 🛠️ Top 10 Git Commands

```bash
1. git init                     # Initialize repo
2. git clone <url>             # Clone repo
3. git add <file>              # Stage file
4. git commit -m "msg"         # Commit changes
5. git status                  # Check status
6. git log                     # Commit history
7. git branch                  # List branches
8. git checkout <branch>       # Switch branch
9. git merge <branch>          # Merge
10. git push origin <branch>   # Push to remote
```
