---
title : "Hạ tầng toàn cầu AWS (AWS Global Infrastructure)"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 2.1.4 </b> "
---

### 1. Trung tâm dữ liệu của AWS

- Một trung tâm dữ liệu có thể chứa hàng chục ngàn máy chủ.
- Tất cả trung tâm dữ liệu của AWS đều sử dụng các thiết bị được tối ưu hóa dành riêng cho hoạt động của AWS.

*Note: (Khác biệt gây hiểu lầm) 1 CPU 4 GB Ram của tất cả các nhà cung cấp đều như nhau. SAP có công cụ đo performance ( với cấu hình như vậy, đạt được hiệu năng là bao nhiêu)*

### 2. Availability Zone

![AZ](/images/2.content/001-AZ.png)

- Một Availability Zone (AZ) bao gồm một hoặc nhiều trung tâm dữ liệu (Data Center), các (AZ) được thiết kế để không xảy ra sự cố ảnh hưởng đồng thời 2 AZ một lúc (fault isolation)
- Giữa 2 AZ là đường kết nối riêng tốc độ cao.
- AWS khuyến nghị nên triển khai ứng dụng tối thiểu trên 2 AZ để đảm bảo tính sẵn sàng cao cho ứng dụng và dịch vụ của mình. (Tùy tính sẵn sàng mà lựa chọn)

*Note: Triển khai ứng dụng và dịch vụ trên 2 AZ tương đương thiết kế một môi trường chạy trên trung tâm dữ liệu Active Active. Trong môi trường truyền thống tốn chi phí, nhưng cloud thì có sẵn các trung tâm dữ liệu được kết nối với nhau bằng đường truyền tốc độ cao rồi, sẵn sàng triển khai ứng dụng và dịch vụ trên các trung tâm dữ liệu đó.*

### 3. Region

![Region](/images/2.content/002-Region.png)

- Một AWS Region bao gồm tối thiểu 3 Availability Zone. 
- Hiện tại có hơn 25 Region trên toàn cầu.
- Các Region được kết nối với nhau bởi mạng backbone của AWS.
- Mặc định dữ liệu và dịch vụ ở các Region độc lập với nhau. (Trừ một số dịch vụ ở quy mô Global). Dữ liệu chạy ở Region nào thì nằm ở bên trong region đó mà thôi. Region thường có vị trí nhất định như Region Singapore, Hồng Kông, … Và ở hiện tại  2024 các dịch vụ chúng ta triển khai thì sẽ nằm ở Region Singapore.
- **Lựa chọn Region:**
    - Phụ thuộc vào người dùng của chúng ta ở đâu (gần với người dùng của mình nhất - độ trễ thấp)
    - Các dịch vụ mới được phát triển thì cần truy cập ở xa hơn Region US như Generative AI
    - Chi phí: dựa trên văn hóa customer obsession của AWS, ta biết các Region càng lâu, có lượng khách hàng càng lớn thì càng rẻ (Region ở US rẻ hơn ở Singapore). Do đó nếu dịch vụ không có yêu cầu về độ trễ thấp thì có thể ưu tiên chọn Region US nhằm tiết kiệm chi phí.

### 4. Edge Locations ( Trung tâm dữ liệu thứ cấp): 

Edge Locations là mạng lưới trung tâm dữ liệu AWS được thiết kế để cung cấp dịch vụ với độ trễ thấp nhất có thể, chạy những dịch vụ mạng biên

- ***Amazon CloudFront:*** Đóng vai trò làm CDN - Content Delivery Network, giúp catching những cái dữ liệu người dùng thường xuyên truy cập
    
    *Note: Chúng ta có ứng dụng web và muốn catch lại những file tĩnh (ảnh, video) của người dùng để người dùng có thể lấy file ảnh tĩnh đó từ cdn thay vì phải gọi lại web server gốc của mình.*
    
    - CDN này được chạy tại edge location hay còn gọi là ***POP (Point of Presence)***
    - Tại Việt Nam có 2 edge location: HCM, Hà Nội
- ***Web Application Firewall (WAF)***: Dịch vụ ***Firewall Layer 7,*** đóng vai trò như lớp bảo vệ cho ứng dụng web của mình và có thể giảm bớt thiệt hại tấn công DDOS
- ***Route 53 (DNS Service) :***
    - là dịch vụ DNS có thể tạo domain cho ứng dụng web của mình
    - có thể request certificate (gắn certificate) vào cái domain của mình