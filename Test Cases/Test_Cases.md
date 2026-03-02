# CA KIỂM THỬ TỔNG HỢP (CONSOLIDATED TEST CASES)

**Phiên bản:** 1.0  
**Ngày tạo:** 03/03/2026  
**Tác giả:** QA Team  
**Ghi chú:** Tổng hợp từ 3 module: Authentication, Product & Cart, Checkout

---

## MODULE 1: XÁC THỰC NGƯỜI DÙNG (AUTHENTICATION)

### TC_AUTH_REG_001
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_REG_001 |
| **Tiêu đề (Title)** | Đăng ký thành công với email và mật khẩu hợp lệ |
| **Điều kiện trước (Precondition)** | - Trình duyệt được mở<br>- Trang đăng ký có thể truy cập |
| **Các bước (Steps)** | 1. Truy cập trang đăng ký<br>2. Nhập email: test@gmail.com<br>3. Nhập mật khẩu: Test@1234<br>4. Nhập xác nhận mật khẩu: Test@1234<br>5. Click nút "Đăng ký" |
| **Kết quả mong đợi (Expected Result)** | - Đăng ký thành công<br>- Hiển thị thông báo "Đăng ký thành công"<br>- Chuyển hướng đến trang đăng nhập<br>- Email được lưu trong hệ thống |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---

### TC_AUTH_REG_002
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_REG_002 |
| **Tiêu đề (Title)** | Không đăng ký khi email sai định dạng |
| **Điều kiện trước (Precondition)** | - Trình duyệt được mở<br>- Trang đăng ký có thể truy cập |
| **Các bước (Steps)** | 1. Truy cập trang đăng ký<br>2. Nhập email: invalidemail (không có @)<br>3. Nhập mật khẩu: Test@1234<br>4. Nhập xác nhận mật khẩu: Test@1234<br>5. Click nút "Đăng ký" |
| **Kết quả mong đợi (Expected Result)** | - Không xảy ra đăng ký<br>- Hiển thị lỗi: "Email không hợp lệ"<br>- Vẫn ở trang đăng ký |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Negative |

---

### TC_AUTH_REG_003
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_REG_003 |
| **Tiêu đề (Title)** | Không đăng ký khi mật khẩu dưới 8 ký tự |
| **Điều kiện trước (Precondition)** | - Trình duyệt được mở<br>- Trang đăng ký có thể truy cập |
| **Các bước (Steps)** | 1. Truy cập trang đăng ký<br>2. Nhập email: test@gmail.com<br>3. Nhập mật khẩu: Test123 (7 ký tự)<br>4. Nhập xác nhận mật khẩu: Test123<br>5. Click nút "Đăng ký" |
| **Kết quả mong đợi (Expected Result)** | - Không xảy ra đăng ký<br>- Hiển thị lỗi: "Mật khẩu tối thiểu 8 ký tự"<br>- Vẫn ở trang đăng ký |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Boundary |

---

### TC_AUTH_REG_004
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_REG_004 |
| **Tiêu đề (Title)** | Không đăng ký khi email đã tồn tại |
| **Điều kiện trước (Precondition)** | - Trình duyệt được mở<br>- Trang đăng ký có thể truy cập<br>- Email "existing@gmail.com" đã tồn tại |
| **Các bước (Steps)** | 1. Truy cập trang đăng ký<br>2. Nhập email: existing@gmail.com<br>3. Nhập mật khẩu: Test@1234<br>4. Nhập xác nhận mật khẩu: Test@1234<br>5. Click nút "Đăng ký" |
| **Kết quả mong đợi (Expected Result)** | - Không xảy ra đăng ký<br>- Hiển thị lỗi: "Email đã tồn tại"<br>- Vẫn ở trang đăng ký |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Negative |

---

