# CA KIỂM THỬ - MODULE 1: XÁC THỰC NGƯỜI DÙNG (AUTHENTICATION)

**Phiên bản:** 1.0  
**Ngày tạo:** 03/03/2026  
**Module:** Authentication  
**Tác giả:** QA Team

---

## 1. ĐĂNG KÝ TÀI KHOẢN (REGISTRATION)

### TC_AUTH_REG_001 - Đăng ký thành công với email và mật khẩu hợp lệ
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_AUTH_REG_001 |
| **Tên test case** | Đăng ký thành công với email và mật khẩu hợp lệ |
| **Module** | Authentication |
| **Tính năng** | Đăng ký tài khoản |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Trình duyệt được mở<br>- Trang đăng ký có thể truy cập |
| **Bước thực thi** | 1. Truy cập trang đăng ký<br>2. Nhập email: test@gmail.com<br>3. Nhập mật khẩu: Test@1234<br>4. Nhập xác nhận mật khẩu: Test@1234<br>5. Click nút "Đăng ký" |
| **Kết quả mong đợi** | - Đăng ký thành công<br>- Hiển thị thông báo "Đăng ký thành công"<br>- Chuyển hướng đến trang đăng nhập<br>- Email được lưu trong hệ thống |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 05/03/2026 |
| **Tester** | QA Engineer 1 |

---

### TC_AUTH_REG_002 - Không đăng ký khi email sai định dạng
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_AUTH_REG_002 |
| **Tên test case** | Không đăng ký khi email sai định dạng |
| **Module** | Authentication |
| **Tính năng** | Đăng ký tài khoản |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Trình duyệt được mở<br>- Trang đăng ký có thể truy cập |
| **Bước thực thi** | 1. Truy cập trang đăng ký<br>2. Nhập email: invalidemail (không có @)<br>3. Nhập mật khẩu: Test@1234<br>4. Nhập xác nhận mật khẩu: Test@1234<br>5. Click nút "Đăng ký" |
| **Kết quả mong đợi** | - Không xảy ra đăng ký<br>- Hiển thị lỗi: "Email không hợp lệ"<br>- Vẫn ở trang đăng ký |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 05/03/2026 |
| **Tester** | QA Engineer 1 |

---

### TC_AUTH_REG_003 - Không đăng ký khi mật khẩu dưới 8 ký tự
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_AUTH_REG_003 |
| **Tên test case** | Không đăng ký khi mật khẩu dưới 8 ký tự |
| **Module** | Authentication |
| **Tính năng** | Đăng ký tài khoản |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Trình duyệt được mở<br>- Trang đăng ký có thể truy cập |
| **Bước thực thi** | 1. Truy cập trang đăng ký<br>2. Nhập email: test@gmail.com<br>3. Nhập mật khẩu: Test123 (7 ký tự)<br>4. Nhập xác nhận mật khẩu: Test123<br>5. Click nút "Đăng ký" |
| **Kết quả mong đợi** | - Không xảy ra đăng ký<br>- Hiển thị lỗi: "Mật khẩu tối thiểu 8 ký tự"<br>- Vẫn ở trang đăng ký |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 05/03/2026 |
| **Tester** | QA Engineer 1 |

---

### TC_AUTH_REG_004 - Không đăng ký khi email đã tồn tại
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_AUTH_REG_004 |
| **Tên test case** | Không đăng ký khi email đã tồn tại |
| **Module** | Authentication |
| **Tính năng** | Đăng ký tài khoản |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Trình duyệt được mở<br>- Trang đăng ký có thể truy cập<br>- Email "existing@gmail.com" đã tồn tại |
| **Bước thực thi** | 1. Truy cập trang đăng ký<br>2. Nhập email: existing@gmail.com<br>3. Nhập mật khẩu: Test@1234<br>4. Nhập xác nhận mật khẩu: Test@1234<br>5. Click nút "Đăng ký" |
| **Kết quả mong đợi** | - Không xảy ra đăng ký<br>- Hiển thị lỗi: "Email đã tồn tại"<br>- Vẫn ở trang đăng ký |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 05/03/2026 |
| **Tester** | QA Engineer 1 |

