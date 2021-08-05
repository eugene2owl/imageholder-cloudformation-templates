# imageholder-cloudformation-templates
Repository with AWS CloudFormation templates designed to automate deployment of the AWS resources required for "imageholder" application.

## Usage
1. Upload the repository templates to the AWS S3 bucket.
2. Create new AWS CloudFormation stack from the declared templates.

### Template files uploaded to the AWS S3
<img src="https://raw.githubusercontent.com/eugene2owl/imageholder-cloudformation-templates/main/assets/CF_s3.png" alt="drawing" width="800"/>

### New AWS CloudFormation stack from the declared templates
<img src="https://raw.githubusercontent.com/eugene2owl/imageholder-cloudformation-templates/main/assets/CF_deploy.png" alt="drawing" width="800"/>

## Defined AWS resources
Several AWS CloudFormation templates are defined for:
* VPC (with Public and Database Subnets, Cidr Blocks, Route Tables, Internet Gateway, etc.)
* EC2 (takes place in one of the subnets)
* Security Groups (for public EC2 instances and for all instances in the network)
* RDS (with its own DB Subnet Group)

## Using Nested Stack technology
Some templates do define creation of the resources with type "AWS::CloudFormation::Stack".
E.g. they do call creation of the other CloudFormation stacks, passing the parameters to them.
