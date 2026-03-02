# TEST EXECUTION DATA & SCREENSHOT GUIDE

**Phiên bản:** 1.0  
**Ngày:** 12/03/2026  
**Tác giả:** QA Team

---

## 📸 SCREENSHOT MANAGEMENT GUIDE

### Folder Structure
```
Screenshots/
├── Module_1_Authentication/
│   ├── Login/
│   │   ├── login_success.png
│   │   ├── login_error_invalid_password.png
│   │   ├── login_timeout.png
│   │   └── login_session_created.png
│   ├── Registration/
│   │   ├── signup_form.png
│   │   ├── signup_validation_email.png
│   │   ├── signup_password_too_short.png
│   │   └── signup_success.png
│   └── Forgot_Password/
│       ├── forgot_pw_email_sent.png
│       └── forgot_pw_reset_link.png
│
├── Module_2_Product_Cart/
│   ├── Search/
│   │   ├── search_results.png
│   │   ├── search_no_results.png
│   │   └── search_filters_applied.png
│   ├── Filter/
│   │   ├── filter_price_range.png
│   │   └── filter_category.png
│   ├── Product_Detail/
│   │   ├── product_page_layout.png
│   │   ├── product_images.png
│   │   └── add_to_cart_button.png
│   └── Cart/
│       ├── cart_items_list.png
│       ├── cart_total_updated.png
│       ├── cart_item_removed.png
│       └── cart_empty_state.png
│
├── Module_3_Checkout/
│   ├── Address/
│   │   ├── address_form.png
│   │   ├── address_validation_error.png
│   │   └── address_saved.png
│   ├── Payment/
│   │   ├── payment_method_selection.png
│   │   ├── cod_selected.png
│   │   ├── visa_form.png
│   │   └── payment_timeout_error.png
│   └── Order/
│       ├── order_confirmation.png
│       ├── order_id_generated.png
│       ├── order_email_sent.png
│       └── order_history.png
│
└── Bugs/
    ├── BUG_2026_001/
    │   ├── special_chars_login_error.png
    │   ├── error_message.png
    │   └── browser_console.png
    ├── BUG_2026_002/
    │   ├── search_slow_loading.png
    │   └── network_timing.png
    └── [More bugs...]
```

### How to Capture Screenshots

#### ✅ **For Test Case Evidence**
```
1. Execute test case step by step
2. Take screenshot AFTER each significant action
3. Label screenshot with:
   - TC ID (e.g., TC_AUTH_LOGIN_001)
   - Action (e.g., "login_success")
   - Date (e.g., 05_03_2026)
4. Save filename: TC_AUTH_LOGIN_001_success_050326.png
```

#### ✅ **For Bug Evidence**
```
1. When bug found, capture:
   - Full screen with error
   - Error message clearly visible
   - Browser address bar (show URL)
   - Browser console (if applicable)
2. Label: BUG_2026_001_error_screenshot.png
3. Also capture:
   - HTML error
   - Network request/response
   - Database log (if relevant)
```

#### ✅ **Screenshot Tools**
- Windows: Snipping Tool / Snip & Sketch
- Chrome: Extension "Take a Full Page Screenshot"
- Firefox: Built-in Screenshot Tool (Ctrl+Shift+S)
- Professional: Snagit / ScreenFlow

---

## 📊 TEST EXECUTION DATA TEMPLATE

### Execution Log CSV Format

```csv
Date,Time,TC_ID,Tester,Module,Feature,Precondition_Status,Step_1,Step_2,Step_3,Result,Status,Notes,Screenshot,Bug_Found
05/03/2026,09:00,TC_AUTH_REG_001,QA Eng 1,Auth,Register,OK,"Navigate to register page","Enter email: test@gmail.com","Enter password: Test@1234",Success,PASS,Smooth flow,register_001.png,NO
05/03/2026,09:05,TC_AUTH_REG_002,QA Eng 1,Auth,Register,OK,"Navigate to register page","Enter email: invalid_email","Click register",Error,PASS,Email validation works,register_error_001.png,NO
05/03/2026,09:15,TC_AUTH_LOGIN_001,QA Eng 1,Auth,Login,OK,"Navigate to login","Enter credentials","Click login",Success,PASS,Session created,login_success_001.png,NO
05/03/2026,09:20,TC_AUTH_LOGIN_002,QA Eng 1,Auth,Login,OK,"Navigate to login","Enter wrong password","Click login",Error,PASS,Error message shown,login_error_001.png,YES - BUG_001
```

### Daily Test Summary

```
Date: 05/03/2026
Day: Monday
Tester(s): QA Engineer 1, 2
Test Environment: UAT Staging
Build: v1.0.0

Module: Authentication
├─ Regression Tests: 8
├─ Passed: 8
├─ Failed: 0
├─ Blocked: 0
├─ Bugs Found: 1 (BUG_2026_001)
└─ Status: ✅ ON TRACK

Time Spent: 4 hours
Issues: 1 HIGH bug found
Next Steps: Report BUG_2026_001, Continue with Module 2
```

---

## 📋 SIMULATED TEST DATA

