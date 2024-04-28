---
title : "Create Group and User"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

1. Access **AWS Management Console**

 - Find **IAM**
 - Select **IAM**

![create group](/aws-fcj-workshop02/images/2.create-role-user/2.1create-role/0001.png?width=90pc)

2. In the **IAM** interface

 - Select **User groups**
 - Select **Create group**

![create group](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0002.png?width=90pc)


3. In the **Create user group** section

{{% notice note %}}
You can name it differently as you like!
{{% /notice %}}

 - **User name group** enter **```GroupLimit```**

![create subnet](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0003.png?width=90pc)

4. Scroll down to the **Attach permissions polices** section

 - Click on the search bar and select **S3**
 - Select **AmazonS3FullAccess**
 - Press **Create group**

![create group](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0004.png?width=90pc)

5. Notification of successful creation

![create group](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0005.png?width=90pc)

#### Next step we create User

6. In the **IAM** interface

 - Select **Users**
 - Select **Create user**

![create user](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0006.png?width=90pc)

7. In the **Specify user details** section

{{% notice note %}}
You can name it differently as you like!
{{% /notice %}}

 - **User name** enter **```User-S3```**
 - Check **Provide user access to the AWS Management Console**
 - Check **I want to create an IAM user**

![create user](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0007.png?width=90pc)

8. Scroll down to **Console password** section

 - Enter **Your Password**
 - Uncheck **Users must create a new password at next sign-in** (I will not need to change the password when logging in for the first time)
 - Click **Next**

![create user](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0008.png?width=90pc)

9. In the **Permissions options** section

 - Select **Add user to group**
 - Check the newly created **GroupLimit**
 - Click **Next**

![create user](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0009.png?width=90pc)

10. Scroll down and press **Create user**

![create user](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0010.png?width=90pc)

11. Notification of successful creation

 - After successfully creating, copy the link and open an incognito page or a new browser and paste it

![create user](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0011.png?width=90pc)

12. Log in the information you just created

![create user](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0012.png?width=90pc)

13. Successfully logged in to **User-S3**

![create user](/aws-fcj-workshop02/images/2.create-role-user/2.2create-usergroup/0013.png?width=90pc)