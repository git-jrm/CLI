# 💯 Essential Node Commands

## 📁 Install fnm: for better performance
using fnm (fast node manager) instead of nvm (node version manager) 
```
curl -fsSL https://fnm.vercel.app/install | bash
fnm --version
source ~/.bashrc
```

```
fnm install 24
fnm dafault 24

fnm ls
fnm --version && node -v
```

## 📁 Install Binary: for local scripting
```
# create directory and extract from XZ file
sudo mkdir -p /opt/node
sudo tar -xJf node-$VER-linux-x64.tar.xz -C /opt/node

# force symbolic link to current node 
sudo ln -sfn /opt/node/node-v24.21.0-linux-x64 /opt/node/current

# set symlinks
sudo ln -sf /opt/node/current/bin/node /usr/local/bin/node
sudo ln -sf /opt/node/current/bin/npm /usr/local/bin/npm
sudo ln -sf /opt/node/current/bin/npx /usr/local/bin/npx

# easy to switch version with:
sudo ln -sfn /opt/node/node-v26.0.0-linux-x64 /opt/node/current

# optional PATH to global packages
echo 'export PATH=/opt/node/current/bin:$PATH' >> ~/.profile
```

