### TC_AUTH_REG_005
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_REG_005 |
| **Tiêu đề (Title)** | Không đăng ký khi email trống |
| **Điều kiện trước (Precondition)** | - Trình duyệt được mở<br>- Trang đăng ký có thể truy cập |
| **Các bước (Steps)** | 1. Truy cập trang đăng ký<br>2. Để trống trường email<br>3. Nhập mật khẩu: Test@1234<br>4. Nhập xác nhận mật khẩu: Test@1234<br>5. Click nút "Đăng ký" |
| **Kết quả mong đợi (Expected Result)** | - Không xảy ra đăng ký<br>- Hiển thị lỗi: "Email là bắt buộc"<br>- Vẫn ở trang đăng ký |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Negative - Boundary |

---
### TC_AUTH_REG_006
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_REG_006 |
| **Tiêu đề (Title)** | Không đăng ký khi mật khẩu trống |
| **Điều kiện trước (Precondition)** | Browser opened, Registration page accessible |
| **Các bước (Steps)** | 1. Truy cập trang đăng ký<br>2. Nhập email: test@gmail.com<br>3. Để trống mật khẩu<br>4. Click "Đăng ký" |
| **Kết quả mong đợi (Expected Result)** | - Lỗi: "Mật khẩu là bắt buộc"<br>- Vẫn ở trang đăng ký |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Boundary |

---

### TC_AUTH_REG_007
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_REG_007 |
| **Tiêu đề (Title)** | Đăng ký thành công với mật khẩu ký tự đặc biệt |
| **Điều kiện trước (Precondition)** | Browser opened, Registration page accessible |
| **Các bước (Steps)** | 1. Truy cập trang đăng ký<br>2. Nhập email: special@gmail.com<br>3. Nhập mật khẩu: P@ss!#2026<br>4. Click "Đăng ký" |
| **Kết quả mong đợi (Expected Result)** | - Đăng ký thành công<br>- Mật khẩu được mã hoá an toàn |
| **Độ ưu tiên (Priority)** | Medium |
| **Loại test (Type)** | Validation/Security |


### TC_AUTH_LOGIN_001
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_LOGIN_001 |
| **Tiêu đề (Title)** | Đăng nhập thành công với email và mật khẩu hợp lệ |
| **Điều kiện trước (Precondition)** | - Trình duyệt được mở<br>- Trang đăng nhập có thể truy cập<br>- Tài khoản test@gmail.com / Test@1234 đã tồn tại |
| **Các bước (Steps)** | 1. Truy cập trang đăng nhập<br>2. Nhập email: test@gmail.com<br>3. Nhập mật khẩu: Test@1234<br>4. Click nút "Đăng nhập" |
| **Kết quả mong đợi (Expected Result)** | - Đăng nhập thành công<br>- Chuyển hướng đến trang chủ (Dashboard)<br>- Hiển thị tên người dùng ở góc phải<br>- Session được tạo |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---

### TC_AUTH_LOGIN_002
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_LOGIN_002 |
| **Tiêu đề (Title)** | Đăng nhập thất bại khi sai mật khẩu |
| **Điều kiện trước (Precondition)** | - Trình duyệt được mở<br>- Trang đăng nhập có thể truy cập<br>- Tài khoản test@gmail.com tồn tại |
| **Các bước (Steps)** | 1. Truy cập trang đăng nhập<br>2. Nhập email: test@gmail.com<br>3. Nhập mật khẩu: WrongPassword<br>4. Click nút "Đăng nhập" |
| **Kết quả mong đợi (Expected Result)** | - Đăng nhập thất bại<br>- Hiển thị lỗi: "Email hoặc mật khẩu không chính xác"<br>- Vẫn ở trang đăng nhập |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Negative |

---

### TC_AUTH_LOGIN_003
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_LOGIN_003 |
| **Tiêu đề (Title)** | Đăng nhập thất bại khi email không tồn tại |
| **Điều kiện trước (Precondition)** | - Trình duyệt được mở<br>- Trang đăng nhập có thể truy cập |
| **Các bước (Steps)** | 1. Truy cập trang đăng nhập<br>2. Nhập email: nonexistent@gmail.com<br>3. Nhập mật khẩu: Test@1234<br>4. Click nút "Đăng nhập" |
| **Kết quả mong đợi (Expected Result)** | - Đăng nhập thất bại<br>- Hiển thị lỗi: "Email hoặc mật khẩu không chính xác"<br>- Vẫn ở trang đăng nhập |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Negative |

