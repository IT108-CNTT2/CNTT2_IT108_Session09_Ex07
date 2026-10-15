# Báo cáo Phân tích và Hiệu chỉnh Cú pháp Markdown

## Phần 1: Phân tích Lỗi

Các lỗi cú pháp xuất hiện trong đoạn Markdown gốc cùng hậu quả khi hệ thống render:

1. **Thiếu khoảng trắng sau thẻ Heading (`###Lưu ý quan trọng`)**
   - **Lỗi:** Dấu `###` dính liền với chữ "Lưu ý quan trọng" mà không có khoảng trắng.
   - **Hậu quả:** Hệ thống không nhận diện đây là tiêu đề (Heading 3), hiển thị nguyên văn chuỗi ký tự `###Lưu ý quan trọng` trên trang web.

2. **Thiếu khoảng trắng sau dấu gạch ngang của danh sách (`-Bước 1:...`)**
   - **Lỗi:** Các dòng danh sách viết liền dấu `-` với nội dung.
   - **Hậu quả:** Trình biên dịch không nhận diện đây là danh sách, khiến các mục hiển thị thành văn bản thông thường (plain text) thay vì danh sách gạch đầu dòng.

3. **Thiếu dấu đóng định dạng in đậm (`**HNKS25CNTT1_IT101_Session08`)**
   - **Hậu quả:** Thẻ mở `**` không có thẻ đóng tương ứng ở cuối, làm hỏng cấu trúc định dạng văn bản khiến toàn bộ phần sau bị lỗi hiển thị.

4. **Thiếu tiền tố giao thức trong đường dẫn (`[GitHub](github.com)`)**
   - **Lỗi:** Đường dẫn liên kết thiếu tiền tố `https://`.
   - **Hậu quả:** Trình duyệt hiểu nhầm đây là đường dẫn tương đối (relative link), dẫn đến lỗi **404 Not Found** khi người dùng bấm vào.

5. **Sai lệch và không đồng bộ thẻ đánh dấu văn bản nghiêng/đậm (`*...**`)**
   - **Lỗi:** Đoạn trích dẫn mở đầu bằng một dấu sao `*` nhưng kết thúc bằng hai dấu sao `**`.
   - **Hậu quả:** Cú pháp bị lỗi phân tích, hiển thị thừa các ký tự thô ra ngoài giao diện trang web.

---

## Phần 2: Sửa lỗi và Hoàn thiện

### 1. Đoạn Markdown đã được sửa chuẩn xác
```markdown
## Hướng Dẫn Nộp Bài Tập - Session 08

### Lưu ý quan trọng

Các bước nộp bài:
- Bước 1: Tạo tài khoản GitHub tại [GitHub](https://github.com)
- Bước 2: Tạo repository mới đặt tên theo định dạng **HNKS25CNTT1_IT101_Session08**
- Bước 3: Upload file .md của bài làm lên repository
- Bước 4: Copy đường dẫn và nộp lên Portal

> Deadline: Chủ nhật 23:59 — *Nộp muộn sẽ bị trừ 50% điểm!*
