# ⚡ Báo Cáo AI - Bản Tối Thượng (Enterprise AI Report Dashboard)

**Báo Cáo AI** là một ứng dụng Web tĩnh (Single-Page Application) mạnh mẽ, hoạt động trực tiếp trên trình duyệt. Ứng dụng giúp tự động hóa quy trình tổng hợp số liệu kinh doanh, phân tích hiệu quả Marketing và cố vấn chiến lược bằng sức mạnh của trí tuệ nhân tạo **Google Gemini**.

Được thiết kế dành riêng cho Quản lý cấp trung, Giám đốc (CMO/CEO) để tiết kiệm hàng giờ đồng hồ làm báo cáo thủ công mỗi tuần.

---

## ✨ Tính năng Nổi bật (Core Features)

### 1. 📊 Đa phương thức đầu vào (Dual-Support)
- **Hỗ trợ Ảnh & Excel/CSV:** Chấp nhận ảnh chụp màn hình từ Sale hoặc đọc trực tiếp file `.xlsx`, `.csv` nhờ thư viện `SheetJS`.
- **Tối ưu hóa dữ liệu:** AI tự động ưu tiên lấy số liệu chính xác tuyệt đối từ Text/Excel, kết hợp phân tích bối cảnh từ Hình ảnh.
- **Tự động cộng dồn:** Module xử lý nội bộ tự động đọc và cộng dồn chi phí, lượt hiển thị, tiếp cận từ các file Excel chạy Ads nhiều cơ sở.

### 2. 🧠 Phân tách tư duy AI (Task Separation)
Hệ thống linh hoạt điều chỉnh "Nhiệt độ" (Temperature) của AI tùy theo tác vụ:
- **Chế độ Kế toán viên (Temperature = 0):** Ép AI bóc tách dữ liệu và điền bảng biểu với độ chính xác 100%, ngăn chặn hoàn toàn tình trạng "ảo giác" (hallucination) tự bịa số liệu.
- **Chế độ Giám đốc (Temperature = 0.4):** Kích hoạt khi cần phân tích, đánh giá. AI sử dụng văn phong sắc bén, linh hoạt để đưa ra góc nhìn đa chiều.

### 3. 💬 Chatbot AI "Có Trí Nhớ" & Tự Rà Soát (Self-Correction)
- **Trí nhớ theo ngữ cảnh (Multi-turn Chat):** Chatbot ghi nhớ toàn bộ cuộc hội thoại, cho phép hỏi dồn, hỏi xoáy các số liệu liên quan.
- **Tự đối chiếu hồ sơ gốc:** Khi người dùng phản hồi *"Số liệu sai"*, Chatbot sẽ tự động lục tìm lại **Dữ liệu thô (Raw Data)** ban đầu để kiểm tra chéo, xin lỗi và tự động tính toán lại kết quả đúng.

### 4. 🔮 Cố vấn Chiến lược & Tương lai
- **Dự báo (Forecasting):** Phân tích tốc độ tiêu tiền và chốt đơn hiện tại để dự phóng doanh thu chu kỳ tới, đưa ra cảnh báo rủi ro sớm.
- **Chẩn đoán Điểm mù:** Tự động tìm ra Cửa hàng "Ngôi sao" và Cửa hàng đang "Báo động đỏ" từ bảng số liệu phức tạp.

### 5. 💾 Tiện ích Trải nghiệm Cao cấp (UX)
- **Quản lý Lịch sử thông minh:** Tự động lưu báo cáo vào bộ nhớ trình duyệt. Tích hợp cơ chế "Cuốn chiếu" (Tự xóa báo cáo cũ nhất khi đầy bộ nhớ) giúp chống lỗi `QuotaExceededError`.
- **Xuất bản Đa dạng:** Hỗ trợ tải báo cáo dưới dạng **Ảnh PNG chất lượng cao**, file **PDF**, hoặc sao chép nguyên định dạng (Copy format) để dán sang Word/Zalo.

