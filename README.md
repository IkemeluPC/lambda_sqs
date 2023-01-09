# lambda_sqs
python code for a lambda function
# Description
This Lambda function using SQS as trigger
This Lambda function will process messages from the SQS queue and insert the message data as records into a DynamoDB table.
# the lambda execution role
this lambda function requires an aws IAM execution role with the following AWS managed permission policies
-AmazonSQSFullAccess
-AmazonDynamoDBFullAccess
-CloudWatchLogsFullAccess
-AWSLambdaExecute
# Initial testing
create and run codes in the file send_message.py from a linux server as a shellscript
with the command  <./send_message.py -q Messages -i 0.1>  (with -i 0.1 SQS, the message sending interval will be ever 1 second)
-this should generate fake text messages that will trigger the lambda function 
# to confirm
explore teh items in the Message table in the DynamoDB table and you should see the generated messages
