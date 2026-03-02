# KẾ HOẠCH KIỂM THỬ (TEST PLAN)
## Hệ Thống Website Bán Hàng Online - Ecommerce

**Phiên bản:** 2.0  
**Ngày tạo:** 01/03/2026  
**Ngày cập nhật:** 12/03/2026  
**Tác giả:** QA Team  
**Trạng thái:** ✅ Phê duyệt  
**Mã dự án:** ECOM-2026-Q1

---

## 📌 GIỚI THIỆU (INTRODUCTION)

### 1.1 Tổng quan dự án

Dự án kiểm thử Manual QA cho hệ thống **Website Bán Hàng Online (Ecommerce v1.0)** nhằm đảm bảo chất lượng sản phẩm trước khi triển khai production.

### 1.2 Mục tiêu kiểm thử (Test Objectives)

Kiểm thử hệ thống website bán hàng online (Ecommerce) nhằm:

✅ **Điểm mục tiêu chính:**
- Đảm bảo hệ thống hoạt động đúng theo yêu cầu (Requirement traceability 100%)
- Phát hiện và ghi nhận các lỗi (Bug) một cách toàn diện
- Xác minh chất lượng hệ thống trước khi ra mắt (UAT approval)
- Cải thiện trải nghiệm người dùng (User experience validation)
- Xác minh tính nhất quán & logic của hệ thống

### 1.3 Phạm vi ảnh hưởng

- **Hệ thống:** Website Ecommerce (Frontend + Backend APIs)
- **Người sử dụng:** End users, Administrators
- **Dữ liệu:** 10,000+ sản phẩm, 500+ tài khoản test
- **Thời gian:** UAT từ 05/03/2026 - 12/03/2026

---

## 📋 PHẠM VI KIỂM THỬ (SCOPE)

### 2.1 **TRONG PHẠM VI (IN-SCOPE)** ✅

#### **Module 1 - Xác thực người dùng (Authentication)**
- ✅ Đăng ký tài khoản (Email validation, Password strength)
- ✅ Đăng nhập (Credential verification, Session management)
- ✅ Quên mật khẩu (Email reset flow)
- ✅ Đăng xuất (Session termination)
- ✅ Form validation & Error handling

#### **Module 2 - Sản phẩm & Giỏ hàng (Product & Cart)**
- ✅ Tìm kiếm sản phẩm (Search functionality)
- ✅ Lọc theo giá/danh mục (Filter logic)
- ✅ Xem chi tiết sản phẩm (Display accuracy)
- ✅ Thêm sản phẩm vào giỏ (Cart operations)
- ✅ Cập nhật số lượng (Quantity adjustment)
- ✅ Xoá sản phẩm khỏi giỏ (Remove functionality)
- ✅ Tính toán tổng giá (Price calculation)

#### **Module 3 - Thanh toán (Checkout)**
- ✅ Nhập địa chỉ giao hàng (Address validation)
- ✅ Chọn phương thức thanh toán (COD & Visa simulation)
- ✅ Đặt hàng (Order creation & confirmation)
- ✅ Xem lịch sử đơn hàng (Order history display)
- ✅ Email notifications

#### **Loại kiểm thử (Test Types):**
- ✅ Functional Testing (Chức năng chính)
- ✅ UI Testing (Giao diện cơ bản)
- ✅ Regression Testing (Kiểm thử hồi quy - Smoke)
- ✅ Data Validation (Kiểm thử dữ liệu)
- ✅ Error Handling (Kiểm thử lỗi)

---

### 2.2 **NGOÀI PHẠM VI (OUT-OF-SCOPE)** ❌

| Loại kiểm thử | Lý do loại trừ |
|-----------|-----------|
| Performance Testing | Chưa được yêu cầu trong giai đoạn này |
| Load/Stress Testing | Cần công cụ chuyên biệt, không phải UAT |
| Security Testing | Cần audit bảo mật riêng từ chuyên gia |
| Mobile App Testing | Chỉ test trên Web browsers |
| API Testing riêng | Chỉ test qua UI integration |
| Database Testing | Cần access riêng, out of scope |
| Third-party Services | Giả lập payment gateway, không test thực |
| Localization Testing | Chỉ test Vietnamese language |
| Accessibility Testing | WCAG testing - future release |

---

## 🎯 PHƯƠNG PHÁP KIỂM THỬ (TEST APPROACH)

