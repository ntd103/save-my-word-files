# save-my-word-files
MS Word is really annoying. I am here to save you.

Vào một ngày đẹp trời, bạn chỉnh sửa file word chỉn chu, giáo viên của bạn đã review ưng. Như một thói quen, bạn cập nhật mục lục, số trang,.. lần cuối.
Bạn lưu cẩn thận và mở lại lần nữa để chắc chắn mọi thứ vẫn bình thường.
Rồi bạn xuất sang định dạng pdf. BOOM. Trang pdf trắng trơn, mở lại file word cũng nhẵn nhụi. Nhưng nó vẫn nặng vài MB dù không có gì bên trong cả. 

Đây là giải pháp cho bạn.

## Usage
*4 cách dưới bạn có thể thử ngẫu nhiên không bắt theo thứ tự. Bạn hoàn toàn có thể chọn luôn cách giải quyết của tác giả*

Ngoài lề: Tác giả khi đó, thằng sinh viên năm 2 khờ khạo có con AI duy nhất là GG Assistant đã lục tung cái internet lên để ra cái sớ phía dưới (giờ có chatgpt chắc nửa tiếng :v)
NHƯNG tất cả đều fail. Tui đã phải xin thầy hoãn lùi 3 ngày để viết lại. Ngồi gõ dc nửa tiếng, tui đã bỏ cuộc vì bản thân quá lười để có thể hồi tưởng lại gần 200 trang mình từng gõ :v

Wel, tui đã ngồi mò được thì file word bản chất là xml thui. Lỗi mất văn bản khả năng là chồng chéo các mục nhảy tự động. Thế là tui code cái tool bên dưới để xoá hết mấy cái mục đó đi, còn nội dung văn bản thì còn nguyên. Chỉ vậy thui.

>WARNING
>Step 0: Luôn lưu backup lại bản lỗi chính đó. Chúng ta chỉ làm việc với bản copied.


Cách 0: Tui k biết mấy cách dưới có hoạt động k nữa, vì tui thử fail hết. 
Đây là tool tui làm. 
1. Đổi đuôi file `mydoc.docx` → `mydoc.zip`
2. Giải nén file zip trên
3. copy file strip_fields.ps1 vào folder giải nén
4. Mở chuột phải → chọn Open Powershell here → gõ `.\strip_fields.ps1` → Enter
5. Xong rồi thì lại nén lại thành file `.zip`, đổi tên lại về `.docx`. DONE



**Cách 1**: Repair built-in
1. Mở word (không mở file trực tiếp)
2. Vào File → Open → Browse
3. Tìm đến file bị lỗi, click 1 lần để chọn (không double-click)
4. Nhấn vào mũi tên nhỏ bên cạnh nút Open
5. Chọn Open and Repair

**Cách 2**: Mở Word ở chế độ Safe Mode
1. Nhấn Windows + R, gõ winword.exe /a → Enter
2. Word mở không có add-ins, template lỗi
3. Vào File → Open → chọn file bị hỏng → Open and Repair

**Cách 3**: Dùng công cụ phục hồi online
Nếu các cách trên thất bại, upload file lên các công cụ chuyên dụng:
1. [File Repair Online - Recover Corrupted DOCX Files Fast](https://www.filerepaironline.com/) — hỗ trợ DOCX đến 4MB, preview miễn phí, trả phí nếu muốn download
2. [DOCX Repair Tool to Repair Damaged & Corrupt DOCX File](https://www.systoolsgroup.com/docx-repair.html) — cài đặt offline, hiệu quả với file nặng

**Cách 4**: Chèn vào document mới
Nếu file vẫn mở được dù trống:
1. Tạo file Word mới blank
2. Vào Insert → Object → Text from File
3. Chọn file bị lỗi → Insert
Word sẽ cố gắng extract nội dung vào document mới
