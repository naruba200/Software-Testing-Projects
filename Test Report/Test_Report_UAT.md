# BÁOMCÁO KIỂM THỬ (TEST REPORT)

**Phiên bản:** 1.0  
**Ngày tạo:** 12/03/2026  
**Giai đoạn:** UAT (User Acceptance Testing)  
**Hệ thống:** Website Bán Hàng Online (Ecommerce)  
**Tác giả:** QA Lead  
**Trạng thái:** APPROVED

---

## EXECUTIVE SUMMARY

Báo cáo kiểm thử tổng hợp kết quả kiểm thử hệ thống Website Bán Hàng Online trong giai đoạn UAT từ ngày 05/03/2026 đến 11/03/2026.

### Kết luận chung:
**✅ HỆ THỐNG SẴN SÀNG CHO RELEASE**

---

## 1. THÔNG TIN CHUNG

| Thông tin | Chi tiết |
|----------|---------|
| **Tên dự án** | Website Bán Hàng Online - Ecommerce |
| **Version tested** | 1.0.0 |
| **Test Period** | 05/03/2026 - 11/03/2026 |
| **Total Test Days** | 7 ngày |
| **Build Number** | Build_2026_001 |
| **Browser Tested** | Chrome, Firefox, Edge |
| **Device** | Desktop, Mobile |
| **OS** | Windows, macOS, Linux |

---

## 2. SCOPE OF TESTING

### Các Module được test:
- ✅ Module 1 - Authentication (Xác thực người dùng)
- ✅ Module 2 - Product & Cart (Sản phẩm & Giỏ hàng)
- ✅ Module 3 - Checkout (Thanh toán)

### Loại kiểm thử:
- ✅ Functional Testing
- ✅ Regression Testing
- ✅ Integration Testing
- ⚠️ Performance Testing (Partial)
- ⚠️ Security Testing (Partial)

---

## 3. TEST EXECUTION SUMMARY

### Thống kê Test Case:

| Chỉ số | Số lượng | % |
|-------|---------|---|
| **Total Test Cases** | 24 | 100% |
| **Test Cases Passed** | 22 | 91.67% |
| **Test Cases Failed** | 2 | 8.33% |
| **Test Cases Skipped** | 0 | 0% |
| **Test Cases Not Run** | 0 | 0% |

### Chi tiết kết quả theo Module:

#### Module 1 - Authentication
| KPI | Value |
|-----|-------|
| Total TC | 8 |
| Passed | 8 |
| Failed | 0 |
| Pass Rate | 100% |

#### Module 2 - Product & Cart
| KPI | Value |
|-----|-------|
| Total TC | 7 |
| Passed | 7 |
| Failed | 0 |
| Pass Rate | 100% |

#### Module 3 - Checkout
| KPI | Value |
|-----|-------|
| Total TC | 9 |
| Passed | 7 |
| Failed | 2 |
| Pass Rate | 77.78% |

### Chi tiết các test case thất bại:

#### Thất bại 1:
- **TC ID**: TC_CHK_Payment_002
- **Issue**: Visa payment simulation timeout
- **Impact**: Medium
- **Status**: In Progress (được fix ngay)

#### Thất bại 2:
- **TC ID**: TC_CHK_History_002
- **Issue**: Order detail page slow loading
- **Impact**: Medium
- **Status**: Resolved (thêm caching)

---

## 4. BUG SUMMARY

### Tổng số Bug phát hiện: 8

| Severity | Open | In Progress | Resolved | Closed | Total |
|----------|------|-------------|----------|--------|-------|
| **CRITICAL** | 0 | 0 | 1 | 0 | 1 |
| **HIGH** | 0 | 1 | 1 | 0 | 2 |
| **MEDIUM** | 0 | 0 | 2 | 2 | 4 |
| **LOW** | 0 | 0 | 1 | 0 | 1 |
| **TOTAL** | **0** | **1** | **5** | **2** | **8** |

### Bug By Module:

| Module | Critical | High | Medium | Low | Total |
|--------|----------|------|--------|-----|-------|
| Authentication | 0 | 0 | 1 | 0 | 1 |
| Product & Cart | 0 | 1 | 2 | 1 | 4 |
| Checkout | 1 | 1 | 1 | 0 | 3 |
| **TOTAL** | **1** | **2** | **4** | **1** | **8** |

### Bug Status Trend:

```
Day 1-2 (05-06/03): Phát hiện 5 bug
Day 3-4 (07-08/03): Phát hiện 2 bug, fix 3 bug
Day 5-6 (09-10/03): Phát hiện 1 bug, fix 2 bug
Day 7   (11/03):    Verify fixes: 2 chưa fix, 6 đã fix
```

### Chi tiết Bug chưa fix:

| Bug ID | Title | Severity | Module | Status |
|--------|-------|----------|--------|--------|
| BUG_2026_004 | Visa payment timeout occasionally | HIGH | Checkout | In Progress |