---
### TC_AUTH_LOGIN_004
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_LOGIN_004 |
| **Tiêu đề (Title)** | Chống SQL Injection trên trường email |
| **Điều kiện trước (Precondition)** | Browser opened, Login page accessible |
| **Các bước (Steps)** | 1. Truy cập trang đăng nhập<br>2. Nhập email: ' OR '1'='1<br>3. Nhập mật khẩu: anything<br>4. Click "Đăng nhập" |
| **Kết quả mong đợi (Expected Result)** | - Đăng nhập thất bại<br>- Lỗi: "Email hoặc mật khẩu không chính xác"<br>- SQL Injection bị chặn<br>- Không có lỗi database |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Validation/Security |

---

### TC_AUTH_LOGIN_005
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_LOGIN_005 |
| **Tiêu đề (Title)** | Không đăng nhập khi để trống email |
| **Điều kiện trước (Precondition)** | Browser opened, Login page accessible |
| **Các bước (Steps)** | 1. Truy cập trang đăng nhập<br>2. Để trống email<br>3. Nhập mật khẩu: Test@1234<br>4. Click "Đăng nhập" |
| **Kết quả mong đợi (Expected Result)** | - Lỗi: "Email là bắt buộc"<br>- Vẫn ở trang đăng nhập |
| **Độ ưu tiên (Priority)** | Medium |
| **Loại test (Type)** | Boundary |


### TC_AUTH_FP_001
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_FP_001 |
| **Tiêu đề (Title)** | Gửi email đặt lại mật khẩu thành công |
| **Điều kiện trước (Precondition)** | - Trình duyệt được mở<br>- Trang quên mật khẩu có thể truy cập<br>- Email test@gmail.com tồn tại |
| **Các bước (Steps)** | 1. Click "Quên mật khẩu" trên trang đăng nhập<br>2. Truy cập trang đặt lại mật khẩu<br>3. Nhập email: test@gmail.com<br>4. Click nút "Gửi" |
| **Kết quả mong đợi (Expected Result)** | - Hiển thị thông báo thành công<br>- Email được gửi tới test@gmail.com<br>- Email chứa link đặt lại mật khẩu |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---
### TC_AUTH_FP_002
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_FP_002 |
| **Tiêu đề (Title)** | Không gửi email với email không hợp lệ |
| **Điều kiện trước (Precondition)** | Browser opened, Forgot password page accessible |
| **Các bước (Steps)** | 1. Click "Quên mật khẩu"<br>2. Nhập email: invalidemail<br>3. Click "Gửi" |
| **Kết quả mong đợi (Expected Result)** | - Không gửi email<br>- Lỗi: "Email không hợp lệ"<br>- Vẫn ở trang quên mật khẩu |
| **Độ ưu tiên (Priority)** | Medium |
| **Loại test (Type)** | Negative |

---

### TC_AUTH_LOGOUT_001
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_LOGOUT_001 |
| **Tiêu đề (Title)** | Đăng xuất thành công |
| **Điều kiện trước (Precondition)** | - Người dùng đã đăng nhập thành công |
| **Các bước (Steps)** | 1. Đăng nhập hệ thống<br>2. Click vào menu người dùng ở góc phải<br>3. Click "Đăng xuất" |
| **Kết quả mong đợi (Expected Result)** | - Đăng xuất thành công<br>- Chuyển hướng đến trang đăng nhập<br>- Session bị xoá<br>- Không thể quay lại Dashboard |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---

## MODULE 2: SẢN PHẨM & GIỎ HÀNG (PRODUCT & CART)

