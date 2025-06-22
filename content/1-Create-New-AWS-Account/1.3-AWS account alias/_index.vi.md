---
title : "Tạo Hoặc Chỉnh Sửa Tài Khoản AWS Của Bạn"
date : "2025-06-19T06:49:25.364"
weight : 3
chapter : false
pre : " <b> 1.3 </b> "
---

####  Quản lý bí danh tài khoản AWS cho người dùng IAM đăng nhập

Người dùng gốc tài khoản AWS và người dùng AWS Identity and Access Management (IAM) trong tài khoản đăng nhập bằng URL web.

Nếu bạn muốn URL cho người dùng IAM của mình chứa tên công ty của bạn (hoặc một mã định danh dễ nhớ khác) thay vì ID tài khoản AWS, bạn có thể tạo bí danh tài khoản. Phần này cung cấp thông tin về bí danh tài khoản AWS và liệt kê các hoạt động API mà bạn có thể sử dụng để tạo bí danh.

Theo mặc định, URL trang đăng nhập cho người dùng IAM của tài khoản bạn có định dạng sau:

```
https://Your_Account_ID.signin.aws.amazon.com/console/
```


INếu bạn tạo bí danh tài khoản AWS cho ID tài khoản AWS của mình, URL trang đăng nhập người dùng IAM sẽ trông giống như ví dụ sau:
```
https://Your_Account_Alias.signin.aws.amazon.com/console/
```


URL gốc chứa ID tài khoản AWS của bạn vẫn hoạt động và vẫn có thể được sử dụng sau khi bạn tạo bí danh tài khoản AWS.

#### Gợi ý: 
Để tạo dấu trang cho trang đăng nhập tài khoản của bạn trong trình duyệt web, chúng tôi khuyên bạn nên nhập thủ công URL đăng nhập vào mục nhập dấu trang. Không sử dụng tính năng "đánh dấu trang này" của trình duyệt web vì nó có thể ghi lại thông tin cụ thể của phiên có thể ảnh hưởng đến các lần truy cập trang trong tương lai.

#### Những lưu ý: 
- Tài khoản AWS của bạn chỉ có thể có một bí danh. Việc tạo bí danh mới sẽ ghi đè lên bí danh trước đó và URL chứa bí danh trước đó sẽ ngừng hoạt động.
- Bí danh tài khoản phải là duy nhất trên tất cả các sản phẩm Amazon Web Services.
- Bí danh chỉ có thể chứa chữ thường, chữ số và dấu gạch nối.

#### Tạo hoặc chinh sửa tài khoản ẩn danh của bạn

#### Quyền truy cập tối thiểu
Để thực hiện các bước sau, bạn phải có ít nhất các quyền IAM sau:

- `iam:ListAccountAliases`
- `iam:CreateAccountAlias`

1. Đăng nhập vào AWS Management Console với tư cách là người dùng gốc của tài khoản AWS hoặc là người dùng hoặc vai trò IAM có quyền tối thiểu.

2. Mở cửa sổ IAM [https://console.aws.amazon.com/iam/](https://console.aws.amazon.com/iam/).

3. Trong bảng điều hướng, chọn **Dashboard**.

4. Trong ngăn bên phải dưới tài khoản AWS, bên cạnh **tài khoản ẩn danh**, chọn **tạo tài khoản**. Nếu đã có tài khoản ẩn danh, hãy chọn **chỉnh sửa**.

5. Trong hộp thoại, nhập tên mới hoặc tên đã cập nhật mà bạn muốn sử dụng cho bí danh của mình, sau đó chọn **Lưu thay đổi**.
**Ghi chú**: Bạn chỉ có thể có một bí danh được liên kết với tài khoản AWS của mình tại một thời điểm. Nếu bạn tạo một bí danh mới, bí danh trước đó sẽ bị xóa và URL đăng nhập được liên kết với bí danh trước đó sẽ ngừng hoạt động.

---

#### Xóa tài khoản ẩn danh

#### Quyền truy cập tối thiểu
Để thực hiện các bước sau, bạn phải có ít nhất các quyền IAM sau:

- `iam:ListAccountAliases`
- `iam:CreateAccountAlias`
- `iam:DeleteAccountAlias`

1.Đăng nhập vào AWS Management Console với tư cách là người dùng gốc của tài khoản AWS hoặc là người dùng hoặc vai trò IAM có quyền tối thiểu.

2. Mở bảng điều khiển IAM tại [https://console.aws.amazon.com/iam/](https://console.aws.amazon.com/iam/).

3. Trong ngăn điều hướng, chọn **Bảng điều khiển**.

4. Trong ngăn bên phải bên dưới tài khoản AWS, bên cạnh **tài khoản ẩn danh**, chọn **Xóa**.
