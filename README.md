# AWS Lambda Functions Templates

https://github.com/aws/aws-lambda-dotnet

```
dotnet new -i "Amazon.Lambda.Templates::*"
```

```
dotnet new list --author AWS  
```

Template Name                  Short Name                                    Language  Tags
-----------------------------  --------------------------------------------  --------  --------------------------------
Empty Top-level Function       lambda.EmptyTopLevelFunction                  [C#]      AWS/Lambda/Serverless
Lambda Annotations Framewo...  serverless.Annotations                        [C#]      AWS/Lambda/Serverless
Lambda ASP.NET Core Minima...  serverless.AspNetCoreMinimalAPI               [C#]      AWS/Lambda/Serverless
Lambda ASP.NET Core Web API    serverless.AspNetCoreWebAPI                   [C#],F#   AWS/Lambda/Serverless
Lambda ASP.NET Core Web AP...  serverless.image.AspNetCoreWebAPI             [C#],F#   AWS/Lambda/Serverless
Lambda ASP.NET Core Web Ap...  serverless.AspNetCoreWebApp                   [C#]      AWS/Lambda/Serverless
Lambda Custom Runtime Func...  lambda.CustomRuntimeFunction                  [C#],F#   AWS/Lambda/Function
Lambda Detect Image Labels     lambda.DetectImageLabels                      [C#],F#   AWS/Lambda/Function
Lambda Empty Function          lambda.EmptyFunction                          [C#],F#   AWS/Lambda/Function
Lambda Empty Function (.NE...  lambda.image.EmptyFunction                    [C#],F#   AWS/Lambda/Function
Lambda Empty Serverless        serverless.EmptyServerless                    [C#],F#   AWS/Lambda/Serverless
Lambda Empty Serverless (....  serverless.image.EmptyServerless              [C#],F#   AWS/Lambda/Serverless
Lambda Function project co...  lambda.NativeAOT                              [C#],F#   AWS/Lambda/Function
Lambda Function with Power...  lambda.Powertools                             [C#]      AWS/Lambda/Function/Powertools
Lambda Giraffe Web App         serverless.Giraffe                            F#        AWS/Lambda/Serverless
Lambda Serverless with Pow...  serverless.Powertools                         [C#]      AWS/Lambda/Serverless/Powertools
Lambda Simple Application ...  lambda.SimpleApplicationLoadBalancerFunction  [C#]      AWS/Lambda/Function
Lambda Simple DynamoDB Fun...  lambda.DynamoDB                               [C#],F#   AWS/Lambda/Function
Lambda Simple Kinesis Fire...  lambda.KinesisFirehose                        [C#]      AWS/Lambda/Function
Lambda Simple Kinesis Func...  lambda.Kinesis                                [C#],F#   AWS/Lambda/Function
Lambda Simple S3 Function      lambda.S3                                     [C#],F#   AWS/Lambda/Function
Lambda Simple SNS Function     lambda.SNS                                    [C#]      AWS/Lambda/Function
Lambda Simple SQS Function     lambda.SQS                                    [C#]      AWS/Lambda/Function
Lex Book Trip Sample           lambda.LexBookTripSample                      [C#]      AWS/Lambda/Function
Order Flowers Chatbot Tuto...  lambda.OrderFlowersChatbot                    [C#]      AWS/Lambda/Function
Serverless Detect Image La...  serverless.DetectImageLabels                  [C#],F#   AWS/Lambda/Serverless
Serverless project configu...  serverless.NativeAOT                          [C#],F#   AWS/Lambda/Serverless
Serverless Simple S3 Function  serverless.S3                                 [C#],F#   AWS/Lambda/Serverless
Serverless WebSocket API       serverless.WebSocketAPI                       [C#]      AWS/Lambda/Serverless
Step Functions Hello World     serverless.StepFunctionsHelloWorld            [C#],F#   AWS/Lambda/Serverless

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


