# 💯 Essential Git Commands

## ssh
* **`ssh-keygen -t ed25519 -C "email@email.com"`:** Generate a new SSH key pair.
* **`ll ~/.ssh`:** List files in the SSH directory.
* **`echo $XDG_SESSION_TYPE`:** Check the current session type.
* **`xclip -sel clip < ~/.ssh/id_ed25519.pub`:** Copy key in X11. (sudo apt install xclip)
* **`wl-copy < ~/.ssh/id_ed25519.pub`:** Copy key in wayland (sudo apt install wl-clipboard).
* **`cat ~/.ssh/id_ed25519.pub`:** Show key.

## SSH

* **`ssh-keygen -t ed25519 -C "email@email.com"`**: Generates a new SSH key pair using the Ed25519 algorithm.
* **`ll ~/.ssh`**: Lists all files in the SSH directory, including hidden ones and permissions.
* **`echo $XDG_SESSION_TYPE`:** Check the current session type.
* **`xclip -selection clipboard < ~/.ssh/id_ed25519.pub`**: Copies the public key to the clipboard (for **X11** sessions).
* **`xsel --clipboard < ~/.ssh/id_ed25519.pub`**: Copies the public key to the clipboard (for **Wayland** sessions with compatibility, or alternative X11 setups).
* **`cat ~/.ssh/id_ed25519.pub`**: Prints the public key to the terminal to copy it manually (universal method).


## local config
* **`git --version`:** Show installed version.
* **`sudo apt install git -y`:** Install Git on Debian/Ubuntu.
* **`git config --global user.name ""`:** Set global username.
* **`git config --global user.email ""`:** Set global email.
* **`git config --global core.autocrlf input`:** Set Linux line endings.
* **`git config --global core.abbrev 5`:** Set 5-character commit hash abbreviation.
* **`git config --global core.editor "code --wait"`:** Set VS Code as default editor.
* **`git config --global color.ui true`:** terminal output colors.
* **`git init`:** Initialize a new local repository.
* **`git clone git@github.com:account/repo.git`:** Clone repository.
* **`git clone git@github.com:account/repo.git --depth=1`:** Shallow clone (only the latest commit history).

## remote config
* **`git remote`:** Show remote repository names.
* **`git remote -v`:** Show remote names and URLs.
* **`git remote show origin`:** Show detailed information of remote origin.

## frequent
* **`git status`:** Show branch and working directory status.

* **`git add .`:** Stage all changes in working directory.
* **`git commit -m "message"`:** Create commit with a message.
* **`git commit -am "message"`:** Stage tracked files and commit in one step.
* **`git add file.txt`:** Stage a specific file safely.
* **`git restore file.txt`:** Discard local changes in working directory.

* **`git show`:** Show detailed content of the current commit.
* **`git show file.txt`:** Show changes for a specific file in the last commit.

* **`git diff`:** Compare Working Directory against Stage.
* **`git diff --staged`:** Compare Stage against the last commit.

* **`git log --oneline`:** List commit history in compact single lines.

* **`git rebase -i HEAD~3`:** Back to the past to edit history.
* **`git commit --amend`:** Replace the current commit.
* **`git rebase --continue`:** Apply pending commits in blocks.

* **`git stash`:** Hide working directory changes in a limbo.
* **`git stash pop`:** Restore hidden changes and clean the stash.

* **`git reset --soft a1a1a`:** Back to past commit a1a1a, keeping future changes staged.
* **`git reset --soft HEAD~1`:** Back to past 1 commit (undo last commit), keeping changes staged.

* **`git switch -c "fix-issues"`:** Create and switch to a new branch (--create-ref).
git branch: 
git merge feature-login: Joins two or more development histories together.

* **`git push -u origin fix-issues`:** Upload branch & link it for future pushes (--set-upstream).
* **`git push`:** Upload branch.

* **`git pull origin main`:** .
* **`git pull origin main`:** Fetch and merge changes from the remote `main` branch into your current local branch.

git revert: 
git cherry-pick: Copies a specific commit from one branch and applies it directly to your current branch.
git reflog: Keeps a detailed safety log of every single action taken in your local repository.
git worktree add: Lets you check out multiple branches at the exact same time into separate physical directories.

