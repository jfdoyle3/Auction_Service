# Auction Services
 Serverless Framework with Node.js, React, AWS & Microservices, DynamoDB, Bucket S3, Auth0

Install: AWS CLI
 https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html

Install: Serverless CLI - using npm: npm install -g serverless
 https://www.serverless.com/framework/docs/getting-started/

VS Code Extension:
Name: Serverless IDE
Id: threadheap.serverless-ide-vscode
Description: Enhanced support for AWS SAM, CloudFormation and Serverless Framework
Version: 0.5.30
Publisher: ThreadHeap
VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=ThreadHeap.serverless-ide-vscode

sls usage:
switches
-v verbose
-f 'function name'
-t logtail
-l logs

To deploy project
sls deploy -v   : used at first startup or changes to yml file
sls deploy -f 'function name' -v : used when changing a function , runs deploy faster.

Run a function
sls invoke -f 'function name' -l

Show log of a function
sls logs -f 'function name' -t

To remove project 
sls remove -v

Create Auction.js
    Customized for front end 
    Setting the Auction time to end
        endDate.setHours(now.getHours()+1); // 1 hour
        endDate.setDays(now.getDays()+1);   // 1 day 

Test Auth0 token:

curl --location --request POST 'https://YOUR_AUTH0_DOMAIN/oauth/token' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'client_id=YOUR_AUTH0_CLIENT_ID' \
--data-urlencode 'username=YOUR_USERNAME' \
--data-urlencode 'password=YOUR_PASSWORD' \
--data-urlencode 'grant_type=password' \
--data-urlencode 'scope=openid'


Create Secret.pem file
This file will contain your Auth0 public certificate, used to verify tokens.
Create a secret.pem file in the root folder of this project. Simply paste your public certificate in there.