---
title : "Cập Nhật Tài Khoản AWS"
date : "2025-06-19T06:49:25.364"
weight : 2
chapter : false
pre : " <b> 1.2 </b> "
---

#### Cập nhật tên tài khoản, địa chỉ email, mật khẩu của người dùng

#### Chỉnh sửa thông tin tài khoản AWS người dùng
- Để thay đổi tên tài khoản AWS, mật khẩu người dùng gốc hoặc địa chỉ email người dùng gốc, hãy làm theo các bước dưới đây. Địa chỉ email và mật khẩu của bạn đóng vai trò là thông tin xác thực để đăng nhập với tư cách là người dùng gốc của tài khoản AWS.

> **Ghi chú:** những thay đổi được thực hiện trên tài khoản AWS có thể mất tới bốn giờ để lan truyền trên tất cả các dịch vụ.


#### Chỉnh sửa tên tài khoản, mật khẩu người dùng, hoặc địa chỉ email.

**Quyền truy cập tối thiểu:**
  Để tiến hành các bước sau, bạn cần có ít nhất các quyền IAM sau:

- Bạn phải đăng nhập với tư cách là người dùng gốc của tài khoản AWS. Không yêu cầu thêm quyền IAM nào. Người dùng hoặc vai trò IAM không thể thực hiện các bước này.

1. Đăng nhập vào AWS Management Console bằng địa chỉ email và mật khẩu của tài khoản AWS của bạn.

2. Ở góc trên bên phải của bảng điều khiển, nhấp vào tên tài khoản hoặc số tài khoản của bạn, sau đó chọn "Tài khoản"

3. Trên trang Tài khoản, tìm mục "Cài đặt tài khoản" và nhấp vào "Chỉnh sửa". Bạn sẽ được yêu cầu xác thực lại vì lý do bảo mật.

   > **Ghi Chú:** Nếu không thấy tùy chọn chỉnh sửa, điều này có nghĩa là bạn đang không đăng nhập với tư cách người dùng root của tài khoản AWS. Cài đặt tài khoản không thể thay đổi khi bạn đăng nhập dưới dạng người dùng IAM hoặc vai trò.

4. Trên trang cập nhật cài đặt tài khoản, chọn "Chỉnh sửa" bên cạnh trường bạn muốn cập nhật.

   - Đối với **Tên tài khoản** Trên trang cập nhật tên tài khoản của bạn, nhập tên tài khoản mới vào trường "Tên tài khoản mới", sau đó nhấp vào "Lưu thay đổi."

     > **Ghi chú:** Đối với Email: Trên trang cập nhật địa chỉ email của bạn, cung cấp thông tin cần thiết cho "Địa chỉ email mới," "Xác nhận địa chỉ email mới," và xác nhận mật khẩu hiện tại của bạn. Sau đó, nhấp vào "Lưu thay đổi." Một mã xác minh sẽ được gửi đến địa chỉ email mới của bạn từ "no-reply@verify.signin.aws."Trên trang "Xác minh địa chỉ email mới của bạn", nhập mã xác minh bạn nhận được qua email, sau đó nhấp vào "Lưu thay đổi."

     > **Ghi Chú:** Mã xác minh có thể mất đến 5 phút để đến. Nếu không tìm thấy email trong hộp thư đến, hãy nhớ kiểm tra trong thư mục spam hoặc junk.

   - Đối với **Mật Khẩu**: Trên trang "Cập nhật mật khẩu của bạn", điền vào các trường "Mật khẩu hiện tại," "Mật khẩu mới," và "Xác nhận mật khẩu mới." Sau đó, nhấp vào "Lưu thay đổi." Để biết thêm hướng dẫn và các thực hành tốt nhất về quản lý mật khẩu của người dùng root, có thể tham khảo thêm tại [Thay Đổi Mật Khẩu Với Người Dùng Tại AWS](link-to-documentation).

5. Sau khi hoàn tất mọi thay đổi mong muốn, hãy chọn "OK".
