---
title : "Các công cụ dùng để quản lý AWS Services"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 2.1.5 </b> "
---

**1. AWS Management Console - Root login**

Chúng ta có thể login bằng tài khoản root hoặc bằng tài khoản IAM User ( tài khoản
con giúp quản lý truy suất các tài nguyên của AWS)

**2. AWS Management Console - IAM user login**

Khi login bằng IAM User chúng ta cần cung cấp thêm thông tin Account ID (chuỗi 12 chữ số) để xác định Account AWS.

**3. AWS Management Console - Service Search**
- Sau khi login vào giao diện AWS Management Console, chúng ta có thể tìm
kiếm các dịch vụ (service) của AWS.
- Mỗi một dịch vụ sẽ có trang management riêng cho phép chúng ta sử dụng các tính năng (feature) của dịch vụ đó.

**4. AWS Management Console - Support Center**

![AWS Management Console](/images/2.content/003-AWSManagementConsole.png)

Có thể vào  Support Center để tạo các support case để yêu cầu hỗ trợ từ đội ngũ của AWS.

**5. AWS Command Line Interface (CLI)**
- Giao diện dòng lệnh AWS (AWS CLI) là một công cụ mã nguồn mở cho phép bạn tương tác với các dịch vụ AWS bằng cách sử dụng các lệnh (command).
- AWS CLI cho phép bạn chạy các lệnh triển khai chức năng tương đương với chức năng được cung cấp bởi AWS Management Console dựa trên trình duyệt.

![AWS CLI](/images/2.content/004-AWSCLI.png)

- AWS CLI cho phép triển khai các chức năng gần tương đương được cung cấp bởi AWS Management Console

**6. AWS SDK (Software Development Kit)**
- AWS SDK đơn giản hóa việc sử dụng AWS services cho ứng dụng bằng cách cung cấp một bộ thư viện nhất quán và quen thuộc cho đội ngũ phát triển ứng dụng.
    
    *Note thực tế:  Sử dụng AWS SDK ta sẽ có bộ thư viện hỗ trợ nhiều ngôn ngữ khác nhau. Giả sử muốn sử dụng dữ liệu, lưu trữ dữ liệu vào những cơ sở dữ liệu nằm ở trên cloud được AWS cung cấp dưới dạng DBS of Service thì chúng ta sẽ sử dụng AWS SDK này. Cách thức access thay vì User thì là Apps thông qua AWS Tools and SDKs và cuối cùng gửi các API request tới AWS ServicesEndpoint.*  
    
- AWS SDK cung cấp hỗ trợ cho những công việc quản lý vòng đời của API tới AWS services như quản lý thông tin xác thực ( manage credentials), thử lại (retry) , sắp xếp dữ liệu (data marshalling - chuẩn bị dữ liệu), tuần tự hóa (serialization chuyển object sang bytes stream) và giải mã hóa (deserialization chuyển bytes stream về lại object)
