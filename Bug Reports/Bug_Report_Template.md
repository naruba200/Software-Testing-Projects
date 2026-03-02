# TEMPLATE BÁO CÁO LỖI (BUG REPORT)

**Created:** [Ngày tạo]  
**Project:** Website Bán Hàng Online (Ecommerce)

---

## MẪU BÁO CÁO LỖI

### BUG_2026_001

| Trường | Nội dung |
|-------|---------|
| **Bug ID** | BUG_2026_001 |
| **Title** | Đăng nhập không hoạt động với ký tự đặc biệt trong mật khẩu |
| **Module** | Authentication |
| **Feature** | Login |
| **Severity** | 🔴 **HIGH** |
| **Priority** | 🔴 **P1 - HIGH** |
| **Status** | Open |
| **Assigned to** | Developer 1 |
| **Reported by** | QA Engineer 1 |
| **Report Date** | 05/03/2026 |
| **Environment** | Production |
| **Browser** | Chrome 120 |
| **OS** | Windows 10 |

#### Mô tả (Description):
Khi mật khẩu chứa ký tự đặc biệt (!@#$%^&*), hệ thống không cho đăng nhập mặc dù mật khẩu đúng.

#### Các bước lặp lại (Steps to Reproduce):
1. Go to login page
2. Enter email: test@test.com
3. Enter password: Test@!@#$ (with special characters)
4. Click Login button

#### Kết quả mong đợi (Expected Result):
- Người dùng đăng nhập thành công
- Chuyển hướng đến Dashboard

#### Kết quả thực tế (Actual Result):
- Lỗi đăng nhập
- Hiển thị thông báo: "Login failed"
- Không chuyển hướng

#### Screenshot:
[Attach screenshot]

#### Logs:
```
Error: Invalid character in password
Stack trace: ...
```

#### Root Cause:
Mật khẩu không được escape trong form submission

#### Solution / Fix:
Cần encode mật khẩu trước khi gửi request

#### Workaround:
Sử dụng mật khẩu mà không có ký tự đặc biệt

#### Related Issues:
- BUG_2026_002 (tương tự ở form đăng ký)

---

### BUG_2026_002

| Trường | Nội dung |
|-------|---------|
| **Bug ID** | BUG_2026_002 |
| **Title** | Tìm kiếm sản phẩm chậm khi có dữ liệu lớn |
| **Module** | Product & Cart |
| **Feature** | Search |
| **Severity** | 🟡 **MEDIUM** |
| **Priority** | 🟡 **P2 - MEDIUM** |
| **Status** | In Progress |
| **Assigned to** | Developer 2 |
| **Reported by** | QA Engineer 2 |
| **Report Date** | 06/03/2026 |
| **Environment** | Staging |
| **Browser** | Firefox 121 |
| **OS** | Windows 10 |

#### Mô tả (Description):
Tìm kiếm sản phẩm mất hơn 5 giây khi tìm trong database có 10,000+ sản phẩm

#### Các bước lặp lại (Steps to Reproduce):
1. Go to Product page
2. Search for popular keyword (e.g., "phone")
3. Measure response time

#### Kết quả mong đợi (Expected Result):
- Kết quả trả về trong < 2 giây
- UX không bị frozen

#### Kết quả thực tế (Actual Result):
- Mất 5-8 giây để trả về kết quả
- UI bị đơ trong khi chờ

#### Performance Data:
| Số sản phẩm | Thời gian |
|-----------|----------|
| 1,000 | 0.5s |
| 5,000 | 2.3s |
| 10,000 | 5.8s |

#### Root Cause:
Database query không có index trên trường search

#### Solution / Fix):
Thêm database index trên trường product name

#### Workaround:
Không có workaround hiệu quả

---

### BUG_2026_003

| Trường | Nội dung |
|-------|---------|
| **Bug ID** | BUG_2026_003 |
| **Title** | Tổng giá trong giỏ hàng tính sai khi áp dụng discount |
| **Module** | Product & Cart |
| **Feature** | Cart |
| **Severity** | 🔴 **CRITICAL** |
| **Priority** | 🔴 **P0 - BLOCKER** |
| **Status** | Resolved |
| **Assigned to** | Developer 1 |
| **Reported by** | QA Engineer 3 |
| **Report Date** | 06/03/2026 |
| **Environment** | Development |
| **Browser** | Chrome 120 |
| **OS** | macOS 14 |

#### Mô tả (Description):
Khi áp dụng discount code 50%, tổng giá không giảm đúng

#### Các bước lặp lại (Steps to Reproduce):
1. Add product to cart: $100
2. Apply discount code: SAVE50 (50% off)
3. Check total price

#### Kết quả mong đợi (Expected Result):
- Giá sản phẩm: $100
- Discount: -$50
- Tổng: $50

#### Kết quả thực tế (Actual Result):
- Giá sản phẩm: $100
- Discount: -$25 (chỉ 25%)
- Tổng: $75

#### Root Cause:
Discount calculation bug - nhân với 0.5 thay vì trừ đi discount percentage

#### Solution / Fix (Resolved):
Fixed discount calculation logic in cart.js line 245

#### Fixed Version:
- Version: 1.2.1
- Fixed Date: 07/03/2026

#### Testing:
- ✅ Unit tests passed
- ✅ Integration tests passed
- ✅ UAT approved

---

### BUG_2026_004

| Trường | Nội dung |
|-------|---------|
| **Bug ID** | BUG_2026_004 |
| **Title** | Giỏ hàng không update khi xóa sản phẩm |
| **Module** | Product & Cart |
| **Feature** | Cart Management |
| **Severity** | 🔴 **HIGH** |
| **Priority** | 🔴 **P1 - HIGH** |
| **Status** | In Progress |
| **Assigned to** | Developer 2 |
| **Reported by** | QA Engineer 2 |
| **Report Date** | 08/03/2026 |
| **Environment** | Staging |
| **Browser** | Safari 17 |
| **OS** | iOS 17 |

#### Mô tả (Description):
Khi xoá sản phẩm khỏi giỏ trên mobile (Safari iOS), giao diện không update ngay lập tức. Người dùng phải refresh trang để thấy sản phẩm được xoá.

#### Các bước lặp lại (Steps to Reproduce):
1. Truy cập website trên iPhone/iPad
2. Thêm 2 sản phẩm vào giỏ
3. Mở giỏ hàng
4. Click nút xoá sản phẩm
5. Quan sát giỏ hàng

#### Kết quả mong đợi (Expected Result):
- Sản phẩm bị xoá ngay lập tức
- Giỏ hàng cập nhật tổng giá
- Không cần reload trang

#### Kết quả thực tế (Actual Result):
- Sản phẩm vẫn hiển thị trong giỏ
- Phải F5 hoặc pull-to-refresh để cập nhật
- Gây confused cho người dùng

#### Root Cause:
Ajax call không trigger UI re-render trên Safari iOS, có thể do JavaScript version incompatibility

#### Solution / Fix (Pending):
Cần test và fix compatibility với Safari iOS, có thể sử dụng XHR thay vì fetch API

#### Workaround:
Nhấn F5 hoặc pull-to-refresh để cập nhật giỏ

---

### BUG_2026_005

| Trường | Nội dung |
|-------|---------|
| **Bug ID** | BUG_2026_005 |
| **Title** | Mã khuyến mãi không được áp dụng sau khi update số lượng |
| **Module** | Checkout |
| **Feature** | Discount Code |
| **Severity** | 🟡 **MEDIUM** |
| **Priority** | 🟡 **P2 - MEDIUM** |
| **Status** | Resolved |
| **Assigned to** | Developer 3 |
| **Reported by** | QA Engineer 1 |
| **Report Date** | 08/03/2026 |
| **Environment** | Production |
| **Browser** | Chrome 120 |
| **OS** | Windows 10 |

#### Mô tả (Description):
Sau khi áp dụng mã khuyến mãi "SAVE10", nếu người dùng update số lượng sản phẩm, discount sẽ bị mất.

#### Các bước lặp lại (Steps to Reproduce):
1. Thêm sản phẩm vào giỏ: iPhone 15 (giá 2.000.000đ)
2. Áp dụng mã: SAVE10 (giảm 10%)
3. Tổng hiện thị: 1.800.000đ ✓
4. Thay đổi số lượng từ 1 → 2
5. Xem tổng giỏ hàng

#### Kết quả mong đợi (Expected Result):
- Tổng = (2.000.000 × 2) × 90% = 3.600.000đ
- Discount SAVE10 vẫn được áp dụng

#### Kết quả thực tế (Actual Result):
- Tổng = 2.000.000 × 2 = 4.000.000đ
- Discount bị xoá

#### Root Cause:
Cart quantity update không gọi function recalculate discount, discount state bị reset

#### Solution / Fix (Resolved):
Fixed updateQuantity function để gọi applyDiscount khi quantity thay đổi

#### Fixed Date: 09/03/2026

#### Testing:
- ✅ Tested on Chrome, Firefox, Edge
- ✅ Tested on multiple discount codes
- ✅ UAT passed

---

## THỐNG KÊ BUG (UPDATED)

| Severity | Count | % |
|----------|-------|---|
| 🔴 CRITICAL | 1 | 10% |
| 🔴 HIGH | 3 | 30% |
| 🟡 MEDIUM | 5 | 50% |
| 🟢 LOW | 1 | 10% |
| **TOTAL** | **10** | **100%** |

| Priority | Count | % |
|----------|-------|---|
| P0 - BLOCKER | 1 | 10% |
| P1 - HIGH | 3 | 30% |
| P2 - MEDIUM | 5 | 50% |
| P3 - LOW | 1 | 10% |
| **TOTAL** | **10** | **100%** |

| Status | Count | % |
|--------|-------|---|
| Open | 1 | 10% |
| In Progress | 1 | 10% |
| Resolved | 8 | 80% |
| Closed | 0 | 0% |
| **TOTAL** | **10** | **100%** |

---

## HƯỚNG DẪN TẠO BUG REPORT

### Thông tin bắt buộc:
✅ **Bug ID**: BUG_YYYY_NNN format  
✅ **Title**: Mô tả ngắn gọn lỗi  
✅ **Module & Feature**: Nơi lỗi xảy ra  
✅ **Severity**: CRITICAL, HIGH, MEDIUM, LOW  
✅ **Priority**: P0, P1, P2, P3  
✅ **Steps to Reproduce**: Các bước chi tiết  
✅ **Expected vs Actual Result**: So sánh  

### Thông tin bổ sung:
- Screenshot hoặc Video
- Log files
- Environment details
- Browser/OS version
- Data used for testing

### Severity Definition:
| Level | Định nghĩa | Ví dụ |
|-------|-----------|-------|
| **CRITICAL** | Hệ thống crash, không thể sử dụng | Cannot login, website down |
| **HIGH** | Tính năng chính broken | Payment failed, no product display |
| **MEDIUM** | Tính năng phụ bị ảnh hưởng | Search slow, UI glitch |
| **LOW** | Lỗi nhỏ, không ảnh hưởng nhiều | Text alignment, minor typo |

### Priority Definition:
| Priority | Định nghĩa | Deadline |
|----------|-----------|----------|
| **P0 - BLOCKER** | Phải sửa ngay, chặn release | 24 hours |
| **P1 - HIGH** | Phải sửa trước release | 3 days |
| **P2 - MEDIUM** | Nên sửa nhưng không chặn | 1 week |
| **P3 - LOW** | Có thể sửa sau | As time permits |

---

**END OF BUG REPORT TEMPLATE**
