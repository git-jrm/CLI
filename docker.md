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
//Add the repository to Apt sources:
* **`sudo tee /etc/apt/sources.list.d/docker.sources <<EOF ... EOF`:** Agrega el repositorio oficial de Docker a las fuentes de Apt, usando el formato deb822. Escribe:
    * `Types: deb` — repositorio de paquetes binarios.
    * `URIs: https://download.docker.com/linux/ubuntu` — URL del repo oficial de Docker.
    * `Suites: $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}")` — detecta automáticamente el codename de Ubuntu (en mi caso, `resolute`).
    * `Components: stable` — canal estable del repo.
    * `Architectures: $(dpkg --print-architecture)` — detecta automáticamente la arquitectura (`amd64`).
    * `Signed-By: /etc/apt/keyrings/docker.asc` — usa la llave GPG descargada previamente para verificar los paquetes.
`:** .
* **``:** .
* **``:** .


## 📁 Setup
* **``:** .
* **``:** .
* **``:** .
* **`git remote show origin`:** Show detailed information of remote origin.

## 🔄 Workflow
* **``:** .
* **``:** .
* **``:** .




