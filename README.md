# Hướng dẫn triển khai Zalo Chat Widget

Tài liệu này hướng dẫn các bước chi tiết để tích hợp Zalo Chat Widget vào website của bạn.

## 1. Khởi tạo và thiết lập Zalo Official Account (OA)
Để sử dụng Zalo Chat Widget, trước tiên bạn cần phải có một tài khoản Zalo Official Account.

- Đăng ký hoặc đăng nhập vào trang quản lý Zalo OA.
- Tạo một tài khoản OA mới cho doanh nghiệp/cửa hàng của bạn.
- **Tài liệu tham khảo:** [Link docs: Dán link hướng dẫn tạo Zalo OA của bạn vào đây]

## 2. Lấy mã OA ID
Mỗi tài khoản Zalo OA đều có một mã định danh duy nhất gọi là OA ID. Bạn sẽ cần mã này để nhúng vào website.

- Truy cập phần Quản lý thông tin chung của OA.
- Sao chép dãy số OA ID.
- **Tài liệu tham khảo:** [Link docs: Dán link hướng dẫn lấy OA ID vào đây]

## 3. Cấu hình tên miền (Domain)
Để widget có thể hoạt động được trên website của bạn, bạn cần phải khai báo tên miền với Zalo để được cấp quyền.

- Vào phần Quản lý > Quản lý liên kết hoặc Quản lý Chat Widget trong Zalo OA.
- Thêm tên miền website của bạn (ví dụ: `demo-shop.com`).
- **Tài liệu tham khảo:** [Link docs: Dán link hướng dẫn cấu hình domain vào đây]

## 4. Lấy mã nhúng và nhúng vào Website
Zalo cung cấp một đoạn mã HTML/JavaScript để bạn chèn vào website.

- Lấy đoạn mã nhúng (thường có dạng `<div class="zalo-chat-widget"...></div>` và `<script src="https://sp.zalo.me/plugins/sdk.js"></script>`).
- Dán đoạn mã này vào tệp HTML của bạn (ưu tiên đặt ngay trước thẻ đóng `</body>`).
- Thay thế `YOUR_OA_ID` trong đoạn mã bằng OA ID bạn đã lấy ở **Bước 2**.
- **Tài liệu tham khảo:** [Link docs: Dán link hướng dẫn nhúng code vào đây]

## 5. Tùy chỉnh Widget (Tùy chọn)
Bạn có thể tùy chỉnh các thông số của widget để phù hợp với website của mình bằng cách thay đổi các thuộc tính `data-*` trong thẻ `<div>`.

Một số thuộc tính phổ biến:
- `data-welcome-message`: Lời chào mặc định khi khách mở chat.
- `data-autopopup`: Tự động mở khung chat (0: không, 1: có).
- `data-width`: Chiều rộng khung chat (pixel).
- `data-height`: Chiều cao khung chat (pixel).

- **Tài liệu tham khảo:** [Link docs: Dán link hướng dẫn tùy chỉnh thông số widget vào đây]

---
**Lưu ý:** Nếu widget không hiển thị sau khi nhúng, hãy kiểm tra lại:
1. OA ID đã chính xác chưa.
2. Tên miền đang chạy đã được khai báo trên Zalo OA chưa.
3. Trạng thái hoạt động của Zalo OA (đã được duyệt hay chưa).
