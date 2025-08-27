## 1) creating an s3 bucket
```
aws s3api create-bucket --bucket <name-of-bucket> --region <your-region>
```
## 2) listing the contents of an s3 bucket 
```
aws s3 ls s3://YOUR_BUCKET_NAME/
```
## 3) copying a file to an s3 bucket
```
 aws s3 cp <local_file_path> s3://<your_bucket_name>/<destination_key>
```

## 4) Deleting a bucket
```
#fisrt  empty the bucket
aws s3 rm s3://bucket-name --recursive

#then delete the bucket
aws s3api delete-bucket --bucket amzn-s3-demo-bucket --region us-east-1
```
