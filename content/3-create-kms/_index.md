---
title : "Create Key Management Service"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

#### Create KMS

1. Access **AWS Management Console**

 - Find **KMS**
 - Select **Key Management Service**

![create kms](/aws-fcj-workshop02/images/3.create-kms/0001.png?width=90pc)

2. In the **KMS** interface

 - Select **Customer managed keys**
 - Select **Create**

![create kms](/aws-fcj-workshop02/images/3.create-kms/0002.png?width=90pc)


3. In the **Configure key** section
 - In this section we will create a symmetric key to encrypt data. You can refer to symmetric and asymmetric keys at [AWS Key Management Service](https://docs.aws.amazon.com/kms/latest/developerguide/key-types.html)
 - **Key type** select **Symmetric**
 - **Key usage** select **Encrypt and decrypt**
 - Click **Next**

![create kms](/aws-fcj-workshop02/images/3.create-kms/0003.png?width=90pc)

4. In the **Add lables** section

{{% notice note %}}
You can name it differently as you like!
{{% /notice %}}
 - **Alias** import **```kms-key-encrypt-decrypt```**

![create kms](/aws-fcj-workshop02/images/3.create-kms/0004.png?width=90pc)

5. Next step, scroll down and press **Next**

![create kms](/aws-fcj-workshop02/images/3.create-kms/0005.png?width=90pc)

6. In the **Define key administrative permissions** section

 - **Key administrator** find **kms**
 - Select **kms-key-role**
 - **Key deletion** check the line **Allow key administrators to delete this key**
 - Click **Next**

![create kms](/aws-fcj-workshop02/images/3.create-kms/0006.png?width=90pc)

7. In the **Define key usage permissions** section

 - **Key usage** find **kms**
 - Select **kms-key-role**
 - Click **Next**

![create kms](/aws-fcj-workshop02/images/3.create-kms/0007.png?width=90pc)

8. Next step we scroll down and press **Finish**

![create kms](/aws-fcj-workshop02/images/3.create-kms/0008.png?width=90pc)

9. Notification of successful creation

![create kms](/aws-fcj-workshop02/images/3.create-kms/0010.png?width=90pc)


{{% notice warning %}}
From section 10 onwards, additional information is for reference only. For the purpose of this lab, we do not need to use this feature!
{{% /notice %}}

Auto-key rotation in AWS KMS is a feature that helps you automatically change your encryption keys after a certain period of time (From 90 days and up to 2560 days). This helps increase the security of your data by minimizing the risk of your keys being exposed or compromised. Additional reference link [Rotating AWS KMS keys](https://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html)


10. You return to the KMS interface

 - Select the newly created Key

![create kms](/aws-fcj-workshop02/images/3.create-kms/0011.png?width=90pc)

11. Next

 - Select **Key rotation**
 - Select **Edit**

![create kms](/aws-fcj-workshop02/images/3.create-kms/0012.png?width=90pc)

12. In the **Edit automaton key rotation** section

 - Select **Ebale**
 - In the **Rotation period (in days)** section, you can customize how many days to automatically change your encryption key.

![create kms](/aws-fcj-workshop02/images/3.create-kms/0013.png?width=90pc)