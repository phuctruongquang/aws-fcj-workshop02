---
title : "Create Bucket"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---

#### Create Bucket

1. Access **AWS Management Console**

 - Find **S3**
 - Select **S3**

![create bucket](/images/4.create-s3/4.1create-bucket/0001.png?width=90pc)

2. In the **S3** interface

 - Select **Buckets**
 - Select **Create bucket**

![create bucket](/images/4.create-s3/4.1create-bucket/0002.png?width=90pc)

3. In the **Create bucket** interface

{{% notice note %}}
You can name it differently as you like!
{{% /notice %}}

 - **Bucket type** select **General purpose**
 - **Bucket name** enter **```kms-key-s3```**

![create bucket](/images/4.create-s3/4.1create-bucket/0003.png?width=90pc)

4. Next step we scroll down to the **Object Ownership** section

 - Select **ACLs enabled**
 - **Object ownership** select **Object writer8**

![create bucket](/images/4.create-s3/4.1create-bucket/0004.png?width=90pc)

5. Next step we scroll down to **Block Public Access settings for this bucket** section

 - Uncheck **Block all public accesses**
 - Check **I acknowledge that the current settings might result in this bucket and the objects within becoming public**

![create bucket](/images/4.create-s3/4.1create-bucket/0005.png?width=90pc)

6. Next step we scroll down to the **Default encryption** section

 - **Encryption type** select **Server-side encryption with AWS Key Management Service keys (SSE-KMS)**
 - **AWS kMS Key** select **Choose fromy your AWS KMS keys**
 - **Availiable AWS KMS keys** select **kms-key-encrypt-decrypt**

![create bucket](/images/4.create-s3/4.1create-bucket/0006.png?width=90pc)

6. Next step we scroll down and press **Create bucket**

![create bucket](/images/4.create-s3/4.1create-bucket/0007.png?width=90pc)

7. Notification of successful creation

![create bucket](/images/4.create-s3/4.1create-bucket/0008.png?width=90pc)