# BÀI LÀM – HACKATHON 02

- **Mã đề:** 01
- **Họ tên: Lê Anh Duy**
- **Lớp: CNTT3**
- **[Link repository](https://github.com/maingwen2007-ops/CNTT3_Nhap-mon-CNTT_Hackathon02)**
- **Hệ điều hành (Windows/macOS): Windows**

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```powershell
PS C:\Luyen_Tap\starter-kit\starter-kit\san-bong-website> pwd
PS C:\Luyen_Tap\starter-kit\starter-kit\san-bong-website> ls -Force
PS C:\Luyen_Tap\starter-kit\starter-kit\san-bong-website> mv .\ghi_chu_ban_giao.txt .\docs\
PS C:\Luyen_Tap\starter-kit\starter-kit\san-bong-website> mkdir backup
PS C:\Luyen_Tap\starter-kit\starter-kit\san-bong-website> cp .\data\dat_san_thang_10.xlsx .\backup\
PS C:\Luyen_Tap\starter-kit\starter-kit\san-bong-website> rm .\temp_002.tmp -Force
PS C:\Luyen_Tap\starter-kit\starter-kit\san-bong-website> cd .\logs\
PS C:\Luyen_Tap\starter-kit\starter-kit\san-bong-website\logs> ls -Force
PS C:\Luyen_Tap\starter-kit\starter-kit\san-bong-website\logs> cd..
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
PS C:\Luyen_Tap\starter-kit\starter-kit\san-bong-website> ls -Force


    Directory: C:\Luyen_Tap\starter-kit\starter-kit\san-bong-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         11/3/2026   1:52 PM                data
d-----         11/3/2026   1:50 PM                docs
d-----         11/3/2026   1:50 PM                evidence
d-----         11/3/2026   1:52 PM                logs
d-r---         11/3/2026   1:49 PM                web
-a----         11/3/2026   1:47 PM             76 .env
-a----         11/3/2026   1:47 PM            154 ghi_chu_ban_giao.txt
-a----         11/3/2026   1:47 PM             22 temp_002.tmp
```

## 4.3. Lọc log truy cập website

### a) Lệnh lọc các dòng status=500

```powershell
PS C:\Luyen_Tap\starter-kit\starter-kit\san-bong-website> gc .\logs\access.log|sls "status=500" > .\logs\loi_500.txt
```

### 2 dòng đầu tiên trong logs/loi_500.txt

```text
2026-10-28 08:24:34 POST /api/thanh-toan status=500
2026-10-28 08:28:45 POST /api/thanh-toan status=500
```

### b) Lệnh đếm số dòng status=404 và kết quả

```powershell
PS C:\Luyen_Tap\starter-kit\starter-kit\san-bong-website> (gc .\logs\access.log|sls "status=404").count
```

```text
4
```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```powershell
PS C:\Luyen_Tap\starter-kit\starter-kit\san-bong-website> Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
PS C:\Luyen_Tap\starter-kit\starter-kit\san-bong-website> .\tong_hop.ps1
```

### Nội dung file logs/tong_hop.txt

```text
=== BAO CAO SU CO WEBSITE ===

2026-10-28 08:07:39 GET /tin-tuc status=404
2026-10-28 08:13:01 GET /dat-san-cu status=404
2026-10-28 08:34:07 GET /images/san-7.jpg status=404
2026-10-28 08:57:24 GET /khuyen-mai status=404




Count    : 6
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property : 
```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [x] README.md: Heading 1, mô tả có **in đậm** và *in nghiêng*, bảng, code block, task list, blockquote
- [ ] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [ ] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | --- | --- | --- |
| 1 | Network | logo.png | mở web/index.html bằng VS Code, tại dòng 10 có đoạn src="images/logo.png"; thay logo.png bằng đúng tên file ảnh trong thư mục web/images. Lưu file, tải lại trang (Ctrl + Shift + R) để logo hiển thị |
| 2 | Console | ERR_FILE_NOT_FOUND | Nhờ trưởng nhóm hỗ trợ |

> Ảnh chụp màn hình lưu trong thư mục `evidence/` 
![]()

### Báo cáo lỗi gửi trưởng nhóm

- **Context:** 
- **Expected:** 
- **Actual:** 
- **Log:** 

### Câu tìm kiếm Google

```text
(Ghi câu tìm kiếm vào đây – xoá dòng này)

```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/dat_san_thang_10.xlsx`, không cần ghi vào đây.
