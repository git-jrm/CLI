# 💯 Essentials commands

## 🛠️ SSH
* **`ssh-keygen -t ed25519 -C "email@email.com"`:** Generate a new SSH key pair.
* **`ll ~/.ssh`:** List files in the SSH directory.
* **`cat ~/.ssh/id_ed25519.pub`:** Show key.
* **`echo $XDG_SESSION_TYPE`:** Check the current session type.
* **`xclip -sel clip < ~/.ssh/id_ed25519.pub`:** Copy key in X11. (xclip --version || sudo apt install xclip)
* **`wl-copy < ~/.ssh/id_ed25519.pub`:** Copy key in wayland (wl-clipboard --version || sudo apt install wl-clipboard).

## 🛠️ Git commands

[See more](https://github.com/git-jrm/git/blob/main/git.md)

## 🛠️ Docker commands

[See more](https://github.com/git-jrm/git/blob/main/docker.md)

## 🛠️ AWS CLI commands

[See more](https://github.com/git-jrm/git/blob/main/aws.md)

