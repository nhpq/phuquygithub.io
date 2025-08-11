+++
title = "Thực nghiệm"
date = 2021
weight = 7
chapter = false
pre = "<b>7. </b>"
+++

1.	Quay lại phần **Instance**, bạn sẽ thấy một **EC2 Instance** vừa được tạo ra bởi **ASG**  
![SG](/images/6-ASG/16.png)

2.	Bấm vào và chạy thử như ở bước **3.15**, sẽ cho ra kết quả tương tự như hình **3.16**  
![SG](/images/6-ASG/17.png)  
![SG](/images/7-TN/12.png)

3.	Quay về trang **Auto Scaling Group**, chọn **workshop-ASG**  
![SG](/images/7-TN/1.png)

4.	Tại trang **workshop-ASG**, chọn **Edit**  
![SG](/images/7-TN/2.png)

5.	Khi hiện ra bảng như hình, phần **Min** chỉnh từ `1` thành `2`, phần **Desired capacity** chuyển từ `1` thành `2`. Chọn **Update**  
![SG](/images/7-TN/3.png)  
![SG](/images/7-TN/4.png)

6.	Quay về phần **Instance**, bạn sẽ thấy đã có thêm một máy chủ nữa được tạo ra. Vì ta vừa chỉnh số lượng lên `2`  
![SG](/images/7-TN/5.png)

7.	Chuyển qua phần **Target Groups**, tại trang chính chọn vào **workshop-tg**  
![SG](/images/7-TN/6.png)

8.	Tại trang **workshop-tg**, bạn sẽ thấy có **2 instance**. Hai instance này do **ASG** tạo ra và được gắn vào **Target Group**. Lúc này **ALB** sẽ dựa vào **Target Group** để phân tải  
![SG](/images/7-TN/7.png)

9.	Chuyển sang phần **Load Balancer** và chọn **workshop-ALB**  
![SG](/images/7-TN/8.png)

10.	Copy **DNS name** và dán vào thanh tìm kiếm trình duyệt  
![SG](/images/7-TN/9.png)  
![SG](/images/7-TN/10.png)

11.	**F5** liên tục sẽ thấy sự **cân bằng tải** giữa 2 instance  
![SG](/images/7-TN/11.png)  
![SG](/images/7-TN/12.png)
