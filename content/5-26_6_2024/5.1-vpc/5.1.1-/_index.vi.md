---
title : "Khái niệm"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 5.1.1. </b> "
---

*Đây là một dịch vụ cốt lõi cho phép chúng ta tạo ra một mạng riêng ảo được cô lập khỏi các mạng riêng khác chúng ta sẽ khám phá cách thiết lập và cấu hình VPC tạo subnet, bảng định tuyến root table, internet getway, Nat gateway và các dịch vụ tườngng lửa đi kèm*

Amazon Virtual Private Cloud (Amazon VPC) cho phép bạn khởi chạy các tài nguyên AWS vào một mạng ảo mà bạn đã xác định.

*Các tài nguyên của chúng ta, các máy chủ, các máy ảo, cơ sở dữ liệu, các thiết bị cân bằng tải của chúng ta sẽ đặt ở đâu ở trong cái lớp Mạng ảo này và cái lớp Mạng ảo này nó có cái mối liên hệ như thế nào với khái niệm Availability Zone mà chúng ta đã học ở tuần trước?*

![Untitled](/images/5/000.png)

Sau khi mà mình tạo xong account-> chọn region (Singapore) khoảng dưới 50 milisecond nếu ưu tiên độ trễ.

Dưới Region có các AZ, tối thiểu 1R-3AZ, để đơn giản hóa ở đây ta sử
dụng 2 AZ.
VPC bao quát nhiều AZ, ý nghĩa kiến trúc được vẽ trên hình là mình có thể chạy nhiều máy chủ ảo, các cơ sở dữ liệu của mình trên nhiều AZ khác nhau. (Trên hình) Vùng không gian mạng có địa chỉ 10.10.0.0/16, mục tiêu của VPC này của mình chứa các máy chủ mà mỗi máy chủ có thể chạy ở các AZ khác nhau. (AZ là các cụm trung tâm dữ liệu) Việc ta chạy ứng dụng ở 2 AZ giống như mô hình mình có DC(data center) và DA(disaster recovery data center) ở môi trường On-Premise.

- VPC nằm trong 1 Region, khi tạo VPC cần khai báo 1 lớp mạng **CIDR** IPv4 (bắt buộc) và IPv6 ( tùy chọn)
- Giới hạn của VPC hiện tại là **5 VPC** trên 1 AWS Region trên 1 AWS Account.
- Mục đích chính sử dụng VPC thường dùng để **phân tách** các môi trường.
(Trong một Software Development Cycle chia ra Production/Dev/Test/Staging)
- Lưu ý : Nếu muốn các tài nguyên tách biệt hẳn ( User không thể nhìn thấy một tài nguyên cụ
thể thì cần tách thành nhiều AWS account, nhiều VPC không giải quyết được vấn đề này - chỉ ở mức network )

{{% notice note %}}
User chỉ được vào môi trường VPC Dev Test thôi, tuy nhiên họ vẫn có thể thấy các máy chủ ảo ở môi trường Production, môi trường Staging. Nếu muốn User không nhìn thấy ta phải tạo nhiều AWS Account. - Đây là điều cần lưu ý khi nhận được yêu cầu phân tách môi trường trong môi trường thực tế.
{{% /notice %}}

![Untitled](/images/5/001.png)

Kiến trúc này minh họa chúng ta sử dụng VPC để phân tách các môi trường khác nhau