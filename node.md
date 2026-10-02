# 💯 Essential Node Commands

## 📁 Install node via fnm: for better performance
using fnm (fast node manager) instead of nvm (node version manager) 
```
curl -fsSL https://fnm.vercel.app/install | bash
source ~/.bashrc
fnm --version
```

```
fnm install 24
fnm dafault 24

fnm ls
fnm --version && node -v
#  fnm 1.39.0
#  v24.21.0
```

using pnpm (performant node package manager) instead of npm (node package manager) 
```
ldd --version
#  ldd (Ubuntu GLIBC 2.43-2ubuntu2.4) 2.43
#  Copyright (C) 2024 Free Software Foundation, Inc.

ldconfig -p | grep libatomic

#  libatomic.so.1 (libc6,x86-64) => /usr/lib/x86_64-linux-gnu/libatomic.so.1

curl -fsSL https://get.pnpm.io/install.sh | sh -
source ~/.bashrc
pnpm --version
#  12.8.1

pnpm install
pnpm test
```
```
pnpm init  # npm init
pnpm add express  # npm install express / npm i express
pnpm add -D dotenv  # npm install --save-dev dotenv / npm i -D dotenv
pnpm dev  # npm run dev
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

















