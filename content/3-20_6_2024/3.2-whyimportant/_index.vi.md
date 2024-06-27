---
title : "Tại sao AWS WELL ARCHITECTED FRAMEWORK lại quan trọng?"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 3.2. </b> "
---
Bạn có thể tự hỏi tại sao việc hiểu điều này lại quan trọng; nếu không có kế hoạch và kiến trúc đúng đắn, các công ty có thể dễ dàng bị bất ngờ bởi những thay đổi đột ngột đối với cơ sở hạ tầng của họ. Ví dụ, khi có một sự tăng đột biến về lưu lượng truy cập, kết quả có thể là hệ thống bị sập, khách hàng không hài lòng và vô số giờ dành cho việc kiểm soát thiệt hại. Trong thời đại kỹ thuật số của chúng ta, bất kỳ thời gian ngừng hoạt động hay gián đoạn nào không chỉ có thể khiến các công ty mất rất nhiều tiền mà còn gây tổn hại đến danh tiếng và mất niềm tin của khách hàng. Đó là lý do tại sao việc xây dựng các kiến trúc bền vững không còn là một lựa chọn mà là một điều bắt buộc. Hiểu và áp dụng Khung Kiến trúc Tốt của AWS có thể giúp bạn tránh các cạm bẫy thông thường, giảm thiểu rủi ro và đảm bảo rằng các ứng dụng của bạn được kiến trúc tốt.

Cũng cần lưu ý rằng framework này là kết quả của nhiều năm kinh nghiệm thực tế từ những người thiết kế và quản lý các khối lượng công việc trong đám mây. Khi bạn hiểu và sử dụng AWS Well Architected Framework, bạn đang khai thác kiến thức tổng hợp của vô số kiến trúc sư đám mây đã đối mặt với các vấn đề tương tự và đã tìm ra cách để giảm thiểu chúng một cách hiệu quả. Bằng cách hiểu và triển khai khung này, bạn không chỉ tận dụng được chuyên môn của AWS mà còn đảm bảo rằng hệ thống của bạn có thể xử lý các kịch bản thực tế. Nó giống như có một bản đồ chỉ đường cho kiến trúc trong đám mây, giúp bạn đạt được thành công.

Qua nhiều năm kinh nghiệm tư vấn các kiến trcs cho khách hàng AWS kết luận khi khách hàng lên cloud họ cần tập trung vào 6 phần chính

- **Operational excellence**: RUNNING AND MONITORING SYSTEMS TO DELIVER BUSINESS VALUE AND CONTINUITY - đảm bảo kiến trúc của họ được backup được monitoring để mang lại giá trị kinh doanh và tính liên tục.

{{% notice note %}}
Note: Khi làm việc với KH trước khi họ lên profesion?? môi trường unity, môi trường dev thì phải đảm bảo ứng dụng của họ đã có giải pháp backup, monitoring, logging, có được bagging??? Xong phần này thì có thể yên tâm về phần operation chuyển từ unity?? lên production??
{{% /notice %}}

- **Security:**
    - Focuses on protecting data, systems & assets (hệ thống và tài sản)
    - Confidentiality of data (bảo mật dữ liệu)
    - Identity & Access management (quản lí danh tính và truy cập)
    - Controls to detect security threats (Kiểm soát để phát hiện các mối đe dọa an ninh)
- **Reliability:** FOCUSES ON THE ABILITY OF A SYSTEM TO RECOVER FROM DISRUPTIONS, DYNAMICALLY MEET DEMAND & MITIGATE DISRUPTIONS - TẬP TRUNG VÀO KHẢ NĂNG CỦA HỆ THỐNG TRONG VIỆC PHỤC HỒI SAU SỰ GIÁN ĐOẠN, ĐÁP ỨNG NHU CẦU MỘT CÁCH LINH HOẠT VÀ GIẢM THIỂU SỰ GIÁN ĐOẠN.
- **Sustianability**: Minimizing environmental impact of running cloud workloads

{{% notice note %}}
Note: KH muốn dịch vụ của chúng tôi chạy ổn định khi 1 server chết hệ thống vẫn hoạt động. Mỗi Region có nhiều AZ, vậy thì cần đảm bảo về mặt liability, đảm bảo có chế độ auto scaling (5:00??) khi library database chết thì hệ thống tự động root sang stand by database??
{{% /notice %}}

- **Performance Efficiency:**
    - Using computing resources efficiently (Sử dụng tài nguyên máy tính một cách hiệu quả)
    - Maintaining the efficiency as changes occur (Duy trì hiệu quả khi có thay đổi xảy ra)

{{% notice note %}}
Note: có hơn 15 databse engine cho khách hàng. Database cần có độ trễ thấp thì sử dụng ??. Hoặc là database có khả năng lưu trữ các dạng document, file JSON thì có thể sử dụng document DB hoặc ?? (6:00)
{{% /notice %}}
- **Cost optimization: (Tối ưu hóa chi phí)**
    - Avoiding unnecessary costs ( Tránh các chi phí không cần thiết)
    - Using the right type of resources (Sử dụng đúng loại tài nguyên)
    - Making cost-effective decisions (Đưa ra các quyết định hiệu quả về chi phí)