### TC_PROD_SEARCH_001
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PROD_SEARCH_001 |
| **Tiêu đề (Title)** | Tìm kiếm hiển thị đúng kết quả |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Ở trang sản phẩm |
| **Các bước (Steps)** | 1. Truy cập trang sản phẩm<br>2. Nhập từ khóa "iphone" vào ô tìm kiếm<br>3. Nhấn Enter hoặc click nút "Tìm kiếm" |
| **Kết quả mong đợi (Expected Result)** | - Hiển thị danh sách sản phẩm chứa "iphone"<br>- Kết quả có liên quan đến từ khóa<br>- Số lượng sản phẩm được hiển thị |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---

### TC_PROD_SEARCH_002
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PROD_SEARCH_002 |
| **Tiêu đề (Title)** | Tìm kiếm không trả về kết quả |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Ở trang sản phẩm |
| **Các bước (Steps)** | 1. Truy cập trang sản phẩm<br>2. Nhập từ khóa "xyzabc123" (không tồn tại)<br>3. Nhấn Enter |
| **Kết quả mong đợi (Expected Result)** | - Không hiển thị sản phẩm<br>- Hiển thị thông báo "Không tìm thấy sản phẩm" |
| **Độ ưu tiên (Priority)** | Medium |
| **Loại test (Type)** | Negative |

---

### TC_PROD_SEARCH_003
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PROD_SEARCH_003 |
| **Tiêu đề (Title)** | Tìm kiếm với ký tự đặc biệt |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Ở trang sản phẩm |
| **Các bước (Steps)** | 1. Truy cập trang sản phẩm<br>2. Nhập ký tự đặc biệt: @#$%^&*<br>3. Nhấn Enter |
| **Kết quả mong đợi (Expected Result)** | - Không gây lỗi hệ thống<br>- Hiển thị thông báo: "Từ khóa không hợp lệ"<br>- Hoặc không trả về kết quả |
| **Độ ưu tiên (Priority)** | Medium |
| **Loại test (Type)** | Negative - Boundary |

---

### TC_PROD_SEARCH_004
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PROD_SEARCH_004 |
| **Tiêu đề (Title)** | Tìm kiếm với tập dữ liệu lớn |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Database có 10000+ sản phẩm |
| **Các bước (Steps)** | 1. Truy cập trang sản phẩm<br>2. Nhập từ khóa phổ biến: "phone"<br>3. Quan sát thời gian tải kết quả |
| **Kết quả mong đợi (Expected Result)** | - Kết quả được hiển thị trong < 3 giây<br>- Hiển thị phân trang để dễ quản lý<br>- Tất cả sản phẩm liên quan được hiển thị |
| **Độ ưu tiên (Priority)** | Medium |
| **Loại test (Type)** | Boundary |

---

### TC_PROD_FILTER_001
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PROD_FILTER_001 |
| **Tiêu đề (Title)** | Lọc theo giá hoạt động đúng |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Ở trang sản phẩm<br>- Có sản phẩm với giá khác nhau |
| **Các bước (Steps)** | 1. Truy cập trang sản phẩm<br>2. Click vào mục "Lọc theo giá"<br>3. Chọn khoảng: 1.000.000 - 5.000.000 VNĐ<br>4. Click "Lọc" |
| **Kết quả mong đợi (Expected Result)** | - Hiển thị chỉ sản phẩm trong khoảng giá<br>- Giá sản phẩm nằm trong 1-5 triệu<br>- Số lượng sản phẩm giảm |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---

### TC_PROD_FILTER_002
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PROD_FILTER_002 |
| **Tiêu đề (Title)** | Lọc theo danh mục hoạt động đúng |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Ở trang sản phẩm<br>- Có nhiều danh mục sản phẩm |
| **Các bước (Steps)** | 1. Truy cập trang sản phẩm<br>2. Click vào mục "Danh mục"<br>3. Chọn "Điện thoại" |
| **Kết quả mong đợi (Expected Result)** | - Hiển thị chỉ sản phẩm danh mục "Điện thoại"<br>- Số lượng sản phẩm giảm<br>- Tất cả sản phẩm đều là điện thoại |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---

