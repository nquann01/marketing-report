# ⚡ Báo Cáo Tổng Hợp — AI

Đây là một ứng dụng Web Single-Page (SPA) hỗ trợ tổng hợp và phân tích báo cáo kinh doanh Tuần/Tháng tự động. Ứng dụng tận dụng sức mạnh của **Google Gemini API** (Mô hình đa phương thức) để đọc, trích xuất số liệu từ văn bản, hình ảnh, file Excel/CSV và đưa ra các đánh giá, đề xuất chiến lược chuyên sâu.

## ✨ Tính năng nổi bật

- **Tự động hóa hoàn toàn:** Đọc dữ liệu từ văn bản thô (Sale copy), hình ảnh chụp bảng biểu cửa hàng và file Excel/CSV.
- **Phân tích Đa phương thức (Multimodal):** Hỗ trợ kéo thả ảnh báo cáo KPI, doanh thu cửa hàng để AI tự động nhận diện và đối chiếu số liệu.
- **AI Cố vấn Chiến lược:** Tính năng đề xuất tối ưu và chẩn đoán "điểm mù" của các cửa hàng dựa trên dữ liệu kinh doanh thực tế.
- **Lưu trữ Lịch sử:** Tự động lưu các bản báo cáo đã tạo vào `localStorage` của trình duyệt, dễ dàng xem lại hoặc xóa bất cứ lúc nào.
- **Xuất Báo Cáo:** Hỗ trợ xuất báo cáo ra file **PDF** hoặc **Ảnh (PNG)** chất lượng cao, đồng thời hỗ trợ nút "Sao chép" chuẩn format để dán vào Zalo/Telegram/Word.
- **Quản lý API Key an toàn:** Lưu trữ API Key trực tiếp trên trình duyệt của người dùng (Local Storage), không gửi dữ liệu qua bất kỳ máy chủ trung gian nào ngoài Google.

## 🚀 Hướng dẫn cài đặt & Sử dụng

Ứng dụng được xây dựng hoàn toàn bằng HTML, CSS, và Vanilla JavaScript, không yêu cầu cài đặt môi trường phức tạp.

1. **Tải mã nguồn:** Clone repository này hoặc tải file `index.html` về máy.
2. **Khởi chạy:** - Bạn chỉ cần nhấp đúp chuột vào file `index.html` để mở trực tiếp trên trình duyệt (Chrome, Edge, Safari...).
   - *Khuyến nghị:* Dùng extension như **Live Server** trên VS Code để có trải nghiệm tốt nhất nếu bạn muốn chỉnh sửa code.
3. **Cài đặt API Key:**
   - Truy cập [Google AI Studio](https://aistudio.google.com/app/apikey) để tạo Gemini API Key.
   - Mở ứng dụng, dán mã Key vào ô **Cài đặt API Key** ở cột bên trái và nhấn **Lưu & Kiểm tra**.
4. **Tạo Báo Cáo:**
   - Chọn loại báo cáo (Tuần/Tháng).
   - Dán dữ liệu text hoặc tải ảnh/file Excel tương ứng vào các ô được yêu cầu.
   - Nhấn **✦ Tạo báo cáo bằng AI** và chờ kết quả.

## 🛠️ Công nghệ sử dụng

- **Frontend:** HTML5, CSS3, JavaScript (Vanilla).
- **Phông chữ:** [Be Vietnam Pro](https://fonts.google.com/specimen/Be+Vietnam+Pro), JetBrains Mono.
- **AI Model:** Google Gemini 2.5 Flash API (`gemini-2.5-flash`).
- **Thư viện bên thứ 3:** - [html2canvas](https://html2canvas.hertzen.com/) (Hỗ trợ render HTML sang Canvas/Image).
  - [html2pdf.js](https://ekoopmans.github.io/html2pdf.js/) (Hỗ trợ xuất file PDF).

## ⚠️ Lưu ý bảo mật

- **API Key:** Ứng dụng lưu API key của bạn trong `localStorage` của trình duyệt. Hãy cẩn thận khi sử dụng ứng dụng trên các thiết bị công cộng. Nhấn nút **Xoá** ở phần API Key sau khi sử dụng xong nếu dùng chung máy tính.
- **Dữ liệu:** Các file ảnh và text bạn tải lên sẽ được gửi trực tiếp đến server của Google Gemini để phân tích. Không có backend nội bộ nào lưu trữ dữ liệu này. Nếu bạn host ứng dụng này công khai lên mạng (như GitHub Pages, Vercel), hãy đảm bảo người dùng hiểu rõ dữ liệu của họ sẽ đi đâu.

## 📝 Giấy phép (License)
Dự án được phân phối dưới giấy phép MIT. Xem thêm chi tiết trong file `LICENSE` (nếu có).
