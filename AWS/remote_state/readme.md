# usage

```
# make sure you are on the right aws account
pip install awscli
aws s3 ls

# If you don't set default region in your aws configuration, and you want to create the resources in region "us-east-1"
export AWS_DEFAULT_REGION=us-east-1
export AWS_REGION=us-east-1

# Dry-run
terraform init
terraform plan

# apply the change
terraform apply
```
