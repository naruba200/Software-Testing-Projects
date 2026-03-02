# KẾ HOẠCH KIỂM THỬ (TEST PLAN)
## Hệ Thống Website Bán Hàng Online - Ecommerce

**Phiên bản:** 2.0  
**Ngày tạo:** 01/03/2026  
**Ngày cập nhật:** 12/03/2026  
**Tác giả:** QA Team  
**Trạng thái:**  Phê duyệt  
**Mã dự án:** ECOM-2026-Q1

---

## 1 GIỚI THIỆU (INTRODUCTION)

### 1.1 Tổng quan dự án

Dự án kiểm thử Manual QA cho hệ thống **Website Bán Hàng Online (Ecommerce v1.0)** nhằm đảm bảo chất lượng sản phẩm trước khi triển khai production.

### 1.2 Mục tiêu kiểm thử (Test Objectives)

Kiểm thử hệ thống website bán hàng online (Ecommerce) nhằm:

 **Điểm mục tiêu chính:**
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

## 2 PHẠM VI KIỂM THỬ (SCOPE)

### 2.1 **TRONG PHẠM VI (IN-SCOPE)** 

#### **Module 1 - Xác thực người dùng (Authentication)**
-  Đăng ký tài khoản (Email validation, Password strength)
-  Đăng nhập (Credential verification, Session management)
-  Quên mật khẩu (Email reset flow)
-  Đăng xuất (Session termination)
- Form validation & Error handling

#### **Module 2 - Sản phẩm & Giỏ hàng (Product & Cart)**
-  Tìm kiếm sản phẩm (Search functionality)
-  Lọc theo giá/danh mục (Filter logic)
-  Xem chi tiết sản phẩm (Display accuracy)
-  Thêm sản phẩm vào giỏ (Cart operations)
-  Cập nhật số lượng (Quantity adjustment)
-  Xoá sản phẩm khỏi giỏ (Remove functionality)
-  Tính toán tổng giá (Price calculation)

#### **Module 3 - Thanh toán (Checkout)**
-  Nhập địa chỉ giao hàng (Address validation)
-  Chọn phương thức thanh toán (COD & Visa simulation)
-  Đặt hàng (Order creation & confirmation)
-  Xem lịch sử đơn hàng (Order history display)
-  Email notifications

#### **Loại kiểm thử (Test Types):**
-  Functional Testing (Chức năng chính)
-  UI Testing (Giao diện cơ bản)
-  Regression Testing (Kiểm thử hồi quy - Smoke)
-  Data Validation (Kiểm thử dữ liệu)
-  Error Handling (Kiểm thử lỗi)

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

## 3 PHƯƠNG PHÁP KIỂM THỬ (TEST APPROACH)
3.1 Chiến lược kiểm thử (Testing Strategy)
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

## 4 MÔI TRƯỜNG KIỂM THỬ (TEST ENVIRONMENT)
### 4.1 Thông số kỹ thuật (Hardware & Software)
Trình duyệt: Google Chrome (phiên bản mới nhất)
Hệ điều hành: Windows 10/11
Server: Localhost 
Database: Dữ liệu giả lập
Tài khoản test: Email giả lập 
Thanh toán: COD và Visa giả lập


## 5 ĐIỀU KIỆN VÀO/RA (ENTRY / EXIT CRITERIA)

### 5.1 Điều kiện bắt đầu kiểm thử (Entry Criteria)

Kiểm thử **CHỈ ĐƯỢC PHÉP** bắt đầu khi:

-  **Test Plan được phê duyệt** bởi QA Lead & PM
-  **Build/Version được deploy** vào UAT environment
-  **Test data được chuẩn bị** (Accounts, Products, Orders)
-  **Environment sẵn sàng**
  - Database restored & working
  - Web server up & accessible
  - All APIs responding
  - Third-party services (email, payment) mocked
-  **Test Cases được viết xong** (24 TCs)
-  **Access được cấp** cho tester (User/Pass, VPN, etc.)
-  **Tools được cà i đặt** (Browser, Email client, Screenshot tools)
-  **RTM được tạo** (Requirements mapped)

### 5.2 Điều kiện kỳ thúc kiểm thử (Exit Criteria)

Kiểm thử **ĐÃ HOÀN THÀNH & SẴN SÀNG RELEASE** khi:

-  **100% Test Cases đã chạy** (24/24 TCs executed)
-  **Pass rate ≥ 85%** (Hiện tại 91.67%)
-  **Không có CRITICAL bug còn open** (1 CRITICAL đã fix)
-  **HIGH bugs ≤ 2** và trong progress fix (2 HIGH, 1 đã fix, 1 in progress)
-  **Requirement traceability 100%** (RTM complete)
-  **Test Report được tạo & approved**
-  **Metrics được tính & documented**
-  **Sign-off từ:**
  - QA Lead 
  - Development Lead 
  - Product Owner 
  - Project Manager 
-  **Regression testing completed** (Smoke test after fix)
-  **Documentation hoàn chỉnh**

---

## ⚠️6 RỦI RO & BIỆN PHÁP GIẢM THIỂU (RISKS & MITIGATION)

### 6.1 Risk Register

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

### 6.2 Contingency Plan

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

## 7 VAI TRÒ & TRÁCH NHIỆM (ROLES & RESPONSIBILITIES)

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

Thu 12/03: QA sign-off 
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
| Test Plan Approved | 02/03/2026 |  | Test_Plan_v2.0 |
| Test Cases Ready | 04/03/2026 |  | 24 TCs + RTM |
| Test Execution Done | 11/03/2026 |  | Test Results |
| All Bugs Fixed | 11/03/2026 |  | Build v1.0.1 |
| Test Report Final | 12/03/2026 |  | Test_Report_UAT |
| **Go Live** | **13/03/2026** | **Ready** | **Production Release** |