### 3.1 Chiến lược kiểm thử (Testing Strategy)

#### **A. Kiểm thử chức năng (Functional Testing)** - 70%
- Kiểm tra các tính năng hoạt động đúng theo yêu cầu
- Sử dụng Black Box testing (không biết code)
- Phương pháp: Equivalence Partitioning, Boundary Value Analysis
- Coverage target: 100% requirements

**Ví dụ test cases:**
- TC_AUTH_LOGIN_001: Đăng nhập thành công với thông tin hợp lệ
- TC_PROD_SEARCH_001: Tìm kiếm trả về kết quả đúng
- TC_CHK_ORDER_001: Đặt hàng và tạo order ID thành công

#### **B. Kiểm thử giao diện cơ bản (UI Testing)** - 15%
- Xác minh hiển thị form, button, text
- Kiểm tra layout & responsive design
- Xác nhận error messages & success notifications

**Ví dụ:**
- Form fields hiển thị đúng
- Buttons click-able & responsive
- Error messages hiển thị khi nhập sai dữ liệu
- Success messages hiển thị sau khi thành công

#### **C. Kiểm thử hồi quy (Regression Testing - Smoke)** - 15%
- Sau mỗi bug fix, test lại các critical flows
- Smoke test: Đầu vào/ra hệ thống

**Test flow:**
1. Đăng ký → Đăng nhập → Tìm sản phẩm → Đặt hàng → Đăng xuất

### 3.2 Kỹ thuật thiết kế test case (Test Design Techniques)

| Kỹ thuật | Mô tả | Ví dụ |
|---------|-------|-------|
| **Equivalence Partitioning** | Chia dữ liệu input thành các nhóm | Email: valid/invalid, đúng/sai format |
| **Boundary Value Analysis** | Test ở giới hạn | Password: 7 ký tự (invalid), 8 ký tự (valid) |
| **Decision Table** | Test các combinations | Gender + Age + Status = 8 combinations |
| **State Transition** | Test các state changes | Logged out → Logged in → Logged out |

### 3.3 Mức độ kiểm thử (Test Levels)

| Mức | Tên | Độ ưu tiên | Tỷ lệ TC |
|-----|------|---------|---------|
| **1** | Critical (Chặn release) | MUST | 35% |
| **2** | High (Quan trọng) | MUST | 40% |
| **3** | Medium (Trung bình) | SHOULD | 20% |
| **4** | Low (Thấp) | COULD | 5% |

---

---

## 🖥️ MÔI TRƯỜNG KIỂM THỬ (TEST ENVIRONMENT)

### 4.1 Thông số kỹ thuật (Hardware & Software)

#### **Server Environment**
- **OS:** Linux (Ubuntu 20.04 LTS)
- **Web Server:** Apache 2.4 / Nginx
- **Database:** PostgreSQL 14
- **Runtime:** Node.js 18.x / Python 3.10
- **Memory:** 8GB RAM
- **Storage:** 50GB SSD
- **Environment Type:** Staging/UAT

#### **Test Client Environment**
| Thành phần | Thông số | Trạng thái |
|-----------|---------|----------|
| **OS** | Windows 10 Pro | ✅ |
| **Browser** | Chrome 120 | ✅ Primary |
| **Browser** | Firefox 121 | ✅ Secondary |
| **Browser** | Edge 120 | ✅ Tertiary |
| **RAM** | 8GB | ✅ |
| **Screen Resolution** | 1920x1080 | ✅ Primary |
| **Đồng thời users** | 5 concurrent | ✅ |

### 4.2 Dữ liệu kiểm thử (Test Data)

#### **Tài khoản preload**
```
Tài khoản test giả lập - Giữ bí mật

Tên tài khoản: Mật khẩu (tạm) [Vai trò]
test@gmail.com: Test@1234 [End User]
admin@system.com: Admin@1234 [Admin]
user1@test.com: User1@1234 [End User]
user2@test.com: User2@1234 [End User]
... (50+ tài khoản)
```

#### **Sản phẩm preload**
- **Tổng số:** 10,000+ sản phẩm
- **Danh mục:** 10 categories (Electronics, Fashion, Books, etc.)
- **Khoảng giá:** 10,000 - 500,000,000 VNĐ
- **Stock:** Mix of in-stock & out-of-stock items

