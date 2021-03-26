# Auction Services
 Serverless Framework with Node.js, AWS & Microservices, DynamoDB

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
    Setting the Auction time to end
        endDate.setHours(now.getHours()+1); // 1 hour
        endDate.setDays(now.getDays()+1);   // 1 day 
