# AWS

## ⚙️ AWS CLI
```bash
 curl -fsSL https://awscli.amazonaws.com/v2/install.sh | bash
 echo 'export PATH=/home/user/.local/bin:$PATH' >> ~/.bashrc
 source ~/.bashrc
 aws --version
 aws update
```

```
### ACCESS KEY Config
* AWS: S3>Create bucket.
* AWS: IAM user>Security credentials>Create access key.
* Repo: settings>Actions secrets and variables>Actions>New repository secrets: Add 2 secrets: access key & secret key.
```
