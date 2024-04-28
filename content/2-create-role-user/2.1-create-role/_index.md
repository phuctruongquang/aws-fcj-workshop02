---
title : "Create Policy and Role"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

#### Create Role

1. Access **AWS Management Console**

   - Search **IAM**
   - Select **IAM**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0001.png?width=90pc)

2. In the interface **IAM**

   - Select **Policies**
   - Select **Create policy**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0002.png?width=90pc)

3. In the interface **Specify permissions**

   - Select **JSON** delete the old code and copy the new code below

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0003.png?width=90pc)

{{% notice warning %}}
This policy will grant permissions to each function in this lab. You can customize the permissions in this policy. This code is delegating authority to Region US East (Virginia), so this part will be "aws:RequestedRegion": "us-east-1" (If you are in another Region, you should edit each "aws:RequestedRegion")
{{% /notice %}}

         {
            "Version": "2012-10-17",
            "Statement": [
               {
                     "Sid": "VisualEditor0",
                     "Effect": "Allow",
                     "Action": [
                        "cloudtrail:List*",
                        "cloudtrail:PutInsightSelectors",
                        "cloudtrail:PutEventSelectors",
                        "cloudtrail:StopLogging",
                        "cloudtrail:StartLogging",
                        "cloudtrail:AddTags",
                        "cloudtrail:UpdateTrail",
                        "cloudtrail:CreateTrail",
                        "cloudtrail:Describe*",
                        "cloudtrail:Get*"
                     ],
                     "Resource": "*",
                     "Condition": {
                        "ForAllValues:StringEquals": {
                           "aws:RequestedRegion": "us-east-1"
                        }
                     }
               },
               {
                     "Sid": "VisualEditor1",
                     "Effect": "Allow",
                     "Action": [
                        "cloudwatch:List*",
                        "cloudwatch:Get*",
                        "cloudwatch:Describe*"
                     ],
                     "Resource": "*",
                     "Condition": {
                        "ForAllValues:StringEquals": {
                           "aws:RequestedRegion": "us-east-1"
                        }
                     }
               },
               {
                     "Sid": "VisualEditor2",
                     "Effect": "Allow",
                     "Action": [
                        "config:Get*",
                        "config:List*",
                        "config:Describe*"
                     ],
                     "Resource": "*",
                     "Condition": {
                        "StringEquals": {
                           "aws:RequestedRegion": "us-east-1"
                        }
                     }
               },
               {
                     "Sid": "VisualEditor3",
                     "Effect": "Allow",
                     "Action": [
                        "iam:Get*",
                        "iam:List*",
                        "iam:AttachRolePolicy"
                     ],
                     "Resource": "*",
                     "Condition": {
                        "StringEquals": {
                           "aws:RequestedRegion": "us-east-1"
                        }
                     }
               },
               {
                     "Sid": "VisualEditor4",
                     "Effect": "Allow",
                     "Action": [
                        "kms:EnableKeyRotation",
                        "kms:EnableKey",
                        "kms:Decrypt",
                        "kms:TagResource",
                        "kms:UntagResource",
                        "kms:List*",
                        "kms:Encrypt",
                        "kms:Get*",
                        "kms:CreateAlias",
                        "kms:Describe*",
                        "kms:CreateKey",
                        "kms:DisableKey"
                     ],
                     "Resource": "*",
                     "Condition": {
                        "StringEquals": {
                           "aws:RequestedRegion": "us-east-1"
                        }
                     }
               },
               {
                     "Sid": "VisualEditor5",
                     "Effect": "Allow",
                     "Action": [
                        "organizations:Describe*",
                        "organizations:List*"
                     ],
                     "Resource": "*",
                     "Condition": {
                        "StringEquals": {
                           "aws:RequestedRegion": "us-east-1"
                        }
                     }
               },
               {
                     "Sid": "VisualEditor6",
                     "Effect": "Allow",
                     "Action": [
                        "s3:PutAccountPublicAccessBlock",
                        "s3:PutBucketPublicAccessBlock",
                        "s3:PutBucketOwnershipControls",
                        "s3:Get*",
                        "s3:CreateBucket",
                        "s3:List*",
                        "s3:PutObject",
                        "s3:PutObjectVersionAcl",
                        "s3:PutBucketAcl",
                        "s3:PutBucketPolicy",
                        "s3:PutAccessPointPolicy",
                        "s3:PutBucketVersioning",
                        "s3:PutObjectAcl",
                        "iam:PassRole",
                        "iam:CreateServiceLinkedRole"
                     ],
                     "Resource": "*"
               },
               {
                     "Sid": "VisualEditor7",
                     "Effect": "Allow",
                     "Action": "tag:Get*",
                     "Resource": "*",
                     "Condition": {
                        "StringEquals": {
                           "aws:RequestedRegion": "us-east-1"
                        }
                     }
               },
               {
                     "Sid": "VisualEditor8",
                     "Effect": "Deny",
                     "Action": "s3:*",
                     "Resource": "*",
                     "Condition": {
                        "ForAllValues:StringNotEqualsIfExists": {
                           "aws:RequestedRegion": "us-east-1"
                        }
                     }
               }
            ]
         }



4. After completing the above step, we scroll down to the bottom of the page and click **Next**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0004.png?width=90pc)

5. In section **Review and create**

{{% notice note %}}
You can name it differently as you like!
{{% /notice %}}

   - **Policy name** import **```kms-key-policy```**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0005.png?width=90pc)

6. After entering the Policy name, scroll down to the bottom of the page and click **Create policy**
  
![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0006.png?width=90pc)

7. Notice of successful creation of **Policy**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0007.png?width=90pc)

#### Next step we will create Role

8. In the interface **IAM**

   - Select **Roles**
   - Select **Create role**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0008.png?width=90pc)

9. In section **Select trusted entity**

   - Select **AWS service**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0009.png?width=90pc)

10. Scroll down to the section **Use case**

 - In the **Service or use case** section, select **S3**
 - In the **Use case** section, select **S3**
 - And press **Next**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0010.png?width=90pc)

11. In the **Add permissions** section

 - Select the search bar and search for the newly created **kms** policy
 - Select the policy you just created
 - Click **Next**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0011.png?width=90pc)

12. In the **Name, review, and create** section

{{% notice note %}}
You can name it differently as you like!
{{% /notice %}}

   - **Role name** import **```kms-key-role```**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0012.png?width=90pc)

13. Scroll down and press **Create role**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0013.png?width=90pc)

14. Notice of successful role creation

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0014.png?width=90pc)


