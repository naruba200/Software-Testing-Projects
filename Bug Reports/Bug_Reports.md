# Bug Reports (Generated from Log v2.0)

### BUG_2026_001

| Trường | Nội dung |
|---|---|
| **Bug ID** | BUG_2026_001 |
| **Tóm tắt (Summary)** | Đăng nhập không hoạt động với ký tự đặc biệt trong mật khẩu |
| **Các bước tái hiện (Steps to Reproduce)** | 1. Truy cập trang đăng nhập.<br>2. Nhập email hợp lệ.<br>3. Nhập mật khẩu chứa ký tự đặc biệt (ví dụ: `password!@#`).<br>4. Nhấn nút "Đăng nhập". |
| **Kết quả mong đợi (Expected)** | Người dùng đăng nhập thành công và được chuyển hướng đến trang chủ. |
| **Kết quả thực tế (Actual)** | Hiển thị thông báo lỗi "Email hoặc mật khẩu không hợp lệ" và vẫn ở lại trang đăng nhập. |
| **Mức độ nghiêm trọng (Severity)** | HIGH |
| **Độ ưu tiên (Priority)** | P1 |
| **Môi trường (Environment)** | Chrome 120, Windows 11 |

---

### BUG_2026_002

| Trường | Nội dung |
|---|---|
| **Bug ID** | BUG_2026_002 |
| **Tóm tắt (Summary)** | Tìm kiếm sản phẩm chậm khi có dữ liệu lớn |
| **Các bước tái hiện (Steps to Reproduce)** | 1. Chuẩn bị cơ sở dữ liệu với hơn 10,000 sản phẩm.<br>2. Truy cập trang sản phẩm.<br>3. Nhập một từ khóa tìm kiếm phổ biến (ví dụ: "phone").<br>4. Bấm Enter và đo thời gian phản hồi. |
| **Kết quả mong đợi (Expected)** | Kết quả tìm kiếm trả về trong vòng dưới 2 giây. |
| **Kết quả thực tế (Actual)** | Thời gian phản hồi từ 5 đến 8 giây, giao diện người dùng bị treo trong khi chờ. |
| **Mức độ nghiêm trọng (Severity)** | MEDIUM |
| **Độ ưu tiên (Priority)** | P2 |
| **Môi trường (Environment)** | Staging Server, Firefox 121 |

---

### BUG_2026_003

| Trường | Nội dung |
|---|---|
| **Bug ID** | BUG_2026_003 |
| **Tóm tắt (Summary)** | Tổng giá trong giỏ hàng tính sai khi áp dụng discount |
| **Các bước tái hiện (Steps to Reproduce)** | 1. Thêm một sản phẩm có giá 100,000đ vào giỏ hàng.<br>2. Áp dụng mã giảm giá "SALE50" (giảm 50%).<br>3. Kiểm tra tổng số tiền của giỏ hàng. |
| **Kết quả mong đợi (Expected)** | Tổng số tiền trong giỏ hàng là 50,000đ. |
| **Kết quả thực tế (Actual)** | Tổng số tiền trong giỏ hàng hiển thị là 75,000đ (chỉ giảm 25%). |
| **Mức độ nghiêm trọng (Severity)** | CRITICAL |
| **Độ ưu tiên (Priority)** | P0 |
| **Môi trường (Environment)** | Production, Chrome 120 |

---

### BUG_2026_004

| Trường | Nội dung |
|---|---|
| **Bug ID** | BUG_2026_004 |
| **Tóm tắt (Summary)** | Giỏ hàng không update khi xóa sản phẩm trên mobile |
| **Các bước tái hiện (Steps to Reproduce)** | 1. Sử dụng trình duyệt Safari trên iOS.<br>2. Thêm hai sản phẩm vào giỏ hàng.<br>3. Truy cập trang giỏ hàng.<br>4. Nhấn nút "Xóa" trên một sản phẩm. |
| **Kết quả mong đợi (Expected)** | Sản phẩm bị xóa khỏi giỏ hàng ngay lập tức và tổng giá được cập nhật. |
| **Kết quả thực tế (Actual)** | Sản phẩm vẫn còn trong giỏ hàng. Người dùng phải làm mới trang để thấy sự thay đổi. |
| **Mức độ nghiêm trọng (Severity)** | HIGH |
| **Độ ưu tiên (Priority)** | P1 |
| **Môi trường (Environment)** | Safari on iOS 17 |

---

### BUG_2026_005

| Trường | Nội dung |
|---|---|
| **Bug ID** | BUG_2026_005 |
| **Tóm tắt (Summary)** | Mã khuyến mãi không được áp dụng sau khi update số lượng |
| **Các bước tái hiện (Steps to Reproduce)** | 1. Thêm sản phẩm vào giỏ hàng.<br>2. Áp dụng mã giảm giá.<br>3. Thay đổi số lượng của sản phẩm trong giỏ hàng. |
| **Kết quả mong đợi (Expected)** | Mã giảm giá vẫn được áp dụng và tổng tiền được tính toán lại chính xác. |
| **Kết quả thực tế (Actual)** | Mã giảm giá bị xóa và tổng tiền được tính lại mà không có giảm giá. |
| **Mức độ nghiêm trọng (Severity)** | MEDIUM |
| **Độ ưu tiên (Priority)** | P2 |
| **Môi trường (Environment)** | Production, All Browsers |

