---
title : "Tạo CloudTrail"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 5.1 </b> "
---

### Tạo CloudTrail

1. Truy cập **AWS Management Console**

   - Tìm **CloudTrail**
   - Chọn **CloudTrail**

![create cloudtrail](/aws-fcj-workshop02/images/5.create-cloudtrail/5.1create-cloudtrail/0001.png?width=90pc)

2. Trong giao diện **CloudTrail**

   - Chọn **Trails**
   - Chọn **Create trail**
  
![create cloudtrail](/aws-fcj-workshop02/images/5.create-cloudtrail/5.1create-cloudtrail/0002.png?width=90pc)

3. Trong phần **Choose trail attributes**
{{% notice note %}}
Bạn có thể tự đặt tên khác theo ý của các bạn nhé!
{{% /notice %}}
    - **Trail name** nhập **```kms-key-cloudtrail```**
    - **Storage location** chọn **Use existing S3 bucket**
    - Chọn **Browse**

![create cloudtrail](/aws-fcj-workshop02/images/5.create-cloudtrail/5.1create-cloudtrail/0003.png?width=90pc)


4. Bước tiếp theo

    - Chọn **kms-key-s3**
    - Ấn **Choose**

![create cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.1create-cloudtrail/0004.png?width=90pc)

5. Trong phần **Prefix - optional**
{{% notice note %}}
Bạn có thể tự đặt tên khác theo ý của các bạn nhé!
{{% /notice %}}
    - Nhập **```cloudtrail```**

![create cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.1create-cloudtrail/0005.png?width=90pc)

6. Chúng ra kéo xuống phần và ấn **Next**

![create cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.1create-cloudtrail/0006.png?width=90pc)

7. Trong phần **Choose log events**

    - **Event type** tích chọn **Management events**
    - Tích chọn **Data evntes**

![create cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.1create-cloudtrail/0007.png?width=90pc)

8. Bước tiếp theo chúng ta kéo xuống phần **Data events**

    - Chọn vào dòng chữ **Switch to basic event selector** để chuyển đổi chế độ

![create cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.1create-cloudtrail/0008.png?width=90pc)

9. Bước tiếp theo ấn **Continue**

![create cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.1create-cloudtrail/0009.png?width=90pc)

10. Trong phần **Data event: S3**

    - **Data event source** chọn **S3**
    - **S3 bucket** bỏ chọn **Read** và **Write**
    - **Individual bucket selection** ấn **Browse**

![create cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.1create-cloudtrail/0010.png?width=90pc)


11. Bước tiếp theo

    - Chọn **kms-key-s3**
    - Ấn **Choose**

![create cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.1create-cloudtrail/0011.png?width=90pc)

12. Bước tiếp theo ấn **Next**

![create cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.1create-cloudtrail/0012.png?width=90pc)

13. Bước tiếp theo kéo xuống dưới ấn **Create trail**

![create cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.1create-cloudtrail/0013.png?width=90pc)

14. Thông báo tạo thành công

![create cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.1create-cloudtrail/0014.png?width=90pc)

15. Các bạn truy cập vào lại **S3**

![create cloudtrai](/images/5.create-cloudtrail/5.1create-cloudtrail/0015.png?width=90pc)

16. Chọn **Buckets** chọn **kms-key-s3**

![create cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.1create-cloudtrail/0016.png?width=90pc)

17. Chúng ta sẽ thấy một thư mục được tạo ra có tên là **cloudtrail/**, thư mục này sẽ chứa tất cả nhật ký liên quan đến **kms-key-s3**

![create cloudtrai](/aws-fcj-workshop02/images/5.create-cloudtrail/5.1create-cloudtrail/0017.png?width=90pc)
