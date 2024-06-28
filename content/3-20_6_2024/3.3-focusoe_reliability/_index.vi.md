---
title : "Tập trung nghiên cứu vào 2 phần Operational Execllence & Reliability"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 3.3. </b> "
---
Quan trọng vì it’s provide you with architect best practices and guidance to improve the resilence of your workloads

### A. Operational Excellence

- Mục tiêu: không chỉ efficient, reliable mà also improve over time
- Một vài nguyên tắc thiết kế cho **OE pillar**
    1. Perform Operations as Code:
        1. Think of your workload as a piece of software (Hãy nghĩ về khối lượng công việc của bạn như một phần mềm)
        2. By turning operations into scripts & automating them (Bằng cách biến các hoạt động thành script và tự động hóa chúng)
        - We can reduce mistakes that come with human error (Chúng ta có thể giảm sai sót do lỗi con người)
        - Create predictable responses when certain events occur (Tạo ra các predictable responses khi xảy ra các sự kiện nhất định)
    2. Make Frequent, Small, Reversible Changes:
        1. Make changes in small steps that can be undone (Thực hiện các thay đổi theo từng bước nhỏ có thể hoàn tác)
        2. This helps you deal with issues quickly (Điều này giúp bạn xử lý các vấn đề một cách nhanh chóng)
        - Without major effects on your customers (Mà không gây ảnh hưởng lớn đến khách hàng của bạn)
    3. Refine Operations Procedures Frequently: (Tinh chỉnh các quy trình vận hành thường xuyên:)
    • All about "Constant Improvement" ( Cải tiến liên tục)
    • As your workloads evolves, procedures should also evolve (Khi khối lượng công việc của bạn thay đổi, các quy trình cũng nên thay đổi)
    • Be on the lookout for ways to refine & streamline operations (Luôn tìm kiếm các cách để tinh chỉnh và hợp lý hóa hoạt động)
    4. Anticipate Failure:  (Dự đoán sự cố)
        1. Identify possible failures before they occur
        2. By regularly testing these scenarios
            - Understand their impact better (Hiểu rõ hơn về tác động của chúng)
            - Ensure response procedures are up to the task (Đảm bảo các quy trình ứng phó phù hợp với nhiệm vụ)
    5. Learn from Operational Failures:
        1. Every operational event / failure is a learning opportunity (Mỗi sự cố vận hành là một cơ hội học hỏi)
        2. Use these lessons to build stronger, more resilient systems (Sử dụng những bài học này để xây dựng các hệ thống mạnh mẽ và bền bỉ hơn)
        3. Sharing this knowledge can lead to significant improvements (Chia sẻ kiến thức này có thể dẫn đến những cải tiến đáng kể)
        
- Một vài nguyên tắc thiết kế cho **Reliability**
    ### B. Reliability
    
    1. Automatically Recover from Failure: (Tự động phục hồi từ sự cố:)
        1. Monitor important metrics closely (Giám sát chặt chẽ các chỉ số quan trọng)
        2. Use automation to fix issues as soon as they occur (Sử dụng tự động hóa để khắc phục sự cố ngay khi chúng xảy ra)
        3. Your system bounces back when something goes wrong (Hệ thống của bạn sẽ phục hồi khi có sự cố xảy ra)
    2. Test Recovery Procedures: (Kiểm tra các quy trình phục hồi:) 
        1. Actively test how our systems handle failures (Chủ động kiểm tra cách hệ thống của chúng tôi xử lý các sự cố)
        2. Use automation to simulate different failure scenarios (Sử dụng tự động hóa để mô phỏng các kịch bản sự cố khác nhau)
    3. Horizontally Scale to Increase Aggregate Workload Availability: (Mở rộng theo chiều ngang để tăng khả năng chịu tải tổng thể:)
        1. The goal is to spread workload across multiple small resources (Mục tiêu là phân bổ công việc trên nhiều tài nguyên nhỏ)
        2. If one part fails, it won't shut down everything (Nếu một phần gặp sự cố, nó sẽ không làm tê liệt toàn bộ hệ thống)
    4. Stop Guessing Capacity: (Ngừng đoán dung lượng:)
        1. Monitor how much our systems are being used (Giám sát mức độ sử dụng của hệ thống)
        2. Adjust our resources accordingly (Điều chỉnh tài nguyên phù hợp)
        3. The goal is to have the exact resources we need (Mục tiêu là có đúng tài nguyên cần thiết)
            - Automation is the key to achieving this (Tự động hóa là chìa khóa để đạt được điều này)
    5. Manage Change Through Automation: (Quản lý thay đổi thông qua tự động hóa:)
        1. Automate changes to our infrastructure (Tự động hóa các thay đổi đối với cơ sở hạ tầng của chúng tôi)
        2. This method ensures consistent, easily trackable and smooth running results (Phương pháp này đảm bảo kết quả nhất quán, dễ dàng theo dõi và vận hành trơn tru)
    
    Để đưa ra một ví dụ về cách sử dụng các trụ cột Độ Tin Cậy và Xuất Sắc Vận Hành, hãy lấy Công ty A làm ví dụ. Công ty A là một cửa hàng trực tuyến bán đồng hồ. Họ đã ra mắt một bộ sưu tập đồng hồ mới mà hàng nghìn người trên khắp thế giới muốn mua, dẫn đến một đợt bùng nổ lưu lượng truy cập web khổng lồ. Đây là cách họ xử lý tình huống:
    
    Bất cứ khi nào những chiếc đồng hồ mới được thêm vào danh mục trực tuyến, một hệ thống tự động sẽ kích hoạt tất cả các hệ thống cần thiết để cập nhật. Họ cũng có các công cụ giám sát theo thời gian thực để theo dõi và phản hồi bất kỳ sự cố nào, vì vậy nếu có lỗi trong hệ thống, họ sẽ được thông báo ngay lập tức. Nhờ vào trụ cột Xuất Sắc Vận Hành, họ đã có thể điều hướng đợt bùng nổ này mà không gặp bất kỳ vấn đề gì.
    
    Nhưng còn những đợt bùng nổ lưu lượng truy cập lớn hơn, ví dụ như trong mùa lễ khi mọi người mua đồng hồ cho bạn bè và gia đình thì sao? Đó là lúc trụ cột Độ Tin Cậy phát huy tác dụng. Công ty A đã thiết kế các hệ thống của họ để xử lý tải tăng một cách linh hoạt bằng cách tự động mở rộng cơ sở hạ tầng đám mây của họ. Vì vậy, nếu một máy chủ gặp sự cố, một máy chủ dự phòng sẽ ngay lập tức hoạt động, giữ cho cửa hàng trực tuyến luôn khả dụng.
    
    Bằng cách áp dụng các trụ cột Xuất Sắc Vận Hành và Độ Tin Cậy từ Khung Kiến Trúc Tốt, Công ty A đã có thể xây dựng một hệ thống hiệu quả và đáng tin cậy, có khả năng cung cấp trải nghiệm mua sắm liền mạch cho khách hàng của họ.