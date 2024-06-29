---
title : "Route Table"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 6.1.3 </b> "
---

- Route table (Bảng định tuyến), tập hợp các Route, để xác định đường đi cho mạng.
- Khi tạo VPC, AWS sẽ tạo một Default Route table, Default Route table không thể bị xóa và chỉ chứa 1 Route duy nhất là Route cho phép tất cả các Subnet trong VPC liền lạc với nhau.
- Route table sẽ được gán vào Subnet.

![Untitled](/images/5/002.png)

10.10.0.0/16 là default root entry và thông tin này sẽ không thể bị xóa. All các máy chủ của chúng ta nằm trong VPC này, bất kể nằm ở subnet nào cũng có thể kết nối được với nhau

Default Route Table sẽ được gán vào các subnet mà chúng ta tạo

- Để có thể tạo ra public subnet tức là subnet bên trong máy chủ có thể ra đc ngoài Internet. Chúng ta tạo Custom Route table ( bảng định tuyến tùy chỉnh), tuy nhiên sẽ không thể xóa default route. (VPC CIDR - Local)