---
title : "Giới thiệu"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---

#### Giới thiệu về AWS Key Management Service (KMS)

![kms](/aws-fcj-workshop02/images/1.introduce/0001.png?width=150)

KMS là viết tắt của **Key Management Service** đây là dịch vụ dùng để tạo và quản lý khóa. AWS đảm bảo key của bạn được quản lý hoàn toàn bảo mật. Tức là ngay cả các kỹ sư của AWS cũng không thể biết được key của bạn.

Ở KMS bạn có thể lựa chọn tạo **Symmetric key** (khóa đối xứng) hoặc **Asymmetric key** (khóa bất đối xứng) để làm CMK (Customer Master Key). Sau khi tạo khóa thì có thể thiết đặt key policy để control quyền access và sử dụng key. Bạn có thể sử dụng kết hợp với AWS CloudTrail để ghi lại nhật ký.

**Khóa đối xứng (Symmetric key):**
- Một khóa duy nhất: Khóa đối xứng chỉ sử dụng một khóa duy nhất để thực hiện cả hai tác vụ mã hóa và giải mã dữ liệu.
- Dễ dàng chia sẻ: Khóa này có thể được chia sẻ an toàn giữa những người dùng được tin cậy cần truy cập vào dữ liệu đã mã hóa.
- Nhanh hơn: Mã hóa và giải mã dữ liệu bằng khóa đối xứng thường nhanh hơn so với khóa bất đối xứng.
- Bảo mật yêu cầu cao: Việc giữ an toàn cho khóa đối xứng rất quan trọng vì bất kỳ ai có quyền truy cập vào khóa đều có thể giải mã dữ liệu.

**Khóa bất đối xứng (Asymmetric key):**
- Cặp khóa: Gồm bộ đôi khóa, một khóa công khai (public key) và một khóa riêng tư (private key).
- Công khai và riêng tư: Khóa công khai được phân phối cho những người cần mã hóa dữ liệu, trong khi khóa riêng tư - được giữ bí mật.
- Mã hóa và giải mã riêng biệt: Khóa công khai chỉ dùng để mã hóa dữ liệu, còn khóa riêng tư dùng để giải mã.
- Phân phối an toàn hơn: Khóa công khai có thể được phân phối rộng rãi mà không ảnh hưởng đến tính bảo mật của dữ liệu, chỉ cần giữ an toàn cho khóa riêng tư.
- Chậm hơn: Mã hóa và giải mã bằng khóa bất đối xứng thường chậm hơn so với khóa đối xứng.

Đường dẫn tham khảo thêm [AWS Key Management Service](https://docs.aws.amazon.com/kms/latest/developerguide/overview.html)

#### Giới thiệu về Amazon S3

![s3](/aws-fcj-workshop02/images/1.introduce/0002.png?width=10pc)

**Amazon Simple Storage Service** (Amazon S3) là một dịch vụ lưu trữ đối tượng cung cấp khả năng thay đổi quy mô, mức độ sẵn sàng của dữ liệu, độ bảo mật và hiệu suất hàng đầu trong ngành. Khách hàng thuộc mọi quy mô và ngành nghề có thể lưu trữ và bảo vệ dữ liệu thuộc mọi kích thước cho hầu hết tất cả các trường hợp sử dụng, chẳng hạn như hồ dữ liệu, ứng dụng hoạt động trên đám mây và ứng dụng di động. Với các lớp lưu trữ tiết kiệm chi phí và tính năng quản lý dễ sử dụng, bạn có thể tối ưu hóa chi phí, tổ chức dữ liệu và cấu hình các biện pháp kiểm soát quyền truy cập được tinh chỉnh để đáp ứng yêu cầu cụ thể về kinh doanh, tổ chức và tuân thủ.

S3 có khả năng mở rộng cao vì nó tự động tăng dung lượng lưu trữ của bạn theo yêu cầu và bạn chỉ trả tiền cho bộ nhớ bạn sử dụng.

Trường hợp sử dụng Amazon S3
- Xây dựng hồ dữ liệu
- Sao lưu và khôi phục dữ liệu quan trọng
- Lưu trữ dữ liệu với chi phí thấp nhất
- Chạy các ứng dụng hoạt động trên đám mây

Đường dẫn tham khảo thêm [Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)

#### Giới thiệu về AWS CloudTrail

![cloudtrail](/aws-fcj-workshop02/images/1.introduce/0003.png?width=10pc)

**AWS CloudTrail** là một dịch vụ cho phép thực hiện việc quản lý, kiểm tra vận hành và đánh giá rủi ro cho tài khoản AWS của bạn. Với CloudTrail, bạn có thể ghi nhật ký, giám sát liên tục và duy trì hoạt động của tài khoản có liên quan đến các hoạt động diễn ra trên cơ sở hạ tầng AWS của bạn.

Kiểm tra lịch sử của events/API call trong AWS account của bạn, events/API call đó có thể tạo bởi:
- Console
- SDK
- CLI
- AWS services

CloudTrail mặc định sẽ được Enable

Ví dụ: Bạn muốn kiểm tra xem 1 EC2 instance bị xóa bởi ai, thời gian nào...

Event được lưu lại tối đa 90 ngày trên CloudTrail

Để có thể lưu lại lâu hơn hãy log lại trên một S3 bucket và Athena để query data

Đường dẫn tham khảo thêm [AWS CloudTrail](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html)

#### Giới thiệu về Amazon Athena

![athena](/aws-fcj-workshop02/images/1.introduce/0004.png?width=10pc)

**Amazon Athena** là dịch vụ truy vấn dữ liệu tương tác trên Amazon S3. Nó cho phép bạn thực hiện truy vấn SQL trên dữ liệu lưu trữ trong các tệp tin được lưu trữ trong S3 mà không cần phải di chuyển hoặc sao chép dữ liệu vào cơ sở dữ liệu truyền thống. Athena giúp bạn dễ dàng truy vấn và phân tích dữ liệu lớn lưu trữ trong S3 mà không cần triển khai hoặc quản lý cơ sở dữ liệu.

Trường hợp sử dụng
- Thực hiện truy vấn trên S3, tại chỗ hoặc trên các đám mây khác
- Chuẩn bị dữ liệu cho các mô hình ML
- Xây dựng công cụ đối chiếu dữ liệu lớn phân tán
- Thực hiện phân tích đa đám mây

Đường dẫn tham khảo thêm [Amazon Athena](https://docs.aws.amazon.com/athena/latest/ug/what-is.html)