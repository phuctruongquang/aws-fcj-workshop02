---
title : "Resource cleanup"
date : "`r Sys.Date()`"
weight : 7
chapter : false
pre : " <b> 7. </b> "
---

### Delete KMS resource

1. Access **AWS Management Console**

 - Find **KMS**
 - Select **KMS**

![delete kms](/aws-fcj-workshop02/images/7.delete-resources/7.1delete-kms/0001.png?width=90pc)

2. In the KMS interface

 - Check **kms-key-encrypt-decrypt**
 - Select **Key actions**
 - Select **Disable**

![delete kms](/aws-fcj-workshop02/images/7.delete-resources/7.1delete-kms/0002.png?width=90pc)

3. Next step

 - Check **Comfirm that you want to disable this key**
 - Press **Disable key**

![delete kms](/aws-fcj-workshop02/images/7.delete-resources/7.1delete-kms/0003.png?width=90pc)

4. Return to the KMS interface
 - Check **kms-key-encrypt-decrypt**
 - Select **Key actions**
 - Select **Schedule key deletion**

![delete kms](/aws-fcj-workshop02/images/7.delete-resources/7.1delete-kms/0004.png?width=90pc)

5. Next

 - **Waiting period (in days)** enter **7**
 - Check **Confirm that you want to schedule these keys for deletion after a 7 day waiting period**
 - Click **Schedule deletion**

![delete kms](/aws-fcj-workshop02/images/7.delete-resources/7.1delete-kms/0005.png?width=90pc)

6. Notification of success

![delete kms](/aws-fcj-workshop02/images/7.delete-resources/7.1delete-kms/0006.png?width=90pc)

### Delete CloudTrail resources

1. Access **AWS Management Console**

 - Find **CloudTrail**
 - Select **CloudTrail**

![delete cloudtrail](/aws-fcj-workshop02/images/7.delete-resources/7.2delete-cloudtrail/0001.png?width=90pc)

2. In the CloudTrail interface

 - Select **Trail**
 - Select **kms-key-cloudtrail**

![delete cloudtrail](/aws-fcj-workshop02/images/7.delete-resources/7.2delete-cloudtrail/0002.png?width=90pc)

3. Next step

 - Press **Stop logging**

![delete cloudtrail](/aws-fcj-workshop02/images/7.delete-resources/7.2delete-cloudtrail/0003.png?width=90pc)

 4. Next

 - Select **Stop logging**

![delete cloudtrail](/aws-fcj-workshop02/images/7.delete-resources/7.2delete-cloudtrail/0004.png?width=90pc)

5. After **Stop logging**, go back and press **Delete**

![delete cloudtrail](/aws-fcj-workshop02/images/7.delete-resources/7.2delete-cloudtrail/0005.png?width=90pc)

6. Next

 - Press **Delete**

![delete cloudtrail](/aws-fcj-workshop02/images/7.delete-resources/7.2delete-cloudtrail/0006.png?width=90pc)

7. Notification of success

![delete cloudtrail](/aws-fcj-workshop02/images/7.delete-resources/7.2delete-cloudtrail/0007.png?width=90pc)

### Delete S3 resource

1. Access **AWS Management Console**

 - Find **S3**
 - Select **S3**

![delete S3](/aws-fcj-workshop02/images/7.delete-resources/7.3delete-s3/0001.png?width=90pc)

2. In the **S3** interface

 - Select **aws-athena-query-results-058264191537-us-east-1**
 - Select **Empty**

![delete S3](/aws-fcj-workshop02/images/7.delete-resources/7.3delete-s3/0002.png?width=90pc)

3. Next step

 - Enter **```permanently delete```**
 - Press **Empty**

![delete S3](/aws-fcj-workshop02/images/7.delete-resources/7.3delete-s3/0003.png?width=90pc)

 4. Notice of **Empty** success

![delete S3](/aws-fcj-workshop02/images/7.delete-resources/7.3delete-s3/0004.png?width=90pc)

5. Continue returning to the CloudTrail interface

 - Select **aws-athena-query-results-058264191537-us-east-1**
 - Select **Delete**

![delete S3](/aws-fcj-workshop02/images/7.delete-resources/7.3delete-s3/0005.png?width=90pc)

6. Next step

 - Enter **```aws-athena-query-results-058264191537-us-east-1```**
 - Press **Delete bucket**

![delete S3](/aws-fcj-workshop02/images/7.delete-resources/7.3delete-s3/0006.png?width=90pc)

7. Continue returning to the CloudTrail interface

 - Select **kms-key-s3**
 - Select **Empty**

![delete S3](/aws-fcj-workshop02/images/7.delete-resources/7.3delete-s3/0007.png?width=90pc)

8. Next step

 - Enter **```permanently delete```**
 - Press **Empty**

![delete S3](/aws-fcj-workshop02/images/7.delete-resources/7.3delete-s3/0008.png?width=90pc)

9. Notification of success

![delete S3](/aws-fcj-workshop02/images/7.delete-resources/7.3delete-s3/0009.png?width=90pc)

10. Return to the CloudTrail interface

 - Select **kms-key-s3**
 - Select **Delete**

![delete S3](/aws-fcj-workshop02/images/7.delete-resources/7.3delete-s3/0010.png?width=90pc)

11. Next we press **Empty** again

![delete S3](/aws-fcj-workshop02/images/7.delete-resources/7.3delete-s3/0011.png?width=90pc)

12. Next step

 - Enter **```permanently delete```**
 - Press **Empty**

![delete S3](/aws-fcj-workshop02/images/7.delete-resources/7.3delete-s3/0012.png?width=90pc)

13. We return to the CloudTrail interface

 - Select **kms-key-s3**
 - Select **Delete**

![delete S3](/aws-fcj-workshop02/images/7.delete-resources/7.3delete-s3/0014.png?width=90pc)

14. Next

 - Enter **```kms-key-s3```**
 - Press **Delete bucket**

![delete S3](/aws-fcj-workshop02/images/7.delete-resources/7.3delete-s3/0015.png?width=90pc)

15. Deletion successful

![delete S3](/aws-fcj-workshop02/images/7.delete-resources/7.3delete-s3/0016.png?width=90pc)

### Delete User and Group resources

1. Access **AWS Management Console**

 - Find **IAM**
 - Select **IAM**

![delete user group](/aws-fcj-workshop02/images/7.delete-resources/7.4delete-usergroup/0001.png?width=90pc)

2. In the **IAM** interface

 - Select **User-S3**
 - Select **Delete**

![delete user group](/aws-fcj-workshop02/images/7.delete-resources/7.4delete-usergroup/0002.png?width=90pc)

3. Next step

 - Enter **```User-S3```**
 - Press **Delete user**

![delete user group](/aws-fcj-workshop02/images/7.delete-resources/7.4delete-usergroup/0003.png?width=90pc)

 4. Notification of success

![delete user group](/aws-fcj-workshop02/images/7.delete-resources/7.4delete-usergroup/0004.png?width=90pc)

5. Return to the **IAM** interface

 - Check **GroupLimit**
 - Select **Delete**

![delete user group](/aws-fcj-workshop02/images/7.delete-resources/7.4delete-usergroup/0005.png?width=90pc)

6. Next
 - Enter **```GroupLimit```**
 - Press **Delete**

![delete user group](/aws-fcj-workshop02/images/7.delete-resources/7.4delete-usergroup/0006.png?width=90pc)

7. Notification of success

![delete user group](/aws-fcj-workshop02/images/7.delete-resources/7.4delete-usergroup/0007.png?width=90pc)