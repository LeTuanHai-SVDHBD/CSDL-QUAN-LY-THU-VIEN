# [cite_start]📚 Dự Án: Quản Lý Thư Viện [cite: 1]

[cite_start]Dự án này tập trung vào việc thiết kế và xây dựng cơ sở dữ liệu cho hệ thống Quản lý Thư viện. [cite: 1]

---

## [cite_start]👥 Thành viên nhóm và Phân công [cite: 2, 8]

| MSSV | Họ và tên | Nhiệm vụ chính |
| :--- | :--- | :--- |
| 23050084 | [cite_start]Lê Ngọc Sang [cite: 3] | [cite_start]Ý tưởng, E-R [cite: 10] |
| 23050108 | [cite_start]La Trần Duy Đạt [cite: 4] | [cite_start]Lý do chọn đề tài, Ý tưởng, E-R [cite: 9, 10] |
| 23050116 | [cite_start]Lê Tuấn Hải [cite: 5] | [cite_start]Lược đồ Quan hệ [cite: 11] |
| 23050118 | [cite_start]Nguyễn Tuấn Anh [cite: 6] | [cite_start]Ý tưởng, E-R [cite: 10] |
| 23050120 | [cite_start]Nguyễn Minh Cang [cite: 7] | [cite_start]Lược đồ Quan hệ [cite: 11] |

---

## [cite_start]💡 Phân Tích Hệ Thống [cite: 12]

### [cite_start]1. Thực thể và Thuộc tính [cite: 13, 14]
* [cite_start]**Sách:** Mã sách, tên sách, tên tác giả, tên NXB. [cite: 15]
* [cite_start]**Loại sách:** Mã loại sách, Thể loại. [cite: 16]
* [cite_start]**Khách Hàng:** Mã KH, tên, tuổi, số ĐT, email. [cite: 17]
* [cite_start]**Nhà Xuất Bản:** Mã nhà xuất bản, tên, địa chỉ, Số ĐT, email. [cite: 18]
* [cite_start]**Nhân Viên:** Mã nhân viên, tên, địa chỉ, Số ĐT, email, Chức vụ. [cite: 19]
* [cite_start]**Phòng Ban:** Mã Phòng ban, Tên Phòng, Loại Phòng. [cite: 20]

### [cite_start]2. Các Mối Quan Hệ [cite: 21, 22]
* [cite_start]**Sách và Khách hàng (Nhiều – Nhiều):** Một cuốn sách có thể được mượn bởi nhiều khách hàng và một khách hàng có thể mượn nhiều cuốn sách. [cite: 23]
    * [cite_start]*Ghi chú:* Phát sinh thuộc tính **Số ngày mượn**. [cite: 24]
* [cite_start]**Sách và Nhà Xuất Bản (1 – Nhiều):** Một cuốn sách chỉ được xuất bản bởi một NXB, nhưng một NXB có thể xuất bản nhiều sách. [cite: 25]
* [cite_start]**Sách và Loại Sách (1 – Nhiều):** Một cuốn sách chỉ thuộc một loại duy nhất, một loại sách có thể chứa nhiều sách. [cite: 26]
* [cite_start]**Sách và Phòng Ban (1 – Nhiều):** Một cuốn sách chỉ thuộc về một phòng, một phòng có thể chứa nhiều sách. [cite: 27]
* [cite_start]**Nhân Viên và Phòng Ban (1 – Nhiều):** Một nhân viên chỉ làm việc tại một phòng ban, một phòng ban có nhiều nhân viên. [cite: 28]
* [cite_start]**Nhân Viên và Sách (Nhiều – Nhiều):** Một nhân viên có thể quản lý nhiều sách và một cuốn sách có thể được quản lý bởi nhiều nhân viên. [cite: 29]

---

## [cite_start]📐 Lược Đồ Quan Hệ [cite: 92]

Các bảng trong hệ thống được định nghĩa như sau:

* [cite_start]**Sách:** `Sach(MaSach, NamXB, tenNXB, TenSach, Tacgia, MaNXB, MaLS, MaPHG)` [cite: 85]
* [cite_start]**Nhân Viên:** `NhanVien(MaNV, tenNV, tuoiNV, sdtNV, emailNV, ChucVu, MaPHG)` [cite: 86]
* [cite_start]**Bảng Thống Kê:** `BangThongKe(MaBTK, LoaiBang, MaNV, MaSach)` [cite: 86]
* [cite_start]**Khách Hàng:** `KhachHang(MaKH, tenKH, tuoiKH, sdtKH, emailKH)` [cite: 87]
* [cite_start]**Nhà Xuất Bản:** `NhaXuatBan(MaNXB, tenNXB, dcNXB, sdtNXB, emailNXB)` [cite: 88]
* [cite_start]**Phòng Ban:** `PhongBan(MaPHG, tenPHG, loaiPHG)` [cite: 89]
* [cite_start]**Loại Sách:** `LoaiSach(MaLS, theloai)` [cite: 90]
* [cite_start]**Mượn:** `Muon(MaSach, MaKH, songaymuon)` [cite: 91]

---
