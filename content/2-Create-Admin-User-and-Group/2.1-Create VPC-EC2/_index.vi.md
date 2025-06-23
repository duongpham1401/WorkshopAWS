---
title : "Tạo Một Máy Chủ VPC"
date : "2025-06-19T06:49:25.364"
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

## Tạo một máy chủ ảo VPC (Virtural Private Server)

1. **Đăng nhập vào Bảng điều khiển** ở trang [AWS Web Service page](https://aws.amazon.com/)
2. Nhấn vào thanh tìm kiếm trên aws vào tìm kiếm **VPC Isolated Cloud Resources**
    ![AWS VPC](/images/2/12001.png?featherlight=false&width=90pc)

3. Nhìn vào cửa sổ bên trái nhấn chọn **Yours VPS** (*như hình bước 1*) và ấn chọn **Creat VPC** (như trong hình bước 2)

    ![AWS VPC](/images/2/12002.png?featherlight=false&width=90pc)

4. Nhấn chọn **VPC Only** ở mục đầu tiên
    + Ở mục **Name tag** chúng ta có thể đặt tên cho VPC (*VD: VPC 1, VPC 2,...*) (ở bước 1 như trong hình )
    + Sau đó chọn IPV4 CIDR *(lưu ý CIDR phải nằm giữa /26 và /28)* (ở bước 2)
    + IPV6 CIDR để mặc định (chưa cần dùng đến)
    + Sau các bước nhấn chọn **Create VPC**

    ![AWS VPC](/images/2/12003.png?featherlight=false&width=90pc)

5. Tạo máy chủ ảo thành công
    ![AWS VPC](/images/2/12004.png?featherlight=false&width=90pc)

## Tạo Subnets

1. **Đăng nhập vào Bảng điều khiển** ở trang [AWS Web Service page](https://aws.amazon.com/)
2. Nhấn vào thanh tìm kiếm trên aws vào tìm kiếm **VPC Isolated Cloud Resources**

    ![AWS Subnet](/images/2/12001.png?featherlight=false&width=90pc)

3. Nhìn vào cửa sổ bên trái nhấn chọn **Subnets** (*như hình bước 1*) và ấn chọn **Creat Subnets** (như trong hình bước 2)

    ![AWS Subnet](/images/2/12005.png?featherlight=false&width=90pc)
4. Khi tạo subnet chúng ta phải chọn lại **ID VPC** vừa tạo trước đó
    + Đặt tên cho subnet *(VD:Public subnet 1, public subnet 2,...)*
    + Sau đó chúng ta chọn **Availability Zone**
    + Dựa theo IPV4 CIDR chúng ta chọn IPV4 subnet CIDR
    + Tiếp theo chọn **Tạo subnet**

    ![AWS Subnet](/images/2/12006.png?featherlight=false&width=90pc)

5. Sau khi tạo thành công **Public Subnets 1**

    ![AWS Subnet](/images/2/12007.png?featherlight=false&width=90pc)

6. Tương tự tạo thêm 1 **Public Subnets 2**

    ![AWS Subnet](/images/2/12009.png?featherlight=false&width=90pc)

    *Hoàn thành tạo **Public sbunet 2***
    ![AWS Subnet](/images/2/12010.png?featherlight=false&width=90pc)

7. Tương tự như **Public subnet** chúng ta tạo thêm 2 **Private subnet**

    *Private Subnet 1*
    ![AWS Subnet](/images/2/12009.png?featherlight=false&width=90pc)

    *Private Subnet 2*
    ![AWS Subnet](/images/2/12010.png?featherlight=false&width=90pc)

8. Sau khi hoàn thành tạo được 4 subnet

    ![AWS Subnet](/images/2/12013.png?featherlight=false&width=90pc)

9. Tiếp theo chúng ta sẽ chỉnh sửa 2 **public subnet 1** và **public subnet 2** 
    + Đầu tiên chọn **Public Subnet 1** để chỉnh sửa
    + Chọn **Action** và chọn vào **chỉnh sửa cài đặt subnets**
    + Tiếp theo chọn vào **Enable auto-assign public IPV4 address**
    + Sau đó chọn **Lưu thông tin**
    > **Ghi chú:** Chỉnh sửa để tự động cấp phát ID address

    ![AWS Subnet](/images/2/12014.png?featherlight=false&width=90pc)
    ![AWS Subnet](/images/2/12016.png?featherlight=false&width=90pc)

11. Sau Khi chỉnh sửa thành công sẽ có dòng thông báo màu xanh

    ![AWS Subnet](/images/2/12013.png?featherlight=false&width=90pc)

12. Tương tự như vậy chúng ta chỉnh sửa với **Public subnet 2**

    ![AWS Subnet](/images/2/12017.png?featherlight=false&width=90pc)
    *Sau khi thay đổi public subnet 2 thành công*
    ![AWS Subnet](/images/2/12018.png?featherlight=false&width=90pc)

## Tạo một  Internet Gateway

1. **Đăng nhập vào Bảng điều khiển** ở trang [AWS Web Service page](https://aws.amazon.com/)
2. Nhấn vào thanh tìm kiếm trên aws vào tìm kiếm **VPC Isolated Cloud Resources**

    ![AWS internet gateways](/images/2/12001.png?featherlight=false&width=90pc)

3. Nhìn vào cửa sổ bên trái nhấn chọn **Internet gateways** (*như hình bước 1*) và ấn chọn **tạo internet gateways** (như trong hình bước 2)

    ![AWS internet gateways](/images/2/12019.png?featherlight=false&width=90pc)

4. Đặt tên cho **internet gateways** *(VD: internet-gateways,internetGW!,....)*
    + Chọn tạo **internet gateways**

    ![AWS internet gateways](/images/2/12020.png?featherlight=false&width=90pc)

5. Sau khi tạo thành công **internet gateway**

    ![AWS internet gateways](/images/2/12021.png?featherlight=false&width=90pc)

    ![AWS internet gateways](/images/2/12022.png?featherlight=false&width=90pc)

## Tạo một Router Table
1. **Đăng nhập vào Bảng điều khiển** ở trang [AWS Web Service page](https://aws.amazon.com/)
2. Nhấn vào thanh tìm kiếm trên aws vào tìm kiếm **VPC Isolated Cloud Resources**

    ![AWS Router Table](/images/2/12001.png?featherlight=false&width=90pc)

3. Nhìn vào cửa sổ bên trái nhấn chọn **Route Table** (*như hình bước 1*) và ấn chọn **tạo route table** (như trong hình bước 2)

    ![AWS Router Table](/images/2/12023.png?featherlight=false&width=90pc)

4. Sau khi tạo thành công màn hình sẽ như sau: 

    ![AWS Router Table](/images/2/12024.png?featherlight=false&width=90pc)

5. Chỉnh sửa route table
    + Chọn route cần chỉnh sửa 
    + Muc target chọn **local** và **Internet gateway**
    + Sau đó chọn **Lưu thay đổi**

    ![AWS Router Table](/images/2/12025.png?featherlight=false&width=90pc)










