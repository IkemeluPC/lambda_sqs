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
