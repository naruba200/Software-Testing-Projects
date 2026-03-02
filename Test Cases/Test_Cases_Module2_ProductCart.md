# CA KIỂM THỬ - MODULE 2: SẢN PHẨM & GIỎ HÀNG (PRODUCT & CART)

**Phiên bản:** 1.0  
**Ngày tạo:** 03/03/2026  
**Module:** Product & Cart  
**Tác giả:** QA Team

---

## 1. TÌM KIẾM SẢN PHẨM (SEARCH)

### TC_PROD_SEARCH_001 - Tìm kiếm hiển thị đúng kết quả
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_PROD_SEARCH_001 |
| **Tên test case** | Tìm kiếm hiển thị đúng kết quả |
| **Module** | Product & Cart |
| **Tính năng** | Tìm kiếm sản phẩm |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Ở trang sản phẩm |
| **Bước thực thi** | 1. Truy cập trang sản phẩm<br>2. Nhập từ khóa "iphone" vào ô tìm kiếm<br>3. Nhấn Enter hoặc click nút "Tìm kiếm" |
| **Kết quả mong đợi** | - Hiển thị danh sách sản phẩm chứa "iphone"<br>- Kết quả có liên quan đến từ khóa<br>- Số lượng sản phẩm được hiển thị |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 06/03/2026 |
| **Tester** | QA Engineer 2 |

---

### TC_PROD_SEARCH_002 - Tìm kiếm không trả về kết quả
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_PROD_SEARCH_002 |
| **Tên test case** | Tìm kiếm không trả về kết quả |
| **Module** | Product & Cart |
| **Tính năng** | Tìm kiếm sản phẩm |
| **Ưu tiên** | Medium |
| **Severity** | Medium |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Ở trang sản phẩm |
| **Bước thực thi** | 1. Truy cập trang sản phẩm<br>2. Nhập từ khóa "xyzabc123" (không tồn tại)<br>3. Nhấn Enter |
| **Kết quả mong đợi** | - Không hiển thị sản phẩm<br>- Hiển thị thông báo "Không tìm thấy sản phẩm" |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 06/03/2026 |
| **Tester** | QA Engineer 2 |

---

## 2. LỌC THEO GIÁ / DANH MỤC (FILTER)

### TC_PROD_FILTER_001 - Lọc theo giá hoạt động đúng
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_PROD_FILTER_001 |
| **Tên test case** | Lọc theo giá hoạt động đúng |
| **Module** | Product & Cart |
| **Tính năng** | Lọc theo giá |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Ở trang sản phẩm<br>- Có sản phẩm với giá khác nhau |
| **Bước thực thi** | 1. Truy cập trang sản phẩm<br>2. Click vào mục "Lọc theo giá"<br>3. Chọn khoảng: 1.000.000 - 5.000.000 VNĐ<br>4. Click "Lọc" |
| **Kết quả mong đợi** | - Hiển thị chỉ sản phẩm trong khoảng giá<br>- Giá sản phẩm nằm trong 1-5 triệu<br>- Số lượng sản phẩm giảm |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 06/03/2026 |
| **Tester** | QA Engineer 2 |

---

### TC_PROD_FILTER_002 - Lọc theo danh mục hoạt động đúng
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_PROD_FILTER_002 |
| **Tên test case** | Lọc theo danh mục hoạt động đúng |
| **Module** | Product & Cart |
| **Tính năng** | Lọc theo danh mục |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Ở trang sản phẩm<br>- Có nhiều danh mục sản phẩm |
| **Bước thực thi** | 1. Truy cập trang sản phẩm<br>2. Click vào mục "Danh mục"<br>3. Chọn "Điện thoại" |
| **Kết quả mong đợi** | - Hiển thị chỉ sản phẩm danh mục "Điện thoại"<br>- Số lượng sản phẩm giảm<br>- Tất cả sản phẩm đều là điện thoại |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 06/03/2026 |
| **Tester** | QA Engineer 2 |

---

## 3. XEM CHI TIẾT SẢN PHẨM (PRODUCT DETAIL)

### TC_PROD_DETAIL_001 - Xem chi tiết sản phẩm thành công
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_PROD_DETAIL_001 |
| **Tên test case** | Xem chi tiết sản phẩm thành công |
| **Module** | Product & Cart |
| **Tính năng** | Xem chi tiết sản phẩm |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Ở trang sản phẩm<br>- Có sản phẩm trong danh sách |
| **Bước thực thi** | 1. Truy cập trang sản phẩm<br>2. Click vào sản phẩm "iPhone 15" |
| **Kết quả mong đợi** | - Chuyển đến trang chi tiết sản phẩm<br>- Hiển thị: Tên, giá, mô tả, hình ảnh<br>- Nút "Thêm vào giỏ" có sẵn |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 06/03/2026 |
| **Tester** | QA Engineer 3 |

