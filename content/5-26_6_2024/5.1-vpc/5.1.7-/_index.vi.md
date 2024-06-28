---
title : "Internet Gateway"
date :  "`r Sys.Date()`" 
weight : 7
chapter : false
pre : " <b> 5.1.7. </b> "
---

Chỉ gán IP để đi ra thôi thì chưa đủ mà cần thực hiện tạo ra một cái Internet Router mà Internet Router ở trên aws là internet gateway. Internet Gatewway là 1 thành phần của amazon VPC được quản lý bởi aws và có thể mở rộng theo chiều ngang để đảm bảo cho các máy chủ trong VPC có thể ra ngoài Internet.

- Internet Gateway là một thành phần của Amazon VPC có khả năng mở rộng quy mô theo chiều ngang (scale out) cho phép các EC2 Instance trong VPC có thể truyền thông tin ra ngoài Internet.
- Internet Gateway được quản lý bởi AWS, chúng ta không cần cấu hình autoscale hoặc high availability.

![Untitled](/images/5/004.png)

**Problem:** Máy chủ ảo từ public server truy cập ra Internet

1. Tạo Internet Gateway 
2. Cấu hình bảng định tuyến (root entry 0.0.0.0/0) 
3. Gán bảng định tuyến vào public subnet 