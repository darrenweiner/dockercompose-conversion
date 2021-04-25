Not Meant for prime time.  Just a quick example to show how to use ecs-cli to create a task definition
from a multi-container service.
#to create a task definition from this.  Note that the task def will be registered in the aws-profile account.
#ecs-cli is needed for this.
https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ECS_CLI_installation.html
Create the task definition and register it in the account
ecs-cli  compose create --launch-type EC2 --aws-profile CloudButton-Admin --region us-east-1
#To see the full task definition
#aws ecs --profile CloudButton-Admin --region us-east-1 describe-task-definition --task-definition "dockercompose-conversion:1"
