# 10 Things I Learned Using Serverless

Repository with presentation code

## Context ##

Sample project with some demonstrations of building a Lambda function

## Requirements ##

[Yarn](https://classic.yarnpkg.com/en/docs/install/)

[Docker](https://docs.docker.com/get-docker/)

[AWS Client](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)

[SAM Client](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html)

### AWS Account ###

Create a new AWS Account to use only the free tier

### Role in AWS to create resources using CloudFormation ###

The guide is from serveless framework but explains really well the steps to setup a new Role and access key and secret

[Serverless Setup Credentials Guide](https://www.serverless.com/framework/docs/providers/aws/guide/credentials/)

## Setup ##

To create a Cloudformation stack with all the resources [template.yaml](demo/template.yaml)

1. Configure a new profile in aws-cli

    ```aws configure --profile [profileName]```

2. Export the configured profile name with permissions to create resources in CloudFormation

    ```export AWS_PROFILE=[profileName]```

3. Create a bucket in S3

    ```aws s3 mb s3://[bucketName]```

4. Package and upload the code to the S3 bucket

    ```yarn package```

5. Deploy the stack

    ```yarn deploy```

## Monitoring ##

Please check the branch demo-with-monitoring

```git checkout demo-with-monitoring```