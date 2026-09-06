# 💯 Essential Docker Commands

## 🛠️ Env
* **`sudo apt update`:** Refresh package index.
* **`curl --version`:** Check if curl is installed.
* **`dpkg -s ca-certificates`:** Check if ca-certificates is installed.
* **`sudo apt install ca-certificates curl`:** Install both packages.
* **`ls -ld /etc/apt/keyrings`:** Check if keyrings folder exists.
* **`sudo install -m 0755 -d /etc/apt/keyrings`:** Create keyrings folder.
* **`sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc`:** Download Docker's GPG key.
* **`sudo chmod a+r /etc/apt/keyrings/docker.asc`:** Make key readable by all.

## ⚙️ Config
```bash
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
* **`cat /etc/apt/sources.list.d/docker.sources`:** Verify the file was created correctly.
* **`sudo apt update`:** Refresh index, now including Docker's repo.

## 📦 Install
* **`sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin`:** Install Docker Engine and plugins.

## 🚀 Start
* **`sudo systemctl status docker`:** Check if Docker service is running.
* **`sudo systemctl start docker`:** Start Docker service manually.
* **`sudo docker run hello-world`:** Test full Docker setup end-to-end.

