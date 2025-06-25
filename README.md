# Expense Tracking App

## Giới thiệu

Expense Tracking App là ứng dụng web giúp người dùng quản lý và theo dõi các khoản chi tiêu cá nhân, được xây dựng bằng ASP.NET Core MVC và sử dụng SQL Server làm cơ sở dữ liệu.

## Cấu trúc dự án

- **Controllers/**: Chứa các controller như `CategoryController`, `DashboardController`, `HomeController`, `TransactionController`.
- **Models/**: Chứa các model dữ liệu, ví dụ: `ApplicationDbContext`.
- **Views/**: Chứa các file giao diện Razor (.cshtml).
- **Migrations/**: Chứa các file migration cho Entity Framework.
- **wwwroot/**: Chứa các tài nguyên tĩnh (CSS, JS, ảnh...).
- **appsettings.json**: File cấu hình ứng dụng.
- **Program.cs**: Điểm khởi động ứng dụng.

## Hướng dẫn cài đặt và chạy ứng dụng

### 1. Yêu cầu hệ thống

- [.NET 6 SDK](https://dotnet.microsoft.com/download/dotnet/6.0)
- [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)

### 2. Cài đặt các thư viện/phụ thuộc

Mở terminal/cmd tại thư mục `Expense Tracker` và chạy lệnh:

```bash
dotnet restore
```
### 3. Cấu hình cơ sở dữ liệu

- Mở file `appsettings.json` hoặc `appsettings.Development.json` trong thư mục `Expense Tracker`.
- Cập nhật chuỗi kết nối tại mục `"ConnectionStrings"` cho phù hợp với SQL Server của bạn (chú ý tên server).
Ví dụ:
```json
"ConnectionStrings": {
  "DefaultConnection": "Server=YOUR_SERVER;Database=ExpenseTrackerDb;Trusted_Connection=True;"
}
```
### 4. Chạy ứng dụng

```bash
dotnet run
```
Nếu sử dụng Visual Studio 2022 thì chỉ cần bấm vào nút replay màu xanh là chạy ứng dụng

### 5. Truy cập ứng dụng

Mở trình duyệt và truy cập địa chỉ: `http://localhost:5110`.


## Hướng dẫn sử dụng ứng dụng
### 1. Quản lý danh mục chi tiêu (Category)

- Sau khi đăng nhập, truy cập mục "Category" để xem, thêm, sửa, xóa các danh mục chi tiêu.

### 2. Theo dõi chi tiêu

- Truy cập mục "Transaction" để xem, thêm, sửa, xóa các giao dịch chi tiêu.
- Sử dụng trang "Bảng điều khiển" để xem thống kê chi tiêu theo thời gian, danh mục.

