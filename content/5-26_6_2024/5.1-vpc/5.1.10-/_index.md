---
title : "Network Access Control List (NACL)"
date :  "`r Sys.Date()`" 
weight : 10
chapter : false
pre : " <b> 5.1.10. </b> "
---

- Network Access Control List (NACL) là một **tường lửa ảo không lưu giữ trạng thái *(stateless)*** giúp kiểm soát lượng truy cập đến và đi trong tài nguyên của AWS. (phải cấu hình cả chiều đến và chiều đi)

{{% notice note %}}
Web vào = port 80, trả về enduser thì trả về port khác 
{{% /notice %}}
- NACL được hạn chế theo giao thức, địa chỉ nguồn, cổng kết nối.
- NACL được áp dụng lên các **Amazon VPC Subnets. → khi thay đổi NACL nó sẽ ảnh hưởng đến nhiều máy chủ cùng một lúc**

![](/images/5/009.png)

- Mặc định NACL cho phép mọi truy cập đến và đi.

![](/images/5/010.png)
