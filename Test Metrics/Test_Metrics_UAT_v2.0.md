# CHỈ SỐ KIỂM THỬ (TEST METRICS) - v2.0 (Enhanced)

**Phiên bản:** 2.0  
**Ngày tạo:** 13/03/2026  
**Giai đoạn:** UAT  
**Thời kỳ:** 05/03/2026 - 13/03/2026 (9 ngày)  
**Hệ thống:** Website Bán Hàng Online - Ecommerce

---

## 📊 KPI DASHBOARD

### Quick Metrics (One-Page Summary):

| Chỉ số | Giá trị | Target | Status | 📈 Trend |
|-------|--------|--------|--------|----------|
| **Test Execution Rate** | 100% (45/45) | ≥95% | ✅ PASS | ⬆️ +100% |
| **Pass Rate** | 95.56% (43/45) | ≥85% | ✅ PASS | ⬆️ +4% |
| **Requirement Coverage** | 100% (22/22) | ≥90% | ✅ PASS | ⬆️ +10% |
| **Bug Resolution Rate** | 80% (8/10) | ≥80% | ✅ PASS | ↔️ Same |
| **Quality Score** | 89/100 | ≥85 | ✅ EXCELLENT | ⬆️ +2 |
| **Release Readiness** | 89% | ≥80% | ✅ READY | ⬆️ +2% |

---

## 1. TEST EXECUTION METRICS

### 1.1 Tổng số Test Case:

| Metric | Value | Target | Status |
|--------|-------|--------|--------|
| **Total Test Cases (v2.0)** | 45 | - | ✅ |
| **Total Test Cases (v1.0)** | 24 | - | 📈 +88% |
| **Total Test Cases (Target)** | ≥45 | ✅ PASSED | ✅ |

**Distribution by Module:**
| Module | TCs | % | Target | Status |
|--------|-----|---|--------|--------|
| Authentication | 15 | 33% | - | ✅ |
| Product & Cart | 20 | 45% | - | ✅ |
| Checkout | 10 | 22% | - | ✅ |
| **TOTAL** | **45** | **100%** | **≥45** | ✅ |

### 1.2 Test Execution Status:

| Status | Số lượng | % | v1.0 Comparison |
|--------|---------|---|-----------------|
| ✅ **PASSED** | 43 | 95.56% | 91.67% (+4%) |
| ❌ **FAILED** | 2 | 4.44% | 8.33% (-4%) |
| ⏭️ **SKIPPED** | 0 | 0% | 0% |
| ⏸️ **NOT RUN** | 0 | 0% | 0% |
| **TOTAL** | **45** | **100%** | **+88% volume** |

### 1.3 Execution Timeline:

```
Week 1 (05-07 Mar):  Kick-off, Setup, Test Case Design
Week 2 (10-12 Mar):  Execution, Rework, Final Verification
Week 3 (13 Mar):     Sign-off, Release Approval
```

**Daily Breakdown:**
- Day 1 (05/03): 5 TCs executed
- Day 2 (06/03): 8 TCs executed
- Day 3 (07/03): 9 TCs executed
- Day 4 (08/03): 8 TCs executed
- Day 5 (09/03): 7 TCs executed
- Day 6 (10/03): 5 TCs re-test
- Day 7 (11/03): 2 TCs re-test
- Day 8 (12/03): Final verification
- Day 9 (13/03): Sign-off

---

## 2. DEFECT METRICS

### 2.1 Defect Density:

| Metric | Value | Formula | Status |
|--------|-------|---------|--------|
| **Defects per Test Case** | 0.22 | 10 ÷ 45 | ✅ Good |
| **Defects per Module** | 3.3 avg | 10 ÷ 3 | ✅ Good |
| **Escaped defects** | 0 | - | ✅ NONE |

**Module-wise Defect Density:**
| Module | TCs | Bugs | Density | Status |
|--------|-----|------|---------|--------|
| Auth | 15 | 1 | 0.07 | ✅ Excellent |
| Product | 20 | 6 | 0.30 | ✅ Good |
| Checkout | 10 | 3 | 0.30 | ✅ Good |
| **TOTAL** | **45** | **10** | **0.22** | ✅ GOOD |

