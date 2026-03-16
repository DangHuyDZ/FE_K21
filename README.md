# 🍽️ Hệ Thống Đặt Đồ Ăn Trực Tuyến (Food Delivery System)

Dự án **Hệ thống Đặt Đồ Ăn Trực Tuyến** là một nền tảng web toàn diện được xây dựng bằng **Vue 3** và **Vite**. Hệ thống hỗ trợ 4 vai trò người dùng khác nhau: **Admin**, **Khách hàng**, **Quán ăn**, và **Shipper**.

---

## 📋 Mục Lục

- [Giới thiệu](#giới-thiệu)
- [Công nghệ sử dụng](#công-nghệ-sử-dụng)
- [Chức năng nổi bật](#-chức-năng-nổi-bật)
- [Hướng dẫn cài đặt](#-hướng-dẫn-cài-đặt)
- [Chạy ứng dụng](#-chạy-ứng-dụng)
- [Tài khoản test](#-tài-khoản-test)
- [Cấu trúc dự án](#-cấu-trúc-dự-án)
- [Các trang chính](#-các-trang-chính)

---

## 📝 Giới thiệu

Hệ thống được thiết kế với **4 portal riêng biệt** cho từng đối tượng:

- **👥 Khách hàng**: Duyệt danh sách quán ăn, đặt hàng, theo dõi đơn hàng
- **🏪 Quán ăn**: Quản lý sản phẩm, đơn hàng, voucher, doanh thu
- **🚚 Shipper**: Quản lý giao hàng, xem vị trí, thống kê
- **👨‍💼 Admin**: Quản lý toàn bộ hệ thống, người dùng, quyền hạn

---

## 🛠️ Công nghệ sử dụng

| Công nghệ      | Phiên bản | Mô tả                   |
| -------------- | --------- | ----------------------- |
| **Vue**        | 3.3.4     | Frontend framework      |
| **Vite**       | 4.4.5     | Build tool & dev server |
| **Vue Router** | 4.0.13    | Routing & navigation    |
| **Axios**      | 1.7.9     | HTTP client             |
| **Chart.js**   | 4.4.9     | Data visualization      |
| **Leaflet**    | 1.9.4     | Map & location features |
| **Bootstrap**  | 5.x       | CSS framework           |
| **ApexCharts** | Latest    | Advanced charts         |

---

## 🌟 Chức năng nổi bật

### 1. 👥 Dành cho Khách hàng (Client Portal)

Các tính năng chính:

- ✅ Duyệt danh sách quán ăn
- ✅ Tìm kiếm quán ăn & món ăn theo tên
- ✅ Xem chi tiết sản phẩm (giá, mô tả, hình ảnh)
- ✅ Thêm vào giỏ hàng và đặt hàng
- ✅ Theo dõi trạng thái đơn hàng (Đang chờ, Đang nấu, Đang giao, Đã nhận)
- ✅ Lịch sử đơn hàng
- ✅ Quản lý hồ sơ cá nhân
- ✅ Sử dụng mã giảm giá (Voucher)

**URL:** http://localhost:5173/

**Giao diện Khách Hàng:**

![Trang chủ khách hàng](https://github.com/DangHuyDZ/FE_K21/blob/d5770026661901b7c07ec99d53c99133aa29f827/screencapture-localhost-5174-2026-03-16-10_23_04.png)

*Trang chủ - Danh sách quán ăn được gợi ý*

![Chi tiết quán menu](https://github.com/DangHuyDZ/FE_K21/blob/a45892ce5cfe4917828a57fdeded704842e60be1/screencapture-localhost-5174-khach-hang-list-quan-an-2026-03-16-10_27_22.png)

*Chi tiết menu và giỏ hàng*

![Theo dõi đơn hàng](https://github.com/DangHuyDZ/FE_K21/blob/600ba2d70b11002cf55a5dd8b2be602888d86ddb/screencapture-localhost-5173-khach-hang-don-hang-2026-03-16-09_47_19.png)

### 2. 🏪 Dành cho Quán ăn (Restaurant Portal)

Các tính năng chính:

- ✅ Quản lý danh mục sản phẩm
- ✅ Quản lý thực đơn (thêm, sửa, xóa món ăn)
- ✅ Tiếp nhận & xử lý đơn hàng từ khách
- ✅ Quản lý mã giảm giá (Voucher)
- ✅ Thống kê doanh thu theo thời gian
- ✅ Phân tích bán hàng (top sản phẩm)
- ✅ Quản lý thông tin quán ăn

**URL:** http://localhost:5173/quan-an/don-hang

**Giao diện Quán Ăn:**

![Quán Ăn](https://github.com/DangHuyDZ/FE_K21/blob/dec90db38586f3a89a7db98b60c394115e1c7cce/screencapture-localhost-5173-quan-an-mon-an-2026-03-16-09_51_09.png)

### 3. 🚚 Dành cho Shipper (Giao hàng)

Các tính năng chính:

- ✅ Xem danh sách đơn hàng chờ giao
- ✅ Nhận & từ chối đơn hàng
- ✅ Cập nhật vị trí giao hàng (GPS)
- ✅ Xem bản đồ định vị
- ✅ Quản lý ví tiền (hoàn tiền, phí giao hàng)
- ✅ Lịch sử giao hàng
- ✅ Thống kê thu nhập

**URL:** http://localhost:5173/shipper/don-hang

**Giao diện Shipper:**

*Dashboard - Danh sách đơn hàng chờ giao*

![](https://github.com/DangHuyDZ/FE_K21/blob/2375ae7639e62f25cf7b9b4fde231300448a22c3/screencapture-localhost-5173-shipper-don-hang-2026-03-16-10_02_48.png)

### 4. 👨‍💼 Dành cho Admin (Quản trị viên)

Các tính năng chính:

- ✅ Quản lý khách hàng (xem, sửa, xóa)
- ✅ Quản lý quán ăn
- ✅ Quản lý shipper
- ✅ Quản lý danh mục sản phẩm
- ✅ Quản lý đơn hàng
- ✅ Quản lý voucher hệ thống
- ✅ Quản lý nhân viên & phân quyền
- ✅ Thống kê tổng quát (khách hàng, quán ăn)

**URL:** http://localhost:5173/admin/khach-hang

**Giao diện Admin:**

*Giao diện đăng nhập Admin*

![](https://github.com/DangHuyDZ/FE_K21/blob/684d2667c60486780a9b93ff7daf104d27c2f62d/screencapture-localhost-5173-admin-dang-nhap-2026-03-16-10_03_28.png)

*Dashboard Admin - Quản lý khách hàng*

![Quản lý khách hàng](https://github.com/DangHuyDZ/FE_K21/blob/adf93b7adb6dcc84bc868ead42ac8fbb941384b1/screencapture-localhost-5173-admin-khach-hang-2026-03-16-10_04_05.png)

*Quản lý quán ăn - Tìm kiếm, lọc, thêm/sửa/xóa*

![Đăng nhập Admin](https://github.com/DangHuyDZ/FE_K21/blob/1db5ab06094cbb0f2329a2c8c1432e8e193c9b20/screencapture-localhost-5173-admin-quan-an-2026-03-16-10_03_50.png)

---

## 📦 Hướng dẫn cài đặt

### Yêu cầu hệ thống

- **Node.js**: v14.0 hoặc cao hơn
- **npm**: v6.0 hoặc cao hơn (hoặc yarn)
- **Trình duyệt**: Chrome, Firefox, Safari, Edge (phiên bản gần đây)

### Các bước cài đặt

**Bước 1:** Clone dự án từ GitHub

```bash
git clone https://github.com/DangHuyDZ/FE_K21.git
cd FE_KHOA_21
```

**Bước 2:** Cài đặt dependencies

```bash
npm install
```

**Bước 3:** Tạo file `.env` (nếu cần)

```bash
VITE_API_URL=http://localhost:3000/api
```

---

## 🚀 Chạy ứng dụng

### Chế độ phát triển (Development)

```bash
npm run dev
```

Server sẽ chạy tại: **http://localhost:5173/**

### Build cho sản xuất (Production)

```bash
npm run build
```

### Xem preview build

```bash
npm run preview
```

---

## 🔐 Tài khoản test

### 1. 👤 Tài khoản Khách hàng (Customer)

| Trường            | Giá trị                 |
| ----------------- | ----------------------- |
| **Email**         | voviet@gmail.com        |
| **Mật khẩu**      | 123456                  |
| **URL Đăng nhập** | `/khach-hang/dang-nhap` |

**Test link:** [http://localhost:5173/khach-hang/dang-nhap](http://localhost:5173/khach-hang/dang-nhap)

**Hành động test:**

- Đăng nhập bằng tài khoản trên
- Duyệt danh sách quán ăn
- Chọn quán ăn, xem menu
- Thêm sản phẩm vào giỏ
- Đặt hàng
- Xem lịch sử đơn hàng

---

### 2. 🏪 Tài khoản Quán ăn (Restaurant)

| Trường            | Giá trị              |
| ----------------- | -------------------- |
| **Email**         | bunmamvan@gmail.com  |
| **Mật khẩu**      | 123456               |
| **URL Đăng nhập** | `/quan-an/dang-nhap` |

**Test link:** [http://localhost:5173/quan-an/dang-nhap](http://localhost:5173/quan-an/dang-nhap)

**Hành động test:**

- Đăng nhập bằng tài khoản quán ăn
- Xem danh sách đơn hàng mới
- Chấp nhận/từ chối đơn hàng
- Quản lý menu (thêm/sửa/xóa món)
- Tạo voucher giảm giá
- Xem thống kê doanh thu

---

### 3. 🚚 Tài khoản Shipper (Giao hàng)

| Trường            | Giá trị              |
| ----------------- | -------------------- |
| **Email**         | shippera@gmail.com   |
| **Mật khẩu**      | 123456               |
| **URL Đăng nhập** | `/shipper/dang-nhap` |

**Test link:** [http://localhost:5173/shipper/dang-nhap](http://localhost:5173/shipper/dang-nhap)

**Hành động test:**

- Đăng nhập bằng tài khoản shipper
- Xem danh sách đơn hàng chờ giao
- Nhận đơn hàng
- Cập nhật vị trí giao hàng
- Xem bản đồ định vị
- Xem ví tiền & thống kê

---

### 4. 👨‍💼 Tài khoản Admin (Quản trị viên)

| Trường            | Giá trị            |
| ----------------- | ------------------ |
| **Email**         | admin@master.com   |
| **Mật khẩu**      | 123456             |
| **URL Đăng nhập** | `/admin/dang-nhap` |

**Test link:** [http://localhost:5173/admin/dang-nhap](http://localhost:5173/admin/dang-nhap)

**Hành động test:**

- Đăng nhập bằng tài khoản admin
- Quản lý danh sách khách hàng
- Quản lý danh sách quán ăn
- Quản lý danh sách shipper
- Quản lý voucher toàn hệ thống
- Phân quyền người dùng
- Xem thống kê & báo cáo

---

## 📂 Cấu trúc dự án

```
FE_KHOA_21/
├── src/
│   ├── components/
│   │   ├── Admin/              # Portal quản trị viên
│   │   │   ├── DangNhap/       # Đăng nhập
│   │   │   ├── KhachHang/      # Quản lý khách hàng
│   │   │   ├── DanhMuc/        # Quản lý danh mục
│   │   │   ├── DanhSachDonDat/ # Quản lý đơn hàng
│   │   │   ├── QuanAn/         # Quản lý quán ăn
│   │   │   ├── Shipper/        # Quản lý shipper
│   │   │   ├── Voucher/        # Quản lý voucher
│   │   │   ├── PhanQuyen/      # Phân quyền
│   │   │   ├── NhanVien/       # Quản lý nhân viên
│   │   │   ├── ThongKe/        # Thống kê
│   │   │   └── Profile/        # Thông tin cá nhân
│   │   │
│   │   ├── KhachHang/          # Portal khách hàng
│   │   │   ├── DangNhap/       # Đăng nhập khách
│   │   │   ├── DangKi/         # Đăng ký tài khoản
│   │   │   ├── TrangChu/       # Trang chủ - danh sách quán
│   │   │   ├── QuanAn/         # Danh sách quán yêu thích
│   │   │   ├── MonAn/          # Danh sách món theo danh mục
│   │   │   ├── DonDatHang/     # Đặt hàng - chi tiết menu
│   │   │   ├── DonHang/        # Lịch sử & theo dõi đơn
│   │   │   ├── Profile/        # Thông tin cá nhân
│   │   │   ├── TimKiem/        # Tìm kiếm quán/món
│   │   │   └── Test/           # Component test
│   │   │
│   │   ├── QuanAn/             # Portal quán ăn
│   │   │   ├── DangNhap/       # Đăng nhập quán
│   │   │   ├── DangKy/         # Đăng ký quán ăn
│   │   │   ├── DanhMuc/        # Quản lý danh mục
│   │   │   ├── MonAn/          # Quản lý thực đơn
│   │   │   ├── DongHang/       # Quản lý đơn hàng
│   │   │   ├── Voucher/        # Quản lý voucher
│   │   │   ├── ThongKe/        # Thống kê & báo cáo
│   │   │   ├── Config/         # Cấu hình quán ăn
│   │   │   ├── Profile/        # Thông tin quán ăn
│   │   │   └── Test/           # Component test
│   │   │
│   │   └── Shipper/            # Portal shipper
│   │       ├── DangNhap/       # Đăng nhập shipper
│   │       ├── DangKy/         # Đăng ký shipper
│   │       ├── DonHang/        # Quản lý giao hàng
│   │       ├── ViTriHienTai/   # Cập nhật vị trí GPS
│   │       ├── ViTien/         # Quản lý ví tiền
│   │       ├── Profile/        # Thông tin cá nhân
│   │       ├── ThongKe/        # Thống kê thu nhập
│   │       └── Test/           # Component test
│   │
│   ├── layout/
│   │   ├── components/         # Các thành phần layout (header, sidebar)
│   │   │   ├── Admin/
│   │   │   ├── Client/
│   │   │   ├── QuanAn/
│   │   │   └── Shipper/
│   │   └── wrapper/            # Layout wrapper cho từng portal
│   │       ├── Admin/
│   │       ├── Client/
│   │       ├── QuanAn/
│   │       ├── Shipper/
│   │       └── Blank/
│   │
│   ├── router/
│   │   ├── index.js            # Định nghĩa tất cả routes
│   │   ├── checkNhanVienLogin.js   # Middleware check admin
│   │   ├── checkKhachHang.js       # Middleware check khách
│   │   ├── checkQuanAn.js          # Middleware check quán
│   │   └── checkShipper.js         # Middleware check shipper
│   │
│   ├── assets/
│   │   ├── css/
│   │   │   ├── app.css
│   │   │   ├── bootstrap.css
│   │   │   ├── dark-theme.css
│   │   │   ├── header-colors.css
│   │   │   └── icons.css
│   │   ├── images/
│   │   │   ├── avatars/
│   │   │   ├── products/
│   │   │   ├── gallery/
│   │   │   └── icons/
│   │   ├── fonts/
│   │   ├── flags/
│   │   ├── js/
│   │   │   ├── app.js
│   │   │   ├── index.js
│   │   │   └── widgets.js
│   │   └── plugins/
│   │       ├── apexcharts-bundle/
│   │       ├── chartjs/
│   │       ├── datatable/
│   │       ├── fullcalendar/
│   │       ├── gmaps/
│   │       ├── select2/
│   │       └── vectormap/
│   │
│   ├── App.vue                 # Root component
│   ├── main.js                 # Entry point
│   └── style.css               # Global styles
│
├── public/                     # Tài nguyên tĩnh
├── index.html                  # HTML template
├── package.json                # Dependencies & scripts
├── vite.config.js              # Vite configuration
└── README.md                   # Tài liệu này
```

---

## 📱 Các trang chính

### 👥 Khách hàng (Customer)

| Trang                    | URL                            | Mô tả                    |
| ------------------------ | ------------------------------ | ------------------------ |
| Trang chủ                | `/`                            | Danh sách quán ăn        |
| Đăng nhập                | `/khach-hang/dang-nhap`        | Đăng nhập tài khoản      |
| Đăng ký                  | `/khach-hang/dang-ky`          | Tạo tài khoản mới        |
| Chi tiết quán & menu     | `/khach-hang/quan-an/:id_quan` | Xem menu & đặt hàng      |
| Đơn hàng                 | `/khach-hang/don-hang`         | Lịch sử & theo dõi đơn   |
| Tìm kiếm                 | `/tim-kiem/:thong_tin`         | Tìm kiếm quán/món        |
| Danh sách quán yêu thích | `/khach-hang/list-quan-an`     | Danh sách quán đã follow |
| Hồ sơ                    | `/khach-hang/profile`          | Thông tin cá nhân        |

### 🏪 Quán ăn (Restaurant)

| Trang              | URL                           | Mô tả             |
| ------------------ | ----------------------------- | ----------------- |
| Đăng nhập          | `/quan-an/dang-nhap`          | Đăng nhập quán ăn |
| Đăng ký            | `/quan-an/dang-ky`            | Đăng ký quán mới  |
| Dashboard          | `/quan-an/don-hang`           | Đơn hàng mới      |
| Danh mục           | `/quan-an/danh-muc`           | Quản lý danh mục  |
| Sản phẩm           | `/quan-an/mon-an`             | Quản lý thực đơn  |
| Voucher            | `/quan-an/voucher`            | Quản lý giảm giá  |
| Thống kê sản phẩm  | `/quan-an/thong-ke-mon-an`    | Báo cáo bán hàng  |
| Thống kê doanh thu | `/quan-an/thong-ke-doanh-thu` | Báo cáo tài chính |
| Cấu hình           | `/quan-an/cau-hinh`           | Cài đặt quán ăn   |
| Hồ sơ              | `/quan-an/profile`            | Thông tin quán ăn |

### 🚚 Shipper (Giao hàng)

| Trang           | URL                        | Mô tả                     |
| --------------- | -------------------------- | ------------------------- |
| Đăng nhập       | `/shipper/dang-nhap`       | Đăng nhập shipper         |
| Đăng ký         | `/shipper/dang-ky`         | Đăng ký tài khoản shipper |
| Đơn hàng        | `/shipper/don-hang`        | Danh sách giao hàng       |
| Vị trí hiện tại | `/shipper/vi-tri-hien-tai` | Cập nhật GPS              |
| Ví tiền         | `/shipper/vi-tien`         | Quản lý ví tiền           |
| Thống kê        | `/shipper/thong-ke`        | Báo cáo thu nhập          |
| Hồ sơ           | `/shipper/profile`         | Thông tin cá nhân         |

### 👨‍💼 Admin (Quản trị)

| Trang          | URL                          | Mô tả                    |
| -------------- | ---------------------------- | ------------------------ |
| Đăng nhập      | `/admin/dang-nhap`           | Đăng nhập admin          |
| Khách hàng     | `/admin/khach-hang`          | Quản lý tài khoản khách  |
| Quán ăn        | `/admin/quan-an`             | Quản lý quán ăn          |
| Danh mục       | `/admin/danh-muc`            | Quản lý danh mục         |
| Đơn hàng       | `/admin/danh-sach-don-dat`   | Quản lý tất cả đơn       |
| Shipper        | `/admin/shipper`             | Quản lý shipper          |
| Voucher        | `/admin/voucher`             | Quản lý voucher hệ thống |
| Nhân viên      | `/admin/nhan-vien`           | Quản lý staff            |
| Phân quyền     | `/admin/phan-quyen`          | Cài đặt quyền hạn        |
| Thống kê khách | `/admin/thong-ke-khach-hang` | Báo cáo khách hàng       |
| Thống kê quán  | `/admin/thong-ke-quan-an`    | Báo cáo quán ăn          |
| Hồ sơ          | `/admin/profile`             | Thông tin admin          |

---

## 🔗 Link nhanh

### Khởi động nhanh

```bash
# Cài đặt & chạy
npm install && npm run dev

# Truy cập ứng dụng
http://localhost:5173/
```

### Login nhanh

**Khách hàng:**

- 📧 Email: `voviet@gmail.com`
- 🔑 Pass: `123456`
- Link: http://localhost:5173/khach-hang/dang-nhap

**Quán ăn:**

- 📧 Email: `bunmamvan@gmail.com`
- 🔑 Pass: `123456`
- Link: http://localhost:5173/quan-an/dang-nhap

**Shipper:**

- 📧 Email: `shippera@gmail.com`
- 🔑 Pass: `123456`
- Link: http://localhost:5173/shipper/dang-nhap

**Admin:**

- 📧 Email: `admin@master.com`
- 🔑 Pass: `123456`
- Link: http://localhost:5173/admin/dang-nhap

---

## 📸 Tính năng chính

### Khách Hàng

- **Trang chủ**: Xem danh sách quán ăn được gợi ý
- **Tìm kiếm**: Tìm quán ăn hoặc món ăn theo tên
- **Chi tiết quán**: Xem menu, giá cả, đánh giá
- **Giỏ hàng**: Thêm sản phẩm, quản lý số lượng
- **Thanh toán**: Chọn phương thức, nhập địa chỉ
- **Theo dõi**: Xem trạng thái đơn hàng realtime
- **Lịch sử**: Xem tất cả đơn đã đặt trước đó
- **Hồ sơ**: Cập nhật thông tin cá nhân, địa chỉ

### Quán Ăn

- **Dashboard**: Xem tổng quan đơn hàng, doanh thu
- **Đơn hàng**: Tiếp nhận, chấp nhận, chuẩn bị
- **Thực đơn**: Thêm, sửa, xóa món ăn
- **Danh mục**: Tổ chức sản phẩm theo loại
- **Voucher**: Tạo mã giảm giá cho khách
- **Thống kê**: Báo cáo doanh số, phân tích
- **Cài đặt**: Cập nhật thông tin, giờ mở cửa

### Shipper

- **Danh sách giao**: Xem đơn hàng chờ nhận
- **Nhận đơn**: Chấp nhận để bắt đầu giao
- **GPS tracking**: Cập nhật vị trí realtime
- **Bản đồ**: Xem vị trí khách, quán, vị trí hiện tại
- **Ví tiền**: Xem tiền kiếm, hoàn lại
- **Lịch sử**: Xem tất cả đơn đã giao
- **Thống kê**: Báo cáo thu nhập hàng ngày/tuần/tháng

### Admin

- **Quản lý user**: Thêm, sửa, xóa khách/quán/shipper
- **Danh mục**: Quản lý danh mục chung của hệ thống
- **Voucher**: Tạo voucher hệ thống
- **Phân quyền**: Gán role/permission cho nhân viên
- **Thống kê**: Báo cáo tổng hợp, biểu đồ phân tích

---

## 💡 Ghi chú quan trọng

- ⚠️ **Backend API**: Ứng dụng này là Frontend. Đảm bảo Backend API đang chạy
- ⚠️ **CORS**: Nếu gặp lỗi CORS, kiểm tra cấu hình backend
- 💾 **Local Storage**: Token đăng nhập được lưu trong localStorage
- 📱 **Responsive**: Hỗ trợ desktop, tablet, mobile
- 🌙 **Dark Mode**: Một số trang hỗ trợ giao diện tối
- 🔐 **Authentication**: Sử dụng JWT token cho bảo mật

---

## 📚 Thư viện & plugins sử dụng

- **ApexCharts** - Biểu đồ cao cấp (doanh thu, thống kê)
- **Chart.js** - Biểu đồ cơ bản (pie, bar, line)
- **Leaflet** - Bản đồ & định vị GPS
- **DataTables** - Bảng dữ liệu có sắp xếp, tìm kiếm
- **Fullcalendar** - Lịch theo dõi sự kiện
- **Select2** - Dropdown nâng cao
- **Vue Toaster** - Thông báo popup

---

## 🐛 Troubleshooting

### Lỗi: "Module not found"

```bash
# Xóa node_modules và cài lại
rm -rf node_modules
npm install
```

### Lỗi: Port 5173 đang sử dụng

```bash
# Sử dụng port khác
npm run dev -- --port 3001
```

### Lỗi CORS khi gọi API

- Kiểm tra backend có mở CORS access
- Kiểm tra URL API trong `.env`

### Vui lòng xóa cache & bộ nhớ tạm

```bash
# Chrome: Ctrl + Shift + Delete
# Firefox: Ctrl + Shift + Delete
# Safari: Shift + Cmd + Delete
```

---

## 📸 Hướng dẫn thêm hình ảnh thực tế

README hiện tại sử dụng **placeholder images** từ dịch vụ `placeholder.com`. Để thêm hình ảnh thực tế:

### Cách 1: Sử dụng hình ảnh từ folder `public/` hoặc `src/assets/`

1. Lưu hình ảnh vào: `public/images/` hoặc `src/assets/images/`
2. Thay đổi link trong README:

```markdown
![Mô tả](https://via.placeholder.com/800x400.png?text=Text) # Cũ
![Mô tả](/images/customer-homepage.png) # Mới
```

### Cách 2: Sử dụng link trực tuyến

1. Upload ảnh lên Imgur, GitHub, hoặc GitHub issues
2. Copy URL ảnh
3. Update link trong README

### Cách 3: Thêm screenshots folder

1. Tạo folder `screenshots/` ở thư mục gốc
2. Lưu các ảnh chụp màn hình
3. Update link: `./screenshots/customer-homepage.png`

### Danh sách ảnh cần chụp:

**Khách hàng:**

- `screenshots/01-customer-homepage.png` - Trang chủ
- `screenshots/02-customer-menu.png` - Chi tiết menu
- `screenshots/03-customer-tracking.png` - Theo dõi đơn

**Quán ăn:**

- `screenshots/04-restaurant-dashboard.png` - Dashboard
- `screenshots/05-restaurant-menu-manager.png` - Quản lý menu
- `screenshots/06-restaurant-stats.png` - Thống kê

**Shipper:**

- `screenshots/07-shipper-dashboard.png` - Dashboard
- `screenshots/08-shipper-map.png` - Bản đồ GPS
- `screenshots/09-shipper-wallet.png` - Ví tiền

**Admin:**

- `screenshots/10-admin-dashboard.png` - Dashboard
- `screenshots/11-admin-users.png` - Quản lý người dùng
- `screenshots/12-admin-stats.png` - Thống kê

---

- **Tác giả**: Khóa 21
- **GitHub**: https://github.com/DangHuyDZ/FE_K21
- **Email**: support@fooddelivery.com
- **Issues**: [GitHub Issues](https://github.com/DangHuyDZ/FE_K21/issues)

---

## 📄 Giấy phép

Project này được cấp phép dưới **MIT License** - xem file LICENSE để chi tiết

---

## ✨ Cải tiến trong tương lai

- [ ] Thêm chat realtime (Socket.io)
- [ ] Thêm đánh giá & review
- [ ] Thêm thanh toán online (Stripe, Momo)
- [ ] Mobile app (React Native)
- [ ] Thêm đa ngôn ngữ (i18n)
- [ ] Thêm AI recommendations
- [ ] Tối ưu hóa performance
- [ ] Unit tests coverage

---

**Cập nhật lần cuối**: 16/03/2026 | **Version**: 1.0.0