### TC_PROD_FILTER_003
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PROD_FILTER_003 |
| **Tiêu đề (Title)** | Lọc theo nhiều tiêu chí cùng lúc |
| **Điều kiện trước (Precondition)** | User logged in, On product page |
| **Các bước (Steps)** | 1. Lọc giá: 1M - 5M<br>2. Lọc danh mục: Điện thoại<br>3. Lọc thương hiệu: Apple<br>4. Click Apply |
| **Kết quả mong đợi (Expected Result)** | - Sản phẩm thỏa mãn cả 3 tiêu chí<br>- Số lượng giảm so với không lọc |
| **Độ ưu tiên (Priority)** | Medium |
| **Loại test (Type)** | Validation/Security |

---

### TC_PROD_FILTER_004
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PROD_FILTER_004 |
| **Tiêu đề (Title)** | Lọc với giá trị không hợp lệ |
| **Điều kiện trước (Precondition)** | User logged in, On product page |
| **Các bước (Steps)** | 1. Cố gắng nhập giá tối thiểu: -1000<br>2. Cố gắng nhập giá tối đa: 99999999<br>3. Click Apply |
| **Kết quả mong đợi (Expected Result)** | - Hiển thị lỗi<br>- Filter không áp dụng<br>- Hoặc tự động hiệu chỉnh |
| **Độ ưu tiên (Priority)** | Medium |
| **Loại test (Type)** | Negative |

---

### TC_PROD_DETAIL_001
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PROD_DETAIL_001 |
| **Tiêu đề (Title)** | Xem chi tiết sản phẩm thành công |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Ở trang sản phẩm<br>- Có sản phẩm trong danh sách |
| **Các bước (Steps)** | 1. Truy cập trang sản phẩm<br>2. Click vào sản phẩm "iPhone 15" |
| **Kết quả mong đợi (Expected Result)** | - Chuyển đến trang chi tiết sản phẩm<br>- Hiển thị: Tên, giá, mô tả, hình ảnh<br>- Nút "Thêm vào giỏ" có sẵn |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---

### TC_PROD_DETAIL_002
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PROD_DETAIL_002 |
| **Tiêu đề (Title)** | Hiển thị hình ảnh sản phẩm |
| **Điều kiện trước (Precondition)** | User logged in, Product detail page with images |
| **Các bước (Steps)** | 1. Xem hình ảnh sản phẩm<br>2. Click thumbnail khác nhau<br>3. Thử zoom |
| **Kết quả mong đợi (Expected Result)** | - Hình ảnh hiển thị đúng<br>- Zoom hoặc fullscreen hoạt động |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---

### TC_PROD_DETAIL_003
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PROD_DETAIL_003 |
| **Tiêu đề (Title)** | Hiển thị trạng thái tồn kho sản phẩm |
| **Điều kiện trước (Precondition)** | In-stock and out-of-stock products available |
| **Các bước (Steps)** | 1. Xem sản phẩm có hàng<br>2. Xem sản phẩm hết hàng |
| **Kết quả mong đợi (Expected Result)** | - Còn hàng: Số lượng<br>- Hết hàng: Nút "Thông báo" |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Boundary |

---

### TC_CART_ADD_001
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_ADD_001 |
| **Tiêu đề (Title)** | Thêm sản phẩm vào giỏ thành công |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Ở trang chi tiết sản phẩm |
| **Các bước (Steps)** | 1. Ở trang chi tiết sản phẩm "iPhone 15"<br>2. Chọn số lượng: 1<br>3. Click "Thêm vào giỏ" |
| **Kết quả mong đợi (Expected Result)** | - Sản phẩm được thêm vào giỏ<br>- Hiển thị thông báo thành công<br>- Số lượng giỏ hàng tăng |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---

### TC_CART_ADD_002
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_ADD_002 |
| **Tiêu đề (Title)** | Không thêm sản phẩm hết hàng vào giỏ |
| **Điều kiện trước (Precondition)** | Out-of-stock product page |
| **Các bước (Steps)** | 1. Tìm sản phẩm hết hàng<br>2. Click "Thêm vào giỏ" |
| **Kết quả mong đợi (Expected Result)** | - Nút bị vô hiệu hoá<br>- Hoặc lỗi "Hết hàng"<br>- Sản phẩm không được thêm |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Negative |

