# CA KIỂM THỬ - MODULE 3: THANH TOÁN (CHECKOUT)

**Phiên bản:** 1.0  
**Ngày tạo:** 03/03/2026  
**Module:** Checkout  
**Tác giả:** QA Team

---

## 1. NHẬP ĐỊA CHỈ GIAO HÀNG (DELIVERY ADDRESS)

### TC_CHK_ADDRESS_001 - Thanh toán bắt buộc nhập địa chỉ
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CHK_ADDRESS_001 |
| **Tên test case** | Thanh toán bắt buộc nhập địa chỉ |
| **Module** | Checkout |
| **Tính năng** | Nhập địa chỉ giao hàng |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Giỏ hàng có sản phẩm<br>- Ở trang thanh toán |
| **Bước thực thi** | 1. Truy cập giỏ hàng<br>2. Click "Thanh toán"<br>3. Bỏ qua nhập địa chỉ<br>4. Click "Tiếp tục" |
| **Kết quả mong đợi** | - Không thể tiếp tục<br>- Hiển thị lỗi: "Vui lòng nhập địa chỉ giao hàng"<br>- Vẫn ở trang thanh toán |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 1 |

---

### TC_CHK_ADDRESS_002 - Nhập địa chỉ giao hàng thành công
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CHK_ADDRESS_002 |
| **Tên test case** | Nhập địa chỉ giao hàng thành công |
| **Module** | Checkout |
| **Tính năng** | Nhập địa chỉ giao hàng |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Giỏ hàng có sản phẩm<br>- Ở trang thanh toán |
| **Bước thực thi** | 1. Truy cập giỏ hàng<br>2. Click "Thanh toán"<br>3. Nhập địa chỉ: 123 Nguyễn Huệ, Q1, HCM<br>4. Click "Tiếp tục" |
| **Kết quả mong đợi** | - Địa chỉ được lưu<br>- Chuyển đến bước chọn phương thức thanh toán<br>- Không có lỗi |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 1 |

---

## 2. CHỌN PHƯƠNG THỨC THANH TOÁN (PAYMENT METHOD)

### TC_CHK_PAYMENT_001 - Chọn phương thức thanh toán COD thành công
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CHK_PAYMENT_001 |
| **Tên test case** | Chọn phương thức thanh toán COD thành công |
| **Module** | Checkout |
| **Tính năng** | Chọn phương thức thanh toán |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Đã nhập địa chỉ giao hàng<br>- Ở trang chọn phương thức thanh toán |
| **Bước thực thi** | 1. Ở trang thanh toán (bước 2)<br>2. Chọn "Thanh toán khi nhận (COD)"<br>3. Click "Tiếp tục" |
| **Kết quả mong đợi** | - Phương thức COD được chọn<br>- Chuyển đến trang xác nhận đơn hàng |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 1 |

---

### TC_CHK_PAYMENT_002 - Chọn phương thức thanh toán Visa thành công
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CHK_PAYMENT_002 |
| **Tên test case** | Chọn phương thức thanh toán Visa thành công |
| **Module** | Checkout |
| **Tính năng** | Chọn phương thức thanh toán |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Đã nhập địa chỉ giao hàng<br>- Ở trang chọn phương thức thanh toán |
| **Bước thực thi** | 1. Ở trang thanh toán (bước 2)<br>2. Chọn "Thanh toán bằng Visa"<br>3. Nhập số thẻ: 4111111111111111<br>4. Nhập ngày hết hạn: 12/25<br>5. Nhập CVV: 123<br>6. Click "Tiếp tục" |
| **Kết quả mong đợi** | - Thanh toán bằng Visa được xử lý<br>- Chuyển đến trang xác nhận đơn hàng |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 1 |

---

## 3. ĐẶT HÀNG (PLACE ORDER)