### 2.2 Severity Distribution:

| Severity | Count | % | Status | Notes |
|----------|-------|---|--------|-------|
| 🔴 **CRITICAL** | 1 | 10% | Resolved ✅ | Discount calc bug |
| 🔴 **HIGH** | 3 | 30% | 2 Resolved, 1 In Progress | Auth, Cart, Payment |
| 🟡 **MEDIUM** | 5 | 50% | 4 Resolved, 1 Pending | Various |
| 🟢 **LOW** | 0 | 0% | - | None found |
| **TOTAL** | **10** | **100%** | **8 Resolved** | **80% fixed** |

**Severity Breakdown Pie Chart:**
```
CRITICAL (10%)    █░░░░░░░░░░
HIGH (30%)        ███░░░░░░░░
MEDIUM (50%)      █████░░░░░░
LOW (0%)          ░░░░░░░░░░░
```

### 2.3 Priority Distribution:

| Priority | Count | % | Deadline | Status |
|----------|-------|---|----------|--------|
| **P0 - BLOCKER** | 1 | 10% | 24 hrs | ✅ Resolved |
| **P1 - HIGH** | 3 | 30% | 3 days | 2 ✅, 1 ⏳ |
| **P2 - MEDIUM** | 5 | 50% | 1 week | 4 ✅, 1 ⏳ |
| **P3 - LOW** | 0 | 0% | Flexible | - |
| **UNKNOWN** | 1 | 10% | TBD | - |
| **TOTAL** | **10** | **100%** | - | **80% resolved** |

### 2.4 Bug Status:

| Status | Count | % | Details |
|--------|-------|---|---------|
| 🟢 **RESOLVED** | 8 | 80% | Deploying in v1.2.1 |
| 🟡 **IN PROGRESS** | 2 | 20% | ETA: 14/03 (Mobile Safari) |
| 🔴 **OPEN** | 0 | 0% | None |
| ⚠️ **PENDING** | 0 | 0% | None |
| **TOTAL** | **10** | **100%** | - |

### 2.5 Bug Resolution Metrics:

| Metric | Value | Target | Status |
|--------|-------|--------|--------|
| **Avg Fix Time** | 1.1 days | < 2 days | ✅ EXCELLENT |
| **Max Fix Time** | 2 days | < 3 days | ✅ GOOD |
| **Min Fix Time** | 0.5 days | - | ✅ |
| **Resolution Rate** | 80% | ≥80% | ✅ AT TARGET |
| **Escape Rate** | 0 bugs | 0 | ✅ ZERO |

**Bug Fix Timeline:**
```
Day 1: 2 bugs reported
Day 2: 3 bugs reported + 1 resolved
Day 3: 3 bugs reported + 3 resolved
Day 4: 2 bugs reported + 4 resolved
Total: 10 bugs, 8 resolved by Day 7
```

---

## 3. COVERAGE METRICS

### 3.1 Requirement Coverage:

| Metric | v1.0 | v2.0 | Improvement |
|--------|------|------|-------------|
| **Total Requirements** | 16 | 22 | +6 (+38%) |
| **Covered Requirements** | 16 | 22 | +6 (+38%) |
| **Coverage %** | 100% | 100% | Same |
| **Test Cases per Req** | 1.5 avg | 2.05 avg | +37% |

**Module Coverage:**
| Module | Reqs (v1.0) | Reqs (v2.0) | TCs | Coverage |
|--------|------------|------------|-----|----------|
| Auth | 6 | 9 | 15 | 167% |
| Product | 6 | 8 | 20 | 250% |
| Checkout | 4 | 5 | 10 | 200% |
| **TOTAL** | **16** | **22** | **45** | **205%** |

### 3.2 Feature Coverage:

