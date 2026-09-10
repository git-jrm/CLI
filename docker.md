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
* **`docker run <name>`:** Test full Docker setup end-to-end.

## 💡 Help
* **`docker --help`:** .
* **`docker images --help`:** .
* **`docker build --help`:** .
* **`docker run --help`:** .

## 🖼️ Images
* **`docker images`:** List downloaded images. ***old***
* **`docker image ls`:** List downloaded images.
* **`docker build [-t <tag>] .`:** Build image and tag. ***old***
* **`docker image build .`:** Build image.
* **`docker pull <image>`:** Download image. ***old***
* **`docker image pull <image>`:** Download image.
* **`docker rmi <id|name>`:** Remove image. ***old***
* **`docker image rm <id|name>`:** Remove image.
* **`docker tag <id|name>`:** Tag image. ***old***
* **`docker image tag <id|name>`:** Tag image.
* **`docker push <image>`:** Upload image. ***old***
* **`docker image push <image>`:** Upload image.
* **`docker image prune -a --filter "until=24h"`:** Remove images created more than 24h ago.

## 📦 Containers
* **`docker ps`:** List running containers. ***old***
* **`docker ps -a`:** List all containers. ***old***
* **`docker container ls`:** List running containers.
* **`docker container ls -a`:** List all containers.
* **`docker run <name>`:** Run container. ***old***
* **`docker run -p 8080:80 <name>`:** Run container mapping port.
* **`docker run -d -p 8080:80 <name>`:** Run detached container mapping port.
* **`docker run --rm <name>`:** Run and auto-delete container on exit.
* **`docker run --name <name> -p 8080:80 -d nginx`:** Run and name detached container mapping port.
* **`docker run --name <name> -it ubuntu bash`:** Run and name interactive terminal container.
* **`docker run -it --entrypoint "/bin/bash" ubuntu`:** Run interactive terminal container, forcing bash shell.
* **`docker container run`:** Run containter.
* **`docker stop <id|name>`:** Stop running container. ***old***
* **`docker container stop <id|name>`:** Stop running container.
* **`docker start <id>`:** Restart container. ***old***
* **`docker container start <id>`:** Restart container.
* **`docker restart <id>`:** Restart container. ***old***
* **`docker container restart <id>`:** Restart container.
* **`docker rm <id|name>`:** Delete stopped container. ***old***
* **`docker rm -f <id|name>`:** Force delete running container. ***old***
* **`docker container rm <id|name>`:** Delete stopped container.
* **`docker logs <id>`:** View container output.
* **`docker logs -f <id>`:** Follow container output (like `tail -f`).
* **`docker exec -it <id> bash`:** Open shell in running container. ***old***
* **`docker container exec -it <id> bash`:** Open shell in running container.
* **`docker inspect <id>`:** Config details. ***old***
* **`docker container inspect ,
<id>`:** Config details.
* **`docker cp`:** . ***old***
* **`docker container cp`:** .


docker network ls






