---

### TC_CART_ADD_003
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_ADD_003 |
| **Tiêu đề (Title)** | Không thêm số lượng âm vào giỏ |
| **Điều kiện trước (Precondition)** | User on product detail page |
| **Các bước (Steps)** | 1. Cố gắng nhập số lượng: -5<br>2. Click "Thêm vào giỏ" |
| **Kết quả mong đợi (Expected Result)** | - Không cho phép âm<br>- Lỗi "Số lượng > 0"<br>- Sản phẩm không được thêm |
| **Độ ưu tiên (Priority)** | Medium |
| **Loại test (Type)** | Negative |

---

### TC_CART_UPDATE_001
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_UPDATE_001 |
| **Tiêu đề (Title)** | Cập nhật số lượng sản phẩm trong giỏ |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Giỏ hàng có sản phẩm |
| **Các bước (Steps)** | 1. Truy cập giỏ hàng<br>2. Tìm sản phẩm "iPhone 15"<br>3. Thay đổi số lượng từ 1 → 3 |
| **Kết quả mong đợi (Expected Result)** | - Số lượng được cập nhật thành 3<br>- Tổng giá cập nhật đúng<br>- Không có lỗi |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---

### TC_CART_UPDATE_002
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_UPDATE_002 |
| **Tiêu đề (Title)** | Cập nhật số lượng về 0 xoá sản phẩm |
| **Điều kiện trước (Precondition)** | Cart has products |
| **Các bước (Steps)** | 1. Mở giỏ hàng<br>2. Đổi số lượng về 0<br>3. Nhấn Enter |
| **Kết quả mong đợi (Expected Result)** | - Sản phẩm bị xoá<br>- Thông báo xác nhận<br>- Tổng giá cập nhật |
| **Độ ưu tiên (Priority)** | Medium |
| **Loại test (Type)** | Boundary |

---

### TC_CART_DELETE_001
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_DELETE_001 |
| **Tiêu đề (Title)** | Xoá sản phẩm khỏi giỏ thành công |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Giỏ hàng có sản phẩm |
| **Các bước (Steps)** | 1. Truy cập giỏ hàng<br>2. Tìm sản phẩm "iPhone 15"<br>3. Click nút "Xoá" |
| **Kết quả mong đợi (Expected Result)** | - Sản phẩm bị xoá khỏi giỏ<br>- Hiển thị thông báo xác nhận<br>- Tổng giá được cập nhật |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---

### TC_CART_DELETE_002
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_DELETE_002 |
| **Tiêu đề (Title)** | Xoá tất cả sản phẩm khỏi giỏ |
| **Điều kiện trước (Precondition)** | Cart has multiple products |
| **Các bước (Steps)** | 1. Xoá từng sản phẩm<br>2. Xoá cho đến khi trống |
| **Kết quả mong đợi (Expected Result)** | - Tất cả xoá<br>- Giỏ trống<br>- Thông báo "Giỏ trống" |
| **Độ ưu tiên (Priority)** | Medium |
| **Loại test (Type)** | Boundary |

---

### TC_CART_PERSIST_001
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_PERSIST_001 |
| **Tiêu đề (Title)** | Giỏ hàng được lưu sau khi đăng xuất |
| **Điều kiện trước (Precondition)** | User logged in, Products in cart |
| **Các bước (Steps)** | 1. Thêm 3 sản phẩm<br>2. Ghi lại số lượng<br>3. Đăng xuất<br>4. Đăng nhập lại<br>5. Kiểm tra giỏ |
| **Kết quả mong đợi (Expected Result)** | - Giỏ vẫn có 3 sản phẩm<br>- Dữ liệu không thay đổi<br>- Lưu trữ an toàn |
| **Độ ưu tiên (Priority)** | Medium |
| **Loại test (Type)** | Validation/Security |

---

