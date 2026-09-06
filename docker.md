# 💯 Essential Docker Commands

## 🛠️ Env
* **`sudo apt update`:** .
* **`curl --version`:** .
* **`sudo apt install ca-certificates curl`:** .
* **`ls -ld /etc/apt/keyrings`:** .
* **`sudo install -m 0755 -d /etc/apt/keyrings`:** .
* **`sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc`:** .
* **`sudo chmod a+r /etc/apt/keyrings/docker.asc`:** .

## ⚙️ Config
``` bash
# Add the repository to Apt sources:
sudo tee /etc/apt/sources.list.d/docker.sources <<EOF
Types: deb
URIs: https://download.docker.com/linux/ubuntu
Suites: $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}")
Components: stable
Architectures: $(dpkg --print-architecture)
Signed-By: /etc/apt/keyrings/docker.asc
EOF
```
* **`cat /etc/apt/sources.list.d/docker.sources`:** .
* **`sudo apt update`:** .