---

## 2. ĐĂNG NHẬP (LOGIN)

### TC_AUTH_LOGIN_001 - Đăng nhập thành công với email và mật khẩu hợp lệ
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_AUTH_LOGIN_001 |
| **Tên test case** | Đăng nhập thành công với email và mật khẩu hợp lệ |
| **Module** | Authentication |
| **Tính năng** | Đăng nhập |
| **Ưu tiên** | High |
| **Severity** | Critical |
| **Điều kiện tiên quyết** | - Trình duyệt được mở<br>- Trang đăng nhập có thể truy cập<br>- Tài khoản test@gmail.com / Test@1234 đã tồn tại |
| **Bước thực thi** | 1. Truy cập trang đăng nhập<br>2. Nhập email: test@gmail.com<br>3. Nhập mật khẩu: Test@1234<br>4. Click nút "Đăng nhập" |
| **Kết quả mong đợi** | - Đăng nhập thành công<br>- Chuyển hướng đến trang chủ (Dashboard)<br>- Hiển thị tên người dùng ở góc phải<br>- Session được tạo |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 05/03/2026 |
| **Tester** | QA Engineer 1 |

---

### TC_AUTH_LOGIN_002 - Đăng nhập thất bại khi sai mật khẩu
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_AUTH_LOGIN_002 |
| **Tên test case** | Đăng nhập thất bại khi sai mật khẩu |
| **Module** | Authentication |
| **Tính năng** | Đăng nhập |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Trình duyệt được mở<br>- Trang đăng nhập có thể truy cập<br>- Tài khoản test@gmail.com tồn tại |
| **Bước thực thi** | 1. Truy cập trang đăng nhập<br>2. Nhập email: test@gmail.com<br>3. Nhập mật khẩu: WrongPassword<br>4. Click nút "Đăng nhập" |
| **Kết quả mong đợi** | - Đăng nhập thất bại<br>- Hiển thị lỗi: "Email hoặc mật khẩu không chính xác"<br>- Vẫn ở trang đăng nhập |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 05/03/2026 |
| **Tester** | QA Engineer 1 |

---

### TC_AUTH_LOGIN_003 - Đăng nhập thất bại khi email không tồn tại
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_AUTH_LOGIN_003 |
| **Tên test case** | Đăng nhập thất bại khi email không tồn tại |
| **Module** | Authentication |
| **Tính năng** | Đăng nhập |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Trình duyệt được mở<br>- Trang đăng nhập có thể truy cập |
| **Bước thực thi** | 1. Truy cập trang đăng nhập<br>2. Nhập email: nonexistent@gmail.com<br>3. Nhập mật khẩu: Test@1234<br>4. Click nút "Đăng nhập" |
| **Kết quả mong đợi** | - Đăng nhập thất bại<br>- Hiển thị lỗi: "Email hoặc mật khẩu không chính xác"<br>- Vẫn ở trang đăng nhập |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 05/03/2026 |
| **Tester** | QA Engineer 1 |

---

## 3. QUÊN MẬT KHẨU (FORGOT PASSWORD)

### TC_AUTH_FP_001 - Gửi email đặt lại mật khẩu thành công
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_AUTH_FP_001 |
| **Tên test case** | Gửi email đặt lại mật khẩu thành công |
| **Module** | Authentication |
| **Tính năng** | Quên mật khẩu |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Trình duyệt được mở<br>- Trang quên mật khẩu có thể truy cập<br>- Email test@gmail.com tồn tại |
| **Bước thực thi** | 1. Click "Quên mật khẩu" trên trang đăng nhập<br>2. Truy cập trang đặt lại mật khẩu<br>3. Nhập email: test@gmail.com<br>4. Click nút "Gửi" |
| **Kết quả mong đợi** | - Hiển thị thông báo thành công<br>- Email được gửi tới test@gmail.com<br>- Email chứa link đặt lại mật khẩu |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 05/03/2026 |
| **Tester** | QA Engineer 2 |

---

## 4. ĐĂNG XUẤT (LOGOUT)