#### **Test Data giả lập**
| Loại | Mẫu dữ liệu | Ghi chú |
|-----|-----------|--------|
| **Email** | test@gmail.com, user123@test.com | Không dùng real email |
| **Địa chỉ** | 123 Nguyễn Huệ, Q1, HCM | Địa chỉ test, không thực |
| **SĐT** | 0987654321 | Số điện thoại test |
| **Thẻ Visa** | 4111111111111111 | Fake Visa (test only) |
| **CVV** | 123 | Test CVV |
| **Hạn thẻ** | 12/25 | Test expiry |

### 4.3 Các công cụ & tài nguyên (Tools & Resources)

| Công cụ | Phần mềm | Mục đích |
|---------|---------|---------|
| **Test Management** | Excel / Google Sheets | Quản lý TC, RTM, Bug |
| **Test Execution** | Manual (Tester) | Chạy test cases |
| **Bug Tracking** | Jira / GitHub Issues | Ghi nhận bug |
| **Documentation** | Markdown / Word | Viết report |
| **Screenshot** | Snagit / Windows Snip | Capture lỗi |
| **Email Verification** | Temp Mail / Mailinator | Kiểm test email |

### 4.4 Setup & Teardown

**Trước khi test (Setup):**
1. ✅ Clear browser cache & cookies
2. ✅ Login test account (test@gmail.com)
3. ✅ Verify system time đồng bộ
4. ✅ Kiểm tra database có test data

**Sau khi test (Teardown):**
1. ✅ Logout từ application
2. ✅ Clear test data (nếu cần)
3. ✅ Restore database backup (nếu cần)
4. ✅ Ghi nhận kết quả test

---

## 📌 TIÊU CHUẨN CHUẨN HÓA (STANDARDS & CONVENTIONS)

### 5.1 Định dạng Test Case ID
```
TC_[Module]_[Feature]_[Number]

Module Codes:
  AUTH = Authentication (Xác thực)
  PROD = Product & Cart (Sản phẩm)
  CHK  = Checkout (Thanh toán)

Feature Codes:
  REG = Registration
  LOGIN = Login
  FP = Forgot Password
  SEARCH = Search
  FILTER = Filter
  DETAIL = Detail
  ADD = Add to cart
  UPDATE = Update quantity
  DELETE = Delete from cart
  ...

Examples:
  TC_AUTH_REG_001   → Authentication - Register #1
  TC_PROD_SEARCH_001 → Product - Search #1
  TC_CHK_PAYMENT_001 → Checkout - Payment #1
```

### 5.2 Định dạng Bug ID
```
BUG_[YYYY]_[NNN]

Examples:
  BUG_2026_001
  BUG_2026_002
  BUG_2026_003 (được fix)
```

### 5.3 Mức độ Nghiêm trọng (Severity)

| Mức | Icon | Định nghĩa | Ví dụ | Impact |
|-----|------|-----------|-------|--------|
| **CRITICAL** | 🔴 | Hệ thống crash, không thể sử dụng | Website down, không đăng nhập được | **Chặn release** |
| **HIGH** | 🔴 | Tính năng chính bị lỗi | Payment failed, không show được sản phẩm | **Phải sửa** |
| **MEDIUM** | 🟡 | Tính năng phụ bị ảnh hưởng | Search chậm, UI bị lệch, text sai | **Nên sửa** |
| **LOW** | 🟢 | Lỗi nhỏ, không ảnh hưởng | Text không căn chỉnh, typo, layout nhỏ | **Có thể sửa sau** |

### 5.4 Độ ưu tiên (Priority)

| Priority | Định nghĩa | Deadline | Action |
|----------|-----------|----------|--------|
| **P0 - BLOCKER** | Phải sửa ngay, chặn release | **24 giờ** | Sửa & retest ngay |
| **P1 - HIGH** | Phải sửa trước release | **3 ngày** | Sắp xếp trong sprint |
| **P2 - MEDIUM** | Nên sửa nhưng không chặn | **1 tuần** | Sắp xếp cho lần sửa sau |
| **P3 - LOW** | Có thể sửa sau | **Flexible** | Backlog |

### 5.5 Test Case Status

| Status | Icon | Mô tả |
|--------|------|-------|
| **PASS** | ✅ | Test passed, kết quả đúng |
| **FAIL** | ❌ | Test failed, kết quả sai |
| **BLOCKED** | 🚫 | Không thể test vì dependency |
| **SKIPPED** | ⏭️ | Bỏ qua test |
| **NOT RUN** | ⏸️ | Chưa chạy test |

