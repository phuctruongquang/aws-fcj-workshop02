---
title : "Retrieve data with Athena"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 5.4 </b> "
---

### Retrieve data with Athena

1. Access **AWS Management Console**

 - Find **Athena**
 - Select **Athena**

![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0001.png?width=90pc)

2. In the **Athena** interface

 - Select **Query editor**
 - Select **Edit settings**

![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0002.png?width=90pc)

3. In the **Manage settings** section

 - Select **Browse S3**

![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0003.png?width=90pc)

4. Next step

 - Select **kms-key-s3**
 - Press **Choose**

![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0004.png?width=90pc)


5. Next step press **Save**

![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0005.png?width=90pc)

6. We return to the **Query editor**

 - Select **Editor**
 - Select the 3 dots in the **cloudtrail-log-kms-key-s3-cloudtrail** table
 - Select **Preview table**

![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0006.png?width=90pc)

7. Scroll down and you will see the logs appear

![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0007.png?width=90pc)

8. Try retrieving **eventname** of log **kms-key-s3**

 - Enter into the table the retrieval statement **```SELECT eventname FROM "default". "cloudtrail_logs_kms_key_s3_cloudtrail" limit 100;```**
 - Then press **Run** to run the command

![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0008.png?width=90pc)

9. Scroll down and you will see that **eventname** has been retrieved successfully

![test athena](/aws-fcj-workshop02/images/5.create-cloudtrail/5.4test-athena/0009.png?width=90pc)

{{% notice note %}}
The above is an example to retrieve data. You can retrieve what you need yourself in Query results.
{{% /notice %}}