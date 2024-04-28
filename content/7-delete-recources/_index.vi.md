---
title : "Dọn dẹp tài nguyên"
date :  "`r Sys.Date()`" 
weight : 7
chapter : false
pre : " <b> 7. </b> "
---

### Xóa tài nguyên KMS

1. Truy cập **AWS Management Console**

   - Tìm **KMS**
   - Chọn **KMS**

![delete kms](/images/7.delete-resources/7.1delete-kms/0001.png?width=90pc)

2. Trong giao diện KMS

    - Tích chọn **kms-key-encrypt-decrypt**
    - Chọn **Key actions**
    - Chọn **Disable**

![delete kms](/images/7.delete-resources/7.1delete-kms/0002.png?width=90pc)

3. Bước tiếp theo

    - Tích chọn **Comfirm that you want to disable this key**
    - Ấn **Disable key**

![delete kms](/images/7.delete-resources/7.1delete-kms/0003.png?width=90pc)

4. Quay trở lại giao diện KMS
    - Tích chọn **kms-key-encrypt-decrypt**
    - Chọn **Key actions**
    - Chọn **Schedule key deletion**

![delete kms](/images/7.delete-resources/7.1delete-kms/0004.png?width=90pc)

5. Tiếp theo

    - **Waiting period (in days)** nhập **7**
    - Tích chọn **Confirm that you want to schedule these keys for deletion after a 7 day waiting period**
    - Ấn **Schedule deletion**

![delete kms](/images/7.delete-resources/7.1delete-kms/0005.png?width=90pc)

6. Thông báo thành công

![delete kms](/images/7.delete-resources/7.1delete-kms/0006.png?width=90pc)

### Xóa tài nguyên CloudTrail

1. Truy cập **AWS Management Console**

   - Tìm **CloudTrail**
   - Chọn **CloudTrail**

![delete cloudtrail](/images/7.delete-resources/7.2delete-cloudtrail/0001.png?width=90pc)

2. Trong giao diện CloudTrail

    - Chọn **Trail**
    - Chọn **kms-key-cloudtrail**

![delete cloudtrail](/images/7.delete-resources/7.2delete-cloudtrail/0002.png?width=90pc)

3. Bước tiếp theo

    - Ấn **Stop logging**

![delete cloudtrail](/images/7.delete-resources/7.2delete-cloudtrail/0003.png?width=90pc)
 
 4. Tiếp theo

    - Chọn **Stop logging**

![delete cloudtrail](/images/7.delete-resources/7.2delete-cloudtrail/0004.png?width=90pc)

5. Sau khi **Stop logging** thì quay trở lại ấn **Delete**

![delete cloudtrail](/images/7.delete-resources/7.2delete-cloudtrail/0005.png?width=90pc)

6. Tiếp theo

    - Ấn **Delete**

![delete cloudtrail](/images/7.delete-resources/7.2delete-cloudtrail/0006.png?width=90pc)

7. Thông báo thành công

![delete cloudtrail](/images/7.delete-resources/7.2delete-cloudtrail/0007.png?width=90pc)

### Xóa tài nguyên S3

1. Truy cập **AWS Management Console**

   - Tìm **S3**
   - Chọn **S3**

![delete S3](/images/7.delete-resources/7.3delete-s3/0001.png?width=90pc)

2. Trong giao diện **S3**

    - Tích chọn **aws-athena-query-results-058264191537-us-east-1**
    - Chọn **Empty**

![delete S3](/images/7.delete-resources/7.3delete-s3/0002.png?width=90pc)

3. Bước tiếp theo

    - Nhập vào **```permanently delete```**
    - Ấn **Empty**

![delete S3](/images/7.delete-resources/7.3delete-s3/0003.png?width=90pc)
 
 4. Thông báo **Empty** thành công

![delete S3](/images/7.delete-resources/7.3delete-s3/0004.png?width=90pc)

5. Tiếp tục quay lại giao diện CloudTrail

    - Tích chọn **aws-athena-query-results-058264191537-us-east-1**
    - Chọn **Delete**

![delete S3](/images/7.delete-resources/7.3delete-s3/0005.png?width=90pc)

6. Bước tiếp theo
    
    - Nhập vào **```aws-athena-query-results-058264191537-us-east-1```**
    - Ấn **Delete bucket**

![delete S3](/images/7.delete-resources/7.3delete-s3/0006.png?width=90pc)

7. Tiếp tục quay lại giao diện CloudTrail

    - Tích chọn vào **kms-key-s3**
    - Chọn **Empty**

![delete S3](/images/7.delete-resources/7.3delete-s3/0007.png?width=90pc)

8. Bước tiếp theo

    - Nhập vào **```permanently delete```**
    - Ấn **Empty**

![delete S3](/images/7.delete-resources/7.3delete-s3/0008.png?width=90pc)

9. Thông báo thành công

![delete S3](/images/7.delete-resources/7.3delete-s3/0009.png?width=90pc)

10. Quay lại giao diện CloudTrail

    - Tích chọn vào **kms-key-s3**
    - Chọn **Delete**

![delete S3](/images/7.delete-resources/7.3delete-s3/0010.png?width=90pc)

11. Tiếp theo chúng ta ấn **Empty** một lần nữa

![delete S3](/images/7.delete-resources/7.3delete-s3/0011.png?width=90pc)

12. Bước tiếp theo

    - Nhập vào **```permanently delete```**
    - Ấn **Empty**

![delete S3](/images/7.delete-resources/7.3delete-s3/0012.png?width=90pc)

13. Chúng ta quay lại giao diện CloudTrail

    - Tích chọn vào **kms-key-s3**
    - Chọn **Delete**

![delete S3](/images/7.delete-resources/7.3delete-s3/0014.png?width=90pc)

14. Tiếp theo

    - Nhập **```kms-key-s3```**
    - Ấn **Delete bucket**

![delete S3](/images/7.delete-resources/7.3delete-s3/0015.png?width=90pc)

15. Xóa thành công

![delete S3](/images/7.delete-resources/7.3delete-s3/0016.png?width=90pc)

### Xóa tài nguyên User và Group

1. Truy cập **AWS Management Console**

   - Tìm **IAM**
   - Chọn **IAM**

![delete user group](/images/7.delete-resources/7.4delete-usergroup/0001.png?width=90pc)

2. Trong giao diện **IAM**

    - Tích chọn **User-S3**
    - Chọn **Delete**

![delete user group](/images/7.delete-resources/7.4delete-usergroup/0002.png?width=90pc)

3. Bước tiếp theo

    - Nhập vào **```User-S3```**
    - Ấn **Delete user**

![delete user group](/images/7.delete-resources/7.4delete-usergroup/0003.png?width=90pc)
 
 4. Thông báo thành công

![delete user group](/images/7.delete-resources/7.4delete-usergroup/0004.png?width=90pc)

5. Quay trở lại giao diện **IAM**

    - Tích chọn **GroupLimit**
    - Chọn **Delete**

![delete user group](/images/7.delete-resources/7.4delete-usergroup/0005.png?width=90pc)

6. Tiếp theo
    - Nhập vào **```GroupLimit```**
    - Ấn **Delete**

![delete user group](/images/7.delete-resources/7.4delete-usergroup/0006.png?width=90pc)

7. Thông báo thành công

![delete user group](/images/7.delete-resources/7.4delete-usergroup/0007.png?width=90pc)