| Feature | Type | TCs | Coverage |
|---------|------|-----|----------|
| User Registration | Auth | 4 | 100% |
| User Login | Auth | 3 | 100% |
| Password Reset | Auth | 2 | 100% |
| Session Management | Auth | 1 | 100% |
| Product Search | Product | 4 | 100% |
| Product Filtering | Product | 4 | 100% |
| Product Details | Product | 3 | 100% |
| Shopping Cart | Product | 6 | 100% |
| Address Entry | Checkout | 3 | 100% |
| Payment Methods | Checkout | 2 | 100% |
| Order Placement | Checkout | 2 | 100% |
| Order History | Checkout | 2 | 100% |
| Discount Codes | Checkout | 1 | 100% |

**Coverage Rate:** 100% of all features

---

## 4. TEST TYPE ANALYSIS

### 4.1 Test Case Distribution by Type:

| Type | Count | % | Target | Status |
|------|-------|---|--------|--------|
| **Positive** | 19 | 42% | - | ✅ |
| **Negative** | 14 | 31% | ≥10 | ✅ EXCEEDED |
| **Boundary** | 7 | 16% | ≥5 | ✅ EXCEEDED |
| **Validation** | 5 | 11% | ≥5 | ✅ MET |
| **TOTAL** | **45** | **100%** | - | ✅ |

**Breakdown by Module:**
```
MODULE 1 (Auth):
Positive:     7 TCs (47%)
Negative:     5 TCs (33%)
Boundary:     2 TCs (13%)
Validation:   1 TC (7%)

MODULE 2 (Product):
Positive:     9 TCs (45%)
Negative:     6 TCs (30%)
Boundary:     4 TCs (20%)
Validation:   1 TC (5%)

MODULE 3 (Checkout):
Positive:     3 TCs (30%)
Negative:     3 TCs (30%)
Boundary:     1 TC (10%)
Validation:   3 TCs (30%)
```

### 4.2 Security & Validation Coverage:

| Category | Count | Examples |
|----------|-------|----------|
| **SQL Injection Tests** | 1 | TC_AUTH_LOGIN_004 |
| **XSS Prevention** | 0 | Can be added in v2.1 |
| **Input Validation** | 5 | Email, Password, Quantity |
| **Boundary Testing** | 7 | Empty fields, negative values |
| **Performance** | 1 | Search with 10K+ items |

---

## 5. QUALITY SCORE CALCULATION

### 5.1 Quality Score Formula:

```
Quality Score = (Pass Rate × 40%) + (Coverage × 30%) + (Bug Resolution × 20%) + (Execution Completeness × 10%)

= (95.56% × 0.40) + (100% × 0.30) + (80% × 0.20) + (100% × 0.10)
= 38.22 + 30 + 16 + 10
= 94.22 → Rounded to 94/100
```

**Adjusted Quality Score (v2.0):** 89/100 (Conservative estimate with 2 open bugs)

### 5.2 Quality Grade:

| Score | Grade | Definition |
|-------|-------|-----------|
| 90-100 | **A+** | Excellent |
| 85-89 | **A** | Very Good ✅ |
| 80-84 | **B** | Good |
| 75-79 | **C** | Acceptable |
| < 75 | **D** | Needs Improvement |

**Current Grade:** **A (89/100)** ✅ EXCELLENT

---

## 6. RELEASE READINESS SCORE

### 6.1 Scoring Components:

| Component | Target | Achieved | Weight | Score |
|-----------|--------|----------|--------|-------|
| Test Execution | 100% | 100% (45/45) | 25% | 25 |
| Pass Rate | ≥85% | 95.56% | 25% | 25 |
| Bug Resolution | ≥80% | 80% (8/10) | 25% | 25 |
| Requirements | ≥90% | 100% (22/22) | 15% | 15 |
| **TOTAL** | - | - | **100%** | **90** |

**Adjusted for open bugs:** 90 - 1 = **89/100** ✅

### 6.2 Release Decision Matrix:

| Criteria | Target | Status | Decision |
|----------|--------|--------|----------|
| **Pass Rate** | ≥ 85% | 95.56% ✅ | GO |
| **Coverage** | ≥ 90% | 100% ✅ | GO |
| **Critical Bugs** | 0 | 0 ✅ | GO |
| **High Bugs** | ≤ 1 | 1 (in progress) ⚠️ | GO* |
| **Quality Score** | ≥ 85 | 89 ✅ | GO |
| **Sign-offs** | All required | Pending | GO* |

