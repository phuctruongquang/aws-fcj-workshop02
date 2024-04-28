---
title : "Test and share encrypted data on S3"
date : "`r Sys.Date()`"
weight : 6
chapter : false
pre : " <b> 6. </b> "
---

### Test and share encrypted data on S3

1. Access **AWS Management Console**

 - Find **S3**
 - Select **S3**

![demo](/images/6.demo/0001.png?width=90pc)

2. In the **S3** interface

 - Select **Buckets**
 - Select **kms-key-s3**

![demo](/images/6.demo/0002.png?width=90pc)

3. In the **kms-key-s3** section

 - Select the data **awsstudygroup.jpg**
 - Press **Open**

![demo](/images/6.demo/0003.png?width=90pc)

4. As you can see, after pressing **Open**, the data will be opened. Because I have created access rights for the account as the owner, I will have access to the data.

![demo](/images/6.demo/0004.png?width=90pc)

5. Next we **Make public** the purpose is to allow everyone to test access to data on S3

{{% notice warning %}}
"Making public" an S3 bucket encrypted with KMS creates a conflict of purpose. Even though the content is encrypted, "Make public" bucket means that anyone with the decryption key (which may be shared or accessed without permission) can access and decrypt the content (Purpose make public just for demo purposes).
{{% /notice %}}

6. Return to the **kms-key-s3** interface

 - Select data **awsstudygroup**
 - Select **Actions**
 - Select **Make public using ACL**

![4.2upload-data](/images/4.create-s3/4.2upload-data/0012.png?width=90pc)

7. In the **Make public** section

 - Press **Make public**

![4.2upload-data](/images/4.create-s3/4.2upload-data/0013.png?width=90pc)

8. Notification of success

![4.2upload-data](/images/4.create-s3/4.2upload-data/0014.png?width=90pc)

9. They return to the **kms-key-s3** section

 - Select **awsstudygroup**
 - Press **Copy URL**

![demo](/images/6.demo/0005.png?width=90pc)

10. After pasting the URL into a new tab. You will not be able to open AWS-side data requests that specify server-side encryption with an AWS KMS managed key that requires AWS Signature Version 4.

![demo](/images/6.demo/0006.png?width=90pc)

11. Next, go back to the incognito tab and log in with the user information created in section 2.2 [Create Group and User](2-create-role-user/2.2-create-usergroup)

 - Then access **S3**
 - Select **Buckets**
 - Select **awsstudygroup**
 - Select **Open**

![demo](/images/6.demo/0007.png?width=90pc)

12. On **User-S3** you will receive an access denied message and decryption is not allowed because no policy is applied on this **User-S3** (In this step for see the new owner has permissions to view and open the data)

![demo](/images/6.demo/0008.png?width=90pc)

13. If you are still in **User-S3**, go back to **kms-key-s3**

 - Select **awsstudygroup**
 - **Copy URL**

![demo](/images/6.demo/0009.png?width=90pc)

14. After pasting the URL into a new tab. You will not be able to open AWS-side data requests that specify server-side encryption with an AWS KMS managed key that requires AWS Signature Version 4.

![demo](/images/6.demo/0010.png?width=90pc)

{{% notice info %}}
In this section, a URL will be created to share data with everyone.
{{% /notice %}}

15. You return to your original **User**

 - Access to **S3**
 - Select **qrcode_facebook_awsstudygroup**
 - Select **Actions**

![demo](/images/6.demo/0011.png?width=90pc)

Select **Share with a presigned URL**

![demo](/images/6.demo/0012.png?width=90pc)

16. Next step

 - **Time interval until the presigned URL expires** select **Minutes**
 - **Mumber of minutes** choose **2** (I let this part demo for 2 minutes)
 - Press **Create persigned URL**

![demo](/images/6.demo/0013.png?width=90pc)

17. Notify success and press **Copy persigned URL**

![demo](/images/6.demo/0014.png?width=90pc)

18. Anyone who gets this link can open it to view data within 2 minutes

![demo](/images/6.demo/0015.png?width=90pc)

19. After 2 minutes, there will be a notification Access Denied and access will expire

![demo](/images/6.demo/0016.png?width=90pc)