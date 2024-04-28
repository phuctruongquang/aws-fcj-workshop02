---
title : "Create CloudTrail"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 5.1 </b> "
---

### Create CloudTrail

1. Access **AWS Management Console**

 - Find **CloudTrail**
 - Select **CloudTrail**

![create cloudtrail](/images/5.create-cloudtrail/5.1create-cloudtrail/0001.png?width=90pc)

2. In the **CloudTrail** interface

 - Select **Trails**
 - Select **Create trail**

![create cloudtrail](/images/5.create-cloudtrail/5.1create-cloudtrail/0002.png?width=90pc)

3. In the **Choose trail attributes** section
{{% notice note %}}
You can name it differently as you like!
{{% /notice %}}
 - **Trail name** enter **```kms-key-cloudtrail```**
 - **Storage location** select **Use existing S3 bucket**
 - Select **Browse**

![create cloudtrail](/images/5.create-cloudtrail/5.1create-cloudtrail/0003.png?width=90pc)


4. Next step

 - Select **kms-key-s3**
 - Press **Choose**

![create cloudtrai](/images/5.create-cloudtrail/5.1create-cloudtrail/0004.png?width=90pc)

5. In the **Prefix - optional** section
{{% notice note %}}
You can name it differently as you like!
{{% /notice %}}
 - Enter **```cloudtrail```**

![create cloudtrai](/images/5.create-cloudtrail/5.1create-cloudtrail/0005.png?width=90pc)

6. Scroll down to the section and click **Next**

![create cloudtrai](/images/5.create-cloudtrail/5.1create-cloudtrail/0006.png?width=90pc)

7. In the **Choose log events** section

 - **Event type** select **Management events**
 - Select **Data evntes**

![create cloudtrai](/images/5.create-cloudtrail/5.1create-cloudtrail/0007.png?width=90pc)

8. Next step we scroll down to the **Data events** section

 - Select the words **Switch to basic event selector** to switch modes

![create cloudtrai](/images/5.create-cloudtrail/5.1create-cloudtrail/0008.png?width=90pc)

9. Next step press **Continue**

![create cloudtrai](/images/5.create-cloudtrail/5.1create-cloudtrail/0009.png?width=90pc)

10. In the **Data event: S3** section

 - **Data event source** select **S3**
 - **S3 bucket** uncheck **Read** and **Write**
 - **Individual bucket selection** press **Browse**

![create cloudtrai](/images/5.create-cloudtrail/5.1create-cloudtrail/0010.png?width=90pc)


11. Next step

 - Select **kms-key-s3**
 - Press **Choose**

![create cloudtrai](/images/5.create-cloudtrail/5.1create-cloudtrail/0011.png?width=90pc)

12. Next step press **Next**

![create cloudtrai](/images/5.create-cloudtrail/5.1create-cloudtrail/0012.png?width=90pc)

13. Next step, scroll down and press **Create trail**

![create cloudtrai](/images/5.create-cloudtrail/5.1create-cloudtrail/0013.png?width=90pc)

14. Notification of successful creation

![create cloudtrai](/images/5.create-cloudtrail/5.1create-cloudtrail/0014.png?width=90pc)

15. Please access **S3** again

![create cloudtrai](/images/5.create-cloudtrail/5.1create-cloudtrail/0015.png?width=90pc)

16. Select **Buckets** select **kms-key-s3**

![create cloudtrai](/images/5.create-cloudtrail/5.1create-cloudtrail/0016.png?width=90pc)

17. We will see a folder created named **cloudtrail/**, this folder will contain all logs related to **kms-key-s3**

![create cloudtrai](/images/5.create-cloudtrail/5.1create-cloudtrail/0017.png?width=90pc)