### TC_AUTH_LOGOUT_001 - Đăng xuất thành công
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_AUTH_LOGOUT_001 |
| **Tên test case** | Đăng xuất thành công |
| **Module** | Authentication |
| **Tính năng** | Đăng xuất |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Người dùng đã đăng nhập thành công |
| **Bước thực thi** | 1. Đăng nhập hệ thống<br>2. Click vào menu người dùng ở góc phải<br>3. Click "Đăng xuất" |
| **Kết quả mong đợi** | - Đăng xuất thành công<br>- Chuyển hướng đến trang đăng nhập<br>- Session bị xoá<br>- Không thể quay lại Dashboard |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 05/03/2026 |
| **Tester** | QA Engineer 2 |

---

### TC_AUTH_REG_005 - Không đăng ký khi email trống
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_AUTH_REG_005 |
| **Tên test case** | Không đăng ký khi email trống |
| **Module** | Authentication |
| **Tính năng** | Đăng ký tài khoản |
| **Ưu tiên** | High |
| **Severity** | High |
| **Loại test** | Negative - Boundary |
| **Điều kiện tiên quyết** | - Trình duyệt được mở<br>- Trang đăng ký có thể truy cập |
| **Bước thực thi** | 1. Truy cập trang đăng ký<br>2. Để trống trường email<br>3. Nhập mật khẩu: Test@1234<br>4. Nhập xác nhận mật khẩu: Test@1234<br>5. Click nút "Đăng ký" |
| **Kết quả mong đợi** | - Không xảy ra đăng ký<br>- Hiển thị lỗi: "Email là bắt buộc"<br>- Vẫn ở trang đăng ký |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 06/03/2026 |
| **Tester** | QA Engineer 1 |

---

### TC_AUTH_REG_006 - Không đăng ký khi mật khẩu trống
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_AUTH_REG_006 |
| **Tên test case** | Không đăng ký khi mật khẩu trống |
| **Module** | Authentication |
| **Tính năng** | Đăng ký tài khoản |
| **Ưu tiên** | High |
| **Severity** | High |
| **Loại test** | Negative - Boundary |
| **Điều kiện tiên quyết** | - Trình duyệt được mở<br>- Trang đăng ký có thể truy cập |
| **Bước thực thi** | 1. Truy cập trang đăng ký<br>2. Nhập email: test@gmail.com<br>3. Để trống trường mật khẩu<br>4. Để trống trường xác nhận mật khẩu<br>5. Click nút "Đăng ký" |
| **Kết quả mong đợi** | - Không xảy ra đăng ký<br>- Hiển thị lỗi: "Mật khẩu là bắt buộc"<br>- Vẫn ở trang đăng ký |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 06/03/2026 |
| **Tester** | QA Engineer 1 |

---

### TC_AUTH_REG_007 - Đăng ký thành công với mật khẩu chứa ký tự đặc biệt
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_AUTH_REG_007 |
| **Tên test case** | Đăng ký thành công với mật khẩu chứa ký tự đặc biệt |
| **Module** | Authentication |
| **Tính năng** | Đăng ký tài khoản |
| **Ưu tiên** | Medium |
| **Severity** | Medium |
| **Loại test** | Validation - Security |
| **Điều kiện tiên quyết** | - Trình duyệt được mở<br>- Trang đăng ký có thể truy cập |
| **Bước thực thi** | 1. Truy cập trang đăng ký<br>2. Nhập email: special@gmail.com<br>3. Nhập mật khẩu: P@ss!#2026<br>4. Nhập xác nhận mật khẩu: P@ss!#2026<br>5. Click nút "Đăng ký" |
| **Kết quả mong đợi** | - Đăng ký thành công<br>- Hiển thị thông báo "Đăng ký thành công"<br>- Mật khẩu được mã hoá và lưu trữ an toàn<br>- Chuyển hướng đến trang đăng nhập |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 06/03/2026 |
| **Tester** | QA Engineer 2 |

---