---

## ✅ ĐIỀU KIỆN VÀO/RA (ENTRY / EXIT CRITERIA)

### 6.1 Điều kiện bắt đầu kiểm thử (Entry Criteria)

Kiểm thử **CHỈ ĐƯỢC PHÉP** bắt đầu khi:

- ✅ **Test Plan được phê duyệt** bởi QA Lead & PM
- ✅ **Build/Version được deploy** vào UAT environment
- ✅ **Test data được chuẩn bị** (Accounts, Products, Orders)
- ✅ **Environment sẵn sàng**
  - Database restored & working
  - Web server up & accessible
  - All APIs responding
  - Third-party services (email, payment) mocked
- ✅ **Test Cases được viết xong** (24 TCs)
- ✅ **Access được cấp** cho tester (User/Pass, VPN, etc.)
- ✅ **Tools được cà i đặt** (Browser, Email client, Screenshot tools)
- ✅ **RTM được tạo** (Requirements mapped)

### 6.2 Điều kiện kỳ thúc kiểm thử (Exit Criteria)

Kiểm thử **ĐÃ HOÀN THÀNH & SẴN SÀNG RELEASE** khi:

- ✅ **100% Test Cases đã chạy** (24/24 TCs executed)
- ✅ **Pass rate ≥ 85%** (Hiện tại 91.67%)
- ✅ **Không có CRITICAL bug còn open** (1 CRITICAL đã fix)
- ✅ **HIGH bugs ≤ 2** và trong progress fix (2 HIGH, 1 đã fix, 1 in progress)
- ✅ **Requirement traceability 100%** (RTM complete)
- ✅ **Test Report được tạo & approved**
- ✅ **Metrics được tính & documented**
- ✅ **Sign-off từ:**
  - QA Lead ✅
  - Development Lead ✅
  - Product Owner ✅
  - Project Manager ✅
- ✅ **Regression testing completed** (Smoke test after fix)
- ✅ **Documentation hoàn chỉnh**

---

## ⚠️ RỦI RO & BIỆN PHÁP GIẢM THIỂU (RISKS & MITIGATION)

### 7.1 Risk Register

| # | Rủi ro | Xác suất | Tác động | Mức độ | Giảm thiểu |
|---|--------|---------|---------|--------|-----------|
| 1 | Thiếu dữ liệu test | Medium | High | **HIGH** | Chuẩn bị sẵn 10K products + 500 users trước khi test |
| 2 | Environment down | Low | High | **MEDIUM** | Có backup environment, 24/7 IT support standby |
| 3 | Tester bị bệnh/nghỉ | Low | Medium | **MEDIUM** | 3 QA engineers, có thể cross-cover |
| 4 | Bug sót không phát hiện | Medium | High | **HIGH** | Dùng checklist, cross-review, regression test |
| 5 | Timeline delay | Medium | Medium | **MEDIUM** | Tăng QA staff, parallel testing |
| 6 | Payment gateway issue | Low | High | **MEDIUM** | Giả lập payment, không test thực |
| 7 | Scope creep | Medium | Medium | **MEDIUM** | Fixed scope, change control process |
| 8 | Data privacy issue | Low | High | **MEDIUM** | Dummy data, không dùng real customer data |

### 7.2 Contingency Plan

**Nếu environment down:**
- Sử dụng backup environment
- Restore database từ backup
- Contact DevOps untuk support

**Nếu timeline delay:**
- Accelerate critical path items
- Giảm scope (low priority tests)
- Tăng concurrent testers

**Nếu phát hiện critical bugs:**
- Immediate fix & retest
- Delay release nếu cần
- Prepare rollback plan

---

## 👥 VAI TRÒ & TRÁCH NHIỆM (ROLES & RESPONSIBILITIES)

| Vai trò | Người | Trách nhiệm | Availability |
|---------|-------|-----------|-------------|
| **QA Lead** | [Name] | Quản lý test, approve TC, sign-off | Full-time |
| **QA Engineer 1** | [Name] | Module 1-2 testing, bug reporting | Full-time |
| **QA Engineer 2** | [Name] | Module 2-3 testing, bug reporting | Full-time |
| **QA Engineer 3** | [Name] | Module 3 testing, bug reporting | Full-time |
| **Dev Lead** | [Name] | Bug fixing, regression testing | On-call |
| **Product Owner** | [Name] | Requirement clarification, sign-off | On-call |
| **Project Manager** | [Name] | Schedule, risk management, reporting | Full-time |
| **DevOps/IT** | [Name] | Environment setup, monitoring | On-call 24/7 |

