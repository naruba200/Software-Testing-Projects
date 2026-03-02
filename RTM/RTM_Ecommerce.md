# MA TRẬN TRUY VẾT YÊU CẦU (RTM - REQUIREMENT TRACEABILITY MATRIX)

**Phiên bản:** 1.0  
**Ngày tạo:** 04/03/2026  
**Tác giả:** QA Team  
**Hệ thống:** Website Bán Hàng Online (Ecommerce)

---

## 1. GIỚI THIỆU

Ma trận truy vết yêu cầu (RTM) là tài liệu quan trọng đảm bảo rằng:
- Mỗi yêu cầu (Requirement) được thiết kế thành Test Case
- Mỗi Test Case liên kết với yêu cầu cụ thể
- Không có yêu cầu nào bị sót hoặc bỏ qua
- Tất cả các lỗi được ghi nhận và truy vết về yêu cầu

---

## 2. RTM - DANH SÁCH YÊU CẦU & TEST CASE

### MODULE 1: AUTHENTICATION (Xác thực người dùng)

| Req ID | Yêu cầu (Requirement) | TC ID | Test Case Name | Status | Coverage | Notes |
|--------|--------|-------|--------|--------|----------|-------|
| R1 | Người dùng đăng ký bằng email hợp lệ | TC_AUTH_REG_001 | Đăng ký thành công với email và mật khẩu hợp lệ | ✅ PASS | 100% | Email verification cần kiểm thử thêm |
| R2 | Không cho đăng ký khi email sai định dạng | TC_AUTH_REG_002 | Không đăng ký khi email sai định dạng | ✅ PASS | 100% | Các trường hợp email sai: @, dấu cách, ký tự đặc biệt |
| R3 | Mật khẩu tối thiểu 8 ký tự | TC_AUTH_REG_003 | Không đăng ký khi mật khẩu dưới 8 ký tự | ✅ PASS | 100% | Cần test mật khẩu 1-7 ký tự |
| R3 | Mật khẩu tối thiểu 8 ký tự | TC_AUTH_REG_001 | Đăng ký thành công với email và mật khẩu hợp lệ | ✅ PASS | 50% | Coverage riêng phần mật khẩu |
| R4 | Đăng nhập thành công với thông tin hợp lệ | TC_AUTH_LOGIN_001 | Đăng nhập thành công với email và mật khẩu hợp lệ | ✅ PASS | 100% | Session được tạo đúng |
| R5 | Đăng nhập thất bại khi sai mật khẩu | TC_AUTH_LOGIN_002 | Đăng nhập thất bại khi sai mật khẩu | ✅ PASS | 100% | Ghi nhật ký attempt failed |
| R5 | Đăng nhập thất bại khi sai mật khẩu | TC_AUTH_LOGIN_003 | Đăng nhập thất bại khi email không tồn tại | ✅ PASS | 50% | Cần test email sai format |
| R6 | Quên mật khẩu gửi email đặt lại | TC_AUTH_FP_001 | Gửi email đặt lại mật khẩu thành công | ✅ PASS | 100% | Email phải có token hợp lệ |

---

### MODULE 2: PRODUCT & CART (Sản phẩm & Giỏ hàng)

| Req ID | Yêu cầu (Requirement) | TC ID | Test Case Name | Status | Coverage | Notes |
|--------|--------|-------|--------|--------|----------|-------|
| R7 | Tìm kiếm hiển thị đúng kết quả | TC_PROD_SEARCH_001 | Tìm kiếm hiển thị đúng kết quả | ✅ PASS | 100% | Test case-sensitive search |
| R7 | Tìm kiếm hiển thị đúng kết quả | TC_PROD_SEARCH_002 | Tìm kiếm không trả về kết quả | ✅ PASS | 50% | Khi keyword không tồn tại |
| R8 | Lọc theo giá hoạt động đúng | TC_PROD_FILTER_001 | Lọc theo giá hoạt động đúng | ✅ PASS | 100% | Cần test multiple price ranges |
| R9 | Xem chi tiết sản phẩm | TC_PROD_DETAIL_001 | Xem chi tiết sản phẩm thành công | ✅ PASS | 100% | Hình ảnh, mô tả, rating |
| R10 | Thêm sản phẩm vào giỏ thành công | TC_CART_ADD_001 | Thêm sản phẩm vào giỏ thành công | ✅ PASS | 100% | Multiple products added |
| R11 | Cập nhật số lượng trong giỏ | TC_CART_UPDATE_001 | Cập nhật số lượng sản phẩm trong giỏ | ✅ PASS | 100% | Test increase/decrease |
| R12 | Xoá sản phẩm khỏi giỏ | TC_CART_DELETE_001 | Xoá sản phẩm khỏi giỏ thành công | ✅ PASS | 100% | Cart total updated |

