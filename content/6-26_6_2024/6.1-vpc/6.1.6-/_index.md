---
title : "VPC Endpoint"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : " <b> 6.1.6. </b> "
---

VPC Endpoint cho phép chúng ta kết nối các tài nguyên nằm trong VPC tới các dịch vụ AWS nằm bên ngoài VPC được hỗ trợ ( AWS PrivateLink - đi qua mạng private của AWS) mà không cần thông qua kết nối internet.

Có 2 kiểu VPC Endpoint:

- **Interface Endpoint** : Sử dụng một Elastic Network Interface trong VPC cũng với một địa chỉ IP Private để kết nối tới 1 dịch vụ hỗ trợ
- **Gateway Endpoint** : Sử dụng một route table để định tuyến tới endpoint của dịch vụ hỗ trợ (S3 và Dynamo DB)

Note: các module học về hệ thống lưu trữ, cơ sở dữ liệu thì sẽ hiểu hơn gateway endpoint này

![](/images/5/003.png)

S3 tạo một cái vùng không gian lưu trữ → mặc định nó có phạm vi nằm ngoài VPC và nó độc lập có nghĩa là không cần tạo VPC vẫn có thể tạo S3 rồi kết nối với nó bằng địa chỉ IP public thông qua Internet. Việc kết nối như vậy nó sẽ chậm, và phát sinh chi phí khi mà chúng ta thực hiện đi ra ngoài Internet. Để tiết kiệm ta cần đường đi nội bộ (vì VPC và S3 đều do AWS cung cấp) tạo ra tính năng gateway endpoint cho S3 thì với tính năng này, việc kết nối giữa máy chủ ảo và dịch vụ lưu trữ S3 này ta đi qua mạng riêng và kết nối thông qua địa chỉ IP Private.