### TC_CART_TOTAL_001
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_TOTAL_001 |
| **Tiêu đề (Title)** | Tính tổng giỏ hàng chính xác |
| **Điều kiện trước (Precondition)** | Empty cart |
| **Các bước (Steps)** | 1. Thêm A: 2M (qty 2)<br>2. Thêm B: 1.5M (qty 1)<br>3. Kiểm tra tổng |
| **Kết quả mong đợi (Expected Result)** | - Tổng = 5.5M<br>- Chính xác không làm tròn sai |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Validation/Security |

---

## MODULE 3: THANH TOÁN (CHECKOUT)

### TC_CHK_ADDRESS_001
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHK_ADDRESS_001 |
| **Tiêu đề (Title)** | Thanh toán bắt buộc nhập địa chỉ |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Giỏ hàng có sản phẩm<br>- Ở trang thanh toán |
| **Các bước (Steps)** | 1. Truy cập giỏ hàng<br>2. Click "Thanh toán"<br>3. Bỏ qua nhập địa chỉ<br>4. Click "Tiếp tục" |
| **Kết quả mong đợi (Expected Result)** | - Không thể tiếp tục<br>- Hiển thị lỗi: "Vui lòng nhập địa chỉ giao hàng"<br>- Vẫn ở trang thanh toán |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Negative |

---

### TC_CHK_ADDRESS_002
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHK_ADDRESS_002 |
| **Tiêu đề (Title)** | Nhập địa chỉ giao hàng thành công |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Giỏ hàng có sản phẩm<br>- Ở trang thanh toán |
| **Các bước (Steps)** | 1. Truy cập giỏ hàng<br>2. Click "Thanh toán"<br>3. Nhập địa chỉ: 123 Nguyễn Huệ, Q1, HCM<br>4. Click "Tiếp tục" |
| **Kết quả mong đợi (Expected Result)** | - Địa chỉ được lưu<br>- Chuyển đến bước chọn phương thức thanh toán<br>- Không có lỗi |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---

### TC_CHK_ADDRESS_003
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHK_ADDRESS_003 |
| **Tiêu đề (Title)** | Kiểm tra định dạng địa chỉ |
| **Điều kiện trước (Precondition)** | On address entry page |
| **Các bước (Steps)** | 1. Nhập địa chỉ không hợp lệ<br>2. Click "Tiếp tục" |
| **Kết quả mong đợi (Expected Result)** | - Lỗi validation<br>- Hoặc tự động hiệu chỉnh |
| **Độ ưu tiên (Priority)** | Medium |
| **Loại test (Type)** | Boundary |

---

### TC_CHK_PAYMENT_001
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHK_PAYMENT_001 |
| **Tiêu đề (Title)** | Chọn phương thức thanh toán COD thành công |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Đã nhập địa chỉ giao hàng<br>- Ở trang chọn phương thức thanh toán |
| **Các bước (Steps)** | 1. Ở trang thanh toán (bước 2)<br>2. Chọn "Thanh toán khi nhận (COD)"<br>3. Click "Tiếp tục" |
| **Kết quả mong đợi (Expected Result)** | - Phương thức COD được chọn<br>- Chuyển đến trang xác nhận đơn hàng |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---

### TC_CHK_PAYMENT_002
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHK_PAYMENT_002 |
| **Tiêu đề (Title)** | Chọn phương thức thanh toán Visa thành công |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Đã nhập địa chỉ giao hàng<br>- Ở trang chọn phương thức thanh toán |
| **Các bước (Steps)** | 1. Ở trang thanh toán (bước 2)<br>2. Chọn "Thanh toán bằng Visa"<br>3. Nhập số thẻ: 4111111111111111<br>4. Nhập ngày hết hạn: 12/25<br>5. Nhập CVV: 123<br>6. Click "Tiếp tục" |
| **Kết quả mong đợi (Expected Result)** | - Thanh toán bằng Visa được xử lý<br>- Chuyển đến trang xác nhận đơn hàng |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---

