## cli command to list the latest amazon linux 2 amis available 
```
aws ec2 describe-images \
  --owners amazon \
  --filters "Name=name,Values=amzn2-ami-hvm-*" \
  --query "Images[].Name" \
  --region us-east-1
```
