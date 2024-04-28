---
title : "Đăng tải dữ liệu lên S3"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 4.2 </b> "
---

#### Đăng tải dữ liệu lên S3

    - Chỗ này để tải Source lên




1. Truy cập **AWS Management Console**

   - Tìm **S3**
   - Chọn **S3**

![upload data](/images/4.create-s3/4.2upload-data/0001.png?width=90pc)

2. Trong giao diện **S3**

   - Chọn **Buckets**
   - Chọn **kms-key-s3**
  
![upload data](/images/4.create-s3/4.2upload-data/0002.png?width=90pc)

3. Bước tiếp theo chúng ta chọn **Upload**

![upload data](/images/4.create-s3/4.2upload-data/0003.png?width=90pc)

4. Bước tiếp theo trong phần **Upload**

    - Chọn **Add files**
    - Chọn **File** vừa mới tải về và chọn **Open**

![upload data](/images/4.create-s3/4.2upload-data/0004.png?width=90pc)

5. Bước tiếp theo

    - Bạn sẽ thấy **File** đã được **Upload**
    - Tiếp theo chúng ta sẽ chọn vào phần **Properties**

![upload data](/images/4.create-s3/4.2upload-data/0006.png?width=90pc)

6. Chúng ra kéo xuống phần **Server-side encryption**

    - **Server-side encryption** chọn **Specify an encryption key**
    - **Encryption settings** chọn **Override bucket settings for default encryption**
    - **Encryption type** chọn **Server-side encryption with AWS Key Management Service keys (SSE-KMS)**

![upload data](/images/4.create-s3/4.2upload-data/0007.png?width=90pc)

6. Chúng ra kéo xuống phần **AWS KMS key**

    - Chọn **Choose from your AWS KMS key**
    - **Available AWS KMS keys** chọn **kms-key-encrypt-decrypt**

![upload data](/images/4.create-s3/4.2upload-data/0008.png?width=90pc)

7. Bước tiếp theo chúng ta kéo xuống và chọn **Upload**

![upload data](/images/4.create-s3/4.2upload-data/0009.png?width=90pc)

8. Thông báo đăng tải dữ liệu thành công

![upload data](/images/4.create-s3/4.2upload-data/0010.png?width=90pc)

