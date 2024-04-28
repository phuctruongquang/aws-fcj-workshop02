---
title : "Truy xuất dữ liệu với Athena"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 5.4 </b> "
---

### Truy xuất dữ liệu với Athena

1. Truy cập **AWS Management Console**

   - Tìm **Athena**
   - Chọn **Athena**

![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0001.png?width=90pc)

2. Trong giao diện **Athena**

   - Chọn **Query editor**
   - Chọn **Edit settings**
  
![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0002.png?width=90pc)

3. Trong phần **Manage settings**

    - Chọn **Browse S3**

![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0003.png?width=90pc)

4. Bước tiếp theo

    - Chọn **kms-key-s3**
    - Ấn **Choose**

![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0004.png?width=90pc)


5. Bước tiếp theo ấn **Save**

![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0005.png?width=90pc)

6. Chúng ta quay trở lại phần **Query editor**

    - Chọn **Editor**
    - Chọn dấu 3 chấm ở bảng **cloudtrail-log-kms-key-s3-cloudtrail**
    - Chọn **Preview table**

![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0006.png?width=90pc)

7. Các bạn kéo xuống bên dưới sẽ thấy các nhật ký đã xuất hiện

![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0007.png?width=90pc)

8. Truy xuất thử thử **eventname** của nhật ký **kms-key-s3**

    - Nhập vào bảng câu lệnh truy xuất **```SELECT eventname FROM "default". "cloudtrail_logs_kms_key_s3_cloudtrail" limit 100;```**
    - Sau đó ấn **Run** để chạy câu lệnh

![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0008.png?width=90pc)

9. Các bạn kéo xuống và sẽ thấy đã truy xuất **eventname** thành công
	
![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0009.png?width=90pc)

{{% notice note %}}
Ở trên là một ví dụ để truy xuất dữ liệu. Bạn có thể tự truy xuất những gì mà bạn cần trong Query results.
{{% /notice %}}