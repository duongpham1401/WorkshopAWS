---
title : "Tạo Một Security Group"
date : "2025-06-19T06:49:25.364"
weight : 2.
chapter : false
pre : " <b> 2.2 </b> "
---

## Tạo một Security Group

1. **Đăng nhập vào Bảng điều khiển** ở trang [AWS Web Service page](https://aws.amazon.com/)
2. Nhấn vào thanh tìm kiếm trên aws vào tìm kiếm **VPC Isolated Cloud Resources**

    ![AWS SG](/images/2/12001.png?featherlight=false&width=90pc)

3. Nhìn vào cửa sổ bên trái nhấn chọn **Security group** ở trong mục **Security** (*như hình bước 1*) và ấn chọn ** tạo Security group ** (như trong hình bước 2)

    ![AWS VPC](/images/3/13002.png?featherlight=false&width=90pc)

4. Ngay tại bên dưới **Security group name** hãy đặt tên cho security group: *(vd: SGR-workshop,SG-Public,....)*

    +  Hãy nhập mô tả cho security group
    +  Chọn VPC mà mình đã tạo sẵn ở các bài trước (hoặc tạo lại tại trang [AWS Web Service page](https://ap-southeast-1.console.aws.amazon.com/vpcconsole/home?region=ap-southeast-1#vpcs:))
    + Tại mục Inbound rules ở **type** chọn **SSH** và **Source** ấn chọn **My IP** (như ở bước số 3)
    + Tiếp theo thêm rule tại **type** đầu tiên chọn **ALL ICMP-IPV4** và chọn **Source** là **Anywhere IPV4** (như hình bước 4)
    + Tiếp đến chọn tạo **Security group**

    ![AWS SG](/images/3/13003.png?featherlight=false&width=90pc)

5. Khi tạo xong security public thành công

    ![AWS SG](/images/3/13004.png?featherlight=false&width=90pc)

6. Tiếp tục như thế tạo thêm 1 **Private security group**

    +  Hãy nhập mô tả cho security group
    +  Chọn VPC mà mình đã tạo sẵn ở các bài trước (hoặc tạo lại tại trang [AWS Web Service page](https://ap-southeast-1.console.aws.amazon.com/vpcconsole/home?region=ap-southeast-1#vpcs:))
    + Tại mục Inbound rules ở **type** chọn **SSH** và **Source** ấn chọn **Security group(đã tạo trước đó)** (như ở bước số 3)
    **Ghi chú:** **Source** ở bước này có thể gán trực tiếp vào *Publicsubnet*
    + Tiếp theo thêm rule tại **type** đầu tiên chọn **ALL ICMP-IPV4** và chọn **Source** là **Anywhere IPV4** (như hình bước 4)
    + Tiếp đến chọn tạo **Security group**
    
    ![AWS SG](/images/3/13005.png?featherlight=false&width=90pc)

7. Sau khi tạo thành công thêm 1 **Private security group**

    ![AWS SG](/images/3/13006.png?featherlight=false&width=90pc)

8. Hoàn thành tạo một **Public security group** và **Private security group**

    ![AWS SG](/images/3/13007.png?featherlight=false&width=90pc)

## Tạo một máy chủ EC2

1. **Đăng nhập vào Bảng điều khiển** ở trang [AWS Web Service page](https://aws.amazon.com/)
2. Nhấn vào thanh tìm kiếm trên aws vào tìm kiếm **EC2**

    ![AWS EC2](/images/3/13001.png?featherlight=false&width=90pc)

3. Nhìn vào cửa sổ bên trái nhấn chọn **Instances** ở trong mục **Instances** (*như hình bước 1*) và ấn chọn **tạo Launch instances** (như trong hình bước 2)

    ![AWS EC2](/images/3/13008.png?featherlight=false&width=90pc)

4. Ngay tại bên dưới **Name and tag** hãy đặt tên cho Launch instances: *(vd: EC2 Public,EC2 Private,....)*

    +  Ngay tại **Amazon Machine Image** nên chọn **Amazon linux 2 AMI(HVM)**
    +  Tiếp theo tạo **Key Pair** đặt tên cho keypair và sử dụng keypair ở dạng file .pem, sau đó ấn tạo một keypair

    ![AWS SG](/images/3/13009.png?featherlight=false&width=90pc)
    ![AWS SG](/images/3/13010.png?featherlight=false&width=90pc) 

5.  Chỉnh sửa **Network settings** chọn VPC và Public subnet đã tạo trước đó *(ở bước 1 và bước 2)*
    
    + Kiểm tra **Auto-assign public IP** ở trạng thái **Enable**
    + Chọn **Security existing security group**, ở **Common security group** chọn **Public security** *(như trong hình bước 3)*
    + Kiểm tra lại và chọn **tạo launch instance**

    ![AWS SG](/images/3/13011.png?featherlight=false&width=90pc)

6. Khi tạo xong EC2 public thành công

    ![AWS SG](/images/3/13012.png?featherlight=false&width=90pc)

7. Tiếp tục như **Public EC2** tạo thêm một **EC2 Private**

     Ngay tại bên dưới **Name and tag** hãy đặt tên cho Launch instances: *(vd: EC2 Public,EC2 Private,....)*

    +  Ngay tại **Amazon Machine Image** nên chọn **Amazon linux 2 AMI(HVM)**
    +  Tiếp theo tạo **Key Pair** đặt tên cho keypair và sử dụng keypair ở dạng file .pem, sau đó ấn tạo một keypair

    ![AWS SG](/images/3/13013.png?featherlight=false&width=90pc)
    ![AWS SG](/images/3/13010.png?featherlight=false&width=90pc) 

8.  Chỉnh sửa **Network settings** chọn VPC và Public subnet đã tạo trước đó 
    
    + Kiểm tra **Auto-assign public IP** ở trạng thái **Disable** 
    **Ghi chú:** Vì là **Private EC2** nên phải để ở trạng thái **Disable**
    + Chọn **Security existing security group**, ở **Common security group** chọn **Private security**
    + Kiểm tra lại và chọn **tạo launch instance**

    ![AWS SG](/images/3/13014.png?featherlight=false&width=90pc)

9. Tạo **Private EC2** thành công

    ![AWS SG](/images/3/13015.png?featherlight=false&width=90pc)


11. Sau khi tạo và khởi chạy hai **EC2 Public** và **Private EC2** thành công

    ![AWS SG](/images/3/13016.png?featherlight=false&width=90pc)

12. Dùng **MobaXterm** để kiểm tra kết nối

    ![AWS SG](/images/3/13018.png?featherlight=false&width=50pc)
    ![AWS SG](/images/3/13019.png?featherlight=false&width=50pc)




