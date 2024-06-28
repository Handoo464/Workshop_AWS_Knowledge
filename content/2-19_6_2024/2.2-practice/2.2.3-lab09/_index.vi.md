---
title : "LAB 09"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 2.2.3 </b> "
---

Link LAB: [https://000009.awsstudygroup.com/vi/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbk9VVnJWQl9pWVlXSDRyRHVIdEdGcDdEaG9HUXxBQ3Jtc0trQThsWjM4ZHk3MlhaV1d4WXZWeHpjOFh4WWE0dW9jV0Vybi1od1RVS3l2MVhXaW85eGpsbXJrSlhzTmVHQ2NJSVdmdU0wUzRqMU5xd2lDRGZqZ0J3MVRhaExvcTNfTFRTYnJfb3l1bjVndVNtNXRZUQ&q=https%3A%2F%2F000009.awsstudygroup.com%2Fvi%2F&v=4FDcK0_kbfY)

## LAB 09 - 01: Các gói hỗ trợ của AWS

AWS Support được chia thành 4 gói hỗ trợ với mục tiêu và quyền lợi khác nhau để phù hợp với từng mục đích và nhu cầu của người dùng.

### 1.1 Gói Basic

Gói Basic cung cấp hỗ trợ cơ bản cho các vấn đề liên quan đến tài khoản và thanh toán cùng với các yêu cầu tăng thêm hạn mức cho tài khoản.

Tất cả khách hàng của AWS được cung cấp truy cập 24/7 vào các tính năng sau của gói hỗ trợ Basic:

- Phòng chat trực tiếp 1-1 cho các câu hỏi về tài khoản và thanh toán.
- Diễn đàn hỗ trợ.
- Kiểm tra Dịch vụ.
- Tài liệu, tài liệu kĩ thuật và các hướng dẫn best practice.

### 1.2 Gói Developer

Đối với gói Developer, các tính năng được hỗ trợ sẽ được mở rộng hơn với:

- Các chỉ dẫn thực hiện best practice.
- **Hỗ trợ xây dựng kiến trúc khối:** Chỉ dẫn cách sử dụng và kết hợp các sản phẩm, tính năng và dịch vụ của AWS.
- **Hỗ trợ không giới hạn các yêu cầu hỗ trợ** được tạo bởi tài khoản gốc (*root user*).

### 1.3 Gói Business

Khi nâng lên gói hỗ trợ Business, bạn sẽ có thêm các hỗ trợ sau:

- **Chỉ dẫn theo Use-case cụ thể:** Đưa ra lời khuyên về lựa chọn các sản phẩm, tính năng và dịch vụ của AWS hỗ trợ tốt nhất cho nhu cầu của bạn.
- **AWS Trusted Advisor:** Chức năng tự động khảo sát môi trường sử dụng của khách hàng và xác định cơ hội tiết kiệm chi phí, giảm thiểu rủi ro an ninh và tăng cường độ tin cậy và hiệu suất của hệ thống.
- **Hỗ trợ sử dụng AWS Support API:** Tương tác với Support Center và Trusted Advisor qua API để tự động quản lý yêu cầu hỗ trợ và vận hành AWS Trusted Advisor.
- **Hỗ trợ về phần mềm bên thứ ba:** Hỗ trợ hệ điều hành và cấu hình máy ảo EC2, cùng với hiệu suất của các ứng dụng phổ biến trên nền tảng AWS.
- **Hỗ trợ không giới hạn các yêu cầu hỗ trợ** được tạo bởi tất cả các IAM User.

### 1.4 Gói Enterprise

Thêm vào đó, với khách hàng sử dụng gói Enterprise sẽ có thêm các đặc quyền về tính năng như sau:

- **Chỉ dẫn về kiến trúc phần mềm:** Lời khuyên về cách phối hợp dịch vụ AWS để giải quyết vấn đề về ứng dụng hoặc tải trọng công việc.
- **Quản lý sự kiện hạ tầng:** Phân tích chuyên sâu về use-case của bạn và cung cấp hướng dẫn về quy mô và kiến trúc phù hợp cho sự kiện cụ thể.
- **Technical Account Manager:** Sự hỗ trợ thường trực từ Technical Account Manager (TAM) giải quyết các vấn đề liên quan đến tình huống và ứng dụng của bạn.
- **Ưu tiên và chăm sóc đặc biệt cho các yêu cầu hỗ trợ**
- Hỗ trợ **đánh giá Quản lý Doanh nghiệp**.

## LAB 09 - 02: Truy cập AWS Support

I. Các loại yêu cầu hỗ trợ:

- **Hỗ trợ Tài khoản và Thanh toán** (*Account and Billing Support*): Đây là loại được hỗ trợ cho tất cả người dùng AWS; vì vậy bạn có thể nhận được hỗ trợ cho các câu hỏi liên quan đến nội dung này.
- **Hỗ trợ nâng hạn mức dịch vụ** (*Service limit increase*): Các yêu cầu này được hỗ trợ cho toàn bộ người dùng AWS. Để biết thêm chi tiết về các hạn mức mặc định
- **Hỗ trợ Kỹ thuật** (*Technical support*): Các yêu cầu kết nối đến Technical Support sẽ được hỗ trợ về các vấn đề liên quan đến dịch vụ hoặc ứng dụng bên thứ ba. Nếu bạn đang sử dụng gói Developer, bạn có thể trao đổi thông qua email hoặc qua website của Support Center. Nếu bạn sử dụng gói Business hoặc Enterprise, bạn có thể trao đổi thông qua điện thoại hoặc gửi tin nhắn trực tuyến.

*Note: Sử dụng gói hỗ trợ Basic sẽ không thể tạo yêu cầu hỗ trợ kỹ thuật.*

## LAB 09 - 03: Thay đổi gói hỗ trợ

Link LAB: [https://000009.awsstudygroup.com/vi/2-access-support/2.2-change-support-package/](https://000009.awsstudygroup.com/vi/2-access-support/2.2-change-support-package/)

## LAB 09 - 04: Quản lý yêu cầu hỗ trợ

|  | Nhà phát triển

Khuyên dùng nếu bạn đang thử nghiệm hoặc kiểm thử trên AWS | Kinh doanh

Bậc tối thiểu được khuyên dùng nếu bạn có khối lượng công việc sản xuất trên AWS | Cầu nối dành cho doanh nghiệp

Được khuyên dùng nếu bạn có khối lượng công việc sản xuất và/hoặc kinh doanh tối quan trọng trên AWS | Doanh nghiệp

Được khuyên dùng nếu bạn có khối lượng công việc kinh doanh và/hoặc tối quan trọng trên AWS |
| --- | --- | --- | --- | --- |
| Mức độ nghiêm trọng của trường hợp / Thời gian phản hồi* | Hướng dẫn chung: < 24 giờ**
Hệ thống bị suy yếu: < 12 giờ** | Hướng dẫn chung: < 24 giờ

Hệ thống bị suy yếu: < 12 giờ

Hệ thống sản xuất bị suy yếu: < 4 giờ

Hệ thống sản xuất ngừng hoạt động: < 1 giờ | Hướng dẫn chung: < 24 giờ

Hệ thống bị suy yếu: < 12 giờ

Hệ thống sản xuất bị suy yếu: < 4 giờ

Hệ thống sản xuất ngừng hoạt động: < 1 giờ

Hệ thống trọng yếu của doanh nghiệp ngừng hoạt động: < 30 phút | Hướng dẫn chung: < 24 giờ

Hệ thống bị suy yếu: < 12 giờ

Hệ thống sản xuất bị suy yếu: < 4 giờ

Hệ thống sản xuất ngừng hoạt động: < 1 giờ

Hệ thống kinh doanh/tối quan trọng ngừng hoạt động: < 15 phút |
| Hướng dẫn về kiến trúc | Thông tin chung | Cụ thể theo trường hợp sử dụng của bạn | Xem xét Tư vấn hàng năm và hướng dẫn căn cứ theo ứng dụng của bạn | Xem xét tư vấn và hướng dẫn căn cứ theo ứng dụng của bạn |
