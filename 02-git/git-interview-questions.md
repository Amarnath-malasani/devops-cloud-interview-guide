Git interview question and answers for BEGINER LEVEL


Q1: What is Git?

A1: Git is a distributed version control system that helps developers manage and track changes to their codebase. It allows multiple developers to work on a project simultaneously and facilitates collaboration by providing features such as branching, merging, and conflict resolution.

​

Q2: What is a repository in Git?

A2: A repository, often referred to as a "repo," is a central location where Git stores all the files and directories of a project, along with their complete history. It contains the entire version history of the project, including all the commits and branches.

​

Q3: How do you create a new Git repository?

A3: To create a new Git repository, you can navigate to the desired directory in your terminal and use the command `git init`. This command initializes a new empty Git repository in the current directory.

​

Q4: What is the difference between Git and GitHub?

A4: Git is a version control system, while GitHub is a web-based hosting service for Git repositories. Git is the technology that allows you to manage and track changes in your codebase, whereas GitHub provides a platform to store, collaborate, and share Git repositories with others.

 

Q5: What is the purpose of the "git clone" command?

A5: The `git clone` command is used to create a local copy of a remote Git repository. It downloads the entire repository, including all its files, commit history, and branches, to your local machine.

 

Q6: How do you commit changes in Git?

A6: To commit changes in Git, you need to follow these steps:
   1. Use the command `git add <filename>` to stage the changes you want to include in the commit.
   2. Use the command `git commit -m "Commit message"` to create a new commit with the staged changes. The commit message should provide a brief description of the changes.

 

Q7: What is the difference between "git pull" and "git fetch"?

A7: - `git pull` is a combination of two commands: `git fetch` and `git merge`. It fetches the latest changes from the remote repository and automatically merges them with the local branch.
- `git fetch` only downloads the latest changes from the remote repository, but it doesn't automatically merge them. It updates the remote-tracking branches, allowing you to review the changes before merging.

 

Q8: How do you resolve merge conflicts in Git?

A8: When a merge conflict occurs, it means that Git is unable to automatically merge the changes from different branches. To resolve the conflict, you need to manually edit the conflicting files to choose the desired changes. After resolving the conflicts, you can use the `git add` command to stage the changes, followed by `git commit` to complete the merge.

Q9: How do you revert a commit in Git?

A9: To revert a commit in Git, you can use the `git revert` command followed by the commit hash of the commit you want to revert. This command creates a new commit that undoes the changes introduced by the specified commit, effectively reverting it.

 

Q10: How do you push changes to a remote Git repository?

A10: To push changes to a remote Git repository, you can use the `git push` command followed by the name of the remote repository and the branch you want to push. For example, `git push origin main` pushes the local commits to the "main" branch of the remote repository named "origin."

These are just a few common Git interview questions for beginners. Remember to practice using Git commands and workflows to strengthen your understanding of version control and collaboration with Git.

Git interview question and answers for  INTERMEDIATE LEVEL
Q1: What is the difference between a branch and a tag in Git?

A1: In Git, a branch is a lightweight movable pointer to a specific commit. It allows for parallel development and isolates changes from each other. Developers can create new branches to work on new features or bug fixes. On the other hand, a tag is a reference to a specific commit that is used to mark a significant point in the project's history, such as a release or a stable version.

 

Q2: How do you merge two branches in Git?

A2: To merge two branches in Git, you typically follow these steps:
   1. Switch to the branch where you want to merge changes (e.g., `git checkout branch-to-merge-into`).
   2. Run the command `git merge branch-to-merge-from`. This merges the changes from the specified branch into the current branch.
   3. Resolve any merge conflicts, if they occur.
   4. Commit the merge changes using `git commit`.

 

Q3: What is the purpose of "git rebase"?

A3: Git rebase is a command used to integrate changes from one branch onto another by moving or combining commits. It is an alternative to merging and allows for a cleaner commit history. With rebase, you can apply a series of commits from one branch onto another, resulting in a linear commit history.

 