### User Accounts Created

```
Account Data (Test Environment Only):

Account 1:
  Email: test@gmail.com
  Password: Test@1234
  Name: Test User
  Role: End User
  Status: Active
  Created: 01/03/2026

Account 2:
  Email: admin@system.com
  Password: Admin@1234
  Name: Admin User
  Role: Administrator
  Status: Active
  Created: 01/03/2026

Account 3:
  Email: user.special@test.com
  Password: Test@!@#$ (with special chars)
  Name: Special Char User
  Role: End User
  Status: Active
  Created: 02/03/2026
  Note: Used to test special character handling

[... 497+ more test accounts ...]

Total: 500 test accounts
```

### Product Test Data

```
Sample Products in Database:

Product 1:
  ID: PROD_001
  Name: iPhone 15
  Category: Electronics > Smartphones
  Price: 1,299,000 VNĐ
  Stock: 50 units
  Description: Latest Apple smartphone
  Images: 5 images available
  Rating: 4.5/5 (1000 reviews)
  Status: Active

Product 2:
  ID: PROD_002
  Name: Samsung Galaxy S24
  Category: Electronics > Smartphones
  Price: 899,000 VNĐ
  Stock: 30 units
  Description: Latest Samsung smartphone
  Images: 4 images available
  Rating: 4.3/5 (800 reviews)
  Status: Active

Product 3:
  ID: PROD_003
  Name: MacBook Pro 16"
  Category: Electronics > Laptops
  Price: 4,499,000 VNĐ
  Stock: 5 units
  Description: Professional laptop
  Images: 6 images available
  Rating: 4.8/5 (500 reviews)
  Status: Active

Product 4:
  ID: PROD_004
  Name: Nike Air Force 1
  Category: Fashion > Shoes
  Price: 299,000 VNĐ
  Stock: 100 units
  Description: Classic shoe
  Images: 3 images available
  Rating: 4.4/5 (2000 reviews)
  Status: Active

Product 5:
  ID: PROD_005
  Name: Harry Potter Book
  Category: Books > Fiction
  Price: 89,000 VNĐ
  Stock: 200 units
  Description: Popular book series
  Images: 1 image
  Rating: 4.9/5 (3000 reviews)
  Status: Active

[... 9995+ more products ...]

Total: 10,000+ products
Categories: 10 major categories
Price Range: 10,000 - 500,000,000 VNĐ
Languages: Vietnamese localized
In Stock: 8,000 products
Out of Stock: 2,000 products
```

### Test Orders Created

```
Order 1:
  Order ID: ORD-20260305-001
  User: test@gmail.com
  Items:
    - iPhone 15 x 1 (1,299,000 VNĐ)
    - iPhone Case x 1 (99,000 VNĐ)
  Subtotal: 1,398,000 VNĐ
  Discount: 0 VNĐ
  Shipping: 0 VNĐ (Free)
  Total: 1,398,000 VNĐ
  Address: 123 Nguyễn Huệ, Q1, HCM
  Payment Method: COD
  Status: Confirmed
  Created: 05/03/2026 09:30

Order 2:
  Order ID: ORD-20260307-001
  User: user.special@test.com
  Items:
    - MacBook Pro 16" x 1 (4,499,000 VNĐ)
  Subtotal: 4,499,000 VNĐ
  Discount: -450,000 VNĐ (10% OFF - SAVE10 code)
  Shipping: 0 VNĐ (Free)
  Total: 4,049,000 VNĐ
  Address: 456 Lê Lợi, Q1, HCM
  Payment Method: Visa (Test: 4111111111111111)
  Status: Confirmed
  Created: 07/03/2026 14:20

[... more orders ...]

Total Orders: 50+ test orders created
```

---

## 🐛 DEFECT TRACKING DATA

### Simulated Bug Execution Log

```
BUG_2026_001: Đăng nhập không hoạt động với ký tự đặc biệt trong mật khẩu
├─ Reported: 05/03/2026 09:20
├─ Reporter: QA Engineer 1
├─ Severity: HIGH
├─ Priority: P1
├─ Steps:
│   1. Go to login page
│   2. Email: test@gmail.com
│   3. Password: Test@!@#$
│   4. Click Login
├─ Error: "Login failed - Invalid credentials"
├─ Environment: Chrome 120, Windows 10, v1.0.0
├─ Root Cause Found: 06/03/2026 (Password not escaped)
├─ Fix Applied: 06/03/2026 (Escape input)
├─ Retested: 06/03/2026 16:00
├─ Result: PASSED ✅
└─ Status: CLOSED - VERIFIED

BUG_2026_002: Tìm kiếm sản phẩm chậm với <10K items>
├─ Reported: 06/03/2026 10:15
├─ Reporter: QA Engineer 2
├─ Severity: MEDIUM
├─ Priority: P2
├─ Performance: 5-8 seconds (Target: <2 sec)
├─ Root Cause: Missing database index
├─ Fix: Add index on product.name column
├─ Fix Applied: 07/03/2026
├─ Retested: 07/03/2026 15:00
├─ New Performance: 0.5 seconds ✅
└─ Status: CLOSED - VERIFIED

BUG_2026_003: Tổng giá trong giỏ tính sai khi áp dụng discount (CRITICAL)
├─ Reported: 06/03/2026 11:30
├─ Reporter: QA Engineer 3
├─ Severity: CRITICAL
├─ Priority: P0 - BLOCKER
├─ Issue:
│   Item: 1000 VNĐ
│   Discount (50%): Should be -500, shows -250
│   Total: Should be 500, shows 750
├─ Root Cause: Wrong formula (×0.5 instead of ÷2)
├─ File: cart.js line 245
├─ Fix: Change calculation logic
├─ Fix Applied: 06/03/2026 14:00
├─ Verified: ✅ FIXED
└─ Status: CLOSED (1 day turnaround)

[... 5 more bugs ...]

Bug Metrics:
- Total: 8 bugs
- Critical: 1 (resolved in 1 day)
- High: 2 (avg 1.2 days)
- Medium: 4 (avg 1.5 days)
- Average Resolution: 1.2 days (Target: <2 days) ✅
```

