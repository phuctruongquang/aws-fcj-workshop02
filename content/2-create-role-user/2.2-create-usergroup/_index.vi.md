---
title : "Tạo Group và User"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

#### Tạo Group

1. Truy cập **AWS Management Console**

   - Tìm **IAM**
   - Chọn **IAM**

![create group](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0001.png?width=90pc)

2. Trong giao diện **IAM**

   - Chọn **User groups**
   - Chọn **Create group**
  
![create group](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0002.png?width=90pc)


3. Trong phần **Create user group**

{{% notice note %}}
Bạn có thể tự đặt tên khác theo ý của các bạn nhé!
{{% /notice %}}

   - **User name group** nhập **```GroupLimit```**
  
![create subnet](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0003.png?width=90pc)

4. Kéo xuống phần **Attach permissions polices**

   - Nhấp vào thanh tìm kiếm và chọn **S3**
   - Tích chọn **AmazonS3FullAccess**
   - Ấn **Create group**

![create group](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0004.png?width=90pc)

5. Thông báo tạo thành công

![create group](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0005.png?width=90pc)

#### Bước tiếp theo chúng ta tạo User

6. Trong giao diện **IAM**

   - Chọn **Users**
   - Chọn **Create user**

![create user](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0006.png?width=90pc)

7. Trong phần **Specify user details**

{{% notice note %}}
Bạn có thể tự đặt tên khác theo ý của các bạn nhé!
{{% /notice %}}

   - **User name** nhập **```User-S3```**
   - Tích chọn **Provide user access to the AWS Management Console**
   - Tích chọn **I want to create an IAM user**

![create user](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0007.png?width=90pc)

8. Kéo xuống phần **Console password**

   - Nhập **Password của bạn**
   - Bỏ tích **Users must create a new password at next sign-in** (Mình sẽ không cần đổi mật khẩu khi đăng nhập lần đầu)
   - Ấn **Next**

![create user](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0008.png?width=90pc)

9. Trong phần **Permissions options**

   - Chọn **Add user to group**
   - Tích chọn vào **GroupLimit** mới vừa tạo
   - Ấn **Next**

![create user](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0009.png?width=90pc)

10. Kéo xuống dưới và ấn **Create user**

![create user](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0010.png?width=90pc)

11. Thông báo tạo thành công

   - Sau khi tạo thành công thì bạn sao chép đường đẫn và mở trang ẩn danh hoặc một trình duyệt mới và dán vào

![create user](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0011.png?width=90pc)

12. Đăng nhập các thông tin mà bạn vừa tạo

![create user](//aws-fcj-workshop02images/2.create-role-user/2.2create-usergroup/0012.png?width=90pc)

13. Thành công đăng nhập vào **User-S3**

![create user](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0013.png?width=90pc)
