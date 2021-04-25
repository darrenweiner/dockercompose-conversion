Not Meant for prime time.  Just a quick example to show how to use ecs-cli to create a task definition
from a multi-container service.  
The task def will be registered in the aws-profile account (this maps to the standard ~/.aws/credentials)  
ecs-cli is needed for this:  
https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ECS_CLI_installation.html  
Create the task definition and register it in the account  
<code>ecs-cli  compose create --launch-type EC2 --aws-profile CloudButton-Admin --region us-east-1</code>  
Now to see the full task definition created:  
<code>aws ecs --profile CloudButton-Admin --region us-east-1 describe-task-definition --task-definition "dockercompose-conversion:1"</code>