---

## 4. THÊM SẢN PHẨM VÀO GIỎ (ADD TO CART)

### TC_CART_ADD_001 - Thêm sản phẩm vào giỏ thành công
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CART_ADD_001 |
| **Tên test case** | Thêm sản phẩm vào giỏ thành công |
| **Module** | Product & Cart |
| **Tính năng** | Thêm sản phẩm vào giỏ |
| **Ưu tiên** | High |
| **Severity** | Critical |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Ở trang chi tiết sản phẩm |
| **Bước thực thi** | 1. Ở trang chi tiết sản phẩm "iPhone 15"<br>2. Chọn số lượng: 1<br>3. Click "Thêm vào giỏ" |
| **Kết quả mong đợi** | - Sản phẩm được thêm vào giỏ<br>- Hiển thị thông báo thành công<br>- Số lượng giỏ hàng tăng |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 06/03/2026 |
| **Tester** | QA Engineer 3 |

---

## 5. CẬP NHẬT SỐ LƯỢNG (UPDATE QUANTITY)

### TC_CART_UPDATE_001 - Cập nhật số lượng sản phẩm trong giỏ
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CART_UPDATE_001 |
| **Tên test case** | Cập nhật số lượng sản phẩm trong giỏ |
| **Module** | Product & Cart |
| **Tính năng** | Cập nhật số lượng |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Giỏ hàng có sản phẩm |
| **Bước thực thi** | 1. Truy cập giỏ hàng<br>2. Tìm sản phẩm "iPhone 15"<br>3. Thay đổi số lượng từ 1 → 3 |
| **Kết quả mong đợi** | - Số lượng được cập nhật thành 3<br>- Tổng giá cập nhật đúng<br>- Không có lỗi |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 06/03/2026 |
| **Tester** | QA Engineer 3 |

---

## 6. XOÁ SẢN PHẨM KHỎI GIỎ (REMOVE FROM CART)

### TC_CART_DELETE_001 - Xoá sản phẩm khỏi giỏ thành công
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CART_DELETE_001 |
| **Tên test case** | Xoá sản phẩm khỏi giỏ thành công |
| **Module** | Product & Cart |
| **Tính năng** | Xoá sản phẩm khỏi giỏ |
| **Ưu tiên** | High |
| **Severity** | High |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Giỏ hàng có sản phẩm |
| **Bước thực thi** | 1. Truy cập giỏ hàng<br>2. Tìm sản phẩm "iPhone 15"<br>3. Click nút "Xoá" |
| **Kết quả mong đợi** | - Sản phẩm bị xoá khỏi giỏ<br>- Hiển thị thông báo xác nhận<br>- Tổng giá được cập nhật |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 06/03/2026 |
| **Tester** | QA Engineer 3 |

---

### TC_PROD_SEARCH_003 - Tìm kiếm với ký tự đặc biệt
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_PROD_SEARCH_003 |
| **Tên test case** | Tìm kiếm với ký tự đặc biệt |
| **Module** | Product & Cart |
| **Tính năng** | Tìm kiếm sản phẩm |
| **Ưu tiên** | Medium |
| **Severity** | Medium |
| **Loại test** | Negative - Boundary |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Ở trang sản phẩm |
| **Bước thực thi** | 1. Truy cập trang sản phẩm<br>2. Nhập ký tự đặc biệt: @#$%^&*<br>3. Nhấn Enter |
| **Kết quả mong đợi** | - Không gây lỗi hệ thống<br>- Hiển thị thông báo: "Từ khóa không hợp lệ"<br>- Hoặc không trả về kết quả |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 3 |

---

### TC_PROD_SEARCH_004 - Tìm kiếm với tập dữ liệu lớn (10000+ sản phẩm)
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_PROD_SEARCH_004 |
| **Tên test case** | Tìm kiếm với tập dữ liệu lớn |
| **Module** | Product & Cart |
| **Tính năng** | Tìm kiếm sản phẩm |
| **Ưu tiên** | Medium |
| **Severity** | Medium |
| **Loại test** | Boundary - Performance |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Database có 10000+ sản phẩm |
| **Bước thực thi** | 1. Truy cập trang sản phẩm<br>2. Nhập từ khóa phổ biến: "phone"<br>3. Quan sát thời gian tải kết quả |
| **Kết quả mong đợi** | - Kết quả được hiển thị trong < 3 giây<br>- Hiển thị phân trang để dễ quản lý<br>- Tất cả sản phẩm liên quan được hiển thị |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 3 |

---

