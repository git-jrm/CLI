# 💯 Essential Git Commands

## ssh
* **`ssh-keygen -t ed25519 -C "email@email.com"`:** Generate a new SSH key pair.
* **`ls ~/.ssh`:** List files in the SSH directory.
* **`clip < ~/.ssh/id_ed25519.pub`:** Copy public key to clipboard.

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
* **`git push -u origin fix-issues`:** Upload branch & link it for future pushes (--set-upstream).


