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

## Amazon S3
```bash
aws s3 ls                              # list buckets
aws s3 ls s3://bucket-name             # list bucket contents
aws s3 mb s3://bucket-name             # create bucket
aws s3 rb s3://bucket-name             # delete bucket (empty)
aws s3 cp file.txt s3://bucket-name    # upload file
aws s3 cp s3://bucket-name/file.txt .  # download file
aws s3 sync ./folder s3://bucket-name  # sync folder
aws s3 rm s3://bucket-name/file.txt    # delete file
```

## Amazon DynamoDB
```bash
aws dynamodb list-tables                                    # list tables
aws dynamodb describe-table --table-name TableName          # view table details

aws dynamodb create-table \                                 # create table
    --table-name TableName \
    --attribute-definitions \
        AttributeName=PK,AttributeType=S \
        AttributeName=SK,AttributeType=S \
    --key-schema \
       AttributeName=PK,KeyType=HASH \
       AttributeName=SK,KeyType=RANGE \
    --billing-mode PAY_PER_REQUEST

aws dynamodb delete-table --table-name TableName             # delete table
aws dynamodb put-item --table-name TableName --item '{"id":{"S":"1"}}'  # insert item
aws dynamodb get-item --table-name TableName --key '{"id":{"S":"1"}}'   # get item
aws dynamodb scan --table-name TableName                     # read whole table
```










