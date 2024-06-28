---
title : "Security Group"
date :  "`r Sys.Date()`" 
weight : 8
chapter : false
pre : " <b> 5.1.8. </b> "
---

NAT Gateway cho phép các EC2 instance trong subnet truy cập tới internet hoặc các dịch vụ AWS khác. Chỉ chấp nhận kết nối chiều ra và không chấp nhận kết nối chiều vào.

![](/images/5/005.png)

**Problem:** Máy chủ ảo từ private server truy cập ra Internet (NAT Gateway nằm trong Public Subnet)

- Cấu hình bảng định tuyến: cấu hình thêm một custom route table (1 bảng vào PubSub; 1 bảng vào PriSub
- Đường đi: máy chủ đi qua NAT gateway trước → Internet gateway → Internet

Note: (muốn biết giá vàng - trong một phiên làm việc dữ liệu bên ngoài có thể đi vào được (nhưng user không thể kết nối trực tiếp vào được)