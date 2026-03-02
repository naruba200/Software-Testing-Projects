# CHỈ SỐ KIỂM THỬ (TEST METRICS)

**Phiên bản:** 1.0  
**Ngày tạo:** 12/03/2026  
**Giai đoạn:** UAT  
**Dự án:** Website Bán Hàng Online (Ecommerce)

---

## 1. EXECUTIVE SUMMARY - TÓNG HỢP CHỈ SỐ

```
┌─────────────────────────────────────┐
│        TEST METRICS DASHBOARD       │
├─────────────────────────────────────┤
│ Test Execution Progress:   ✅ 100%  │
│ Test Pass Rate:            ✅ 91.67%│
│ Requirement Coverage:      ✅ 100%  │
│ Critical Issues:           ✅ 0     │
│ Go/No-Go Decision:         ✅ GO    │
└─────────────────────────────────────┘
```

---

## 2. TEST EXECUTION METRICS

### 2.1 Test Case Execution Status

| Metric | Value | Target | Status |
|--------|-------|--------|--------|
| Total Test Cases Planned | 24 | 24 | ✅ 100% |
| Total Test Cases Executed | 24 | 24 | ✅ 100% |
| Test Cases Passed | 22 | 22 | ✅ 91.67% |
| Test Cases Failed | 2 | 0 | ⚠️ 8.33% |
| Test Cases Blocked | 0 | 0 | ✅ 0% |
| Test Cases Skipped | 0 | 0 | ✅ 0% |

### 2.2 Test Execution Timeline

| Phase | Duration | Start | End |
|-------|----------|-------|-----|
| Setup & Preparation | 2 days | 03/03 | 04/03 |
| Test Execution | 7 days | 05/03 | 11/03 |
| Bug Fixing & Retest | 2 days | 10/03 | 11/03 |
| Final Sign-off | 1 day | 12/03 | 12/03 |
| **TOTAL** | **12 days** | 03/03 | 12/03 |

### 2.3 Daily Test Execution Progress

```
Day 1 (05/03): ████████░░ 80% (8/10 TC executed)
Day 2 (06/03): ██████████ 100% (10/10 TC executed)
Day 3 (07/03): ████████░░ 70% (7/10 TC executed)
Day 4 (08/03): ████████░░ 75% (3/4 TC executed + bug fixing)
Day 5 (09/03): ██████████ 100% (retest completed)
Day 6 (10/03): ████████░░ 80% (final verification)
Day 7 (11/03): ██████████ 100% (all tests completed)
```

---

## 3. DEFECT METRICS

### 3.1 Bug Summary

| Category | Value |
|----------|-------|
| Total Defects Logged | 8 |
| Defects Closed | 6 |
| Defects Open | 0 |
| Defects In Progress | 1 |
| Defects Deferred | 0 |
| Defects Rejected | 0 |

### 3.2 Defect Density

| Metric | Value | Formula |
|--------|-------|---------|
| **Defect Density** | 0.33 bugs/TC | 8 bugs ÷ 24 TC |
| **Defect Density (Module)** | 0.27 bugs/module | 8 bugs ÷ 3 modules |
| **High Severity Density** | 0.25% bugs/TC | 6 high bugs ÷ 24 TC |

### 3.3 Defect by Severity

| Severity | Count | % | Trend |
|----------|-------|---|-------|
| 🔴 CRITICAL | 1 | 12.5% | ↓ (1 resolved) |
| 🔴 HIGH | 2 | 25% | ↓ (1 resolved) |
| 🟡 MEDIUM | 4 | 50% | ↓ (2 resolved) |
| 🟢 LOW | 1 | 12.5% | ↓ (1 resolved) |
| **TOTAL** | **8** | **100%** | ↓ **87.5% resolved** |

### 3.4 Defect by Priority

| Priority | Count | % |
|----------|-------|---|
| P0 - BLOCKER | 1 | 12.5% |
| P1 - HIGH | 2 | 25% |
| P2 - MEDIUM | 4 | 50% |
| P3 - LOW | 1 | 12.5% |

### 3.5 Defect by Module

| Module | Defects | TC Count | Density |
|--------|---------|----------|---------|
| Authentication | 1 | 8 | 0.125 |
| Product & Cart | 4 | 7 | 0.571 |
| Checkout | 3 | 9 | 0.333 |
| **TOTAL** | **8** | **24** | **0.333** |

### 3.6 Defect Resolution Metrics