### TC_CHK_ORDER_001
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHK_ORDER_001 |
| **Tiêu đề (Title)** | Đặt hàng thành công |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Đã nhập địa chỉ<br>- Đã chọn phương thức thanh toán<br>- Ở trang xác nhận đơn hàng |
| **Các bước (Steps)** | 1. Ở trang xác nhận đơn hàng<br>2. Reviewed thông tin:<br>   - Sản phẩm: iPhone 15 x 2<br>   - Địa chỉ: 123 Nguyễn Huệ<br>   - Phương thức: COD<br>3. Click "Đặt hàng" |
| **Kết quả mong đợi (Expected Result)** | - Đơn hàng được tạo thành công<br>- Hiển thị mã đơn hàng (Order ID)<br>- Email xác nhận được gửi<br>- Chuyển đến trang thành công |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---

### TC_CHK_ORDER_002
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHK_ORDER_002 |
| **Tiêu đề (Title)** | Đặt hàng thất bại khi thiếu thông tin |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Ở trang thanh toán |
| **Các bước (Steps)** | 1. Ở trang thanh toán<br>2. Bỏ qua các trường bắt buộc<br>3. Click "Đặt hàng" |
| **Kết quả mong đợi (Expected Result)** | - Đặt hàng thất bại<br>- Hiển thị lỗi về thông tin thiếu |
| **Độ ưu tiên (Priority)** | Medium |
| **Loại test (Type)** | Negative |

---

### TC_CHK_HISTORY_001
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHK_HISTORY_001 |
| **Tiêu đề (Title)** | Xem lịch sử đơn hàng thành công |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Có ít nhất 1 đơn hàng |
| **Các bước (Steps)** | 1. Click vào menu người dùng<br>2. Click "Lịch sử đơn hàng"<br>3. Xem danh sách đơn hàng |
| **Kết quả mong đợi (Expected Result)** | - Hiển thị danh sách đơn hàng<br>- Mỗi đơn hàng hiển thị:<br>  - Mã đơn hàng<br>  - Ngày đặt<br>  - Tổng giá<br>  - Trạng thái |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---

### TC_CHK_HISTORY_002
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHK_HISTORY_002 |
| **Tiêu đề (Title)** | Xem chi tiết đơn hàng |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Ở trang lịch sử đơn hàng |
| **Các bước (Steps)** | 1. Ở trang lịch sử đơn hàng<br>2. Click vào một đơn hàng |
| **Kết quả mong đợi (Expected Result)** | - Hiển thị chi tiết đơn hàng:<br>  - Mã đơn hàng<br>  - Danh sách sản phẩm<br>  - Địa chỉ giao hàng<br>  - Phương thức thanh toán<br>  - Trạng thái vận chuyển |
| **Độ ưu tiên (Priority)** | High |
| **Loại test (Type)** | Positive |

---

### TC_CHK_DISCOUNT_001
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHK_DISCOUNT_001 |
| **Tiêu đề (Title)** | Áp dụng mã khuyến mãi hợp lệ |
| **Điều kiện trước (Precondition)** | - Đã đăng nhập<br>- Giỏ hàng có sản phẩm (5.000.000 đ)<br>- Mã "SAVE10" hợp lệ giảm 10% |
| **Các bước (Steps)** | 1. Truy cập giỏ hàng<br>2. Nhập mã khuyến mãi: SAVE10<br>3. Click "Áp dụng"<br>4. Xem tổng giỏ hàng |
| **Kết quả mong đợi (Expected Result)** | - Mã được áp dụng thành công<br>- Tổng giảm từ 5.000.000 đ → 4.500.000 đ<br>- Hiển thị tiền tiết kiệm: 500.000 đ<br>- Có thể xoá mã nếu muốn |
| **Độ ưu tiên (Priority)** | Medium |
| **Loại test (Type)** | Positive |

---

## TỔNG KẾT

**Tổng số Test Case:** 30  
**Phân bố theo Module:**
- Module 1 (Authentication): 9 test case
- Module 2 (Product & Cart): 10 test case
- Module 3 (Checkout): 11 test case

**Phân bố theo Độ ưu tiên:**
- High: 24 test case
- Medium: 6 test case

**Phân bố theo Loại test:**
- Positive: 15 test case
- Negative: 10 test case
- Boundary: 5 test case