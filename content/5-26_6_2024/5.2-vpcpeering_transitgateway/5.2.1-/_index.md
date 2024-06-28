---
title : "VPC Peering & Transit Gateway"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 5.2.1. </b> "
---

*Khi bạn có nhiều VPC thì cái việc kết nối chúng lại với nhau rất là quan trọng. Chúng ta sẽ tìm hiểu về VPC Peering cho phép kết nối hai VPC và transit gateway một giải phép cho phép chúng ta kết nối số lượng lớn VPC một cách dễ dàng và hiệu quả*

- VPC Peering là tính năng giúp kết nối hai hay nhiều VPC để các tài nguyên bên trong hai VPC đó có thể liên lạc trực tiếp với nhaukhông cần phải thông qua Internet, góp phần gia tăng tính bảo mật cho VPC.
- VPC Peering là kết nối cần tạo 1:1 giữa hai VPC thành viên, không hỗ trợ transitive routing.
- VPC Peering không hỗ trợ khi 2 VPC bị overlap IP address space.

**Problem:** Tôi muốn 2 máy chủ kết nối được với nhau nhưng bằng IP Private, để làm được → tạo Peering Connect

![](/images/5/011.png)

Các máy chủ trong 3 conneted 4 nhưng 3 không connected 2 vì 2 chưa cấu hình route table

{{% notice note %}}
Destination có thể là subnet/máy chủ
{{% /notice %}}