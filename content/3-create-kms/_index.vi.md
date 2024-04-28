---
title : "Tạo Key Management Service"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

#### Tạo KMS

1. Truy cập **AWS Management Console**

   - Tìm **KMS**
   - Chọn **Key Management Service**

![create kms](/images/3.create-kms/0001.png?width=90pc)

2. Trong giao diện **KMS**

   - Chọn **Customer managed keys**
   - Chọn **Create**
  
![create kms](/images/3.create-kms/0002.png?width=90pc)


3. Trong phần **Configure key**
    - Ở phần này chúng ta sẽ tạo ra một khóa đối xứng để mã hóa dữ liệu, bạn có thể tham khảo thêm khóa đối xứng và bất đối xứng tại [AWS Key Management Service](https://docs.aws.amazon.com/kms/latest/developerguide/key-types.html)
   - **Key type** chọn **Symmectric**
   - **Key usage** chọn **Encrypt and decrypt**
   - Ấn **Next**
  
![create kms](/images/3.create-kms/0003.png?width=90pc)

4. Trong phần **Add lables**

{{% notice note %}}
Bạn có thể tự đặt tên khác theo ý của các bạn nhé!
{{% /notice %}}
    - **Alias** nhập **```kms-key-encrypt-decrypt```**

![create kms](/images/3.create-kms/0004.png?width=90pc)

5. Bước tiếp theo chúng ra kéo xuống và ấn **Next**

![create kms](/images/3.create-kms/0005.png?width=90pc)

6. Trong phần **Define key administrative permissions**

   - **Key administrator** tìm **kms**
   - Tích chọn **kms-key-role**
   - **Key deletion** tích chọn dòng **Allow key administrators to delete this key**
   - Ấn **Next**

![create kms](/images/3.create-kms/0006.png?width=90pc)

7. Trong phần **Define key usage permissions**

   - **Key usage** tìm **kms**
   - Tích chọn **kms-key-role**
   - Ấn **Next**

![create kms](/images/3.create-kms/0007.png?width=90pc)

8. Bước tiếp theo chúng ta kéo xuống và ấn **Finish**

![create kms](/images/3.create-kms/0008.png?width=90pc)

9. Thông báo tạo thành công

![create kms](/images/3.create-kms/0010.png?width=90pc)


{{% notice warning %}}
Từ phần 10 trở đi là thông tin thêm chỉ để tham khảo, mục đích bài lab này chúng ta không cần sử dụng đến tính năng này!
{{% /notice %}}

Tự động xoay khóa trong AWS KMS là một tính năng giúp bạn tự động thay đổi khóa mã hóa của mình sau một khoảng thời gian nhất định (Từ 90 ngày và lên đến 2560 ngày). Điều này giúp tăng cường bảo mật cho dữ liệu của bạn bằng cách giảm thiểu nguy cơ khóa của bạn bị lộ hoặc xâm phạm. Đường dẫn tham khảo thêm [Rotating AWS KMS keys](https://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html)


10. Các bạn trở lại giao diện **KMS**

    - Chọn vào Key vừa mới tạo

![create kms](/images/3.create-kms/0011.png?width=90pc)

11. Tiếp theo

    - Chọn **Key rotation**
    - Chọn **Edit**

![create kms](/images/3.create-kms/0012.png?width=90pc)

12. Trong phần **Edit automaitic key rotation**

    - Chọn **Ebale**
    - Phần **Rotation period (in days)** bạn có thể tùy chỉnh tự động thay đổi khóa mã hóa của bạn bạn sau bao nhiêu ngày 1 lần nhé.

![create kms](/images/3.create-kms/0013.png?width=90pc)

