# Bảo mật

## Báo lỗ hổng

Vui lòng **không mở issue công khai**. Gửi riêng tới **kythuat@hvn.vn** hoặc qua
[GitHub Security Advisories](https://github.com/hvngroup/universal-mder-app-releases/security/advisories/new),
kèm phiên bản bị ảnh hưởng và các bước tái hiện (một file `.md` mẫu là đủ). HVN GROUP phản hồi trong vài ngày
làm việc và ghi công người báo trong release notes nếu anh/chị muốn.

Không gửi kèm tài liệu chứa thông tin nội bộ hay dữ liệu khách hàng.

## App xử lý tài liệu thế nào

- Tài liệu chỉ được đọc trên máy; app không gửi nội dung đi đâu và không có telemetry.
- HTML trong Markdown được lọc bằng DOMPurify; Content Security Policy chỉ cho chạy script đóng gói sẵn trong app.
- Link tới file cục bộ không phải Markdown chỉ được hiện trong Finder, không bao giờ được mở, để tài liệu không thể
  khởi chạy chương trình.
- Quick Look extension chạy trong sandbox của macOS.
- Kết nối mạng duy nhất do app chủ động: tải ảnh từ link `http(s)` có trong tài liệu, và — khi bản cài có bật cập
  nhật — Sparkle đọc `appcast.xml` từ GitHub Releases của repo này. Bản cập nhật phải có chữ ký EdDSA khớp khoá
  công khai trong app thì mới được cài.

## Phiên bản được hỗ trợ

Chỉ bản phát hành mới nhất được vá lỗi.

---

HVN GROUP · hvn.vn
