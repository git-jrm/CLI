# 💯 Essential Node Commands

## 📁 Bin install
```
VER=v24.21.0
cd /tmp && wget https://nodejs.org/dist/$VER/node-$VER-linux-x64.tar.xz
```

## Integrity check
```
wget https://nodejs.org/dist/$VER/SHASUMS256.txt
grep node-$VER-linux-x64.tar.xz SHASUMS256.txt | sha256sum -c -
```

## Extract
```
sudo mkdir -p /opt/node
sudo tar -xJf node-$VER-linux-x64.tar.xz -C /opt/node
```


