### TC_PROD_FILTER_003 - Lọc theo nhiều tiêu chí cùng lúc
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_PROD_FILTER_003 |
| **Tên test case** | Lọc theo nhiều tiêu chí cùng lúc |
| **Module** | Product & Cart |
| **Tính năng** | Lọc sản phẩm |
| **Ưu tiên** | Medium |
| **Severity** | Medium |
| **Loại test** | Positive - Validation |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Ở trang sản phẩm |
| **Bước thực thi** | 1. Truy cập trang sản phẩm<br>2. Lọc theo giá: 1.000.000 - 5.000.000 đ<br>3. Lọc theo danh mục: Điện thoại<br>4. Lọc theo thương hiệu: Apple<br>5. Xem kết quả |
| **Kết quả mong đợi** | - Kết quả hiển thị sản phẩm thỏa mãn cả 3 tiêu chí<br>- Số lượng sản phẩm giảm so với không lọc<br>- Filter được áp dụng chính xác |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 2 |

---

### TC_PROD_FILTER_004 - Lọc với giá trị không hợp lệ
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_PROD_FILTER_004 |
| **Tên test case** | Lọc với giá trị không hợp lệ |
| **Module** | Product & Cart |
| **Tính năng** | Lọc sản phẩm |
| **Ưu tiên** | Medium |
| **Severity** | Medium |
| **Loại test** | Negative - Boundary |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Ở trang sản phẩm |
| **Bước thực thi** | 1. Truy cập trang sản phẩm<br>2. Cố gắng nhập giá tối thiểu là -1000<br>3. Cố gắng nhập giá tối đa là 99999999<br>4. Click lọc |
| **Kết quả mong đợi** | - Hiển thị thông báo lỗi<br>- Filter không được áp dụng<br>- Hoặc tự động hiệu chỉnh giá trị về hợp lệ |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 1 |

---

### TC_PROD_DETAIL_002 - Hiển thị hình ảnh sản phẩm
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_PROD_DETAIL_002 |
| **Tên test case** | Hiển thị hình ảnh sản phẩm |
| **Module** | Product & Cart |
| **Tính năng** | Chi tiết sản phẩm |
| **Ưu tiên** | High |
| **Severity** | High |
| **Loại test** | Positive |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Sản phẩm có hình ảnh |
| **Bước thực thi** | 1. Truy cập trang sản phẩm<br>2. Click vào sản phẩm "iPhone 15"<br>3. Xem mục hình ảnh<br>4. Click từng hình ảnh |
| **Kết quả mong đợi** | - Hiển thị hình ảnh chính của sản phẩm<br>- Có thumbnail cho các hình ảnh khác<br>- Có thể zoom hoặc xem fullscreen |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 4 |

---

### TC_PROD_DETAIL_003 - Hiển thị trạng thái tồn kho sản phẩm
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_PROD_DETAIL_003 |
| **Tên test case** | Hiển thị trạng thái tồn kho sản phẩm |
| **Module** | Product & Cart |
| **Tính năng** | Chi tiết sản phẩm |
| **Ưu tiên** | High |
| **Severity** | High |
| **Loại test** | Boundary - Validation |
| **Điều kiên tiên quyết** | - Đã đăng nhập<br>- Có sản phẩm hết hàng |
| **Bước thực thi** | 1. Truy cập sản phẩm có sẵn hàng<br>2. Xem status tồn kho (ví dụ: 5 sản phẩm)<br>3. Truy cập sản phẩm hết hàng<br>4. Xem status tồn kho |
| **Kết quả mong đợi** | - Hiển thị số lượng tồn kho chính xác<br>- Sản phẩm còn hàng: "Còn hàng" với số lượng<br>- Sản phẩm hết hàng: "Hết hàng" với nút "Thông báo" |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 3 |

---

### TC_CART_ADD_002 - Không thêm sản phẩm hết hàng vào giỏ
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CART_ADD_002 |
| **Tên test case** | Không thêm sản phẩm hết hàng vào giỏ |
| **Module** | Product & Cart |
| **Tính năng** | Thêm sản phẩm vào giỏ |
| **Ưu tiên** | High |
| **Severity** | High |
| **Loại test** | Negative - Validation |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Có sản phẩm hết hàng |
| **Bước thực thi** | 1. Tìm sản phẩm hết hàng<br>2. Click nút "Thêm vào giỏ"<br>3. Quan sát kết quả |
| **Kết quả mong đợi** | - Nút "Thêm vào giỏ" bị vô hiệu hoá<br>- Hoặc hiển thị lỗi: "Sản phẩm hết hàng"<br>- Sản phẩm không được thêm vào giỏ |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 1 |

---

