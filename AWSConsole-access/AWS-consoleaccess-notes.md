# [AWS Console and Access](https://classroom.udacity.com/courses/ud080/lessons/f5717502-c984-402d-9595-24d2a35bb8a3/concepts/3a6ddf01-bf0b-40ae-9de1-849a28aff210)

## Lession Outline. 

- AWS console and AWS services
- Identity and Access Management (IAM)
- Creating IAM User and Policies
- Creating and using S3 bucket

# IMPORTANT ALWAYS CLEAN RESOURCES

## Multy factor authentication. 

- Damn it this is just 2-factor-auth for the console. for more security. I will just activiate it anyway.

## The console.

- Pretty self explanatory. as it gives you the major stuff then and their. 

## Identity and Acces management. 

This is devided into 2 things. 
- Authenticatoin: who can sign in 
- Autherisation : who can do what. 

Basically Users and roles. 
ACCess controls via policies.

here is the flow chart
IAM -> make Policies -> assign them to users. 

for users it genertates like normal authentications something that is a public key and a private key. 

IAM is granuler and is scoped. 
looks like json files ... it is json files. 

*Example* 
```json
{ 
    "Version": "2012-10-17" 
    "Statement":[
        "Sid":"AllowReadAccessToBucket",
        "Effect":"Allow", 
        "Action":[
            "s3:GetObject",
            "s3:ListeBucket"
        ], 
        "Resource":[
            "arn:aws:s3:::bucket-name", 
            "arn:aws:s3:::bucketname/*"
        ]
    ]
}
```
## Setting up an s3 bucket. 

Open the IAM console -> S3 bucket -> create new -> Add-stuff 

