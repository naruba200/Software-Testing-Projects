# DGore ÁN TESTING - WEBSITE BÁN HÀNG ONLINE

**Tên Dự Án:** Manual QA Testing Project - Ecommerce Website  
**Phiên Bản:** 1.0  
**Ngày Tạo:** 03/03/2026  
**Trạng Thái:** ✅ Hoàn Thành & Approved for Release

---

## 📋 MỤC LỤC

1. [Giới Thiệu](#giới-thiệu)
2. [Cấu Trúc Thư Mục](#cấu-trúc-thư-mục)
3. [Hướng Dẫn Sử Dụng](#hướng-dẫn-sử-dụng)
4. [Các Hệ Thống được Test](#các-hệ-thống-được-test)
5. [Chuẩn Hóa](#chuẩn-hóa)
6. [Key Metrics](#key-metrics)
7. [FAQ](#faq)

---

## 🎯 Giới Thiệu

Dự án này là một **Manual QA Testing** toàn diện cho hệ thống **Website Bán Hàng Online (Ecommerce)**. Dự án bao gồm:

- ✅ **Test Plan**: Kế hoạch kiểm thử chi tiết
- ✅ **Test Cases**: 24 ca kiểm thử chi tiết
- ✅ **RTM**: Ma trận truy vết yêu cầu 100%
- ✅ **Bug Reports**: Tài liệu báo cáo lỗi chuẩn hóa
- ✅ **Test Report**: Báo cáo kiểm thử UAT hoàn chỉnh
- ✅ **Test Metrics**: Chỉ số kiểm thử KPI

**Kết Luận Chung:** ✅ **HỆ THỐNG SẴN SÀNG RELEASE**

---

## 📁 Cấu Trúc Thư Mục

```
Software-Testing-Projects/
│
├── Test Plan/
│   └── Test_Plan_Ecommerce.md
│       ├── Mục đích kiểm thử
│       ├── Phạm vi kiểm thử
│       ├── Chiến lược kiểm thử
│       ├── Tiêu chuẩn chuẩn hóa (TC ID, Bug ID, Severity)
│       ├── Entry/Exit Criteria
│       └── Lịch trình kiểm thử
│
├── Test Cases/
│   ├── Test_Cases_Module1_Authentication.md (8 TC)
│   │   ├── TC_AUTH_REG_001 - Đăng ký thành công
│   │   ├── TC_AUTH_REG_002 - Email không hợp lệ
│   │   ├── TC_AUTH_REG_003 - Mật khẩu < 8 ký tự
│   │   ├── TC_AUTH_REG_004 - Email đã tồn tại
│   │   ├── TC_AUTH_LOGIN_001 - Đăng nhập thành công
│   │   ├── TC_AUTH_LOGIN_002 - Sai mật khẩu
│   │   ├── TC_AUTH_LOGIN_003 - Email không tồn tại
│   │   └── TC_AUTH_FP_001 - Quên mật khẩu
│   │
│   ├── Test_Cases_Module2_ProductCart.md (7 TC)
│   │   ├── TC_PROD_SEARCH_001 - Tìm kiếm đúng kết quả
│   │   ├── TC_PROD_SEARCH_002 - Tìm kiếm không kết quả
│   │   ├── TC_PROD_FILTER_001 - Lọc theo giá
│   │   ├── TC_PROD_FILTER_002 - Lọc theo danh mục
│   │   ├── TC_PROD_DETAIL_001 - Xem chi tiết sản phẩm
│   │   ├── TC_CART_ADD_001 - Thêm vào giỏ
│   │   ├── TC_CART_UPDATE_001 - Cập nhật số lượng
│   │   └── TC_CART_DELETE_001 - Xoá khỏi giỏ
│   │
│   └── Test_Cases_Module3_Checkout.md (9 TC)
│       ├── TC_CHK_ADDRESS_001 - Bắt buộc nhập địa chỉ
│       ├── TC_CHK_ADDRESS_002 - Nhập địa chỉ thành công
│       ├── TC_CHK_PAYMENT_001 - COD thành công
│       ├── TC_CHK_PAYMENT_002 - Visa thành công
│       ├── TC_CHK_ORDER_001 - Đặt hàng thành công
│       ├── TC_CHK_ORDER_002 - Đặt hàng thất bại
│       ├── TC_CHK_HISTORY_001 - Xem lịch sử đơn
│       └── TC_CHK_HISTORY_002 - Xem chi tiết đơn
│
├── RTM/
│   └── RTM_Ecommerce.md
│       ├── Ma trận truy vết yêu cầu (16 R -> 24 TC)
│       ├── 100% Requirement Coverage
│       ├── Gap Analysis
│       └── RTM theo Module
│
├── Bug Reports/
│   └── Bug_Report_Template.md
│       ├── Template báo cáo lỗi chuẩn
│       ├── Ví dụ 3 bug (BUG_2026_001-003)
│       │   - Đăng nhập lỗi với ký tự đặc biệt (HIGH)
│       │   - Tìm kiếm chậm (MEDIUM)
│       │   - Tính giá sai với discount (CRITICAL - RESOLVED)
│       ├── Severity & Priority definition
│       └── Best practices
│
├── Test Report/
│   └── Test_Report_UAT.md
│       ├── Executive Summary
│       ├── Test Execution Summary (91.67% pass rate)
│       ├── Bug Summary (8 bugs, 87.5% resolved)
│       ├── Test Coverage (100%)
│       ├── Browser & Device Coverage
│       ├── Quality Metrics
│       ├── Recommendations
│       └── ✅ Sign-off "APPROVED FOR RELEASE"
│
├── Test Metrics/
│   └── Test_Metrics_UAT.md
│       ├── Test Execution Metrics
│       ├── Defect Metrics & Trend
│       ├── Requirement Coverage (100%)
│       ├── Quality Metrics
│       ├── Test Effort Distribution
│       ├── Risk Assessment
│       ├── GO/NO-GO Decision Matrix
│       └── Release Readiness Score: 87% ✅
│
└── README.md (TẬP TIN NÀY)
```

---

## 📖 Hướng Dẫn Sử Dụng

### 1️⃣ Trước khi bắt đầu kiểm thử

**Bước 1: Đọc Test Plan**
- Mở: `Test Plan/Test_Plan_Ecommerce.md`
- Hiểu: Mục đích, phạm vi, chiến lược
- Kiểm tra: Entry Criteria (Environment, Build, Data)

**Bước 2: Chuẩn bị Test Evironment**
- ✅ Deploy application
- ✅ Chuẩn bị test data
- ✅ Tạo test accounts
- ✅ Verify environment

### 2️⃣ Chạy kiểm thử

**Bước 1: Xem Test Cases**
- Module 1: `Test Cases/Test_Cases_Module1_Authentication.md`
- Module 2: `Test Cases/Test_Cases_Module2_ProductCart.md`
- Module 3: `Test Cases/Test_Cases_Module3_Checkout.md`

**Bước 2: Chạy từng Test Case**
- Đọc "Setup/Precondition"
- Thực thi "Steps" theo đúng thứ tự
- So sánh với "Expected Result"
- Ghi "Actual Result"
- Mark PASS ✅ hoặc FAIL ❌

**Bước 3: Khi phát hiện lỗi**
- Tạo Bug Report theo template
- Format: `BUG_[YYYY]_[NNN]` (e.g., BUG_2026_001)
- Ghi rõ: Severity, Priority, Steps to reproduce
- Tham khảo: `Bug Reports/Bug_Report_Template.md`

### 3️⃣ Sau khi hoàn thành kiểm thử

**Bước 1: Xác nhận RTM**
- Mỗi Requirements phải được cover bởi ít nhất 1 TC
- Xem: `RTM/RTM_Ecommerce.md`
- Verify: 100% Requirement Coverage

**Bước 2: Tổng hợp kết quả**
- Tính: Pass Rate, Fail Rate, Bug Count
- So sánh vs Target
- Ghi: `Test Report/Test_Report_UAT.md`

**Bước 3: Tính toán Metrics**
- Quality KPIs
- Defect metrics
- Coverage metrics
- Xem: `Test Metrics/Test_Metrics_UAT.md`

---

## 🎨 Các Hệ Thống được Test

### Module 1: AUTHENTICATION (Xác thực người dùng)

**Tính năng:**
- ✅ Đăng ký tài khoản (Signup)
- ✅ Đăng nhập (Login)
- ✅ Quên mật khẩu (Forgot Password)
- ✅ Đăng xuất (Logout)

**Test Cases:** 8  
**Pass Rate:** 100% ✅  
**Coverage:** 6 Requirements (R1-R6)

### Module 2: PRODUCT & CART (Sản phẩm & Giỏ hàng)

**Tính năng:**
- ✅ Tìm kiếm sản phẩm
- ✅ Lọc theo giá/danh mục
- ✅ Xem chi tiết sản phẩm
- ✅ Thêm vào giỏ hàng
- ✅ Cập nhật số lượng
- ✅ Xoá khỏi giỏ

**Test Cases:** 7  
**Pass Rate:** 100% ✅  
**Coverage:** 6 Requirements (R7-R12)

### Module 3: CHECKOUT (Thanh toán)

**Tính năng:**
- ✅ Nhập địa chỉ giao hàng
- ✅ Chọn phương thức thanh toán (COD/Visa)
- ✅ Đặt hàng
- ✅ Xem lịch sử đơn hàng

**Test Cases:** 9  
**Pass Rate:** 77.78% (2 failed but resolved)  
**Coverage:** 4 Requirements (R13-R16)

---

## ⚙️ Chuẩn Hóa

### Test Case ID Format

```
TC_[Module]_[Function]_[Number]

Ví dụ:
- TC_AUTH_LOGIN_001 (Authentication - Login #1)
- TC_PROD_SEARCH_001 (Product - Search #1)
- TC_CHK_PAYMENT_001 (Checkout - Payment #1)
```

**Module Codes:**
- `AUTH` = Authentication
- `PROD` = Product & Cart
- `CHK` = Checkout

### Bug ID Format

```
BUG_[YYYY]_[NNN]

Ví dụ:
- BUG_2026_001
- BUG_2026_002
- BUG_2026_003
```

### Severity Levels

| Level | Định Nghĩa | Ví Dụ |
|-------|-----------|-------|
| 🔴 **CRITICAL** | Hệ thống crash, không hoạt động | Website down, không đăng nhập được |
| 🔴 **HIGH** | Tính năng chính không hoạt động | Payment failed, no products show |
| 🟡 **MEDIUM** | Tính năng phụ có vấn đề | Search slow, UI glitch |
| 🟢 **LOW** | Lỗi nhỏ, không ảnh hưởng nhiều | Text misalign, typo |

### Priority Levels

| Priority | Deadline | Ví Dụ |
|----------|----------|-------|
| P0 - BLOCKER | 24 hours | Chặn release, phải sửa ngay |
| P1 - HIGH | 3 days | Phải sửa trước release |
| P2 - MEDIUM | 1 week | Nên sửa nhưng không chặn release |
| P3 - LOW | As time permits | Có thể sửa sau |

---

## 📊 Key Metrics

### Test Execution Summary

```
Total Test Cases:           24
├─ Passed:                  22 (91.67%)
├─ Failed:                  2 (8.33%)
└─ Not Run:                 0 (0%)

Total Bugs Found:           8
├─ Critical:                1 (12.5%)
├─ High:                    2 (25%)
├─ Medium:                  4 (50%)
├─ Low:                     1 (12.5%)
└─ Resolved:                7 (87.5%)

Requirement Coverage:       16/16 (100%)
Module Coverage:            3/3 (100%)
Test Duration:              7 days
QA Team:                    3 QA Engineers + 1 QA Lead
```

### Quality Score

```
Functionality:              90%
Performance:                75%
Compatibility:              95%
Documentation:              80%
User Acceptance:            95%
────────────────────────
Overall Release Score:      87% ✅ READY
```

### Pass Rate by Module

```
Module 1 - Authentication:  ██████████ 100% ✅
Module 2 - Product & Cart:  ██████████ 100% ✅
Module 3 - Checkout:        ████████░░ 77.78% ⚠️ (Fixed)
────────────────────────
OVERALL:                    ███████████ 91.67% ✅
```

---

## ❓ FAQ

### Q1: Test Cases này có thể tái sử dụng được không?
**A:** Có. Tất cả Test Cases được viết theo chuẩn, có thể tái sử dụng cho Regression Testing và các release sau.

### Q2: Nếu phát hiện bug mới, phải làm gì?
**A:** 
1. Tạo Bug Report theo format `BUG_2026_NNN`
2. Ghi rõ Severity, Priority, Reproduction Steps
3. Tham khảo template: `Bug Reports/Bug_Report_Template.md`
4. Assign cho Developer
5. Track resolution status

### Q3: Làm sao để cập nhật RTM khi có requirement mới?
**A:**
1. Mở `RTM/RTM_Ecommerce.md`
2. Thêm requirement vào bảng (e.g., R17)
3. Viết Test Case liên kết
4. Update RTM table (link TC ID)
5. Tính toán lại coverage

### Q4: Test Report phải được tạo định kỳ không?
**A:** Nên. Tạo hàng tuần hoặc hàng ngày tùy theo:
- Daily: Báo cáo tiến độ cho PM
- Weekly: Báo cáo chi tiết cho stakeholders
- Final: Báo cáo UAT cuối cùng

### Q5: Các browser nào cần test?
**A:** Theo Test Plan:
- ✅ Chrome (Latest)
- ✅ Firefox (Latest)
- ✅ Edge (Latest)
- ✅ Safari (Optional - iOS)

### Q6: Release liệu đã sẵn sàng chưa?
**A:** ✅ **CÓ** - Điều kiện đã thỏa mãn:
- ✅ 91.67% pass rate (> 85% target)
- ✅ 100% requirement coverage
- ✅ 87.5% bug resolved
- ✅ Không có Critical issue còn open
- ✅ Quality Score: 87% (Approved)
- ✅ Nhân viên QA, Dev, PM, PO đã sign-off

---

## 📞 Liên Hệ & Support

Nếu có câu hỏi hoặc cần hỗ trợ:

- **QA Lead**: [Name] - [Email]
- **Test Manager**: [Name] - [Email]
- **Project Manager**: [Name] - [Email]

---

## 📝 Version History

| Version | Date | Changes | Author |
|---------|------|---------|--------|
| 1.0 | 12/03/2026 | Initial release | QA Team |
| - | - | - | - |

---

## ✅ Checklist trước khi Release

- [x] Tất cả Test Cases đã được chạy
- [x] Test Report được tạo
- [x] RTM 100% coverage
- [x] Bugs được ghi nhận đầy đủ
- [x] Metrics được tính toán
- [x] Sign-off từ stakeholders
- [x] Documentation hoàn chỉnh
- [x] Environment prepared
- [x] Rollback plan created
- [x] Production ready

---

## 🎉 Conclusion

**Hệ thống Website Bán Hàng Online đã hoàn thành kiểm thử Manual QA.**

**Kết luận:** ✅ **READY FOR PRODUCTION**

**Sign-off:** 12/03/2026  
**Quality Score:** 87/100 (Grade: A)  
**Confidence Level:** 95%

---

**END OF README**

---

*Last Updated: 12/03/2026*  
*Project Status: ✅ COMPLETED & APPROVED*  
*Release Decision: ✅ GO*
