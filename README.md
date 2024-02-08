# AWS Lambda Functions Templates

https://github.com/aws/aws-lambda-dotnet

```
dotnet new -i "Amazon.Lambda.Templates::*"
```

```
dotnet new list --author AWS  
```


lambda.EmptyTopLevelFunction

serverless.Annotations

serverless.AspNetCoreMinimalAPI

serverless.AspNetCoreWebAPI

serverless.image.AspNetCoreWebAPI

serverless.AspNetCoreWebApp

lambda.CustomRuntimeFunction

lambda.DetectImageLabels

lambda.EmptyFunction

lambda.image.EmptyFunction

serverless.EmptyServerless

serverless.image.EmptyServerless

lambda.NativeAOT

lambda.Powertools

serverless.Powertools

lambda.SimpleApplicationLoadBalancerFunction

lambda.DynamoDB

lambda.KinesisFirehose

lambda.Kinesis

lambda.S3

lambda.SNS

lambda.SQS

lambda.LexBookTripSample

lambda.OrderFlowersChatbot

serverless.DetectImageLabels

serverless.NativeAOT

serverless.S3

serverless.WebSocketAPI

serverless.StepFunctionsHelloWorld

To get details about a template, you can use the help command.

```
dotnet new lambda.EmptyFunction --help
```

Template Instantiation Commands for .NET Core CLI.                                                                                          
                                                                                                                                           
**Lambda Empty Function (C#)** 

Author: AWS                                                                                                                                 

Options:                   

**-p|--profile**  The AWS credentials profile set in aws-lambda-tools-defaults.json and used as the default profile when interacting with AWS.
                  string - Optional                                                                                                           
                                                                                                                                           
**-r|--region**   The AWS region set in aws-lambda-tools-defaults.json and used as the default region when interacting with AWS.              
                  string - Optional  

The templates take two optional parameters to set the profile and region. These values are written to the aws-lambda-tools-default.json.

To create a function, run the following command

```
dotnet new lambda.EmptyFunction --name BlogFunction --profile default --region us-east-2
```

Install Amazon.Lambda.Tools Global Tools if not already installed.
```
dotnet tool install -g Amazon.Lambda.Tools
```

If already installed check if new version is available.

```
dotnet tool update -g Amazon.Lambda.Tools
```

Execute unit tests

```
cd "BlogFunction/test/BlogFunction.Tests"
dotnet test
```

Deploy function to AWS Lambda

```
cd "BlogFunction/src/BlogFunction"
dotnet lambda deploy-function
```


