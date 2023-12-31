# Day - 2 (30/12/2023)

Topics: Authentication vs Authorization, IAM (Identity and Access Management) in AWS, JSON Policies Syntax

## Authentication vs Authorization

**Authentication**: Verifies the identity of a user or system. It answers the question, "Who are you?" Common methods include passwords, biometrics, and multi-factor authentication.

**Authorization**: Determines what actions a user or system is allowed to perform. It answers the question, "What are you allowed to do?" Authorization is based on the authenticated user's permissions.

## IAM (Identity and Access Management) in AWS

IAM is a web service that helps securely control access to AWS resources. It enables the management of users and their level of access to the AWS Management Console.

### Key IAM Components

- **Users**: Authenticating users
- **Policies**: Authorization users
- **Groups**: Collections of users. Policies are attached to groups to grant permissions collectively.
- **Roles**: Similar to users but intended for AWS services. Roles are assumed for a temporary time to access resources.

## JSON Policies Syntax Example

json
```

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:*",
                "s3-object-lambda:*"
            ],
            "Resource": "*"
        }
    ]
}
```
Explanation
"Version": "2012-10-17": Indicates the policy language version.
"Effect": "Allow": Specifies whether the statement allows or denies access.
"Action": ["s3:", "s3-object-lambda:"]: Lists the actions allowed, here, all S3 and S3 Object Lambda actions.
"Resource": "*": Specifies the resources to which the actions apply. In this case, it applies to all resources (*).