---

## 📈 TEST EXECUTION TIMELINE

### Week 1 (01-07 March)

**Monday 01/03:**
```
09:00 - 10:00: Kick-off meeting
10:00 - 12:00: Test Plan review
13:00 - 17:00: Environment setup & data preparation
Status: ✅ Test Plan approved
```

**Tuesday 02/03:**
```
08:00 - 12:00: Test data finalization (500 users, 10K products)
13:00 - 17:00: Test environment verification
Status: ✅ Environment ready
```

**Wednesday 03/03:**
```
08:00 - 17:00: Test case design (24 TCs written)
Status: ✅ All TCs ready for execution
```

**Thursday 04/03:**
```
08:00 - 12:00: RTM mapping review
13:00 - 17:00: RTM verification (100% coverage)
Status: ✅ RTM approved
```

**Friday 05/03:**
```
09:00 - 12:00: Start Module 1 (Auth) - TCs 1-4
13:00 - 17:00: Continue Auth - TCs 5-8
Bugs Found: 1 (BUG_2026_001)
Status: ⏳ Module 1 on track
```

**Saturday-Sunday:**
```
Test data backup & bug triage
Prepare for Monday test execution
```

### Week 2 (10-16 March - Retest & Finalization)

**Monday 10/03:**
```
09:00 - 12:00: Module 3 retest (2 failed TCs from last week)
13:00 - 15:00: Regression testing (critical path)
15:00 - 17:00: Bug verification of previously fixed bugs
Status: ✅ 95% tests completed
```

**Tuesday 11/03:**
```
08:00 - 12:00: Final test execution & verification
13:00 - 15:00: Remaining bug retesting
15:00 - 17:00: Final cleanups & environment teardown
Status: ✅ 100% TC execution complete
```

**Wednesday 12/03:**
```
09:00 - 10:00: Test Report finalization
10:00 - 11:00: Metrics calculation
11:00 - 12:00: Sign-off paper signing
13:00 - 14:00: Release preparation
14:00 - 15:00: Stakeholder communication
Status: ✅ Test Report signed & approved
```

**Thursday 13/03:**
```
GO LIVE - Release to Production 🚀
```

---

## 📝 EXECUTION NOTES

### Testing Challenges Faced

1. **Payment Gateway Testing**
   - Challenge: Real Visa card not available
   - Solution: Tested with simulated card (4111111111111111)
   - Impact: Payment flow validated, integration tested

2. **Email Verification**
   - Challenge: Need to verify actual email delivery
   - Solution: Used Mailinator temp email accounts
   - Impact: Email flows confirmed working

3. **Database Performance**
   - Challenge: Search slow with 10K products
   - Solution: Identified missing index, added & retested
   - Impact: Performance improved 10x

4. **Special Character Handling**
   - Challenge: Login failed with special chars
   - Solution: Root cause found & fixed same day
   - Impact: All special char combinations now working

### Lessons Learned

✅ **What Went Well:**
- Strong precondition setup (500 accounts, 10K products)
- Quick bug resolution (avg 1.2 days)
- Good communication between QA & Dev
- Comprehensive documentation

⚠️ **What Could Be Better:**
- Earlier performance testing would have caught search issue
- More edge case testing for payment module
- Security testing should be separate

---

## 🎯 FINAL CHECKLIST

### Pre-Release Verification

- [x] All 24 Test Cases executed
- [x] Pass rate 91.67% (exceeds 85% target)
- [x] Requirement coverage 100%
- [x] All CRITICAL bugs resolved
- [x] All HIGH bugs in progress
- [x] Test Report signed-off
- [x] Metrics documented
- [x] Screenshots captured
- [x] Sign-offs collected
- [x] Documentation complete

### Risk Mitigation

- [x] Rollback plan prepared
- [x] 24/7 support team on-call
- [x] Monitoring setup
- [x] Alert thresholds configured
- [x] Incident response procedure ready

---

**END OF TEST EXECUTION DATA**

---

*Next Step: Execute actual testing following this guide*