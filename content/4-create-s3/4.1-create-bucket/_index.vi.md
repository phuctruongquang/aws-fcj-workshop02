---
title : "Tạo Bucket"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---

#### Tạo Bucket

1. Truy cập **AWS Management Console**

   - Tìm **S3**
   - Chọn **S3**

![create bucket](/images/4.create-s3/4.1create-bucket/0001.png?width=90pc)

2. Trong giao diện **S3**

   - Chọn **Buckets**
   - Chọn **Create bucket**
  
![create bucket](/images/4.create-s3/4.1create-bucket/0002.png?width=90pc)

3. Trong giao diện **Create bucket**

{{% notice note %}}
Bạn có thể tự đặt tên khác theo ý của các bạn nhé!
{{% /notice %}}

   - **Bucket type** chọn **General purpose**
   - **Bucket name** nhập **```kms-key-s3```**

![create bucket](/images/4.create-s3/4.1create-bucket/0003.png?width=90pc)

4. Bước tiếp theo chúng ta kéo xuống phần **Object Ownership**

   - Chọn **ACLs enabled**
   - **Object ownership** chọn **Object writer8**

![create bucket](/images/4.create-s3/4.1create-bucket/0004.png?width=90pc)

5. Bước tiếp theo chúng ta kéo xuống phần **Block Public Access settings for this bucket**

   - Bỏ tích **Block all public acces**
   - Tích chọn **I acknowledge that the current settings might result in this bucket and the objects within becoming public**

![create bucket](/images/4.create-s3/4.1create-bucket/0005.png?width=90pc)

6. Bước tiếp theo chúng ta kéo xuống phần **Default encryption**

    - **Encryption type** chọn **Server-side encryption with AWS Key Management Service keys (SSE-KMS)**
    - **AWS kMS Key** chọn **Choose fromy your AWS KMS keys**
    - **Availiable AWS KMS keys** chọn **kms-key-encrypt-decrypt**

![create bucket](/images/4.create-s3/4.1create-bucket/0006.png?width=90pc)

6. Bước tiếp theo chúng ta kéo xuống và ấn **Create bucket**

![create bucket](/images/4.create-s3/4.1create-bucket/0007.png?width=90pc)

7. Thông báo tạo thành công

![create bucket](/images/4.create-s3/4.1create-bucket/0008.png?width=90pc)

