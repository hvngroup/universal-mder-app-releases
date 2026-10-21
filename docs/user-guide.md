# Hướng dẫn sử dụng HVN Markdown Viewer

HVN Markdown Viewer là ứng dụng xem file Markdown gọn nhẹ cho máy Mac chip Apple, chạy macOS 13 Ventura trở lên. App chỉ dùng để **xem**; muốn sửa nội dung, anh chị mở file bằng editor quen dùng, app sẽ tự cập nhật.

## Cài đặt

1. Tải `HVN-Markdown-Viewer.dmg` tại trang [Releases](https://github.com/hvngroup/universal-mder-app-releases/releases) của repo. Muốn kiểm tra file tải về nguyên vẹn, so mã trong `HVN-Markdown-Viewer.dmg.sha256` với kết quả lệnh `shasum -a 256 HVN-Markdown-Viewer.dmg`.
2. Mở file `.dmg`, kéo **HVN Markdown Viewer** vào lối tắt **Applications** ngay bên cạnh.
3. Mở app từ **Applications**. App được ký Developer ID của HVN GROUP và đã qua kiểm tra của Apple, nên macOS chỉ hỏi xác nhận lần đầu: bấm **Open**. (Bản 1.2.2 trở về trước chưa ký: nếu macOS chặn, vào **System Settings → Privacy & Security** và bấm **Open Anyway**.)
4. Đặt làm app mặc định cho file `.md`: chuột phải một file `.md` → **Get Info** → **Open with** → chọn HVN Markdown Viewer → **Change All…**.

Giao diện mặc định bằng tiếng Việt. Tên menu trong tài liệu này ghi tiếng Việt, kèm tên tiếng Anh trong ngoặc cho máy đang dùng giao diện tiếng Anh.

## Mở tài liệu

- Nhấp đúp file `.md` trong Finder (sau khi đặt làm app mặc định).
- Kéo file thả vào icon app trên Dock.
- **Tệp → Mở…** (File → Open…, ⌘O) hoặc **Tệp → Mở gần đây** (Open Recent).

App nhận các đuôi `.md`, `.markdown`, `.mdown`, `.mkd`, `.mkdn`.

## Giao diện

| Khu vực | Nội dung |
|:--------|:---------|
| Thanh bên trái | Mục lục các heading H1–H4. Bấm một dòng để nhảy tới phần đó. Chân thanh bên ghi tên file, số từ và thời gian đọc ước tính. |
| Thanh công cụ | Tên file, đường dẫn thư mục, ô tìm kiếm, nút In và Xuất PDF. |
| Vùng nội dung | Tài liệu đã định dạng: bảng, task list, khối code có tô màu, trích dẫn, chú thích cuối trang, ảnh. |

Giao diện tự đổi theo chế độ Sáng/Tối của macOS. Ẩn hoặc hiện thanh bên bằng ⌃⌘S, menu **Xem** (View), hoặc nút thanh bên trên thanh công cụ.

## Phím tắt

| Thao tác | Phím tắt |
|:---------|:--------:|
| Tìm trong tài liệu | ⌘F |
| Kết quả tiếp theo | ⌘G |
| Kết quả trước | ⇧⌘G |
| Tải lại từ ổ đĩa | ⌘R |
| Xuất PDF (khổ A4) | ⇧⌘E |
| In | ⌘P |
| Ẩn/hiện thanh bên | ⌃⌘S |
| Mở Cài đặt | ⌘, |
| Mở hướng dẫn này | ⌘? |

## Tự tải lại

Khi file đang mở được lưu từ editor khác, app cập nhật trong khoảng một giây và giữ nguyên vị trí cuộn. Nếu không thấy cập nhật, bấm ⌘R để tải lại.

## Liên kết trong tài liệu

- Link web (`https://…`) và email (`mailto:…`) mở bằng trình duyệt hoặc ứng dụng thư mặc định.
- Link tới mục trong cùng tài liệu (`#ten-muc`) cuộn tới mục đó.
- Link tới file Markdown khác mở trong cửa sổ mới.
- Link tới file khác (PDF, ảnh, ứng dụng…) chỉ hiện file đó trong Finder, không tự mở, để tài liệu không thể khởi chạy chương trình lạ.

## Xem nhanh bằng phím Space (Quick Look)

Chọn file `.md` trong Finder và bấm Space để xem bản đã định dạng mà không cần mở app.

Nếu Quick Look vẫn hiện văn bản thô:

1. Đảm bảo app nằm trong **Applications** và đã được mở ít nhất một lần.
2. Kiểm tra **System Settings → General → Login Items & Extensions → Quick Look** đã bật HVN Markdown Viewer.
3. Chạy `qlmanage -r` trong Terminal rồi thử lại.

Trong Quick Look, ảnh theo đường dẫn tương đối có thể không hiển thị do giới hạn sandbox của macOS; mở bằng app để xem đầy đủ.

## Xuất PDF và In

- **Tệp → Xuất PDF…** (Export as PDF…, ⇧⌘E) lưu tài liệu thành PDF khổ A4, luôn dùng giao diện sáng.
- **Tệp → In…** (Print…, ⌘P) mở hộp thoại in của macOS.

## Cài đặt ứng dụng

Mở bằng **HVN Markdown Viewer → Cài đặt…** (Settings…, ⌘,).

- **Ngôn ngữ:** Tiếng Việt (mặc định), English, hoặc Theo hệ thống. Sau khi đổi, bấm **Khởi động lại** để áp dụng.
- **Tự động kiểm tra bản cập nhật:** bật để app tự tìm bản mới. Cũng có thể kiểm tra thủ công bằng **HVN Markdown Viewer → Kiểm tra cập nhật…**. Bản cập nhật chỉ được cài khi có chữ ký số khớp với khoá của HVN GROUP.

Nếu Cài đặt ghi "Bản cài đặt này chưa bật cập nhật tự động", hãy tải bản mới thủ công từ trang Releases.

## Xử lý sự cố

| Hiện tượng | Cách xử lý |
|:-----------|:-----------|
| macOS báo không mở được app | Làm theo bước 3 phần Cài đặt. |
| Ảnh không hiển thị | Kiểm tra đường dẫn ảnh tương đối so với thư mục chứa file `.md`. |
| Nội dung không tự cập nhật | Bấm ⌘R; nếu file đã bị đổi tên hoặc di chuyển, mở lại file. |
| Quick Look không hoạt động | Xem phần Xem nhanh bằng phím Space. |
| Giao diện không đổi ngôn ngữ | Thoát hẳn app (⌘Q) rồi mở lại sau khi chọn ngôn ngữ trong Cài đặt. |

## Hỗ trợ

- Email kỹ thuật: [kythuat@hvn.vn](mailto:kythuat@hvn.vn)
- Hotline: 024.9999.7777
- Website: [hvn.vn](https://hvn.vn)

---

HVN GROUP · hvn.vn