### TC_CART_ADD_003 - Không thêm số lượng âm vào giỏ
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CART_ADD_003 |
| **Tên test case** | Không thêm số lượng âm vào giỏ |
| **Module** | Product & Cart |
| **Tính năng** | Thêm sản phẩm vào giỏ |
| **Ưu tiên** | Medium |
| **Severity** | Medium |
| **Loại test** | Negative - Boundary |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Ở trang chi tiết sản phẩm |
| **Bước thực thi** | 1. Truy cập chi tiết sản phẩm<br>2. Cố gắng nhập số lượng: -5<br>3. Click "Thêm vào giỏ" |
| **Kết quả mong đợi** | - Không cho phép nhập số âm<br>- Hoặc hiển thị lỗi "Số lượng phải > 0"<br>- Sản phẩm không được thêm |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 2 |

---

### TC_CART_UPDATE_002 - Cập nhật số lượng về 0 xoá sản phẩm khỏi giỏ
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CART_UPDATE_002 |
| **Tên test case** | Cập nhật số lượng về 0 xoá sản phẩm khỏi giỏ |
| **Module** | Product & Cart |
| **Tính năng** | Cập nhật số lượng trong giỏ |
| **Ưu tiên** | Medium |
| **Severity** | Medium |
| **Loại test** | Boundary |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Giỏ hàng có sản phẩm |
| **Bước thực thi** | 1. Truy cập giỏ hàng<br>2. Tìm sản phẩm "iPhone 15"<br>3. Thay đổi số lượng về 0<br>4. Nhấn Enter hoặc update |
| **Kết quả mong đợi** | - Sản phẩm được xoá khỏi giỏ<br>- Hiển thị thông báo xác nhận<br>- Tổng giá được cập nhật |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 3 |

---

### TC_CART_DELETE_002 - Xoá tất cả sản phẩm khỏi giỏ
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CART_DELETE_002 |
| **Tên test case** | Xoá tất cả sản phẩm khỏi giỏ |
| **Module** | Product & Cart |
| **Tính năng** | Xoá sản phẩm khỏi giỏ |
| **Ưu tiên** | Medium |
| **Severity** | Medium |
| **Loại test** | Positive - Boundary |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Giỏ hàng có nhiều sản phẩm (≥2) |
| **Bước thực thi** | 1. Truy cập giỏ hàng<br>2. Xoá từng sản phẩm một<br>3. Xoá cho đến khi giỏ trống |
| **Kết quả mong đợi** | - Tất cả sản phẩm được xoá<br>- Giỏ không còn sản phẩm nào<br>- Hiển thị thông báo "Giỏ hàng trống" |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 1 |

---

### TC_CART_PERSIST_001 - Giỏ hàng được lưu sau khi đăng xuất
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CART_PERSIST_001 |
| **Tên test case** | Giỏ hàng được lưu sau khi đăng xuất |
| **Module** | Product & Cart |
| **Tính năng** | Quản lý giỏ hàng |
| **Ưu tiên** | Medium |
| **Severity** | Medium |
| **Loại test** | Validation |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Giỏ hàng có sản phẩm |
| **Bước thực thi** | 1. Thêm sản phẩm vào giỏ<br>2. Ghi lại số lượng sản phẩm: 3<br>3. Đăng xuất<br>4. Đăng nhập lại<br>5. Trực cập giỏ hàng |
| **Kết quả mong đợi** | - Giỏ hàng vẫn chứa 3 sản phẩm<br>- Số lượng và giá không thay đổi<br>- Dữ liệu giỏ được lưu trữ an toàn |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 07/03/2026 |
| **Tester** | QA Engineer 4 |

---

### TC_CART_TOTAL_001 - Tính tổng giỏ hàng chính xác
| Thuộc tính | Chi tiết |
|-----------|---------|
| **TC ID** | TC_CART_TOTAL_001 |
| **Tên test case** | Tính tổng giỏ hàng chính xác |
| **Module** | Product & Cart |
| **Tính năng** | Tính toán tổng giỏ |
| **Ưu tiên** | High |
| **Severity** | Critical |
| **Loại test** | Validation |
| **Điều kiện tiên quyết** | - Đã đăng nhập<br>- Giỏ hàng trống |
| **Bước thực thi** | 1. Thêm sản phẩm A: 2.000.000 đ (số lượng 2)<br>2. Thêm sản phẩm B: 1.500.000 đ (số lượng 1)<br>3. Xem tổng giỏ hàng<br>4. Kiểm tra phép tính |
| **Kết quả mong đợi** | - Tổng = (2.000.000 × 2) + (1.500.000 × 1) = 5.500.000 đ<br>- Hiển thị chính xác tổng tiền<br>- Không có lỗi làm tròn |
| **Kết quả thực tế** | ✅ PASS |
| **Ngày test** | 08/03/2026 |
| **Tester** | QA Engineer 3 |

---

**END OF TEST CASES - MODULE 2 (20 TOTAL)**
