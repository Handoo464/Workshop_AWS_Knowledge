---
title : "Subnet"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 5.1.2. </b> "
---

Có không gian mạng 10.10.0.0/16 ta sẽ chia ra nhiều lớp mạng con, mỗi lớp mạng con nằm trong một AZ cụ thể. Và không gian mạng con của subnet đó phải là tập hợp con của không gian VPC.

- Amazon VPC cho phép tạo nhiều mạng ảo và chia các mạng ảo này thành các mạng con (**subnet**).
- VPC Subnet sẽ nằm trong 1 Availability Zone cụ thể.
- Khi tạo Subnet, chúng ta chỉ định CIDR cho mạng con đó và đây là một **tập hợp con của khối VPC CIDR.**

Trong thực tế: Tổng hợp không gian của 1 VPC là tổng hợp địa chỉ đánh số của quận 10, 1VPC=1 Quận → 1Subnet = 1Phường

Trong mỗi Subnet, AWS sẽ giữ 5 địa chỉ IP. Ví dụ nếu Subnet có CIDR là 10.10.1.0/24: (mặt định mất 5 địa chỉ IP)

- Địa chỉ network (10.10.1.0)
- Địa chỉ broadcast (10.10.1.255)
- Địa chỉ cho bộ định tuyến (10.10.1.1)
- Địa chỉ cho DNS (10.10.1.2)
- Địa chỉ cho tính năng tương lai (10.10.1.3)