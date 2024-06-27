---
title : "Phương pháp tối ưu hóa dịch vụ sử dụng trên AWS"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : " <b> 2.1.6 </b> "
---

- Lựa chọn cấu hình tài nguyên tính toán và nơi lưu trữ dữ liệu phù hợp. (Cấu hình của tài nguyên máy Onpremise và Cloud là khác nhau)
- Tận dụng các phương thức thanh toán giảm giá như reserved instance, saving plan, spot. (Xài bao nhiêu tính bấy nhiêu - cơ chế on demand, spot-tài nguyên tạm (thuê với giá thấp nhưng  sẽ có thể bị lấy lại),  1 nhà cung cấp dịch vụ bao giờ cũng có tài nguyên sẵn sàng để khách hàng khi cần có thể tự động mở rộng quy mô hệ thống)

{{% notice note %}}
Xu hướng thiết kế máy chủ có thể bị lấy lại bất cứ lúc nào.
Ứng dụng có 10 máy chủ: 4 máy theo saving plane, 6 máy theo cơ chế spot.
{{% /notice %}}

- Xóa các tài nguyên không sử dụng, bật tắt tự động các tài nguyên không cần chạy 24/7.
- Tận dụng các dịch vụ serverless (Tạo cơ sở dữ liệu được quản lý hoàn toàn bằng AWSvà chúng ta không cần quản lý một máy chủ nào cả thì đó là những dịch vụ được gọi với thuật ngữ là serverless.)


{{% notice note %}}
Dữ liệu của mình nên đặt ở trên dịch vụ lưu trữ nào?
Đặt ở đó bao lâu? Bao nhiêu lâu thì đi xuống dịch vụ lưu trữ thứ cấp?
Mình sử dụng dịch vụ cloud native được quản lý bởi aws hay không? hay sử dụng dịch vụ OpenSource chay trên một máy chủ ảo của AWS
{{% /notice %}}

- Thiết kế kiến trúc tối ưu giải quyết yêu cầu đề ra.
- Cài đặt và sử dụng AWS Budget.
- Quản lý chi phí theo phòng ban / ứng dụng với cost allocation tag.
- Liên tục theo dõi và tối ưu hóa chi phí.