Q4: How do you undo the most recent commit in Git?

A4: To undo the most recent commit in Git, you have a few options:
   - You can use the command `git revert HEAD` to create a new commit that undoes the changes introduced by the last commit.
   - Alternatively, you can use `git reset HEAD~1` to move the branch pointer back one commit, effectively removing the last commit. This operation discards the commit and any changes associated with it.

 

Q5: What is the "git stash" command used for?

A5: The `git stash` command allows you to temporarily save changes that are not ready to be committed yet. It's useful when you need to switch to a different branch or apply a hotfix but don't want to commit incomplete work. You can later retrieve the changes from the stash using `git stash apply` or `git stash pop`.

 

Q6: How do you revert a file to a previous commit in Git?

A6: To revert a file to a previous commit in Git, you can use the command `git checkout <commit-hash> -- <file>`. This command replaces the content of the specified file with the version from the given commit. It effectively discards the changes made to the file since that commit.

 

Q7: What is the purpose of the "git cherry-pick" command?

A7: The `git cherry-pick` command is used to apply a specific commit from one branch onto another branch. It allows you to select individual commits and apply them to a different branch, without merging the entire branch. Cherry-picking is useful when you want to selectively apply changes from one branch to another.

 

Q8: How do you delete a branch in Git?

A8: To delete a branch in Git, you can use the command `git branch -d <branch-name>`. This deletes the specified branch locally. If the branch has not been merged, you can use `git branch -D <branch-name>` to force delete it. To delete a remote branch, you can use `git push origin --delete <branch-name>`.

 

Q9: How do you view the commit history in Git?

A9: You can use the command `git log` to view the commit history in Git.

​

Git interview question and answers for ADVANCED LEVEL
Q1: What is Git rebase, and when would you use it?

A1: Git rebase is a command used to modify the commit history of a branch. It allows you to move, combine, or edit commits. You would use `git rebase` when you want to:
- Incorporate changes from one branch onto another with a linear commit history.
- Squash multiple commits into a single commit for a cleaner history.
- Edit or reorder commits to improve readability or resolve conflicts.

 

Q2: What is the difference between `git pull --rebase` and `git pull`?

A2:  - `git pull --rebase` combines the `git fetch` and `git rebase` commands. It downloads the latest changes from the remote repository and then replays your local commits on top of the updated branch, resulting in a linear commit history.
- `git pull` also combines `git fetch` and `git merge`. It downloads the latest changes and merges them into the current branch, creating a merge commit if necessary.

 

Q3: How do you squash multiple commits into a single commit?

A3: To squash multiple commits into a single commit, you can use the interactive rebase feature:
- Run `git rebase -i HEAD~n`, where `n` is the number of commits you want to squash.
- In the interactive rebase editor, change "pick" to "squash" (or "s") for the commits you want to squash.
- Save and exit the editor. Git will combine the selected commits into one and prompt you to provide a new commit message.

 

Q4: What is the "git reflog" command used for?

A4: The `git reflog` command shows a log of all reference changes in your repository, including branch checkouts, commits, resets, and other operations. It is helpful for recovering lost commits or branches, as it provides a history of recent operations even if branch references have been deleted.

 

Q5: How do you set up Git hooks?

A5: Git hooks are scripts that can be executed automatically before or after certain Git events, such as commits or pushes. To set up Git hooks:
- Navigate to the `.git/hooks` directory in your repository.
- Rename the hook you want to use (e.g., `pre-commit.sample`) to remove the `.sample` extension.
- Customize the hook script by adding your desired commands or actions in the corresponding file.

 

Q6: What is the purpose of the "git bisect" command?

A6: The `git bisect` command helps in finding the specific commit that introduced a bug or regression in your codebase. It performs a binary search through the commit history, automatically checking out different points in time and allowing you to mark commits as good or bad until the faulty commit is identified.

 

