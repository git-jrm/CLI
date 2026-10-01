# 💯 Essential Node Commands

## 📁 Bin install
```
# define and donload version in temp dif
VER=v24.21.0
cd /tmp && wget https://nodejs.org/dist/$VER/node-$VER-linux-x64.tar.xz

    --2026-10-01 18:02:10--  https://nodejs.org/dist/v24.21.0/node-v24.21.0-linux-x64.tar.xz
    Resolving nodejs.org (nodejs.org)... 104.16.212.131, 104.16.213.131, 2606:4700::6810:d483, ...
    Connecting to nodejs.org (nodejs.org)|104.16.212.131|:443... connected.
    HTTP request sent, awaiting response... 200 OK
    Length: 31890184 (30M) [application/x-xz]
    Saving to: ‘node-v24.21.0-linux-x64.tar.xz’

    node-v24.21.0-linux 100%[===================>]  30.41M  47.0MB/s    in 0.6s    

    2026-10-01 18:02:10 (47.0 MB/s) - ‘node-v24.21.0-linux-x64.tar.xz’ saved [31890184/31890184]
```

## Integrity check
```
# Integrity check comparison
wget https://nodejs.org/dist/$VER/SHASUMS256.txt
grep node-$VER-linux-x64.tar.xz SHASUMS256.txt | sha256sum -c -
    --2026-10-01 18:02:33--  https://nodejs.org/dist/v24.21.0/SHASUMS256.txt
    Resolving nodejs.org (nodejs.org)... 104.16.212.131, 104.16.213.131, 2606:4700::6810:d583, ...
    Connecting to nodejs.org (nodejs.org)|104.16.212.131|:443... connected.
    HTTP request sent, awaiting response... 200 OK
    Length: 3171 (3.1K) [text/plain]
    Saving to: ‘SHASUMS256.txt’

    SHASUMS256.txt      100%[===================>]   3.10K  --.-KB/s    in 0s      

    2026-10-01 18:02:33 (10.6 MB/s) - ‘SHASUMS256.txt’ saved [3171/3171]

    node-v24.21.0-linux-x64.tar.xz: OK
```

## Extract
```
sudo mkdir -p /opt/node
sudo tar -xJf node-$VER-linux-x64.tar.xz -C /opt/node
```


















