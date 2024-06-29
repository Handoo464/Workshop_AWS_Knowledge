---
title : "Security Group"
date :  "`r Sys.Date()`" 
weight : 9
chapter : false
pre : " <b> 6.1.9. </b> "
---

![](/images/5/006.png)

- **Problem:** Máy chủ ở PubSub kết nối tới PriSub qua một port nhất định → cần tính năng tường lửa xây dựng sẵn trong VPC
- Security Group (SG) là một **tường lửa ảo có lưu giữ trạng thái** ***(stateful)*** giúp kiểm soát lượng truy cập đến và đi trong tài nguyên của AWS.
- Security Group rule được hạn chế theo giao thức, địa chỉ nguồn, cổng kết nối, hoặc một Security Group khác.
- Security Group rule chỉ **cho phép rule allow.** (không chạy role deny)
- Security Group được áp dụng lên các **Elastic Network Interface - card mạng ảo**. (SG không áp dụng lên máy chủ ảo mà áp dụng lên từng ENI)

{{% notice note %}}
Stateful - trong một session nếu ta đi vào được thì cũng đi ra được
{{% /notice %}}

![](/images/5/007.png)

- Mặc định Security Group chặn mọi truy cập đến và cho phép mọi truy cập đi.

![](/images/5/008.png)

Các ENI được áp dụng SG(dưới) sẽ truy cập được vào database server 

{{% notice note %}}
Tại sao không sử dụng một địa chỉ IP nhất định mà dùng tên của SG. Trong 1 số TH mình scale/web server của mình nằm ở nhiều AZ khác nhau thay vì mình vào đây cấu hình lại thì mình chỉ cần cấu hình 1 lần
{{% /notice %}}