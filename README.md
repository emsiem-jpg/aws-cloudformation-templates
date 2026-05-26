# aws-cloudformation-templates

vpc_ec2_s3_subnet - creates a simple vpc with an ec2 within a subnet, and an S3 bucket.
to use: 
aws cloudformation create-stack \
  --stack-name banking-infra \
  --template-body file://templates/vpc-ec2-s3.yaml \
  --parameters \
    ParameterKey=myBucketName,ParameterValue= {unique bucket name} \
    ParameterKey=VpcCidr,ParameterValue=10.0.0.0/16 \
    ParameterKey=SubnetCidr,ParameterValue=10.0.1.0/24 \
    ParameterKey=ec2InstanceType,ParameterValue=t3.micro \
    ParameterKey=AmiImageId,ParameterValue=ami-0b5a4e51202cd98e5