Q7: How do you sign commits and tags in Git?

A7: Git supports commit and tag signing using GPG (GNU Privacy Guard) to verify the authenticity and integrity of commits and tags. To sign commits and tags:
- Configure Git to use your GPG key: `git config --global user.signingkey <key-id>`.
- Sign commits: `git commit -S -m "Commit message"`.
- Sign tags: `git tag -s <tag-name>`.

 

Q8: What are Git submodules?

A8: Git submodules allow you to include a separate Git repository as a subdirectory within your main repository. Submodules are useful when you want to include external dependencies or reuse code from other repositories while keeping them separate and manageable as individual repositories.

 

Q9: How do you set up a Git server?

A9 : There are various ways to set up a Git server, such as using GitLab, Bitbucket, or hosting your own Git server. For self-hosted Git servers, you can use software like Gitolite, Gitea, or GitLab Community Edition to manage and provide Git hosting capabilities.

 

Q10: How can you recover a deleted commit in Git?

A10: If a commit has been deleted or lost, you can use the `git reflog` command to find the commit's reference and recover it. Once you identify the commit hash, you can create a new branch or use `git cherry-pick` to apply the changes from the recovered commit to the appropriate branch.

These advanced-level Git interview questions cover topics that require a deeper understanding of Git's features and workflows. Keep practicing and exploring Git to enhance your proficiency with version control.

​

Git interview question and answers SCENARIO BASED
Scenario 1:
John and Sarah are working on a project together using Git. John made some changes to a file, committed them, and pushed to the remote repository. Now Sarah wants to update her local repository with John's changes. How can Sarah do this?

Answer 1:
Sarah can update her local repository with John's changes by running the following command:
```
git pull
```
This command fetches the changes from the remote repository and merges them into Sarah's current branch.

​

Scenario 2:
Alice has made some changes to a file and committed them locally. However, she realized that she made a mistake and wants to undo the last commit. How can she do this?

Answer 2:
Alice can undo the last commit by using the following command:
```
git reset HEAD~1
```
This command moves the branch pointer one commit behind, effectively removing the last commit. The changes made in that commit will still be present in Alice's working directory, allowing her to make the necessary corrections.

​

Scenario 3:
Mark is working on a feature branch for a long-running project. However, he wants to switch to a different branch to work on a critical bug fix. What should Mark do to switch branches without losing his changes?

Answer 3:
To switch branches without losing his changes, Mark should first commit his changes on the current branch using the following commands:
```
git add .
git commit -m "Save work in progress"
```
Then, he can switch to the desired branch using the command:
```
git checkout <branch-name>
```
Once he completes the bug fix, he can switch back to the feature branch using the same command and continue his work.

​

Scenario 4:
Emma wants to see the history of commits for a particular file in the repository. How can she do that?

Answer 4:
Emma can view the history of commits for a specific file by running the following command:
```
git log <file-name>
```
This command displays the commit history related to the specified file, showing the commit hash, author, date, and commit message for each commit.


Scenario 5:
You've made some changes to a file in your local Git repository and realized that those changes were incorrect. What should you do to discard those changes and revert the file to its previous state?

Answer:
To discard the changes and revert the file to its previous state, you can use the `git checkout` command followed by the file name. Here's the command you can use:

```
git checkout -- <file>
```

This command will replace the current changes in the file with the last committed version, effectively discarding the incorrect changes.

​

Scenario 6:
 You are working on a feature branch in Git, and you realize that some of the changes you made are incorrect and need to be removed. How can you selectively remove specific commits from your branch history?

A6: You can use the git rebase command with the interactive mode to remove specific commits from your branch history. Run the command git rebase -i <commit> where <commit> is the commit before the first commit you want to remove. In the interactive mode, you can delete or squash the commits you don't need. Save the file and exit the editor to apply the changes.

​

Scenario 7:

You have been working on a local branch in Git and want to make it available to others by pushing it to a remote repository. However, you don't want to push all the commits in the branch. How can you push only selected commits to the remote repository?

