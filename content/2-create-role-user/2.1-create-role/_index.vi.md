---
title : "Tạo Policy và Role"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---
#### Tạo Role

1. Truy cập **AWS Management Console**

   - Tìm **IAM**
   - Chọn **IAM**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0001.png?width=90pc)

2. Trong giao diện **IAM**

   - Chọn **Policies**
   - Chọn **Create policy**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0002.png?width=90pc)

3. Trong phần **Specify permissions**

   - Chọn **JSON** xóa đoạn mã cũ và sao chép đoạn mã mới ở dưới vào

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0003.png?width=90pc)

{{% notice warning %}}
Ở đoạn policy này sẽ cấp quyền cho từng chức năng ở trong bài lab này, bạn có thể tùy chỉnh phân quyền ở đoạn policy này. Đoạn mã này đang phân quyền cho Region US East (Virginia) nên phần này sẽ là "aws:RequestedRegion": "us-east-1" (Nếu bạn đang ở Region khác thì nên chỉnh sửa lại từng "aws:RequestedRegion")
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



4. Sau khi hoàn tất bước ở trên, chúng ta kéo xuống cuối trang và ấn **Next**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0004.png?width=90pc)

5. Trong phần **Review and create**

{{% notice note %}}
Bạn có thể tự đặt tên khác theo ý của các bạn nhé!
{{% /notice %}}

   - **Policy name** nhập **```kms-key-policy```**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0005.png?width=90pc)

6. Sau khi nhập Policy name chúng ta kéo xuống cuối trang và ấn **Create policy**
  
![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0006.png?width=90pc)

7. Thông báo tạo **Policy** thành công

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0007.png?width=90pc)

#### Bước tiếp theo chúng ta sẽ tạo Role

8. Trong giao diện **IAM**

   - Chọn **Roles**
   - Chọn **Create role**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0008.png?width=90pc)

9. Trong phần **Select trusted entity**

   - Chọn **AWS service**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0009.png?width=90pc)

10. Kéo xuống phần **Use case**

   - Phần **Service or use case** chọn **S3**
   - Phần **Use case** chọn **S3**
   - Và ấn **Next**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0010.png?width=90pc)

11. Trong phần **Add permissions**

   - Chọn và thanh tìm kiếm và tìm policy **kms** mới vừa tạo
   - Tích chọn vào policy vừa tạo
   - Ấn **Next**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0011.png?width=90pc)

12. Trong phần **Name, review, and create**

{{% notice note %}}
Bạn có thể tự đặt tên khác theo ý của các bạn nhé!
{{% /notice %}}

   - **Role name** nhập **```kms-key-role```**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0012.png?width=90pc)

13. Kéo xuống dưới và ấn **Create role**

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0013.png?width=90pc)

14. Thông báo tạo role thành công

![create role](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0014.png?width=90pc)