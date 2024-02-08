# AWS Lambda Functions Templates

https://github.com/aws/aws-lambda-dotnet

dotnet new -i "Amazon.Lambda.Templates::*"

dotnet new list --author AWS  

To get details about a template, you can use the help command.

dotnet new lambda.EmptyFunction --help

Template Instantiation Commands for .NET Core CLI.                                                                                          
                                                                                                                                           
Lambda Empty Function (C#)                                                                                                                  
Author: AWS                                                                                                                                 
Options:                                                                                                                                    
  -p|--profile  The AWS credentials profile set in aws-lambda-tools-defaults.json and used as the default profile when interacting with AWS.
                string - Optional                                                                                                           
                                                                                                                                           
  -r|--region   The AWS region set in aws-lambda-tools-defaults.json and used as the default region when interacting with AWS.              
                string - Optional  
The templates take two optional parameters to set the profile and region. These values are written to the aws-lambda-tools-default.json.

To create a function, run the following command

dotnet new lambda.EmptyFunction --name BlogFunction --profile default --region us-east-2



