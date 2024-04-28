---
title : "Ghi nhật ký vào CloudTrail"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 5.2 </b> "
---

### Ghi nhật ký vào CloudTrail

1. Truy cập **AWS Management Console**

   - Tìm **S3**
   - Chọn **S3**

![test cloudtrail](/aws-fcj-workshop02/images/5.create-cloudtrail/5.2test-cloudtrail/0001.png?width=90pc)

2. Trong giao diện **S3**

   - Chọn **Buckets**
   - Chọn **kms-key-s3**
  
![test cloudtrail](/aws-fcj-workshop02/images/5.create-cloudtrail/5.2test-cloudtrail/0002.png?width=90pc)

3. Tiếp theo chúng ta chọn vào thư mục **cloudtrail/**

![test cloudtrail](/aws-fcj-workshop02/images/5.create-cloudtrail/5.2test-cloudtrail/0003.png?width=90pc)

4. Bước tiếp theo

    - Các bạn chọn theo đường dẫn và thấy ở trong thư mục **cloudtrail/** chưa có nhật ký nào được ghi lại

![test cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.2test-cloudtrail/0004.png?width=90pc)

5. Các bạn quay trở lại phần **kms-key-s3**

    - Chọn **Upload**

![test cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.2test-cloudtrail/0005.png?width=90pc)

6. Trong phần **Upload**

    - Chọn **Add files**
    - Chọn **File** tải về ở phần 4.2
    - Ấn **Open**

![test cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.2test-cloudtrail/0006.png?width=90pc)

7. Bước tiếp theo

    - Chọn vào **Properties**

![test cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.2test-cloudtrail/0007.png?width=90pc)

8. Chúng ra kéo xuống phần **Server-side encryption**

    - **Server-side encryption** chọn **Specify an encryption key**
    - **Encryption settings** chọn **Override bucket settings for default encryption**
    - **Encryption type** chọn **Server-side encryption with AWS Key Management Service keys (SSE-KMS)**
    - **AWS KMS key** chọn **Choose from your AWS KMS keys**

![test cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.2test-cloudtrail/0008.png?width=90pc)

9. Chúng ta kéo xuống phần **Available AWS KMS keys**

    - Chọn **kms-key-encrypt-decrypt**

![test cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.2test-cloudtrail/0009.png?width=90pc)

10. Kéo xuống và ấn **Upload**

![test cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.2test-cloudtrail/0010.png?width=90pc)

11. Thông báo upload thành công

![test cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.2test-cloudtrail/0011.png?width=90pc)

12. Các bạn quay trở lại và chọn vào thư mục **cloudtrail/**

![test cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.2test-cloudtrail/0012.png?width=90pc)

13. Các bạn chọn theo đường đẫn và thấy nhật ký đã được ghi lại vào trong thư mục **cloudtrail/**

{{% notice note %}}
Ở đây mình upload dữ liệu lên ngày 16/04/2024 nhật ký sẽ tự động tạo ra thư mục **2024/ > 04/ > 16/**. Các bạn upload dữ liệu lên ngày, tháng, năm nào thì nhật ký sẽ tự tạo ra thư mục nhé!
{{% /notice %}}

![test cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.2test-cloudtrail/0013.png?width=90pc)