A7: You can use the git cherry-pick command to pick specific commits and apply them to another branch. First, create a new branch from your current branch using git branch <new-branch-name>. Then, use git cherry-pick <commit> for each commit you want to include in the new branch. Finally, push the new branch to the remote repository using git push origin <new-branch-name>.

​

Scenario 8:

You have made some changes in your local branch and want to update it with the latest changes from the remote branch. However, you don't want to lose your local changes. What is the recommended approach to incorporate the remote changes while keeping your local changes intact?

A8: You can use the git stash command to temporarily save your local changes. Run git stash to stash your changes, and then use git pull to fetch and merge the latest changes from the remote branch. Afterward, use git stash apply or git stash pop to reapply your local changes on top of the updated branch.

​

Scenario 9: You are collaborating with a team on a Git repository, and someone accidentally pushes sensitive information, such as API keys, to the remote repository. How can you remove those sensitive files from the repository history?

A9: To remove sensitive files from the repository history, you can use git filter-branch. Run the command git filter-branch --force --index-filter 'git rm --cached --ignore-unmatch <file-path>' --prune-empty --tag-name-filter cat -- --all where <file-path> is the path to the sensitive file. This command will remove the file from the entire history. Remember to inform your team members about the change as they will need to rebase their work on the updated history.

​

Scenario 10: You have made a mistake in a commit message and want to modify it. How can you change the commit message of the most recent commit?

A10: You can use the git commit --amend command to modify the most recent commit message. Run git commit --amend, and your default text editor will open with the current commit message. Edit the message, save the file, and exit the editor. The commit message will be updated with the new content.
 

Scenario 11:
You are working on a new feature branch, and you realize that some of the changes you made in a commit should have been in a separate commit. How would you split the commit?

Answer:
To split a commit into separate commits, you can use the interactive rebase feature of Git:
1. Run `git rebase -i HEAD~n`, where `n` is the number of commits you want to modify, including the commit you want to split.
2. In the interactive rebase editor, change "pick" to "edit" (or "e") for the commit you want to split.
3. Save and exit the editor. Git will stop at the commit you want to split.
4. Use `git reset HEAD^` to unstage the changes from the commit.
5. Use `git add` to selectively stage the changes you want in the new commit.
6. Use `git commit -m "New commit message"` to create a new commit with the staged changes.
7. Use `git rebase --continue` to resume the rebase process and automatically apply the remaining commits.

​

Scenario 12:
You accidentally committed a sensitive file that should not be included in the repository. How would you remove it from Git history?

Answer:
To remove a sensitive file from Git history, you can use the following steps:
1. Make sure you have a backup of the sensitive file.
2. Run `git filter-branch --tree-filter 'rm -f path/to/sensitive/file' -- --all` to remove the file from the entire history of all branches.
3. Wait for the command to complete. It may take some time, especially for large repositories.
4. After the filter-branch process finishes, run `git push --force` to update the remote repository and overwrite its history with the updated local history.
5. Communicate with other team members and ensure they also update their local repositories by running `git fetch --all` followed by `git reset --hard origin/master` (or the appropriate branch).

​

Scenario 13:
You need to collaborate with another developer on a new feature. How would you set up and manage a collaborative workflow using Git?

Answer:
To set up and manage a collaborative workflow in Git, you can follow these steps:
1. Create a shared remote repository (e.g., on GitHub, GitLab, or a self-hosted server) and give access to the other developer.
2. Each developer clones the remote repository to their local machine using `git clone <repository-url>`.
3. Create a new branch for the feature using `git checkout -b feature-branch`.
4. Develop and make changes in the feature branch, committing and pushing regularly to the remote repository.
5. Use pull requests (PRs) or merge requests to review and merge the changes. The other developer can review the changes, provide feedback, and suggest improvements.
6. Resolve any conflicts that may occur during the review or merge process.
7. After the changes are approved, merge the feature branch into the main branch (or an appropriate branch) using PRs or the `git merge` command.
8. Delete the feature branch once it is merged: `git branch -d feature-branch`.
9. Regularly fetch and pull changes from the remote repository to stay up to date with the work of other developers: `git fetch origin` and `git pull origin <branch-name>`.

