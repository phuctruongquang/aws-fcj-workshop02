---
title : "Kiểm thử và chia sẻ dữ liệu mã hóa trên S3"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : " <b> 6. </b> "
---

### Kiểm thử và chia sẻ dữ liệu mã hóa trên S3

1. Truy cập **AWS Management Console**

   - Tìm **S3**
   - Chọn **S3**

![demo](/images/6.demo/0001.png?width=90pc)

2. Trong giao diện **S3**

   - Chọn **Buckets**
   - Chọn **kms-key-s3**
  
![demo](/images/6.demo/0002.png?width=90pc)

3. Trong phần **kms-key-s3**

    - Tích chọn vào dữ liệu **awsstudygroup.jpg**
    - Ấn **Open**

![demo](/images/6.demo/0003.png?width=90pc)

4. Như bạn đã thấy, sau khi ấn **Open** thì dữ liệu sẽ được mở lên. Tại vì mình đã tạo quyền truy cập cho tài khoản là chủ sở hữu nên sẽ được truy cập vào dữ liệu.

![demo](/images/6.demo/0004.png?width=90pc)

5. Tiếp theo chúng ta **Make public** mục đích là để cho phép mọi người truy cập thử dữ liệu trên S3

{{% notice warning %}}
Việc "make public" một bucket S3 được mã hóa bằng KMS tạo ra mâu thuẫn về mục đích. Mặc dù nội dung được mã hóa, nhưng việc "Make public" bucket có nghĩa là bất kỳ ai có khóa giải mã (có thể được chia sẻ hoặc truy cập trái phép) đều có thể truy cập và giải mã nội dung (Mục đích make public chỉ để làm bài demo).
{{% /notice %}}

6. Quay trở lại giao diện **kms-key-s3**

    - Tích chọn dữ liệu **awsstudygroup**
    - Chọn **Actions**
    - Chọn **Make public using ACL**

![4.2upload-data](/images/4.create-s3/4.2upload-data/0012.png?width=90pc)

7. Trong phần **Make public**

    - Ấn **Make public**

![4.2upload-data](/images/4.create-s3/4.2upload-data/0013.png?width=90pc)

8. Thông báo thành công

![4.2upload-data](/images/4.create-s3/4.2upload-data/0014.png?width=90pc)

9. Chúng quay trở lại phần **kms-key-s3**

    - Tích chọn **awsstudygroup**
    - Ấn **Copy URL**

![demo](/images/6.demo/0005.png?width=90pc)

10. Sau khi dán đường dẫn URL vào một tab mới. Bạn sẽ không thể mở được dữ liệu phía AWS các yêu cầu chỉ định mã hóa phía máy chủ bằng khóa được quản lý AWS KMS yêu cầu AWS Signature Phiên bản 4.

![demo](/images/6.demo/0006.png?width=90pc)

11. Tiếp theo các bạn quay lại tab ẩn danh và đăng nhập thông tin user đã tạo ở phần 2.2 [Tạo Group và User](2-create-role-user/2.2-create-usergroup)

    - Sau đó truy cập vào **S3**
    - Chọn **Buckets**
    - Chọn **awsstudygroup**
    - Chọn **Open**

![demo](/images/6.demo/0007.png?width=90pc)

12. Ở **User-S3** bạn sẽ nhận được thông báo truy cập bị từ chối và không được phép giải mã vì không có chính sách nào được áp dụng trên **User-S3** này (Ở bước này cho thấy chủ sở hữu mới có quyền hạn để xem và mở dữ liệu)

![demo](/images/6.demo/0008.png?width=90pc)

13. Các bạn vẫn ở **User-S3** trở lại phần **kms-key-s3**

    - Tích chọn **awsstudygroup**
    - **Copy URL**

![demo](/images/6.demo/0009.png?width=90pc)

14. Sau khi dán đường dẫn URL vào một tab mới. Bạn sẽ không thể mở được dữ liệu phía AWS các yêu cầu chỉ định mã hóa phía máy chủ bằng khóa được quản lý AWS KMS yêu cầu AWS Signature Phiên bản 4.

![demo](/images/6.demo/0010.png?width=90pc)

{{% notice info %}}
Ở phần này sẽ tạo ra URL để chia sẻ dữ liệu cho tất cả mọi người.
{{% /notice %}}

15. Bạn quay lại **User** lúc đầu của bạn

    - Truy cập vào **S3**
    - Tích chọn **qrcode_facebook_awsstudygroup**
    - Chọn **Actions**

![demo](/images/6.demo/0011.png?width=90pc)

Chọn **Share with a presigned URL**

![demo](/images/6.demo/0012.png?width=90pc)

16. Bước tiếp theo

    - **Time interval until the presigned URL expires** chọn **Minutes**
    - **Mumber of minutes** chọn **2** (Phần này mình để demo là 2 phút)
    - Ấn **Create persigned URL**

![demo](/images/6.demo/0013.png?width=90pc)

17. Thông báo thành công và ấn **Copy persigned URL**

![demo](/images/6.demo/0014.png?width=90pc)

18. Tất cả ai có được đường dẫn này đều có thể mở để xem dữ liệu trong vòng 2 phút

![demo](/images/6.demo/0015.png?width=90pc)

19. Sau hết 2 phút thì sẽ có thông báo Truy cập bị từ chối và hết hạn truy cập

![demo](/images/6.demo/0016.png?width=90pc)
