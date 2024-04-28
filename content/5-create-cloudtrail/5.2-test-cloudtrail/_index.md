---
title : "Logging to CloudTrail"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 5.2 </b> "
---

### Logging to CloudTrail

1. Access **AWS Management Console**

 - Find **S3**
 - Select **S3**

![test cloudtrail](/images/5.create-cloudtrail/5.2test-cloudtrail/0001.png?width=90pc)

2. In the **S3** interface

 - Select **Buckets**
 - Select **kms-key-s3**

![test cloudtrail](/images/5.create-cloudtrail/5.2test-cloudtrail/0002.png?width=90pc)

3. Next we select the **cloudtrail/** folder

![test cloudtrail](/images/5.create-cloudtrail/5.2test-cloudtrail/0003.png?width=90pc)

4. Next step

 - You follow the path and see that in the **cloudtrail/** folder there are no logs recorded

![test cloudtrai](/images/5.create-cloudtrail/5.2test-cloudtrail/0004.png?width=90pc)

5. Go back to **kms-key-s3**

 - Select **Upload**

![test cloudtrai](/images/5.create-cloudtrail/5.2test-cloudtrail/0005.png?width=90pc)

6. In the **Upload** section

 - Select **Add files**
 - Select **File** to download in section 4.2
 - Press **Open**

![test cloudtrai](/images/5.create-cloudtrail/5.2test-cloudtrail/0006.png?width=90pc)

7. Next step

 - Select **Properties**

![test cloudtrai](/images/5.create-cloudtrail/5.2test-cloudtrail/0007.png?width=90pc)

8. Scroll down to the **Server-side encryption** section

 - **Server-side encryption** select **Specify an encryption key**
 - **Encryption settings** select **Override bucket settings for default encryption**
 - **Encryption type** select **Server-side encryption with AWS Key Management Service keys (SSE-KMS)**
 - **AWS KMS key** select **Choose from your AWS KMS keys**

![test cloudtrai](/images/5.create-cloudtrail/5.2test-cloudtrail/0008.png?width=90pc)

9. We scroll down to the **Available AWS KMS keys** section

 - Select **kms-key-encrypt-decrypt**

![test cloudtrai](/images/5.create-cloudtrail/5.2test-cloudtrail/0009.png?width=90pc)

10. Scroll down and press **Upload**

![test cloudtrai](/images/5.create-cloudtrail/5.2test-cloudtrail/0010.png?width=90pc)

11. Notification of successful upload

![test cloudtrai](/images/5.create-cloudtrail/5.2test-cloudtrail/0011.png?width=90pc)

12. Go back and select the **cloudtrail/** folder

![test cloudtrai](/images/5.create-cloudtrail/5.2test-cloudtrail/0012.png?width=90pc)

13. You choose the path and see the log has been recorded in the folder **cloudtrail/**

{{% notice note %}}
Here, I upload data to April 16, 2024. The log will automatically create the folder **2024/ > 04/ > 16/**. If you upload data to any day, month, or year, the diary will automatically create a folder!
{{% /notice %}}

![test cloudtrai](/images/5.create-cloudtrail/5.2test-cloudtrail/0013.png?width=90pc)