---

### BUG_2026_006

| Trường | Nội dung |
|---|---|
| **Bug ID** | BUG_2026_006 |
| **Tóm tắt (Summary)** | Email xác nhận đơn hàng gửi sai template |
| **Các bước tái hiện (Steps to Reproduce)** | 1. Hoàn tất một đơn hàng.<br>2. Kiểm tra email xác nhận đơn hàng được gửi đến. |
| **Kết quả mong đợi (Expected)** | Email xác nhận sử dụng template chính xác cho đơn hàng mới. |
| **Kết quả thực tế (Actual)** | Email xác nhận sử dụng một template cũ hoặc không liên quan (ví dụ: template đặt lại mật khẩu). |
| **Mức độ nghiêm trọng (Severity)** | MEDIUM |
| **Độ ưu tiên (Priority)** | P2 |
| **Môi trường (Environment)** | Production |

---

### BUG_2026_007

| Trường | Nội dung |
|---|---|
| **Bug ID** | BUG_2026_007 |
| **Tóm tắt (Summary)** | Không thể filter sản phẩm khi danh mục có dấu cách |
| **Các bước tái hiện (Steps to Reproduce)** | 1. Truy cập trang sản phẩm.<br>2. Trong bộ lọc danh mục, chọn một danh mục có chứa dấu cách (ví dụ: "Điện thoại di động"). |
| **Kết quả mong đợi (Expected)** | Các sản phẩm thuộc danh mục "Điện thoại di động" được hiển thị. |
| **Kết quả thực tế (Actual)** | Không có sản phẩm nào được hiển thị hoặc trang báo lỗi. |
| **Mức độ nghiêm trọng (Severity)** | MEDIUM |
| **Độ ưu tiên (Priority)** | P2 |
| **Môi trường (Environment)** | All Browsers |

---

### BUG_2026_008

| Trường | Nội dung |
|---|---|
| **Bug ID** | BUG_2026_008 |
| **Tóm tắt (Summary)** | Giỏ hàng bị trống sau khi thanh toán thất bại |
| **Các bước tái hiện (Steps to Reproduce)** | 1. Thêm sản phẩm vào giỏ hàng.<br>2. Tiến hành thanh toán.<br>3. Cố tình làm cho thanh toán thất bại (ví dụ: nhập sai thông tin thẻ).<br>4. Quay lại trang giỏ hàng. |
| **Kết quả mong đợi (Expected)** | Các sản phẩm vẫn còn trong giỏ hàng để người dùng có thể thử lại. |
| **Kết quả thực tế (Actual)** | Giỏ hàng trống, buộc người dùng phải thêm lại sản phẩm từ đầu. |
| **Mức độ nghiêm trọng (Severity)** | HIGH |
| **Độ ưu tiên (Priority)** | P1 |
| **Môi trường (Environment)** | Production, All Browsers |

---

### BUG_2026_009

| Trường | Nội dung |
|---|---|
| **Bug ID** | BUG_2026_009 |
| **Tóm tắt (Summary)** | Không thể xem order history trên mobile Safari |
| **Các bước tái hiện (Steps to Reproduce)** | 1. Đăng nhập vào tài khoản trên trình duyệt Safari của iPhone.<br>2. Điều hướng đến trang "Lịch sử đơn hàng". |
| **Kết quả mong đợi (Expected)** | Danh sách các đơn hàng đã đặt được hiển thị. |
| **Kết quả thực tế (Actual)** | Trang trống hoặc hiển thị một vòng quay tải vô tận. |
| **Mức độ nghiêm trọng (Severity)** | MEDIUM |
| **Độ ưu tiên (Priority)** | P2 |
| **Môi trường (Environment)** | Safari on iOS 17 |

---

### BUG_2026_010

| Trường | Nội dung |
|---|---|
| **Bug ID** | BUG_2026_010 |
| **Tóm tắt (Summary)** | Mã khuyến mãi không hiển thị giá gốc sau khi áp dụng |
| **Các bước tái hiện (Steps to Reproduce)** | 1. Thêm sản phẩm vào giỏ hàng.<br>2. Áp dụng một mã giảm giá.<br>3. Quan sát phần tóm tắt giỏ hàng. |
| **Kết quả mong đợi (Expected)** | Hiển thị cả giá gốc, số tiền được giảm và tổng tiền cuối cùng. |
| **Kết quả thực tế (Actual)** | Chỉ hiển thị tổng tiền cuối cùng, gây khó khăn cho người dùng trong việc xác nhận mức giảm giá. |
| **Mức độ nghiêm trọng (Severity)** | MEDIUM |
| **Độ ưu tiên (Priority)** | P2 |
| **Môi trường (Environment)** | Production, All Browsers |

---