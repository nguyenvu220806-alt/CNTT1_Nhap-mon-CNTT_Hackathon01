# BÀI LÀM – HACKATHON 01

- **Mã đề:** 22
- **Họ tên:** Nguyễn Hồng Vũ 
- **Lớp:** CNTT1
- **Link repository:** 
- **Hệ điều hành (Windows/macOS):** Windown

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
B1: pwd
B2: ls -force 
B3: mv .\bang_quy_trinh.txt .\docs\
B4: mv .\logo_rua_xe.PNG .\media\
B5: cp .\media\logo_rua_xe.PNG .\backup\
B6: rm .\temp_305.tmp
B7: cd logs
    ls
    cd ..
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
PS C:\Users\GIGA\Downloads\starter-kit\starter-kit\rua-xe-website> pwd

Path
----
C:\Users\GIGA\Downloads\starter-kit\starter-kit\rua-xe-website


PS C:\Users\GIGA\Downloads\starter-kit\starter-kit\rua-xe-website> ls -force


    Directory: C:\Users\GIGA\Downloads\starter-kit\starter-kit\rua-xe-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        2026/10/28      7:55                backup
d-----        2026/10/28      8:00                data
d-----        2026/10/28      7:55                docs
d-----        2026/10/28      8:00                logs
d-----        2026/10/28      7:55                media
------        2026/10/27      1:32             64 .env
-a----        2026/10/28      7:52           2190 bai_lam.md
-a----        2026/10/27      1:32             53 bang_quy_trinh.txt
-a----        2026/10/27      1:32           6191 logo_rua_xe.PNG
------        2026/10/27      1:32             22 temp_305.tmp


 Directory: C:\Users\GIGA\Downloads\starter-kit\starter-kit\rua-xe-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        2026/10/27      1:32           1029 carwash.log


PS C:\Users\GIGA\Downloads\starter-kit\starter-kit\rua-xe-website\logs> ls


    Directory: C:\Users\GIGA\Downloads\starter-kit\starter-kit\rua-xe-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        2026/10/27      1:32           1029 carwash.log


```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell


```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
(Dán kết quả vào đây – xoá dòng này)

```

## 4.4. Thao tác với tài liệu Markdown (README.md)

> README.md được chấm trực tiếp trên file `README.md` ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [ ] Heading 1: tên dự án
- [ ] Mô tả ngắn có cả **in đậm** và *in nghiêng*
- [ ] Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu
- [ ] Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án
- [ ] Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành
- [ ] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
## Script: auto_report.ps1
# Tac gia: Nguyễn Hồng Vũ 
# Ngay tao: 28/10/2026

Write-Host "Dang loc log ... "

" === BAO CAO LOI === "> ni carwash.log
Get-Content logs/carwash.log | Select-String "ERROR" >> logs/daily_report.txt

Write-Host "Hoan thanh!"

```

### Kết quả hiển thị

```text
Script: auto_report.ps1
 Tac gia: Nguyễn Hồng Vũ 
 Ngay tao: 28/10/2026

Write-Host "Dang loc log ... "

" === BAO CAO LOI === "> ni carwash.log
Get-Content logs/carwash.log | Select-String "ERROR" >> logs/daily_report.txt

Write-Host "Hoan thanh!"

```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
select-string "ERROR" carwash.log | Measure-Object | out-file daily_report.txt -Append

```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```text
2

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
 ni logs/tong_hop.txt
 "=== TONG HOP LOG ===" >  tong_hop.txt    
 select-string "WARNING" carwash.log | Out-file tong_hop.txt -Append
 select-string "ERROR" carwash.log | Measure-Object | out-file tong_hop.txt -Append 

```

### Nội dung file logs/tong_hop.txt

```text


```

## 4.8. Excel

> Phần Excel được chấm trực tiếp trên file `data/luot_rua_xe_thang_2.xlsx`, không cần ghi vào đây.