---

## 🛠️ Công nghệ Sử dụng (Tech Stack)

Dự án này chạy hoàn toàn ở phía Client (Front-end), không yêu cầu cài đặt Backend hay Database phức tạp:
- **Ngôn ngữ:** HTML5, CSS3, Vanilla JavaScript.
- **AI Core:** [Google Gemini API](https://aistudio.google.com/) (Khuyên dùng `gemini-1.5-flash` để cân bằng tốc độ và chi phí).
- **Thư viện bổ trợ (CDN):**
  - `SheetJS` (`xlsx`): Xử lý và trích xuất text từ file Excel trực tiếp trên trình duyệt.
  - `html2canvas`: Render giao diện HTML thành Ảnh.
  - `html2pdf.js`: Render giao diện HTML thành file PDF.

---

## 🚀 Hướng dẫn Cài đặt & Sử dụng

### 1. Khởi chạy Ứng dụng
Ứng dụng không cần cài đặt môi trường. Bạn chỉ cần:
1. Giải nén source code.
2. Click đúp chuột mở file `index.html` bằng trình duyệt web hiện đại (Google Chrome, Microsoft Edge, hoặc Safari).

### 2. Cấu hình API Key
Để AI có thể hoạt động, bạn cần cung cấp API Key:
1. Truy cập [Google AI Studio](https://aistudio.google.com/app/apikey) để tạo API Key miễn phí.
2. Copy chuỗi Key.
3. Mở ứng dụng, dán vào ô **"Nhập Gemini API Key của bạn..."** ở cột bên trái và bấm **Lưu & Kiểm tra**. Key sẽ được lưu an toàn tại máy của bạn (`localStorage`).

### 3. Quy trình Tạo báo cáo chuẩn
1. Chọn **Loại báo cáo** (Tuần / Tháng). Nhập thông tin thời gian.
2. Tải dữ liệu đầu vào (Paste text vào khung Sale, kéo thả Ảnh hoặc file Excel vào các ô Cửa hàng/KPI).
3. Nhập **Ghi chú thêm cho AI** (nếu muốn AI nhấn mạnh một khía cạnh nào đó).
4. Bấm **"✦ Tạo báo cáo bằng AI"** và chờ hệ thống xử lý.
5. Sử dụng các nút chức năng (Đề xuất, Dự báo, Tải PDF) hoặc chat trực tiếp với AI để khai thác sâu hơn.

---

## ⚠️ Lưu ý Quan trọng (Best Practices & Troubleshooting)

* **Giới hạn API Miễn phí (Lỗi HTTP 429):** Bản miễn phí của Google Gemini giới hạn **15 yêu cầu / phút**. Nếu bạn thao tác các nút phân tích, dự báo hoặc chat quá nhanh liên tục, hệ thống sẽ báo lỗi. Hãy chờ 1-2 phút và thử lại.
* **Tối ưu file Excel Đầu vào:**
  * **Sử dụng `.csv` nếu có thể:** File CSV nhẹ và giúp AI đọc chuẩn xác 100% vì không chứa định dạng ẩn.
  * **Nếu dùng `.xlsx`:** Hãy "dọn dẹp" file (bỏ Merge Cells - gộp ô, bỏ các cột rác không cần thiết) trước khi upload. 
  * Định dạng quá lớn (hàng chục nghìn dòng) có thể làm tràn bộ nhớ AI (Payload too large). Khuyến nghị chỉ nạp dữ liệu đã lọc của kỳ báo cáo.
* **Quyền riêng tư:** Vì đây là ứng dụng gọi trực tiếp API của Google, không đưa các dữ liệu bảo mật cấp quốc gia, mật khẩu hệ thống hay số thẻ tín dụng vào file báo cáo. Toàn bộ tính năng lưu trữ lịch sử chỉ diễn ra tại máy tính cục bộ của bạn (Offline LocalStorage).
