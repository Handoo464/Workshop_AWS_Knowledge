---
title : "Transite Gateway"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 6.2.2. </b> "
---

- **Problem:** Khắc phục vấn đề kết nối 1:1 của peering connection khi cần kết nối 1 → nhiều máy
- Transit Gateway (như 1 hub center) được dùng để kết nối các VPC và mạng on-premises thông qua một hub trung tâm. Điều này đơn giản hoá mạng và kết thúc các mối quan hệ định tuyến phức tạp.
- **Transit Gateway Attachment** là một công cụ để gán các subnet của từng VPC cần kết nối với nhau vào một TGW đã được khởi tạo. Transit Gateway Attachment hoạt động ở quy mô Availability Zone (AZ-level).
- Trong VPC, khi một subnet ở một AZ có Transit Gateway Attachment với một TGW, các subnet khác trong cùng AZ đều có thể kết nối tới TGW đó. ***(Mỗi AZ gán 1 Transit Gateway Attachment cho dù AZ có nhiều subnet)***

![](/images/5/012.png)

1. Transit Gateway
2. Transit Gateway Attachment 
3. Cấu hình Route table