| Metric | Value | Target | Status |
|--------|-------|--------|--------|
| Defects Resolved | 6 | 6 | ✅ |
| Resolution Rate | 87.5% | > 80% | ✅ |
| Avg Resolution Time | 1.2 days | < 2 days | ✅ |
| First Time Fix Rate | 85% | > 80% | ✅ |

---

## 4. REQUIREMENT COVERAGE METRICS

### 4.1 Requirement Coverage

| Metric | Value | Target | Status |
|--------|-------|--------|--------|
| Total Requirements | 16 | 16 | ✅ |
| Requirements Covered | 16 | 16 | ✅ 100% |
| Requirements Uncovered | 0 | 0 | ✅ |
| Requirements Traced | 16 | 16 | ✅ 100% |

### 4.2 Traceability Matrix (RTM) Status

| Requirement | Linked TC | Status |
|-------------|-----------|--------|
| R1 | TC_AUTH_REG_001 | ✅ |
| R2 | TC_AUTH_REG_002 | ✅ |
| R3 | TC_AUTH_REG_003 | ✅ |
| R4 | TC_AUTH_LOGIN_001 | ✅ |
| R5 | TC_AUTH_LOGIN_002, TC_AUTH_LOGIN_003 | ✅ |
| R6 | TC_AUTH_FP_001 | ✅ |
| R7 | TC_PROD_SEARCH_001, TC_PROD_SEARCH_002 | ✅ |
| R8 | TC_PROD_FILTER_001 | ✅ |
| R9 | TC_PROD_DETAIL_001 | ✅ |
| R10 | TC_CART_ADD_001 | ✅ |
| R11 | TC_CART_UPDATE_001 | ✅ |
| R12 | TC_CART_DELETE_001 | ✅ |
| R13 | TC_CHK_ADDRESS_001, TC_CHK_ADDRESS_002 | ✅ |
| R14 | TC_CHK_PAYMENT_001, TC_CHK_PAYMENT_002 | ✅ |
| R15 | TC_CHK_ORDER_001, TC_CHK_ORDER_002 | ✅ |
| R16 | TC_CHK_HISTORY_001, TC_CHK_HISTORY_002 | ✅ |

### 4.3 Coverage by Module

| Module | Requirements | Coverage | Status |
|--------|-------------|----------|--------|
| Authentication | 6 | 100% | ✅ |
| Product & Cart | 6 | 100% | ✅ |
| Checkout | 4 | 100% | ✅ |
| **TOTAL** | **16** | **100%** | ✅ |

---

## 5. QUALITY METRICS

### 5.1 Pass Rate Analysis

```
Module 1 - Authentication
████████████████████ 100% (8/8 passed)

Module 2 - Product & Cart
███████████████████░ 100% (7/7 passed)

Module 3 - Checkout
████████████████░░░░ 77.78% (7/9 passed)

OVERALL
███████████████████░ 91.67% (22/24 passed)
```

### 5.2 Quality Trend

| Week | Total TC | Passed | Pass Rate | Trend |
|------|----------|--------|-----------|-------|
| Week 1 | 24 | 22 | 91.67% | ↑ Improving |
| (baseline) | - | - | - | - |

### 5.3 Test Effectiveness

| Metric | Value | Interpretation |
|--------|-------|-----------------|
| Defect Detection Rate | 33% | 1 bug per 3 TC - GOOD |
| Critical Issue Rate | 12.5% | 1 critical bug - ACCEPTABLE |
| Escape Rate | 0% | No bugs escaped to production - EXCELLENT |

---

## 6. TEST EFFORT METRICS

### 6.1 Resource Allocation

| Role | Count | Hours | Cost (estimate) |
|------|-------|-------|-----------------|
| QA Lead | 1 | 40 | $2,000 |
| QA Engineer | 3 | 120 | $4,500 |
| Developer (for fixes) | 2 | 30 | $1,500 |
| **TOTAL** | **6** | **190** | **$8,000** |

### 6.2 Test Effort Distribution

| Activity | Hours | % |
|----------|-------|---|
| Test Planning & Setup | 16 | 8.4% |
| Test Case Design | 24 | 12.6% |
| Test Execution | 96 | 50.5% |
| Bug Reporting & Tracking | 32 | 16.8% |
| Defect Verification | 22 | 11.6% |
| **TOTAL** | **190** | **100%** |

### 6.3 Productivity Metrics

| Metric | Value |
|--------|-------|
| TC per QA per day | 3.4 |
| Bugs per 100 TC | 33 |
| Time per TC execution | 0.4 hours |
| Time per bug report | 4 hours |

---

## 7. RISK METRICS

### 7.1 Risk Assessment

