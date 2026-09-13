# AWS

## ⚙️ AWS CLI instalation (Linux)
```bash
 curl -fsSL https://awscli.amazonaws.com/v2/install.sh | bash
 echo 'export PATH=/home/user/.local/bin:$PATH' >> ~/.bashrc
 source ~/.bashrc
 aws --version
 aws update
```

## Access Key creation (AWS console)
```bash
 AWS: S3>Create bucket.
 AWS: Create IAM user>Security credentials>Create access key.
 ```

## Access Key config (Linux)
```bash
 aws configure
 aws configure list
```