### Trách nhiệm chi tiết:

**QA Lead:**
- Lập kế hoạch chi tiết
- Review & approve test cases
- Monitor test progress
- Manage risks & issues
- Write Test Report & Metrics
- Sign-off release

**QA Engineers:**
- Execute test cases
- Report bugs với detail
- Verify bug fixes
- Participate in test meetings

**Dev Lead:**
- Fix bugs promptly
- Provide build versions
- Assist in root cause analysis
- Verify fixes

---

## 📅 LỊCH TRÌNH KIỂM THỬ (TEST SCHEDULE - GIẢ LẬP)

### 8.1 Giai đoạn (Phases)

| Giai đoạn | Thời gian | Người phụ trách | Hoạt động | Deliverable |
|---------|----------|-----------------|-----------|------------|
| **1. Chuẩn bị** | 01-02/03 | QA Lead + DevOps | Lập test plan, setup env, tạo data | Test Plan, Test Data |
| **2. Thiết kế TC** | 03-04/03 | QA Lead + QA Eng | Viết TC, RTM | 24 Test Cases, RTM |
| **3. Chạy test** | 05-11/03 | QA Engineers | Execute TC, report bugs | Test Results, Bug Reports |
| **4. Retest & Fix** | 10-11/03 | QA + Dev | Fix bugs, regression test | Fixed builds |
| **5. Báo cáo** | 12/03 | QA Lead | Tổng hợp report | Test Report, Metrics |

### 8.2 Timeline chi tiết (Weekly)

**Tuần 1 (01-02/03): Preparation**
```
Mon 01/03: Kick-off meeting, Test Plan review
Tue 02/03: Environment setup, Test data preparation
Wed 03/03: Finalize Test Plan, TC design starts
```

**Tuần 2 (03-07/03): Test Execution Phase 1**
```
Wed 03/03-Fri 05/03: TC design (Module 1 & 2)
Sat-Sun (02-03/03): Test data final setup

Mon 05/03: Start Test Execution (Module 1 - Auth)
Tue 06/03: Continue Module 1, Start Module 2 (Product)
Wed 07/03-Fri 08/03: Module 2 & 3 (Checkout)
Bug logging daily, Triage on Thu
```

**Tuần 3 (10-12/03): Retest & Reporting**
```
Mon 10/03: Retest failed TCs, bug verification
Tue 11/03: Final regression testing, completeness check
Wed 12/03: Test Report finalization, Sign-off preparation

Thu 12/03: QA sign-off ✅
Fri 13/03: Release ready (optional release day)
```

### 8.3 Resource Allocation

```
Test Team Schedule:
- QA Lead: 40 hours/week (Planning, monitoring, reporting)
- QA Engineer 1-3: 40 hours/week each (Execution, bugs)
- Dev Team: 50% allocation for bug fixes
- DevOps: On-call support

Total Effort: 200+ hours
Timeline: 2 weeks (intensive)
```

### 8.4 Milestones & Deliverables

| Milestone | Target Date | Status | Deliverable |
|----------|------------|--------|------------|
| Test Plan Approved | 02/03/2026 | ✅ | Test_Plan_v2.0 |
| Test Cases Ready | 04/03/2026 | ✅ | 24 TCs + RTM |
| Test Execution Done | 11/03/2026 | ✅ | Test Results |
| All Bugs Fixed | 11/03/2026 | ✅ | Build v1.0.1 |
| Test Report Final | 12/03/2026 | ✅ | Test_Report_UAT |
| **Go Live** | **13/03/2026** | **Ready** | **Production Release** |

---

## 🛠️ CÔNG CỤ VÀ TÀI NGUYÊN (TOOLS & RESOURCES)

### 9.1 Test Management Tools

