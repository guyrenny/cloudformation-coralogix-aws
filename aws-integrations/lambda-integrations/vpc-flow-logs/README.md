# Coralogix-VPC-Flow-Logs

This template were created automatically from coralogix/coralogix-aws-serverless.
To make a change in the template go to the link below.

https://github.com/coralogix/coralogix-aws-serverless/tree/master/src/vpc-flow-logs

This application retrieves **VPC Flow** logs from S3 and sends them to your **Coralogix** account.

## Prerequisites
* Active VPC with flow logs 
* Permissions to create lambda functions
* An AWS account.
* A coralogix account.


## Fields 

**Application name** - The stack name of this application created via AWS CloudFormation.

**NotificationEmail** (optinal) - If the lambda fails a notification email will be sent to this address via SNS (requires you have a working SNS, with a validated domain).

**S3BucketName** - The name of the S3 bucket with CloudTrail logs to watch (must be in the same region as stack that you will create).

**ApplicationName** - Application Name as it will be seen in Coralogix UI.

**CoralogixRegion** - The Coralogix location region, possible options are [Europe, Europe2, India, Singapore, US].In case that you want to use Custom domain, leave this as default and write the Custom doamin in the ``CustomDomain`` filed.

**CustomDomain** - The Coralogix custom domain,leave empty if you don't use Custom domain.

**FunctionArchitecture** - Lambda function architecture, possible options are [x86_64, arm64]. 

**FunctionMemorySize** - The maximum allocated memory this lambda may consume, the default is 1024. Don't change

**FunctionTimeout** - The maximum time in seconds the function may be allowed to run, the default is 300. Don't change

**PrivateKey** - Your Coralogix secret key.

* **SsmEnabled** - Set this to True to use AWS Secrets  (When enable it creates the secret in with the following pattern "lambda/coralogix/<AWS_REGION>/<Cloudwatch_lambda_name>") - optional. The field receive 'True' or 'False'. 
**Note:** Both layers and lambda need to be in the same AWS Region.

* **LayerARN** - This is the ARN of the Coralogix SecurityLayer. Copy from the ``SSM`` serverless application the ARN that was installed on the AWS account. 

**SubsystemName** - Sybsystem Name as it will be seen in Coralogix UI.

**S3KeyPrefix** - The prefix of the path within the log, this way you can choose if only part of your bucket is shipped.

**S3KeySuffix** - A filter for the suffix of the file path in your bucket, the default is .json.gz.

`S3KeyPrefix` and `S3KeySuffix` should be adjusted based on your configuration.

## License

This project is licensed under the Apache-2.0 License.

test
test
test
test
test
test
test
test
test
test
test
test
test
test
test
test
test
test
test
test
test
test
test
test