### TC_CHK_ORDER_001 - Đặt hàng thành công
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CHK_ORDER_001 |
| **Tên test case** | Đặt hàng thành công |
| **Module** | Checkout |
| **Tính năng** | Đặt hàng |
| **Ưu tiên** | High |
| **Severity** | Critical |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Đã nhập địa chỉ<br>- Đã chọn phương thức thanh toán<br>- Ở trang xác nhận đơn hàng |
| **Bước thực thi** | 1. Ở trang xác nhận đơn hàng<br>2. Reviewed thông tin:<br>   - Sản phẩm: iPhone 15 x 2<br>   - Địa chỉ: 123 Nguyễn Huệ<br>   - Phương thức: COD<br>3. Click "Đặt hàng" |
| **Kết quả mong đợi** | - Đơn hàng được tạo thành công<br>- Hiển thị mã đơn hàng (Order ID)<br>- Email xác nhận được gửi<br>- Chuyển đến trang thành công |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 2 |

---

### TC_CHK_ORDER_002 - Đặt hàng thất bại khi thiếu thông tin
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CHK_ORDER_002 |
| **Tên test case** | Đặt hàng thất bại khi thiếu thông tin |
| **Module** | Checkout |
| **Tính năng** | Đặt hàng |
| **Ưu tiên** | Medium |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Ở trang thanh toán |
| **Bước thực thi** | 1. Ở trang thanh toán<br>2. Bỏ qua các trường bắt buộc<br>3. Click "Đặt hàng" |
| **Kết quả mong đợi** | - Đặt hàng thất bại<br>- Hiển thị lỗi về thông tin thiếu |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 2 |

---

## 4. XEM LỊCH SỬ ĐƠN HÀNG (ORDER HISTORY)

### TC_CHK_HISTORY_001 - Xem lịch sử đơn hàng thành công
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CHK_HISTORY_001 |
| **Tên test case** | Xem lịch sử đơn hàng thành công |
| **Module** | Checkout |
| **Tính năng** | Xem lịch sử đơn hàng |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Có ít nhất 1 đơn hàng |
| **Bước thực thi** | 1. Click vào menu người dùng<br>2. Click "Lịch sử đơn hàng"<br>3. Xem danh sách đơn hàng |
| **Kết quả mong đợi** | - Hiển thị danh sách đơn hàng<br>- Mỗi đơn hàng hiển thị:<br>  - Mã đơn hàng<br>  - Ngày đặt<br>  - Tổng giá<br>  - Trạng thái |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 2 |

---

### TC_CHK_HISTORY_002 - Xem chi tiết đơn hàng
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CHK_HISTORY_002 |
| **Tên test case** | Xem chi tiết đơn hàng |
| **Module** | Checkout |
| **Tính năng** | Xem lịch sử đơn hàng |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Ở trang lịch sử đơn hàng |
| **Bước thực thi** | 1. Ở trang lịch sử đơn hàng<br>2. Click vào một đơn hàng |
| **Kết quả mong đợi** | - Hiển thị chi tiết đơn hàng:<br>  - Mã đơn hàng<br>  - Danh sách sản phẩm<br>  - Địa chỉ giao hàng<br>  - Phương thức thanh toán<br>  - Trạng thái vận chuyển |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 3 |

---

## 5. MÍTOTT KHUYẾN MÃI (DISCOUNT CODE)

### TC_CHK_DISCOUNT_001 - Áp dụng mã khuyến mãi hợp lệ
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CHK_DISCOUNT_001 |
| **Tên test case** | Áp dụng mã khuyến mãi hợp lệ |
| **Module** | Checkout |
| **Tính năng** | Áp dụng mã khuyến mãi |
| **Ưu tiên** | Medium |
| **Severity** | High |
| **Loại test** | Validation |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Giỏ hàng có sản phẩm (5.000.000 đ)<br>- Mã "SAVE10" hợp lệ giảm 10% |
| **Bước thực thi** | 1. Truy cập giỏ hàng<br>2. Nhập mã khuyến mãi: SAVE10<br>3. Click "Áp dụng"<br>4. Xem tổng giỏ hàng |
| **Kết quả mong đợi** | - Mã được áp dụng thành công<br>- Tổng giảm từ 5.000.000 đ → 4.500.000 đ<br>- Hiển thị tiền tiết kiệm: 500.000 đ<br>- Có thể xoá mã nếu muốn |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 08/03/2026 |
| **Tester** | QA Engineer 4 |

---

**END OF TEST CASES - MODULE 3 (10 TOTAL)**
