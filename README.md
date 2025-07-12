# AWS_Journey
Tracks the learning outcome of AWS CLI interaction

## AWS CLI Setup and Configuration

1. Create an access key for the IAM user. not the root user account.
<img width="1320" height="1189" alt="image" src="https://github.com/user-attachments/assets/6408121e-3542-433a-af89-07bf48b9e47e" />

Reference:
https://docs.aws.amazon.com/cli/latest/userguide/getting-started-quickstart.html

## Create a S3 bucket
1. Create a new S3 bucket using: (bucketname = jaechul-s3-bucket-2025) <br>
aws s3 mb s3://jaechul-s3-bucket-2025

2. Use the aws s3 ls command to list all the S3 buckets under your AWS account:
aws s3 ls

3. Create a text file named test.txt and add some content to it. Upload the file to your previously created S3 bucket using:
aws s3 cp test.txt s3://jaechul-s3-bucket-2025

4. Verify the file was uploaded successfully by listing the contents of your bucket:
aws s3 ls s3://jaechul-s3-bucket-2025

## Create a new IAM user <br>
1. aws iam create-user --user-name jaechul_demo

2. 