---

## 5. TEST COVERAGE

### Coverage by Module:

| Module | Requirements | TC Count | Coverage | Status |
|--------|-------------|----------|----------|--------|
| Authentication | 6 | 8 | 100% | ✅ |
| Product & Cart | 6 | 7 | 100% | ✅ |
| Checkout | 4 | 9 | 100% | ✅ |
| **TOTAL** | **16** | **24** | **100%** | ✅ |

### Browser Coverage:

| Browser | Version | Status | Notes |
|---------|---------|--------|-------|
| Chrome | 120 | ✅ PASS | Primary browser |
| Firefox | 121 | ✅ PASS | Good compatibility |
| Edge | 120 | ✅ PASS | Minor CSS issues fixed |
| Safari | 17 | ⚠️ PARTIAL | iOS tested only |

### Device Coverage:

| Device | Resolution | Status | Notes |
|--------|-----------|--------|-------|
| Desktop | 1920x1080 | ✅ PASS | Primary |
| Tablet | 768x1024 | ✅ PASS | iPad tested |
| Mobile | 375x667 | ✅ PASS | iPhone tested |
| Mobile | 360x720 | ✅ PASS | Android tested |

---

## 6. QUALITY METRICS

### Test Effectiveness:

| Metric | Value | Target | Status |
|--------|-------|--------|--------|
| Defect Detection Rate | 8 bugs / 24 TC = 33% | > 20% | ✅ GOOD |
| Pass Rate | 91.67% | > 85% | ✅ GOOD |
| Severity Distribution | 1 CRITICAL (12.5%) | < 15% | ✅ GOOD |
| Requirement Coverage | 100% | 100% | ✅ EXCELLENT |

### Performance Metrics:

| Metric | Value | Target | Status |
|--------|-------|--------|--------|
| Avg Test Execution Time | 1.5 hours/QA | - | ✅ GOOD |
| Bug Fix Turnaround | 1.2 days avg | < 2 days | ✅ GOOD |
| Test Case Reusability | 85% | > 80% | ✅ GOOD |

---

## 7. RECOMMENDATIONS

### Để sẵn sàng cho Release:

✅ **MUST HAVE (Critical)**:
- [ ] Fix BUG_2026_004 (Visa payment timeout)

✅ **SHOULD HAVE (High Priority)**:
- [ ] Performance optimization cho Search feature
- [ ] Add logging cho Checkout process

⚠️ **NICE TO HAVE (Medium Priority)**:
- [ ] Add unit tests cho payment module
- [ ] Improve error messages

### Testing cần cải thiện:

1. **Performance Testing**: Cần conduct load test trước production
2. **Security Testing**: Cần security audit cho payment module
3. **User Acceptance Testing**: Cần feedback từ end users
4. **API Testing**: Cần test API endpoints riêng biệt

---

## 8. RISKS & MITIGATION

| Risk | Probability | Impact | Mitigation |
|------|-----------|--------|-----------|
| Visa payment failure in production | High | High | Rollback plan, 24/7 support |
| Performance degradation with load | Medium | High | Load test, caching strategy |
| User adoption delay | Low | Medium | User training, documentation |

---

## 9. SIGN-OFF

### Kiểm thử đã hoàn thành với kết luận:

**✅ APPROVED FOR RELEASE**

Các điều kiện sau đã được thỏa mãn:
- ✅ Tất cả test cases được chạy
- ✅ 100% requirement coverage
- ✅ Không có CRITICAL bug còn open
- ✅ Chỉ 1 HIGH bug, đang được fix
- ✅ Performance trong acceptable range
- ✅ Browser compatibility OK

### Phê duyệt:

| Vị trí | Tên | Chữ ký | Ngày |
|--------|------|--------|------|
| **QA Lead** | [Tên QA Lead] | _____ | 12/03/2026 |
| **Development Lead** | [Tên Dev Lead] | _____ | 12/03/2026 |
| **Product Owner** | [Tên PO] | _____ | 12/03/2026 |
| **Project Manager** | [Tên PM] | _____ | 12/03/2026 |

---

## 10. APPENDIX

### A. Test Environment Details
- **Server**: AWS t3.medium instance
- **Database**: PostgreSQL 14
- **Browser Stack**: BrowserStack
- **Test Data**: 10,000 products, 500 users

### B. Test Team
- **QA Lead**: 1 person
- **QA Engineer**: 3 persons
- **Total QA Hours**: 168 hours

### C. Test Tools Used
- Test Management: Excel & Jira
- Automation: Selenium (partial)
- Bug Tracking: Jira
- Documentation: Confluence

### D. Known Issues for Future Release
1. Search performance with > 100K products
2. Mobile app compatibility
3. Multi-language support

---

**END OF TEST REPORT**
