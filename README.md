# Hướng dẫn triển khai Zalo Chat Widget

Tài liệu này hướng dẫn các bước chi tiết để tích hợp Zalo Chat Widget vào website của bạn.

## 1. Khởi tạo và thiết lập Zalo Official Account (OA)
Để sử dụng Zalo Chat Widget, trước tiên bạn cần phải có một tài khoản Zalo Official Account.

- Đăng ký hoặc đăng nhập vào trang quản lý Zalo OA.
- Tạo một tài khoản OA mới cho doanh nghiệp/cửa hàng của bạn.
- **Tài liệu tham khảo:** [Zalo OA create](https://id.zalo.me/account/login?continue=https%3A%2F%2Foauth.zaloapp.com%2Fv4%2Fpermission%3Fapp_id%3D2867666335705903556%26redirect_uri%3Dhttps%253A%252F%252Foa.zalo.me%252Fzoauth%252Fadmin%252Fverify%26code_challenge%3DiQBh3TT2kEapqGms_hB35JpynQUHLtxMtqwj-r8fsCc%26state%3DgMFYwmCuBrnxcl01rh753Q)

## 2. Lấy mã OA ID
Mỗi tài khoản Zalo OA đều có một mã định danh duy nhất gọi là OA ID. Bạn sẽ cần mã này để nhúng vào website.

- Truy cập phần Quản lý thông tin chung của OA.
- Sao chép dãy số OA ID.
- **Tài liệu tham khảo:** [Zalo OA ID](https://oa.zalo.me/home/documents/guides/lay-oa-id_2183147545189302941)


## 3. Lấy mã nhúng và nhúng vào Website
Zalo cung cấp một đoạn mã HTML/JavaScript để bạn chèn vào website.

- Lấy đoạn mã nhúng (thường có dạng )
`<div class="zalo-chat-widget" 
    data-oaid="YOUR_OA_ID" 
    data-welcome-message="Rất vui khi được hỗ trợ bạn!"
    data-autopopup="0" 
    data-width="300" 
    data-height="300">
</div>

<script src="https://sp.zalo.me/plugins/sdk.js"></script>`

- Dán đoạn mã này vào tệp HTML của bạn (ưu tiên đặt ngay trước thẻ đóng `</body>`).
- Thay thế `YOUR_OA_ID` trong đoạn mã bằng OA ID bạn đã lấy ở **Bước 2**.
- **Tài liệu tham khảo:** [Zalo widget chat](https://oa.zalo.me/home/documents/guides/lay-oa-id_2183147545189302941)

## 4. Tùy chỉnh Widget (Tùy chọn)
Bạn có thể tùy chỉnh các thông số của widget để phù hợp với website của mình bằng cách thay đổi các thuộc tính `data-*` trong thẻ `<div>`.

Một số thuộc tính phổ biến:
- `data-oaid`: Zalo Official Account ID (bắt buộc phải có).
- `data-welcome-message`: Lời chào mặc định khi khách mở chat.
- `data-autopopup`: Tự động mở khung chat (0: không, 1: có).
- `data-width`: Chiều rộng khung chat (pixel).
- `data-height`: Chiều cao khung chat (pixel).

- **Tài liệu tham khảo:** [Zalo widget chat](https://developers.zalo.me/docs/social/zalo-chat-widget)

---
**Lưu ý:** Nếu widget không hiển thị sau khi nhúng, hãy kiểm tra lại:
1. OA ID đã chính xác chưa.
2. Trạng thái hoạt động của Zalo OA (đã được duyệt hay chưa).
