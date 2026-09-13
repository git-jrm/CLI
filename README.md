# 💯 Essential Git Commands

## 🛠️ Env
* **`ssh-keygen -t ed25519 -C "email@email.com"`:** Generate a new SSH key pair.
* **`ll ~/.ssh`:** List files in the SSH directory.
* **`cat ~/.ssh/id_ed25519.pub`:** Show key.
* **`echo $XDG_SESSION_TYPE`:** Check the current session type.
* **`xclip -sel clip < ~/.ssh/id_ed25519.pub`:** Copy key in X11. (xclip --version || sudo apt install xclip)
* **`wl-copy < ~/.ssh/id_ed25519.pub`:** Copy key in wayland (wl-clipboard --version || sudo apt install wl-clipboard).

## ⚙️ Config
* **`git --version`:** Show installed version.
* **`sudo apt install git -y`:** Install Git on GNU/Linux.
* **`git config --global user.name ""`:** Set global username.
* **`git config --global user.email ""`:** Set global email.
* **`git config --global core.autocrlf input`:** Set Linux line endings.
* **`git config --global init.defaultBranch main`:** Set default branch name to main.
* **`git config --global core.abbrev 5`:** Set 5-character commit hash abbreviation.
* **`git config --global core.editor "code --wait"`:** Set VS Code as default editor.
* **`git config --global color.ui true`:** terminal output colors.
* **`git config --global core.excludesfile ~/.gitignore_global`:** Set global ignore.
* **`git config --global alias.log2 "log --online --all --graph"`:** Set alias.

## 📁 Setup
* **`git init`:** Initialize a new local repository.
* **`git clone git@github.com:account/repo.git`:** Download full copy and history of repo.
* **`git clone git@github.com:account/repo.git --depth=1`:** Shallow clone (only the latest commit history).
* **`git remote`:** Show remote repository names.
* **`git remote -v`:** Show remote names and URLs.
* **`git remote show origin`:** Show detailed information of remote origin.

## 🔄 Workflow
* **`git status`:** Show branch and working directory status.
* **`git add .`:** Stage all changes in working directory.
* **`git add <file>`:** Stage a specific file safely.
* **`git commit -m "message"`:** Create commit with a message.
* **`git commit -am "message"`:** Stage tracked files and commit in one step.
* **`git push origin main`:** Upload branch.
* **`git push -u origin fix-issues`:** Upload branch and link. (--set-upstream)
* **`git push`:** Upload current branch.
* **`git pull origin main`:** Fetch and merge changes from the remote main branch.
* **`git pull -u origin main`:** Fetch and merge changes and link.
* **`git pull`:** Fetch and merge changes from the remote main branch.
* **`git fetch --prune`:** Fetch remote updates and clean up deleted remote branches. **(no visto aún: repasar)**

## 🌿 Branching & Merging
* **`git branch`:** List local branches.
* **`git branch <name>`:** Create local branch.
* **`git switch <name>`:** Switch to an existing branch.
* **`git checkout <name>`:** Switch to an existing branch. *(Legacy/Not-recommended)*
* **`git switch -c <name>`:** Create and switch to a new branch. (--create)
* **`git checkout -b <name>`:** Create and switch to a new branch. (--branch) *(Legacy/Not-recommended)*
* **`git branch -d <name>`:** Safe delete branch (--delete).
* **`git branch -D <name>`:** Force delete branch.
* **`git branch -m <name> <new-name>`:** Modify name in specific branch.
* **`git branch -m <name>`:** Rename current branch.
* **`git merge <name>`:** Join specified branch into current branch.
* **`git merge --continue`:** Continue merge process after resolving conflicts.

## 🔍 Inspection & Diff
* **`git log --oneline`:** Compact single-line commit history.
* **`git log --oneline --all`:** List all branches and history.
* **`git log --oneline --graph --all`:** Visual graph of all branches and history.
* **`git reflog`:** Keep a detailed safety log of every local action taken.
* **`git show`:** Show changes in Current Commit.
* **`git show <file>`:** Show changes for a specific file.
* **`git ls-tree -r -n a1a1a`:** List all tracked files in commit a1a1a. (--recursive --name-only)
* **`git ls-tree -r -n HEAD`:** List all tracked files in current commit. (--recursive --name-only)
* **`git ls-tree -l HEAD`:** List top-level tracked files sizes in current commit. (--long)
* **`git diff`:** Compare Working Directory against Staging area.
* **`git diff --staged`:** Compare Staging area against Current Commit.

## ⏪ Undoing & Rewriting History
* **`git restore <file>`**: Discard local unstaged changes.
* **`git checkout -- <file>`**: Discard local unstaged changes *(legacy/not-recommended)*.
* **`git commit --amend`:** Replace the current commit.
* **`git revert`:** Create a new commit that undoes the changes of a past commit. **(no visto aún: repasar)**
* **`git reset --soft a1a1a`:** Move to commit, keeping all changes staged.
* **`git reset --mixed a1a1a`:** Move to commit, unstage but keep changes in working directory (default).
* **`git reset --hard HEAD~1`:** Move 1 commit back, discard changes, sync stage and working directory.
* **`git reset --hard a1a1a`:** Move to commit, discard changes, sync stage and working directory.
* **`git rebase -i HEAD~3`:** Back to the past to edit history.
* **`git rebase --continue`:** Apply pending commits in blocks.

## 🧰 Advanced Utilities
* **`git stash`:** Hide working directory changes in a limbo.
* **`git stash pop`:** Restore hidden changes and clean the stash.
* **`git cherry-pick`:** Copy a specific commit from another branch to your current branch.
* **`git worktree add`:** Check out multiple branches at the same time in separate folders.



