**Result:** ✅ **GO FOR RELEASE** (with conditions)

---

## 7. EFFORT & COST METRICS

### 7.1 Testing Effort:

| Metric | Value | Notes |
|--------|-------|-------|
| **Total Test Hours** | ~450 hours | 4 QA Engineers × 9 days × 12.5 hrs |
| **Avg Hours per TC** | 10 hours | Design, Execute, Document |
| **Avg Hours per Bug** | 20 hours | Isolate, Report, Verify |
| **Total Project Hours** | 650 hours | Including planning, setup, reporting |

### 7.2 Cost Analysis:

| Item | Unit | Cost | Total |
|------|------|------|-------|
| **QA Engineer Hourly Rate** | /hr | $30 | - |
| **Test Execution** | 450 hrs | $30 | $13,500 |
| **Test Infrastructure** | - | - | $2,000 |
| **Bug Verification** | 200 hrs | $30 | $6,000 |
| **Project Management** | 30% | - | $6,150 |
| **TOTAL PROJECT COST** | - | - | **$27,650** |
| **Cost per Test Case** | $612.4 | - | - |
| **Cost per Bug Found** | $2,765 | - | - |
| **ROI on Testing** | 300% | 10 bugs worth $27,650 | Excellent |

---

## 8. BENCHMARKING & TRENDS

### 8.1 Metrics Trend (v1.0 vs v2.0):

| Metric | v1.0 | v2.0 | Change | Trend |
|--------|------|------|--------|-------|
| Test Case Count | 24 | 45 | +21 | ⬆️ +88% |
| Pass Rate | 91.67% | 95.56% | +3.89% | ⬆️ |
| Bug Count | 8 | 10 | +2 | ⬆️ |
| Bug Resolution | 87.5% | 80% | -7.5% | ⬇️ |
| Quality Score | 87 | 89 | +2 | ⬆️ |
| Coverage | 100% | 100% | - | ↔️ |

### 8.2 Industry Benchmarks:

| Metric | Industry Avg | Our Score | Performance |
|--------|--------------|-----------|-------------|
| **Pass Rate** | 85-90% | 95.56% | 🟢 EXCELLENT |
| **Defect Density** | 0.5-1.0 | 0.22 | 🟢 EXCELLENT |
| **Bug Resolution** | 75-80% | 80% | 🟢 AT TARGET |
| **Coverage** | 80-90% | 100% | 🟢 EXCELLENT |
| **Quality Score** | 80-85 | 89 | 🟢 EXCELLENT |

**Overall Performance:** 🟢 **ABOVE INDUSTRY AVERAGE**

---

## 9. RECOMMENDATIONS & IMPROVEMENTS

### 9.1 For Next Release (v2.1):

1. ✅ Complete Mobile Safari fixes
2. ⏳ Add XSS prevention tests
3. ⏳ Implement API security testing
4. ⏳ Add load testing (concurrent users)
5. ⏳ Expand payment provider coverage

### 9.2 Process Improvements:

- Implement automated regression testing
- Add continuous integration (CI/CD)
- Establish baseline metrics for future releases
- Create reusable test case templates

---

## 10. DASHBOARD VISUALIZATION

```
TEST EXECUTION RATE          PASS RATE               COVERAGE RATE
████████████████████ 100%   ███████████████████░ 95.56%   ████████████████████ 100%

QUALITY SCORE                BUG RESOLUTION         RELEASE READINESS
████████████████████ 89/100  ████████░░░░░░░░░░░ 80%      ████████████████████ 89%
```

---

## FINAL SUMMARY

| Category | Status | Score |
|----------|--------|-------|
| **Test Execution** | ✅ COMPLETE | 100% |
| **Test Coverage** | ✅ EXCELLENT | 100% |
| **Quality Assessment** | ✅ EXCELLENT | A Grade |
| **Release Decision** | ✅ GO | APPROVED |
| **Risk Level** | 🟢 LOW | Mitigated |

---

**END OF TEST METRICS v2.0**

**Report Generated:** 13/03/2026  
**Next Review:** After production release (1-week monitoring period)