### TC_AUTH_LOGIN_004 - Đánh giá khả năng chống SQL Injection trên trường email
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_AUTH_LOGIN_004 |
| **Tên test case** | Đánh giá khả năng chống SQL Injection trên trường email |
| **Module** | Authentication |
| **Tính năng** | Đăng nhập |
| **Ưu tiên** | High |
| **Severity** | Critical |
| **Loại test** | Negative - Security |
| **Điều kiện tiên quyết** | - Trình duyệt được mở<br>- Trang đăng nhập có thể truy cập |
| **Bước thực thi** | 1. Truy cập trang đăng nhập<br>2. Nhập email: ' OR '1'='1<br>3. Nhập mật khẩu: anything<br>4. Click nút "Đăng nhập" |
| **Kết quả mong đợi** | - Đăng nhập thất bại<br>- Hiển thị lỗi: "Email hoặc mật khẩu không chính xác"<br>- SQL Injection bị chặn<br>- Trong log không có lỗi database |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 06/03/2026 |
| **Tester** | QA Engineer 2 |

---

### TC_AUTH_LOGIN_005 - Không đăng nhập khi để trống email
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_AUTH_LOGIN_005 |
| **Tên test case** | Không đăng nhập khi để trống email |
| **Module** | Authentication |
| **Tính năng** | Đăng nhập |
| **Ưu tiên** | Medium |
| **Severity** | Medium |
| **Loại test** | Negative - Boundary |
| **Điều kiện tiên quyết** | - Trình duyệt được mở<br>- Trang đăng nhập có thể truy cập |
| **Bước thực thi** | 1. Truy cập trang đăng nhập<br>2. Để trống trường email<br>3. Nhập mật khẩu: Test@1234<br>4. Click nút "Đăng nhập" |
| **Kết quả mong đợi** | - Đăng nhập thất bại<br>- Hiển thị lỗi: "Email là bắt buộc"<br>- Vẫn ở trang đăng nhập |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 06/03/2026 |
| **Tester** | QA Engineer 1 |

---

### TC_AUTH_FP_002 - Không được phép đặt lại mật khẩu với email không hợp lệ
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_AUTH_FP_002 |
| **Tên test case** | Không được phép đặt lại mật khẩu với email không hợp lệ |
| **Module** | Authentication |
| **Tính năng** | Quên mật khẩu |
| **Ưu tiên** | Medium |
| **Severity** | Medium |
| **Loại test** | Negative - Validation |
| **Điều kiện tiên quyết** | - Trình duyệt được mở<br>- Trang quên mật khẩu có thể truy cập |
| **Bước thực thi** | 1. Click "Quên mật khẩu" trên trang đăng nhập<br>2. Truy cập trang đặt lại mật khẩu<br>3. Nhập email không hợp lệ: invalidemail<br>4. Click nút "Gửi" |
| **Kết quả mong đợi** | - Không gửi email<br>- Hiển thị lỗi: "Email không hợp lệ"<br>- Vẫn ở trang quên mật khẩu |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 06/03/2026 |
| **Tester** | QA Engineer 2 |

---

### TC_AUTH_SESSION_001 - Session hết hạn sau 30 phút không hoạt động
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_AUTH_SESSION_001 |
| **Tên test case** | Session hết hạn sau 30 phút không hoạt động |
| **Module** | Authentication |
| **Tính năng** | Quản lý session |
| **Ưu tiên** | Medium |
| **Severity** | High |
| **Loại test** | Validation - Security |
| **Điều kiện tiên quyết** | - Người dùng đã đăng nhập<br>- Có thể kiểm soát thời gian hệ thống để test |
| **Bước thực thi** | 1. Đăng nhập hệ thống<br>2. Chuyển hướng thời gian hệ thống đi 31 phút<br>3. Thực hiện hành động bất kỳ (click button, refresh trang)<br>4. Quan sát kết quả |
| **Kết quả mong đợi** | - Session bị hủy sau 30 phút<br>- Người dùng bị chuyển hướng đến trang đăng nhập<br>- Hiển thị thông báo: "Session của bạn đã hết hạn"<br>- Phải đăng nhập lại |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 06/03/2026 |
| **Tester** | QA Engineer 2 |

---

**END OF TEST CASES - MODULE 1 (15 TOTAL)**
