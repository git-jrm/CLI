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
* **`sudo docker run <name>`:** Test full Docker setup end-to-end.

## 🖼️ Images
* **`sudo docker images`:** List downloaded images *old*.
* **`sudo docker image ls`:** List downloaded images.
* **`sudo docker build .`:** Build image from Dockerfile.
* **`sudo docker build -t <tag> .`:** Build image and tag.
* **`sudo docker image rm <id>`:** Remove image.
* **`sudo docker pull <image>`:** Download image from Docker Hub.

## 📦 Containers
* **`sudo docker ps`:** List running containers. *old*
* **`sudo docker ps -a`:** List all containers. *old*
* **`sudo docker container ls`:** List running containers. *new*
* **`sudo docker container ls -a`:** List all containers. *new*
* **`sudo docker run myapp`:** Run attached container.
* **`sudo docker run -p 5024:5024 myapp`:** Run attached container mapping port.
* **`sudo docker run -d -p 5024:5024 myapp`:** Run detached container mapping port.
* **`sudo docker run --rm myapp`:** Run and auto-delete container on exit.
* **`sudo docker run --name <name> -p 8080:80 -d nginx`:** Run and open interactive shell inside mapping port.
* **`sudo docker run --name <name> -it ubuntu bash`:** Run interactive terminal container.
* **`sudo docker run -it --entrypoint "/bin/bash" ubuntu`:** Run interactive terminal container, forcing bash shell.
* **`sudo docker stop <id|name>`:** Stop a running container.
* **`sudo docker start <id>`:** Restart a stopped container.
* **`sudo docker restart <id>`:** Stop + start in one command.
* **`sudo docker rm <id|name>`:** Delete a stopped container.
* **`sudo docker rm -f <id|name>`:** Force delete a running container.
* **`sudo docker exec -it <id> bash`:** Open a shell inside a running container.
* **`sudo docker logs <id>`:** View container output/logs.
* **`sudo docker logs -f <id>`:** Follow logs in real time (like `tail -f`).
* **`sudo docker pull ubuntu`:** Download Ubuntu image.