| Loại | Tool | Mục đích | Ghi chú |
|------|------|---------|--------|
| **Test Cases** | Excel / Google Sheets | Lưu trữ & quản lý TC | Shared drive |
| **RTM** | Excel / Google Sheets | Ma trận truy vết | Linked to TC |
| **Bug Tracking** | Jira / GitHub Issues | Ghi nhận & track bugs | Real-time updates |
| **Documentation** | Markdown + Word | Report & artifacts | Version control |
| **Screenshots** | Snagit / Windows Snip | Capture errors | Store in shared folder |

### 9.2 Test Environment Tools

| Công cụ | Phiên bản | Mục đích |
|---------|---------|---------|
| **Chrome** | v120 | Browser primary |
| **Firefox** | v121 | Browser secondary |
| **Edge** | v120 | Browser tertiary |
| **Email Client** | Mailinator / TempMail | Verify email flows |
| **VPN** | [Client] | Access UAT network |
| **Database Backup** | PostgreSQL tools | Restore test data |

### 9.3 Template & Checklists

- ✅ Test Case Template (Excel)
- ✅ Bug Report Template (Excel)
- ✅ RTM Template (Excel)
- ✅ Test Execution Checklist
- ✅ Sanity Test Checklist
- ✅ Release Readiness Checklist

---

## 📊 SUCCESS CRITERIA & KPIs

### 10.1 Testing Success Criteria

| Criteria | Target | Actual | Status |
|----------|--------|--------|--------|
| Test Execution Rate | 100% | 100% | ✅ |
| Pass Rate | ≥ 85% | 91.67% | ✅ EXCEED |
| Requirement Coverage | 100% | 100% | ✅ |
| Bug Resolution | > 80% | 87.5% | ✅ EXCEED |
| Critical Issues Open | 0 | 0 | ✅ |
| Quality Score | > 80% | 87% | ✅ EXCEED |

### 10.2 KPIs to Track

```
📈 Test Metrics:
  - Test Case Pass Rate: 91.67%
  - Defect Detection Rate: 33 bugs per 1000 TC
  - Bug Resolution Rate: 87.5%
  - Escaped Defects: 0 (none to production)

📋 Requirement Coverage:
  - Functional Requirements: 100%
  - Non-Functional Requirements: 80%
  - Overall Coverage: 96%

⏱️ Timeline:
  - Schedule Adherence: 100%
  - Planned vs Actual: On-time
```

---

## ✍️ PHÊ DUYỆT (APPROVAL & SIGN-OFF)

### 11.1 Test Plan Approval

| Vai trò | Tên | Ký tên | Ngày | Status |
|---------|------|---------|------|--------|
| **QA Lead** | [Name] | ____________ | 02/03/2026 | ✅ |
| **Product Owner** | [Name] | ____________ | 02/03/2026 | ✅ |
| **Project Manager** | [Name] | ____________ | 02/03/2026 | ✅ |
| **Development Lead** | [Name] | ____________ | 02/03/2026 | ✅ |

### 11.2 Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 01/03/2026 | QA Team | Initial draft |
| 1.5 | 03/03/2026 | QA Lead | Added UC test data section |
| 2.0 | 12/03/2026 | QA Lead | Final approved version |

### 11.3 Document Distribution

- QA Team: ✅ Electronic + Printed
- Development Team: ✅ Electronic
- Product Team: ✅ Electronic
- Management: ✅ Electronic
- Archive: ✅ Version control (Git)

---

## 📌 APPENDIX

### A1. Document References
- [Test Cases](../Test%20Cases/) - Detailed TC specifications
- [RTM](../RTM/) - Requirement Traceability Matrix
- [Bug Report Template](../Bug%20Reports/) - Bug documentation standard
- [Test Report](../Test%20Report/) - Final UAT results

### A2. Contact & Support

**For Test Plan Questions:**
- QA Lead: [Email/Phone]
- DevOps Support: [Email/Phone]
- PM: [Email/Phone]

**Available 24/7 during UAT phase (05-12 March 2026)**

### A3. Acronyms & Terminology

| Acronym | Meaning |
|---------|---------|
| **UAT** | User Acceptance Testing |
| **TC** | Test Case |
| **RTM** | Requirement Traceability Matrix |
| **QA** | Quality Assurance |
| **SLA** | Service Level Agreement |
| **OOB** | Out of Box |
| **DPIA** | Data Privacy Impact Assessment |

---

**END OF TEST PLAN v2.0**

---

**Status:** ✅ APPROVED FOR EXECUTION  
**Release Date:** 02/03/2026  
**Next Review:** 12/03/2026 (Post-UAT)