---

### MODULE 3: CHECKOUT (Thanh toán)

| Req ID | Yêu cầu (Requirement) | TC ID | Test Case Name | Status | Coverage | Notes |
|--------|--------|-------|--------|--------|----------|-------|
| R13 | Thanh toán bắt buộc nhập địa chỉ | TC_CHK_ADDRESS_001 | Thanh toán bắt buộc nhập địa chỉ | ✅ PASS | 100% | Validation on address field |
| R13 | Thanh toán bắt buộc nhập địa chỉ | TC_CHK_ADDRESS_002 | Nhập địa chỉ giao hàng thành công | ✅ PASS | 100% | Address saved to user profile |
| R14 | Chọn phương thức thanh toán | TC_CHK_PAYMENT_001 | Chọn phương thức thanh toán COD thành công | ✅ PASS | 50% | COD method |
| R14 | Chọn phương thức thanh toán | TC_CHK_PAYMENT_002 | Chọn phương thức thanh toán Visa thành công | ✅ PASS | 50% | Visa payment simulation |
| R15 | Đặt hàng thành công | TC_CHK_ORDER_001 | Đặt hàng thành công | ✅ PASS | 100% | Order ID generated + email sent |
| R15 | Đặt hàng thành công | TC_CHK_ORDER_002 | Đặt hàng thất bại khi thiếu thông tin | ✅ PASS | 50% | Error handling |
| R16 | Lưu lịch sử đơn hàng | TC_CHK_HISTORY_001 | Xem lịch sử đơn hàng thành công | ✅ PASS | 100% | Order list display |
| R16 | Lưu lịch sử đơn hàng | TC_CHK_HISTORY_002 | Xem chi tiết đơn hàng | ✅ PASS | 100% | Order detail display |

---

## 3. TÓNG HỢP RTM

### Thống kê yêu cầu:
- **Tổng số Requirement (R)**: 16
- **Requirement được cover**: 16 (100%)
- **Requirement chưa cover**: 0 (0%)

### Thống kê Test Case:
- **Tổng số Test Case**: 24
- **TC Passed (✅)**: 24 (100%)
- **TC Failed (❌)**: 0 (0%)
- **TC Not Run**: 0 (0%)

### Thống kê độ bao phủ:
| Requirement | Số TC | Độ bao phủ |
|-----------|--------|-----------|
| R1 | 1 | 100% |
| R2 | 1 | 100% |
| R3 | 2 | 100% |
| R4 | 1 | 100% |
| R5 | 2 | 100% |
| R6 | 1 | 100% |
| R7 | 2 | 100% |
| R8 | 1 | 100% |
| R9 | 1 | 100% |
| R10 | 1 | 100% |
| R11 | 1 | 100% |
| R12 | 1 | 100% |
| R13 | 2 | 100% |
| R14 | 2 | 100% |
| R15 | 2 | 100% |
| R16 | 2 | 100% |

---

## 4. GAP ANALYSIS (Phân tích khoảng trống)

### Requirement chưa được test:
- ✅ Không có requirement nào chưa được test

### Recommendation:
- Cần test thêm các edge cases cho search (special characters, unicode)
- Cần test performance khi có nhiều sản phẩm
- Cần test payment timeout scenarios
- Cần test concurrent orders (multiple users ordering same product)

---

## 5. RTM THEO MODULE

### Module 1 - Authentication:
- **Total Requirements**: 6 (R1-R6)
- **Total Test Cases**: 8
- **Coverage**: 100%
- **Status**: ✅ Hoàn thành

### Module 2 - Product & Cart:
- **Total Requirements**: 6 (R7-R12)
- **Total Test Cases**: 7
- **Coverage**: 100%
- **Status**: ✅ Hoàn thành

### Module 3 - Checkout:
- **Total Requirements**: 4 (R13-R16)
- **Total Test Cases**: 8
- **Coverage**: 100%
- **Status**: ✅ Hoàn thành

---

## 6. PHÊ DUYỆT RTM

| Vị trí | Tên | Chữ ký | Ngày |
|--------|------|--------|------|
| QA Lead | [Tên] | _____ | ___ |
| Product Owner | [Tên] | _____ | ___ |

---

**END OF RTM**
