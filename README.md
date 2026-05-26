# aws-cloudformation-templates

vpc_ec2_s3_subnet - creates a simple vpc with an ec2 within a subnet, and an S3 bucket.
to use: 
aws cloudformation create-stack \
  --stack-name banking-infra \
  --template-body file://templates/vpc-ec2-s3.yaml \
  --parameters ParameterKey=myBucketName,ParameterValue=moj-bucket
