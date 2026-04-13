# 📚 Dự Án: Quản Lý Thư Viện

Dự án này tập trung vào việc thiết kế và xây dựng cơ sở dữ liệu cho hệ thống Quản lý Thư viện.

---

## 👥 Thành viên nhóm và Phân công

| MSSV | Họ và tên | Nhiệm vụ chính |
| :--- | :--- | :--- |
| 23050084 | Lê Ngọc Sang | Ý tưởng, E-R |
| 23050108 | La Trần Duy Đạt | Lý do chọn đề tài, Ý tưởng, E-R |
| 23050116 | Lê Tuấn Hải | Lược đồ Quan hệ |
| 23050118 | Nguyễn Tuấn Anh | Ý tưởng, E-R |
| 23050120 | Nguyễn Minh Cang | Lược đồ Quan hệ |

---

## 💡 Phân Tích Hệ Thống

### 1. Thực thể và Thuộc tính
* **Sách:** Mã sách, tên sách, tên tác giả, tên NXB.
* **Loại sách:** Mã loại sách, Thể loại.
* **Khách Hàng:** Mã KH, tên, tuổi, số ĐT, email.
* **Nhà Xuất Bản:** Mã nhà xuất bản, tên, địa chỉ, Số ĐT, email.
* **Nhân Viên:** Mã nhân viên, tên, địa chỉ, Số ĐT, email, Chức vụ.
* **Phòng Ban:** Mã Phòng ban, Tên Phòng, Loại Phòng.

### 2. Các Mối Quan Hệ
* **Sách và Khách hàng (Nhiều – Nhiều):** Một cuốn sách có thể được mượn bởi nhiều khách hàng và một khách hàng có thể mượn nhiều cuốn sách.
    * *Ghi chú:* Phát sinh thuộc tính **Số ngày mượn**.
* **Sách và Nhà Xuất Bản (1 – Nhiều):** Một cuốn sách chỉ được xuất bản bởi một NXB, nhưng một NXB có thể xuất bản nhiều sách.
* **Sách và Loại Sách (1 – Nhiều):** Một cuốn sách chỉ thuộc một loại duy nhất, một loại sách có thể chứa nhiều sách.
* **Sách và Phòng Ban (1 – Nhiều):** Một cuốn sách chỉ thuộc về một phòng, một phòng có thể chứa nhiều sách.
* **Nhân Viên và Phòng Ban (1 – Nhiều):** Một nhân viên chỉ làm việc tại một phòng ban, một phòng ban có nhiều nhân viên.
* **Nhân Viên và Sách (Nhiều – Nhiều):** Một nhân viên có thể quản lý nhiều sách và một cuốn sách có thể được quản lý bởi nhiều nhân viên.

---

## 📐 Lược Đồ Quan Hệ

Các bảng trong hệ thống được định nghĩa như sau:

* **Sách:** `Sach(MaSach, NamXB, tenNXB, TenSach, Tacgia, MaNXB, MaLS, MaPHG)`
* **Nhân Viên:** `NhanVien(MaNV, tenNV, tuoiNV, sdtNV, emailNV, ChucVu, MaPHG)`
* **Bảng Thống Kê:** `BangThongKe(MaBTK, LoaiBang, MaNV, MaSach)`
* **Khách Hàng:** `KhachHang(MaKH, tenKH, tuoiKH, sdtKH, emailKH)`
* **Nhà Xuất Bản:** `NhaXuatBan(MaNXB, tenNXB, dcNXB, sdtNXB, emailNXB)`
* **Phòng Ban:** `PhongBan(MaPHG, tenPHG, loaiPHG)`
* **Loại Sách:** `LoaiSach(MaLS, theloai)`
* **Mượn:** `Muon(MaSach, MaKH, songaymuon)`

---

🙏 **Cảm ơn Cô và các bạn đã lắng nghe bài thuyết trình của nhóm!**