| Area | Risk Level | Mitigation |
|------|-----------|-----------|
| High Severity Issues | 🟢 LOW | 1 critical bug resolved |
| Performance | 🟡 MEDIUM | Monitor in production |
| Payment Gateway | 🟡 MEDIUM | 24/7 support on standby |
| Browser Compatibility | 🟢 LOW | Tested on 3 major browsers |
| Mobile Support | 🟢 LOW | Responsive design verified |

### 7.2 Release Readiness Score

```
Functionality:        ████████████████░░ 90%
Performance:          ████████████░░░░░░ 75%
Compatibility:        ██████████████████ 95%
Documentation:        ██████████████░░░░ 80%
User Acceptance:      ██████████████████ 95%

Overall Release Score: 87% - READY FOR RELEASE ✅
```

---

## 8. TEST ENVIRONMENT METRICS

### 8.1 Test Lab Setup

| Component | Count | Status |
|-----------|-------|--------|
| Test Machines | 5 | ✅ |
| Database Instances | 2 | ✅ |
| Test Accounts | 50 | ✅ |
| Test Data Sets | 3 | ✅ |

### 8.2 Environment Availability

| Week | Uptime | Issues |
|------|--------|--------|
| Week 1 | 98% | 1 DB restart |
| Week 2 | 100% | 0 |
| **Average** | **99%** | **1 issue** |

---

## 9. TREND ANALYSIS

### 9.1 Defect Trend (Daily)

```
Day 1: ▲▲▲▲▲ 5 bugs found (peak)
Day 2: ▲▲ 2 bugs found
Day 3: ▼▼▼ 3 bugs fixed
Day 4: ▼▼ 2 bugs fixed
Day 5: ▼ 1 bug fixed
Day 6: ∼ 0 new bugs
Day 7: ∼ 0 new bugs
```

### 9.2 Pass Rate Trend

```
Day 1: ██████░░░░ 60% (6/10 TC)
Day 2: ██████████ 100% (10/10 TC)
Day 3: ███████░░░ 70% (7/10 TC)
Day 4: ████████░░ 80% (8/10 TC)
Day 5: ██████████ 100% (10/10 TC)
Day 6: ██████████ 100% (10/10 TC)
Day 7: ███████████ 91.67% (overall)
```

---

## 10. GO/NO-GO DECISION

### 10.1 Release Criteria

| Criteria | Status | Comments |
|----------|--------|----------|
| All requirements covered | ✅ YES | 100% RTM completion |
| Pass Rate > 85% | ✅ YES | 91.67% achieved |
| No CRITICAL bugs open | ✅ YES | 1 critical resolved |
| Test Report completed | ✅ YES | Approved |
| Sign-off obtained | ✅ YES | All stakeholders agreed |

### 10.2 Decision Matrix

| Factor | Weight | Score | Result |
|--------|--------|-------|--------|
| Functionality | 40% | 95/100 | 38 |
| Quality | 25% | 92/100 | 23 |
| Risk | 20% | 85/100 | 17 |
| Timeline | 15% | 90/100 | 13.5 |
| **TOTAL SCORE** | **100%** | - | **91.5/100** |

### 10.3 FINAL DECISION

```
╔═════════════════════════════════════╗
║  ✅ GO FOR RELEASE                  ║
║                                     ║
║  Score: 91.5/100 (Grade: A)         ║
║  Confidence Level: 95%              ║
║  Ready for Production: YES          ║
╚═════════════════════════════════════╝
```

### Điều kiện cho Release:
✅ Sửa xong BUG_2026_004 (Payment timeout)  
✅ Conduct final smoke test  
✅ Full regression test  
✅ Performance monitoring setup  
✅ Rollback plan prepared  

---

## 11. APPENDIX

### 11.1 KPI Summary

| KPI | Target | Actual | Status |
|-----|--------|--------|--------|
| Test Coverage | 100% | 100% | ✅ |
| Pass Rate | 90% | 91.67% | ✅ |
| Defect Density | < 50 per 1000 TC | 33 per 1000 TC | ✅ |
| Critical Issues | 0 | 1 (resolved) | ✅ |
| Resolution Rate | 80% | 87.5% | ✅ |

### 11.2 Approval Sign-off

| Role | Name | Signature | Date |
|------|------|-----------|------|
| QA Lead | [Name] | _____ | 12/03/2026 |
| Test Manager | [Name] | _____ | 12/03/2026 |
| Project Manager | [Name] | _____ | 12/03/2026 |
| Product Owner | [Name] | _____ | 12/03/2026 |

---

**END OF TEST METRICS**
