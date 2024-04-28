---
title : "Mã hóa ở trạng thái lưu trữ với AWS KMS"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---

# Mã hóa ở trạng thái lưu trữ với AWS KMS

#### Tổng quan

Dưới đây là sơ đồ mã hóa dữ liệu **S3 Object** bằng **Key Management Service** (KMS), ghi lại nhật ký bằng **Amazon CloudTrail** và truy xuất dữ liệu bằng **Amazon Athena. Bạn có thể tham khảo:

![introduce](/images/1.introduce/workshop02-introduce.png?width=90pc)


#### Nội dung
1. [Giới thiệu](1-introduce)
2. [Các bước chuẩn bị](2-create-role-user)
3. [Tạo Key Management Service](3-create-kms)
4. [Tạo Amazon S3](4-create-s3)
5. [Tạo AWS CloudTrail và Amazon Athena](5-create-cloudtrail)
6. [Kiểm thử và chia sẻ dữ liệu mã hóa trên S3](6-demo)
7. [Dọn dẹp tài nguyên](7-delete-recources)