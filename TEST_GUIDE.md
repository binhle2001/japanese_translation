# 🇯🇵 Hướng dẫn Test Japanese Text Analysis API

![Japanese Text Analysis](https://img.shields.io/badge/API-Test%20Guide-blue?style=for-the-badge&logo=japan)

> 🎯 **Mục tiêu**: Test API phân tích văn bản tiếng Nhật thông qua giao diện web đẹp mắt

---

## 🚀 Cách sử dụng

### 1. Khởi động ứng dụng
```bash
# Cài đặt dependencies
pip install -r requirements_streamlit.txt

# Chạy ứng dụng
streamlit run test_app.py
```

### 2. Truy cập giao diện
Mở trình duyệt và truy cập: **http://localhost:8501**

![Main Interface](https://via.placeholder.com/800x400/1f77b4/ffffff?text=Japanese+Text+Analysis+Tester)

> 💡 **Giao diện chính**: Ứng dụng có 2 cột - sidebar cấu hình bên trái và khu vực test bên phải

## 📝 Cách test

### Bước 1: Kiểm tra API 🏥
- Nhấn nút **"Kiểm tra sức khỏe API"** trong sidebar
- Đảm bảo hiển thị "✅ API hoạt động bình thường"

![Health Check](https://via.placeholder.com/400x200/28a745/ffffff?text=API+Health+Check)

### Bước 2: Nhập văn bản test 📝
- Nhập văn bản tiếng Nhật vào ô **"Văn bản tiếng Nhật"**
- Chọn trình độ JLPT (tùy chọn)
- Nhấn nút **"🔍 Phân tích văn bản"**

![Text Input](https://via.placeholder.com/400x200/007bff/ffffff?text=Text+Input+Area)

### Bước 3: Xem kết quả 📊
- Kết quả phân tích sẽ hiển thị dưới dạng markdown đẹp mắt
- Có thể xem dữ liệu JSON gốc bằng cách mở phần **"🔧 Xem dữ liệu JSON gốc"**

![Analysis Result](https://via.placeholder.com/400x200/17a2b8/ffffff?text=Analysis+Result)

## 🧪 Các test case cần thực hiện

<div align="center">

![Test Cases](https://via.placeholder.com/600x100/6f42c1/ffffff?text=Test+Cases+Overview)

</div>

### ✅ Test 1: Từ đơn có Hán tự 🚃
**Nhập**: `電車`
**Trình độ**: N5
**Kết quả mong đợi**: Phân tích từ "tàu điện", giải thích Hán tự 電 (điện) và 車 (xe)

![Test 1](https://via.placeholder.com/300x150/28a745/ffffff?text=電車+Test)

### ✅ Test 2: Từ Hiragana 📚
**Nhập**: `たくさん`
**Trình độ**: N5
**Kết quả mong đợi**: Phân tích từ "nhiều, rất nhiều", loại từ và cách sử dụng

![Test 2](https://via.placeholder.com/300x150/007bff/ffffff?text=たくさん+Test)

### ✅ Test 3: Cụm từ 🗾
**Nhập**: `日本の文化`
**Trình độ**: N3
**Kết quả mong đợi**: Phân tích cụm từ "văn hóa Nhật Bản", cấu trúc ngữ pháp

![Test 3](https://via.placeholder.com/300x150/17a2b8/ffffff?text=日本の文化+Test)

### ✅ Test 4: Câu đơn giản 👨‍🎓
**Nhập**: `私は学生です。`
**Trình độ**: N5
**Kết quả mong đợi**: Dịch "Tôi là học sinh", phân tích cấu trúc câu

![Test 4](https://via.placeholder.com/300x150/ffc107/000000?text=私は学生です+Test)

### ✅ Test 5: Câu phức tạp 🧠
**Nhập**: `池田さんは木村さんを疑っているようだ。`
**Trình độ**: N2
**Kết quả mong đợi**: Dịch và phân tích ngữ pháp phức tạp

![Test 5](https://via.placeholder.com/300x150/dc3545/ffffff?text=Complex+Sentence+Test)

### ✅ Test 6: Câu nghi vấn lịch sự 🍚
**Nhập**: `ご飯を一杯いただけますか？`
**Trình độ**: N3
**Kết quả mong đợi**: Phân tích cấu trúc lịch sự, giải thích mức độ lịch sự

![Test 6](https://via.placeholder.com/300x150/20c997/ffffff?text=Polite+Question+Test)

### ✅ Test 7: Lỗi validation ❌
**Nhập**: `Em ăn cơm chưa`
**Kết quả mong đợi**: Hiển thị lỗi "Text must contain valid Japanese characters"

![Error Example](https://via.placeholder.com/300x150/dc3545/ffffff?text=Validation+Error)

### ✅ Test 8: Văn bản rỗng ⚠️
**Nhập**: (để trống)
**Kết quả mong đợi**: Hiển thị lỗi "Text cannot be empty"

![Empty Input](https://via.placeholder.com/300x150/ffc107/000000?text=Empty+Input+Error)

## 📊 Checklist đánh giá

<div align="center">

![Evaluation](https://via.placeholder.com/600x100/6f42c1/ffffff?text=Evaluation+Checklist)

</div>

### 🎯 Chất lượng phân tích
- [ ] Dịch nghĩa chính xác
- [ ] Giải thích rõ ràng bằng tiếng Việt
- [ ] Phân tích Hán tự chi tiết (nếu có)
- [ ] Câu ví dụ phù hợp
- [ ] Phân tích ngữ pháp đúng

![Quality Check](https://via.placeholder.com/400x200/28a745/ffffff?text=Quality+Analysis)

### ⚡ Hiệu năng
- [ ] Thời gian phản hồi < 5 giây
- [ ] Giao diện mượt mà, không lag
- [ ] Không bị timeout

![Performance](https://via.placeholder.com/400x200/007bff/ffffff?text=Performance+Check)

### 🛡️ Xử lý lỗi
- [ ] Thông báo lỗi rõ ràng
- [ ] Không crash khi có lỗi
- [ ] Validation hoạt động đúng

![Error Handling](https://via.placeholder.com/400x200/dc3545/ffffff?text=Error+Handling)

## 🎯 Tiêu chí đánh giá

<div align="center">

![Rating System](https://via.placeholder.com/600x100/6f42c1/ffffff?text=Rating+System)

</div>

### ⭐⭐⭐⭐⭐ Tuyệt vời (5/5)
- Phân tích chính xác 100%
- Thời gian phản hồi < 2 giây
- Giao diện đẹp, dễ sử dụng
- Xử lý lỗi hoàn hảo

![Excellent](https://via.placeholder.com/300x150/28a745/ffffff?text=Excellent+5/5)

### ⭐⭐⭐⭐ Tốt (4/5)
- Phân tích chính xác > 90%
- Thời gian phản hồi < 3 giây
- Giao diện ổn định
- Xử lý lỗi tốt

![Good](https://via.placeholder.com/300x150/007bff/ffffff?text=Good+4/5)

### ⭐⭐⭐ Khá (3/5)
- Phân tích chính xác > 80%
- Thời gian phản hồi < 5 giây
- Giao diện cơ bản
- Xử lý lỗi cơ bản

![Fair](https://via.placeholder.com/300x150/ffc107/000000?text=Fair+3/5)

### ⭐⭐ Trung bình (2/5)
- Phân tích chính xác > 70%
- Thời gian phản hồi > 5 giây
- Giao diện có vấn đề
- Xử lý lỗi chưa tốt

![Poor](https://via.placeholder.com/300x150/fd7e14/ffffff?text=Poor+2/5)

### ⭐ Kém (1/5)
- Phân tích chính xác < 70%
- Thời gian phản hồi > 10 giây
- Giao diện lỗi nhiều
- Xử lý lỗi kém

![Very Poor](https://via.placeholder.com/300x150/dc3545/ffffff?text=Very+Poor+1/5)

## 📝 Báo cáo test

<div align="center">

![Test Report](https://via.placeholder.com/600x100/6f42c1/ffffff?text=Test+Report+Form)

</div>

Sau khi hoàn thành test, vui lòng ghi lại:

### 📋 Thông tin đánh giá

| Tiêu chí | Điểm số |
|----------|---------|
| **Điểm đánh giá tổng thể** | ___/5 ⭐ |
| **Thời gian phản hồi trung bình** | ___ giây ⏱️ |

### 🎯 Chi tiết đánh giá

1. **Test case nào hoạt động tốt nhất**: 
   - _________________________________
   - _________________________________

2. **Test case nào có vấn đề**: 
   - _________________________________
   - _________________________________

3. **Đề xuất cải thiện**: 
   - _________________________________
   - _________________________________

![Report Template](https://via.placeholder.com/400x200/17a2b8/ffffff?text=Test+Report+Template)

---

<div align="center">

![Important Note](https://via.placeholder.com/600x100/dc3545/ffffff?text=Important+Note)

**⚠️ Lưu ý**: Đảm bảo API server đang chạy tại `http://localhost:8000` trước khi test!

</div>
