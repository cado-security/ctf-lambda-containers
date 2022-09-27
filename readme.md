## Cado Cloud Capture the Flag - Sep 2022

Step 1 - Install the [Cado Community Edition](https://www.cadosecurity.com/cado-community-edition/)

Step 2 - Download the files in the GitHub repository 

Step 3 - Upload the files to the S3 bucket for your deployment (you can find the identifier in the AWS Console under CloudFormation - Stacks - *stack name* - Outputs - S3Bucket)

Step 4 - Create 2  projects - named Lambda CTF and ECS CTF, 

Step 5 - In each project click Import - Artifacts from S3 and import the following files into their respective projects

---

| Project | File |
|---------|------|
| Lambda CTF | lambda-demo.zip |
| ECS CTF |  ecs-ip100061uswest1computeinternal-165641308414671.zip |

---



Background
Your company runs a number of applications that use a range of AWS services.

You’ve been asked to investigate a spike in your AWS bill and you see that usage is unexpectedly high for Lambda functions, ECS Fargate and an EKS cluster

Lambda CTF 
Looking in the AWS Console, you discover a Lambda function that nobody knows anything about.

You use Cado Response to acquire the Lambda function and its associated logs and immediately find that it’s a cryptominer running in Lambda.

Questions to answer
What are the three URLs embedded in the script?
When was the first time this function was run?

ECS CTF
The AWS Console also shows some containers that request way more vCPU resources than your standard containers do.

You use Cado Response to acquire the container, and again, you find that someone installed a cryptominer.

Questions to answer
What users did the attacker create? 
What command did the attacker run from Pastebin.com?
How did the attacker find out what the external IP address of the system was?
BONUS POINTS: What might be some additional data you want to collect to understand more?
