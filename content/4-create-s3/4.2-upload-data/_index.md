---
title : "Upload data to S3"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---

#### Upload data to S3

You download the data at this link and extract it to perform the next steps [Data to post](https://github.com/phuctruongquang/aws-fcj-workshop02/blob/main/DATA.rar )

1. Access **AWS Management Console**

 - Find **S3**
 - Select **S3**

![upload data](/aws-fcj-workshop02/images/4.create-s3/4.2upload-data/0001.png?width=90pc)

2. In the **S3** interface

 - Select **Buckets**
 - Select **kms-key-s3**

![upload data](/aws-fcj-workshop02/images/4.create-s3/4.2upload-data/0002.png?width=90pc)

3. Next step we choose **Upload**

![upload data](/aws-fcj-workshop02/images/4.create-s3/4.2upload-data/0003.png?width=90pc)

4. Next step in **Upload** section

 - Select **Add files**
 - Select the **File** you just downloaded and select **Open**

![upload data](/aws-fcj-workshop02/images/4.create-s3/4.2upload-data/0004.png?width=90pc)

5. Next step

 - You will see **File** has been **Uploaded**
 - Next we will select the **Properties** section

![upload data](/aws-fcj-workshop02/images/4.create-s3/4.2upload-data/0006.png?width=90pc)

6. Scroll down to the **Server-side encryption** section

 - **Server-side encryption** select **Specify an encryption key**
 - **Encryption settings** select **Override bucket settings for default encryption**
 - **Encryption type** select **Server-side encryption with AWS Key Management Service keys (SSE-KMS)**

![upload data](/aws-fcj-workshop02/images/4.create-s3/4.2upload-data/0007.png?width=90pc)

6. Scroll down to the **AWS KMS key** section

 - Select **Choose from your AWS KMS key**
 - **Available AWS KMS keys** select **kms-key-encrypt-decrypt**

![upload data](/aws-fcj-workshop02/images/4.create-s3/4.2upload-data/0008.png?width=90pc)

7. Next step we scroll down and select **Upload**

![upload data](/aws-fcj-workshop02/images/4.create-s3/4.2upload-data/0009.png?width=90pc)

8. Notification of successful data upload

![upload data](/aws-fcj-workshop02/images/4.create-s3/4.2upload-data/0010.png?width=90pc)