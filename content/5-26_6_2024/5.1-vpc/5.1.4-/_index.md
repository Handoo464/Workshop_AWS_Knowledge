---
title : "Elastic Network Interface (ENI)"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 5.1.4. </b> "
---

- Elastic Network Interface (ENI) là một card mạng ảo, chúng ta có thể chuyển sang các EC2 Instance khác.
- Khi chuyển sang một máy chủ mới, một card mạng ảo sẽ vẫn duy trì:
    - Địa chỉ IP Private
    - Địa chỉ Elastic IP address
    - Địa chỉ MAC

{{% notice note %}}
Khi ở trong VPC, chúng ta bật máy chủ lên, tạo ra máy chủ ở trong VPC thì máy chủ của chúng ta sẽ được cấp địa chỉ IP nhưng địa chỉ IP đó không trực tiếp gán vào các tài nguyên máy chủ mà nó gán vào các card mạng ở đây là các Elastic Network Interface (ENI) - giống như là chúng ta có số nhà gán trước cái cổng nhà của chúng ta. Thì ở đây chúng ta hiểu là chúng ta có một cái card mạng ảo giống như máy chủ vật lý.
{{% /notice %}}


Các máy chủ EC2 của chúng ta ở trên AWS chúng ta gắn các card mạng Ảo tên là Elastic Network Interface vào (việc này được aws tiến hành gắn tự động) và địa chỉ IP của chúng ta khi mà được aws cấp thì cũng sẽ được gán vào cái card mạng ảo

chúng ta tạo ra cái máy chủ ảo thì chúng ta sẽ đi kèm với việc là tạo ra một cái Elastic Network Interface (ENI) ở trong VPC. Chúng ta có thể làm được khá là nhiều thứ với cái eni này ví dụ: tạo ra một cái Network Interface chúng ta có thể gán nó vào một cái máy chủ này Hoặc là tháo cái cái card mạng ảo đó ra và gán vào một máy chủ khác.
Khi chúng ta tháo ra gắn vào như vậy thì nó vẫn sẽ giữ được cái địa chỉ IP Private = như chúng ta mượn cái biển số nhà này gắn sang cái nhà khác. Nó không chỉ duy trì được cái địa chỉ IP Private mà nó còn bao gồm cả địa chỉ Elastic IP Address - nó là một cái địa chỉ public hoặc là cả địa chỉ MAC luôn là địa chỉ vật lý