These scenario-based Git interview questions assess your practical knowledge and problem-solving skills related to specific situations that may arise during software development with Git. Remember to understand the underlying concepts and practice Git commands to effectively handle such scenarios.

​

Scenario 14:
You accidentally pushed a commit to the wrong branch. How would you revert that commit and apply it to the correct branch?

Answer:
To revert the commit and apply it to the correct branch, you can follow these steps:
1. Identify the commit hash of the commit you want to revert.
2. Run `git log` to find the commit hash and note it down.
3. Checkout the correct branch using `git checkout correct-branch`.
4. Run `git cherry-pick <commit-hash>` to apply the commit to the correct branch.
5. Resolve any conflicts that may occur during the cherry-pick process.
6. After resolving conflicts, commit the changes using `git commit`.
7. If you no longer need the commit in the wrong branch, you can run `git branch -D wrong-branch` to delete the branch (replace `wrong-branch` with the actual branch name).

​

Scenario 15:
You are working on a project with multiple contributors, and you accidentally merged a feature branch with a bug into the main branch. How would you revert the merge and fix the bug?

Answer:
To revert the merge and fix the bug, you can follow these steps:
1. Identify the commit hash of the merge commit that introduced the bug.
2. Run `git log` to find the commit hash and note it down.
3. Checkout the main branch using `git checkout main`.
4. Run `git revert -m 1 <commit-hash>` to create a new commit that undoes the changes from the merge commit. The `-m 1` option specifies the main branch as the parent.
5. Resolve any conflicts that may occur during the revert process.
6. After resolving conflicts, commit the changes using `git commit` with an appropriate message mentioning the bug fix.
7. Push the changes to the remote repository using `git push origin main` to share the bug fix with other contributors.

​

Scenario 16:
You are working on a long-lived feature branch, and you want to keep it up to date with the changes in the main branch. How would you incorporate the latest changes from the main branch into your feature branch?

Answer:
To incorporate the latest changes from the main branch into your feature branch, you can follow these steps:
1. Commit or stash any pending changes in your feature branch to avoid conflicts.
2. Checkout the main branch using `git checkout main` and run `git pull` to fetch and merge the latest changes.
3. Checkout your feature branch again using `git checkout feature-branch`.
4. Run `git merge main` to merge the changes from the main branch into your feature branch.
5. Resolve any conflicts that may occur during the merge process.
6. After resolving conflicts, commit the changes using `git commit`.
7. If you had stashed changes in step 1, you can apply them again using `git stash apply` or `git stash pop`.

These additional scenario-based Git interview questions delve into specific situations you may encounter while working with Git in real-world scenarios. Understanding the concepts behind each scenario will help you respond effectively and demonstrate your proficiency in Git.

GIT Commands
1. git init: Initialize a new Git repository.
   Example: `git init`

 

2. git clone: Clone a remote repository to your local machine.
   Example: `git clone https://github.com/user/repo.git`

 

3. git add: Add files or changes to the staging area.
   Example: `git add file.txt`

 

4. git commit: Commit the staged changes to the repository.
   Example: `git commit -m "Commit message"`

 

5. git status: Show the current status of the repository.
   Example: `git status`

 

6. git log: View the commit history.
   Example: `git log`

 

7. git diff: Show the differences between files or commits.
   Example: `git diff file.txt`

 

8. git branch: List, create, or delete branches.
   Example: `git branch branchname`

 

9. git checkout: Switch to a different branch.
   Example: `git checkout branchname`

 

10. git merge: Merge changes from one branch into another.
    Example: `git merge branchname`

 

