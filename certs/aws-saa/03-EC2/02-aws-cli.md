- interact with AWS using command line
  - ie. `aws s3 ls` will list all buckets in aws account

```bash
aws configure
# enter access key and secret key id
aws s3 ls
# lists buckets

# create bucket
aws s3 mb s3://name_of_bucket
aws s3 ls
# name_of_bucket

echo "hello" > test.txt
aws s3 cp test.txt s3://name_of_bucket
# upload: ./name_of_bucket/test.txt
```

Review
- principal of least privilege
- use [[IAM]] [[IAM Group|groups]]
  - group permissions with [[policy document]]s
  - users will inherit perms of [[IAM Group|group]]
- secret access key
  - password for using AWS [[Command Line Interface|CLI]]
  - can regenerate it, will need to do `aws configure` again
- each person should have their own key pair
- supports linux, mac, win
