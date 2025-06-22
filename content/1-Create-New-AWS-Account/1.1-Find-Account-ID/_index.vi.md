---
title : "Xem ID Tài Khoản Người Dùng"
date : "2025-06-19T06:49:25.364"
weight : 1
chapter : false
pre : " <b> 1.1 </b> "
---

#### Xem ID Tài Khoản Người Dùng

#### Tìm ID Tài Khoản Người Dùng

Bạn có thể tìm ID tài khoản AWS bằng **AWS Management Console** hoặc **AWS Command Line Interface** (AWS CLI). Trong bảng điều khiển, vị trí của ID tài khoản phụ thuộc vào việc bạn đã đăng nhập với tư cách là người dùng gốc hay người dùng IAM. ID tài khoản vẫn giữ nguyên cho dù bạn đã đăng nhập với tư cách là người dùng gốc hay người dùng IAM.

#### Quyền Truy Cập Tối Thiểu 

Để thực hiện các bước sau, bạn phải có ít nhất các quyền IAM sau:

- Khi bạn đăng nhập với tư cách là người dùng gốc, bạn không cần bất kỳ quyền IAM nào.
- Trong thanh điều hướng ở góc trên bên phải, hãy chọn tên hoặc số tài khoản của bạn, sau đó chọn **Thông tin xác thực bảo mật**.

**Tip:** Nếu bạn không thấy tùy chọn **Thông tin xác thực bảo mật**, bạn có thể đã đăng nhập với tư cách là người dùng liên kết có vai trò IAM, thay vì là người dùng IAM. Trong trường hợp này, hãy tìm mục **Tài khoản** và số ID tài khoản bên cạnh mục đó.

Trong phần **Chi tiết tài khoản**, số tài khoản sẽ xuất hiện bên cạnh **ID tài khoản AWS**.

#### Tìm ID tài khoản AWS của bạn với tư cách là Người dùng IAM

#### Quyền tối thiểu

Để thực hiện các bước sau, bạn phải có ít nhất các quyền IAM sau:

- `aws-portal:ViewAccount`

1. Trong thanh điều hướng ở góc trên bên phải, hãy chọn tên người dùng của bạn rồi chọn **Thông tin xác thực bảo mật**.

> **Tip:** Nếu bạn không thấy tùy chọn **Thông tin xác thực bảo mật**, bạn có thể đã đăng nhập với tư cách là người dùng liên kết có vai trò IAM, thay vì là người dùng IAM. Trong trường hợp này, hãy tìm mục **Tài khoản** và số ID tài khoản bên cạnh mục đó.

2. Ở đầu trang, bên dưới **Chi tiết tài khoản**, số tài khoản sẽ xuất hiện bên cạnh **ID tài khoản AWS**.

#### Tìm ID người dùng chuẩn cho tài khoản AWS của bạn

Bạn có thể tìm ID người dùng chuẩn cho tài khoản AWS của mình bằng AWS Management Console hoặc AWS CLI. ID người dùng chuẩn cho tài khoản AWS là ID dành riêng cho tài khoản đó. Bạn có thể truy xuất ID người dùng chuẩn cho tài khoản AWS của mình dưới dạng người dùng gốc, người dùng liên kết hoặc người dùng IAM.

#### Tìm ID chuẩn là người dùng gốc hoặc người dùng IAM

Để tìm ID chuẩn cho tài khoản của bạn khi đăng nhập vào bảng điều khiển với tư cách là người dùng gốc hoặc người dùng IAM:

**Quyền tối thiểu:**

Để thực hiện các bước sau, bạn phải có ít nhất các quyền IAM sau:

- Khi bạn chạy lệnh với tư cách là người dùng gốc, bạn không cần bất kỳ quyền IAM nào.
- Khi bạn đăng nhập với tư cách là người dùng IAM, thì bạn phải có:
- `aws-portal:ViewAccount`

1. Đăng nhập vào AWS Management Console với tư cách là người dùng gốc hoặc người dùng IAM.
2. Trong thanh điều hướng ở góc trên bên phải, hãy chọn tên hoặc số tài khoản của bạn, sau đó chọn "Thông tin xác thực bảo mật".

> **Tip:** Nếu bạn không thấy tùy chọn "Thông tin xác thực bảo mật", có thể bạn đã đăng nhập với tư cách là người dùng liên kết có vai trò IAM, thay vì là người dùng IAM. Trong trường hợp này, hãy tìm mục "Tài khoản" và số ID tài khoản bên cạnh mục đó.

3. Trong phần "Chi tiết tài khoản", ID người dùng chuẩn sẽ xuất hiện bên cạnh "ID người dùng chuẩn". Bạn có thể sử dụng ID người dùng chuẩn của mình để định cấu hình danh sách kiểm soát truy cập (ACL) của Amazon S3.

#### Tìm ID chuẩn khi là người dùng liên kết có vai trò IAM

Để tìm ID chuẩn cho tài khoản của bạn khi đã đăng nhập vào bảng điều khiển với tư cách là người dùng liên kết có vai trò IAM

#### Quyền tối thiểu
Bạn phải có quyền để liệt kê và xem thùng Amazon S3.

1. Đăng nhập vào Bảng điều khiển quản lý AWS với tư cách là người dùng liên kết có vai trò IAM.
2. Trong bảng điều khiển Amazon S3, hãy chọn tên thùng để xem chi tiết về thùng.
3. Chọn tab Quyền.
4. Trong phần Danh sách kiểm soát truy cập, bên dưới Chủ sở hữu thùng, ID chuẩn cho tài khoản AWS của bạn sẽ xuất hiện.