11. git remote: Manage remote repositories.
    Example: `git remote add origin https://github.com/user/repo.git`

 

12. git push: Push local changes to a remote repository.
    Example: `git push origin branchname`

 

13. git pull: Fetch and merge changes from a remote repository.
    Example: `git pull origin branchname`

 

14. git fetch: Fetch changes from a remote repository.
    Example: `git fetch origin`

 

15. git stash: Save changes that are not ready to be committed.
    Example: `git stash`

 

16. git stash pop: Apply the most recent stash and remove it from the stash list.
    Example: `git stash pop`

 

17. git reset: Reset the repository to a previous commit.
    Example: `git reset commit_hash`

 

18. git revert: Create a new commit that undoes a previous commit.
    Example: `git revert commit_hash`

 

19. git tag: Create and manage tags for marking specific points in history.
    Example: `git tag v1.0.0`

 

20. git remote -v: View the URLs of the remote repositories.
    Example: `git remote -v`

 

21. git config: Set or get repository options.
    Example: `git config --global user.name "Your Name"`

 

22. git show: Show the details of a specific commit.
    Example: `git show commit_hash`

 

23. git cherry-pick: Apply a specific commit from one branch to another.
    Example: `git cherry-pick commit_hash`

 

24. git rebase: Reapply commits on top of another base commit.
    Example: `git rebase branchname`

 

25. git blame: Show who changed which lines in a file.
    Example: `git blame file.txt`

 

26. git remote add: Add a new remote repository.
    Example: `git remote add origin https://github.com/user/repo.git`

 

27. git remote remove: Remove a remote repository.
    Example: `git remote remove origin`

 

28. git log --oneline: Show the commit history in a condensed format.
    Example: `git log --oneline`

 

29. git log --graph: Show the commit history in a graphical representation.
    Example: `git log --graph`

 

30. git log --author: Show the commit history by a specific author.
    Example: `git log --author "John Doe"`

 

31. git blame: Show who changed which lines in a file.
    Example: `git blame file.txt`

 

32. git branch -d: Delete a branch.
    Example:

 `git branch -d branchname`

 

33. git branch -m: Rename a branch.
    Example: `git branch -m new_branchname`

 

34. git show-branch: Show branches and their commits.
    Example: `git show-branch`

 

35. git clean: Remove untracked files from the working directory.
    Example: `git clean -f`

 

36. git remote prune: Remove remote-tracking branches that no longer exist on the remote.
    Example: `git remote prune origin`

 

37. git log --grep: Show the commit history that matches a specific pattern.
    Example: `git log --grep "bug fix"`

 

38. git log --since: Show the commit history since a specific date.
    Example: `git log --since "2022-01-01"`

 

39. git log --until: Show the commit history until a specific date.
    Example: `git log --until "2022-12-31"`

 

40. git bisect: Find the commit that introduced a bug using binary search.
    Example: `git bisect start`

 

41. git reflog: Show a log of all reference changes in the repository.
    Example: `git reflog`

 

42. git remote show: Show information about a remote repository.
    Example: `git remote show origin`

 

43. git revert --no-commit: Revert changes but do not create a new commit.
    Example: `git revert --no-commit commit_hash`

 

44. git reset --hard: Discard all changes and reset the repository to a specific commit.
    Example: `git reset --hard commit_hash`

 

45. git config --global alias: Set up an alias for a Git command.
    Example: `git config --global alias.ci commit`

 

46. git archive: Create a tar or zip archive of a Git repository.
    Example: `git archive --format=zip --output=archive.zip master`

 

47. git submodule: Manage Git submodules within a repository.
    Example: `git submodule add https://github.com/user/repo.git`

 

48. git clean -n: Dry run of git clean to preview files that will be removed.
    Example: `git clean -n`

 

49. git log --follow: Show the commit history of a renamed file.
    Example: `git log --follow file.txt`

 

50. git show-branch --all: Show the commit history of all branches.
    Example: `git show-branch --all`
