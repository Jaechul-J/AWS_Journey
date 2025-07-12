# AWS_Journey
Tracks the learning outcome of AWS CLI interaction

## AWS CLI Setup and Configuration
Reference:
https://docs.aws.amazon.com/cli/latest/userguide/getting-started-quickstart.html

## Create a S3 bucket
1. Create a new S3 bucket using: (bucketname = jaechul-s3-bucket-2025) <br>
aws s3 mb s3://jaechul-s3-bucket-2025

2. Use the aws s3 ls command to list all the S3 buckets under your AWS account:<br>
aws s3 ls

3. Create a text file named test.txt and add some content to it. Upload the file to your previously created S3 bucket using:<br>
aws s3 cp test.txt s3://jaechul-s3-bucket-2025

4. Verify the file was uploaded successfully by listing the contents of your bucket:<br>
aws s3 ls s3://jaechul-s3-bucket-2025

## Create a new IAM user <br>
1. Create the IAM user: Use the aws iam create-user command to create a new IAM user:<br>
aws iam create-user --user-name jaechul_demo

2. Verify the user creation: List all IAM users to ensure your new user was created successfully <br>
aws iam list-users

3. Attach the policy: Use the aws iam attach-user-policy command to attach the AmazonS3ReadOnlyAccess policy to your newly created user:<br>
aws iam attach-user-policy --user-name jaechul_demo --policy-arn arn:aws:iam::aws:policy/AmazonS3ReadOnlyAccess

4. Verify the policy attachment: Check the attached policies of the user to ensure the AmazonS3ReadOnlyAccess policy is attached:<br>
aws iam list-attached-user-policies --user-name jaechul_demo

5. Create access keys: Generate new access keys for the IAM user:<br>
aws iam create-access-key --user-name jaechul_demo
