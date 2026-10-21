# Hướng dẫn sử dụng HVN Markdown Viewer cho Windows

HVN Markdown Viewer là ứng dụng xem file Markdown gọn nhẹ cho Windows 10 và Windows 11 (64-bit). App chỉ dùng để **xem**; muốn sửa nội dung, anh chị mở file bằng editor quen dùng, app sẽ tự cập nhật.

## Cài đặt

Tại trang [Releases](https://github.com/hvngroup/universal-mder-app-releases/releases) có hai bản:

| File | Dùng khi |
|:-----|:---------|
| `HVN-Markdown-Viewer-windows-x64-setup.exe` | Cài vào máy, gắn với file `.md` để nhấp đúp là mở. Không cần quyền quản trị. |
| `HVN-Markdown-Viewer-windows-x64-portable.zip` | Chạy ngay không cần cài: giải nén rồi mở `HVN Markdown Viewer.exe`. Không gắn với file `.md`. |

Muốn kiểm tra file tải về nguyên vẹn, so mã trong file `.sha256` đi kèm với kết quả lệnh `Get-FileHash <tên file>` trong PowerShell.

Bộ cài chưa được ký số, nên lần đầu Windows có thể hiện **Windows protected your PC**: bấm **More info → Run anyway**. App cần WebView2, có sẵn trên Windows 11 và Windows 10 đã cập nhật; bộ cài tự tải WebView2 nếu máy thiếu.

Giao diện mặc định bằng tiếng Việt. Tên nút trong tài liệu này ghi tiếng Việt, kèm tên tiếng Anh trong ngoặc cho máy đang dùng giao diện tiếng Anh.

## Mở tài liệu

- Nhấp đúp file `.md` trong File Explorer (bản cài đặt). Nếu Windows hỏi chọn app, chọn HVN Markdown Viewer và tích **Always**.
- Kéo file thả vào cửa sổ app.
- Bấm **Mở…** (Open…) trên thanh công cụ, hoặc Ctrl+O.

Mỗi tài liệu mở trong một cửa sổ riêng; mở lại file đang mở thì app đưa cửa sổ đó lên trước. App nhận các đuôi `.md`, `.markdown`, `.mdown`, `.mkd`, `.mkdn`.

## Giao diện

| Khu vực | Nội dung |
|:--------|:---------|
| Thanh bên trái | Mục lục các heading H1–H4. Bấm một dòng để nhảy tới phần đó. Chân thanh bên ghi tên file, số từ và thời gian đọc ước tính. |
| Thanh công cụ | Tên file, đường dẫn thư mục, ô tìm kiếm, nút In, Xuất PDF, Mở… và nút **⋯** (Cài đặt, hướng dẫn, hỗ trợ, giới thiệu). |
| Vùng nội dung | Tài liệu đã định dạng: bảng, task list, khối code có tô màu, trích dẫn, chú thích cuối trang, ảnh. |

Giao diện tự đổi theo chế độ Sáng/Tối của Windows.

## Phím tắt

| Thao tác | Phím tắt |
|:---------|:--------:|
| Mở file | Ctrl+O |
| Tìm trong tài liệu | Ctrl+F |
| Kết quả tiếp theo | F3, Enter hoặc Ctrl+G |
| Kết quả trước | Shift+F3, Shift+Enter hoặc Ctrl+Shift+G |
| Xoá ô tìm kiếm | Esc |
| Tải lại từ ổ đĩa | Ctrl+R hoặc F5 |
| Xuất PDF (khổ A4) | Ctrl+Shift+E |
| In | Ctrl+P |
| Mở Cài đặt | Ctrl+, |
| Mở hướng dẫn này | F1 |
| Đóng cửa sổ | Ctrl+W |

## Tìm kiếm

Gõ vào ô tìm kiếm: mọi kết quả được tô vàng, kết quả đang chọn tô cam, bên cạnh ghi thứ tự (ví dụ `2/15`). Tìm không phân biệt chữ hoa, chữ thường; chữ có dấu phải gõ đúng dấu (`má` không khớp `ma`). Ô tìm kiếm chuyển màu đỏ và ghi **Không thấy** khi tài liệu không có từ đó.

## Tự tải lại

Khi file đang mở được lưu từ editor khác, app cập nhật ngay và giữ nguyên vị trí cuộn; kết quả tìm kiếm được tìm lại trên nội dung mới. Nếu không thấy cập nhật, bấm Ctrl+R.

## Liên kết trong tài liệu

- Link web (`https://…`) và email (`mailto:…`) mở bằng trình duyệt hoặc ứng dụng thư mặc định.
- Link tới mục trong cùng tài liệu (`#ten-muc`) cuộn tới mục đó.
- Link tới file Markdown khác mở trong cửa sổ mới.
- Link tới file khác (PDF, ảnh, ứng dụng…) chỉ hiện file đó trong File Explorer, không tự mở, để tài liệu không thể khởi chạy chương trình lạ.

## Xuất PDF và In

- **Xuất PDF** (Export as PDF, Ctrl+Shift+E) hỏi nơi lưu rồi ghi tài liệu thành PDF khổ A4, chỉ gồm nội dung tài liệu.
- **In** (Print, Ctrl+P) mở hộp thoại in. Có thể chọn máy in **Microsoft Print to PDF** để lưu PDF với khổ giấy khác.

## Cài đặt ứng dụng

Bấm **⋯ → Cài đặt** (Settings, Ctrl+,).

- **Ngôn ngữ:** Tiếng Việt (mặc định), English, hoặc Theo Windows. Mọi cửa sổ đổi ngôn ngữ ngay, không cần khởi động lại.
- **Tự động kiểm tra bản cập nhật:** bật (mặc định) để app tự tìm bản mới mỗi ngày một lần.

## Cập nhật

Bấm **⋯ → Kiểm tra cập nhật…** (Check for Updates…) để tìm bản mới ngay. Khi có bản mới, app hiện số phiên bản và ghi chú phát hành:

- **Bản cài đặt:** bấm **Cài đặt và khởi động lại** (Install and Relaunch). App tải bộ cài mới, kiểm chữ ký số, cài rồi tự mở lại. Bản cập nhật chỉ được cài khi chữ ký khớp với khoá của HVN GROUP.
- **Bản portable:** không tự cập nhật. Bấm **Mở trang tải về**, tải file `portable.zip` mới và giải nén thay bản cũ.

Nếu Cài đặt ghi "Bản này chưa bật cập nhật tự động", hãy tải bản mới thủ công từ trang Releases.

## Xử lý sự cố

| Hiện tượng | Cách xử lý |
|:-----------|:-----------|
| Windows chặn bộ cài | Bấm **More info → Run anyway** (xem phần Cài đặt). |
| App mở ra cửa sổ trắng | Cài hoặc cập nhật Microsoft Edge WebView2 Runtime từ trang của Microsoft. |
| Nhấp đúp file `.md` không mở app | Chuột phải file → **Open with → Choose another app** → chọn HVN Markdown Viewer, tích **Always**. |
| Ảnh không hiển thị | Kiểm tra đường dẫn ảnh tương đối so với thư mục chứa file `.md`. |
| Nội dung không tự cập nhật | Bấm Ctrl+R; nếu file đã bị đổi tên hoặc di chuyển, mở lại file. |
| Báo không kiểm tra được bản cập nhật | Kiểm tra kết nối mạng hoặc proxy công ty (app cần truy cập `github.com`), rồi thử lại. |

## Hỗ trợ

- Email kỹ thuật: [kythuat@hvn.vn](mailto:kythuat@hvn.vn)
- Hotline: 024.9999.7777
- Website: [hvn.vn](https://hvn.vn)

---

HVN GROUP · hvn.vn
