# GIỚI THIỆU VỀ LẬP TRÌNH HƯỚNG ĐỐI TƯỢNG
## GIỚI THIỆU THÀNH VIÊN NHÓM 5:
1.Lục Bình Nguyên  
2.Nguyễn Nam Khánh  
3.Phạm Bách Minh  
4.Nguyễn Huyền Trang  
5.Vũ Đức Bình  
## PHÂN CÔNG NHIỆM VỤ
A. Phương pháp tiếp cận hướng đối tượng:  Nguyễn Huyền Trang  
B. Các khái niệm cơ bản  
     + Đối tượng, lớp đối tượng: Vũ Đức Bình  
     + Trừu tượng hóa đối tượng theo chức năng và theo dữ liệu: Phạm Bách Minh  
     + Khái niệm kế thừa và đóng gói: Nguyễn Nam Khánh  
     + Khái niệm đa hình: Lục Bình Nguyên  
## NỘI DUNG
## A. PHƯƠNG PHÁP TIẾP CẬN HƯỚNG ĐỐI TƯỢNG
## PHẦN 1: CÁC PHƯƠNG PHÁP TIẾP CẬN LẬP TRÌNH TRUYỀN THỐNG  
  
### 1.1. Lập trình tuyến tính (Linear Programming Approach)  
- **Khái niệm:** Lập trình tuyến tính là phương pháp lập trình sơ khai nhất, trong đó toàn bộ chương trình được viết thành một chuỗi các câu lệnh nối tiếp nhau từ đầu đến cuối.  
- **Tư duy thiết kế:** Tư duy theo lối tuần tự. Các lệnh được thực thi lần lượt theo đúng thứ tự xuất hiện.  
- **Đặc trưng:**  
  - **Đơn giản:** Không phân chia thành hàm, thủ tục hay lớp phức tạp.  
  - **Đơn luồng (Single-thread):** Xử lý luồng công việc thẳng.  
- **Tính chất:**  
  - **Ưu điểm:** Chương trình đơn giản, dễ hiểu, viết nhanh cho các bài toán quy mô rất nhỏ.  
  - **Nhược điểm:** Không thể dùng để giải quyết các ứng dụng phức tạp. Mã nguồn dễ bị lặp lại, cực kỳ khó bảo trì và mở rộng.  
  
> 📌 **Ví dụ trực quan - Lập trình tuyến tính:**  
> Giống như danh sách việc cần làm (To-Do List) đơn giản tại quán cà phê:  
> `1. Mở cửa quán` $\rightarrow$ `2. Bật đèn` $\rightarrow$ `3. Pha cà phê` $\rightarrow$ `4. Tính tiền cho khách`.  
> Nếu muốn thay đổi quy trình tính tiền hay thêm món mới, người quản lý phải sửa trực tiếp vào từng dòng lệnh trong danh sách cố định từ trên xuống.  
  
---  
  
### 1.2. Lập trình cấu trúc (Structured Programming Approach)  
- **Khái niệm:** Lập trình cấu trúc ra đời nhằm giải quyết bài toán phình to mã nguồn của lập trình tuyến tính bằng cách chia nhỏ chương trình thành các chương trình con (hàm / thủ tục / module).  
- **Đặc trưng cốt lõi:**  
  $$\text{Chương trình} = \text{Cấu trúc dữ liệu} + \text{Giải thuật}$$  
- **Tính chất:**  
  - Mỗi chương trình con (hàm/thủ tục) có thể được gọi thực hiện nhiều lần từ các vị trí khác nhau.  
  - Cung cấp các cấu trúc lệnh điều khiển chương trình chuẩn hóa: Rẽ nhánh (`if-else`, `switch-case`), Vòng lặp (`for`, `while`).  
  - **Ưu điểm:** Chương trình dễ hiểu, dễ theo dõi, tư duy giải thuật rõ ràng, công việc được module hóa.  
  - **Nhược điểm:** **Không hỗ trợ việc sử dụng lại mã nguồn (Code Reusability)** giữa các dự án khác nhau. Dữ liệu và giải thuật bị tách rời, dữ liệu toàn cục dễ bị thay đổi ngoài ý muốn. Khi cấu trúc dữ liệu thay đổi, tất cả các hàm liên quan đều bị ảnh hưởng.
  > 📌 **Ví dụ trực quan - Lập trình cấu trúc:**  
> Giống như một xưởng sản xuất được chia thành các phòng ban chức năng riêng biệt:  
> `Ham_NhanDonHang()`, `Ham_KiemTraKho()`, `Ham_TinhTien()`.  
> Dữ liệu (thông tin đơn hàng, tồn kho) được truyền tự do qua lại giữa các hàm. Nếu cấu trúc dữ liệu đơn hàng bị thay đổi (ví dụ: thêm thông tin voucher), tất cả các hàm xử lý đơn hàng đều phải viết lại hoặc sửa đổi.  
  
---  
  
## PHẦN 2: PHƯƠNG PHÁP TIẾP CẬN HƯỚNG ĐỐI TƯỢNG (OBJECT-ORIENTED APPROACH)  
  
### 2.1. Phương pháp Lập trình Hướng đối tượng (OOP)  
- **Khái niệm:** Phương pháp lập trình hướng đối tượng (OOP) ra đời nhằm khắc phục hoàn toàn những hạn chế của lập trình cấu trúc, lấy "đối tượng" làm trung tâm của mọi thao tác xử lý.  
- **Các đặc trưng cốt lõi:**  
  - **Đóng gói dữ liệu (Encapsulation):** Gộp dữ liệu (thuộc tính) và các thao tác trên dữ liệu đó (phương thức) vào trong một đơn vị duy nhất (Lớp/Đối tượng). Dữ liệu nội bộ được bảo vệ, tránh sự can thiệp trực tiếp từ bên ngoài.  
  - **Sử dụng lại mã nguồn (Code Reusability):** Thông qua cơ chế Kế thừa (Inheritance) và Đa hình (Polymorphism), cho phép mở rộng hệ thống mà không cần viết lại mã nguồn cũ.  
  - **Trừu tượng hóa (Abstraction):** Tập trung vào các đặc tính cốt lõi của đối tượng, ẩn đi sự phức tạp của cài đặt bên trong.  
  - **Đa hình (Polymorphism):** Cho phép các đối tượng thuộc các lớp khác nhau phản ứng khác nhau trước cùng một thông điệp.  
  
---  
  
### 2.2. Phương pháp Phân tích và Thiết kế Hướng đối tượng (OOAD)  
Quy trình chuẩn hóa gồm 6 bước bài bản để phát triển một hệ thống hướng đối tượng:  
  
1. **Mô tả bài toán (Problem Description):** Viết lại bài toán phát biểu bằng ngôn ngữ tự nhiên, làm rõ bối cảnh, phạm vi và mục tiêu của hệ thống cần phát triển.  
2. **Đặc tả yêu cầu (Requirements Specification):** Thu thập và phân loại yêu cầu chức năng (hệ thống phải làm gì) và phi chức năng (hiệu năng, bảo mật). Xây dựng danh sách Use Case.  
3. **Trích chọn đối tượng (Object Identification):** Phân tích các từ ngữ (đặc biệt là danh từ) trong bản đặc tả để tìm ra các thực thể/đối tượng tồn tại trong miền bài toán (Domain Entities).
4. **Mô hình hóa lớp đối tượng (Class Modeling):** Xác định thuộc tính, phương thức cho từng lớp và thiết lập mối quan hệ giữa các lớp (Kế thừa, Nối kết, Thành phần). Xây dựng sơ đồ lớp (Class Diagram).  
5. **Thiết kế tổng quan (High-Level / Architectural Design):** Xác định kiến trúc tổng thể phần mềm (3 lớp, MVC, Microservices), phân chia hệ thống thành các phân hệ (subsystems/packages).  
6. **Thiết kế chi tiết (Detailed Design):** Thiết kế chi tiết nội bộ từng lớp, thuật toán cụ thể cho từng phương thức, thiết kế cơ sở dữ liệu và sơ đồ tương tác tuần tự (Sequence Diagram).  
  
---  
  
## PHẦN 3: BẢNG SO SÁNH TỔNG HỢP CÁC PHƯƠNG PHÁP TIẾP CẬN  
  
| Tiêu chí so sánh | Lập trình Tuyến tính | Lập trình Cấu trúc | Lập trình Hướng đối tượng (OOP) |  
| :--- | :--- | :--- | :--- |  
| **Tư duy tiếp cận** | Tuần tự từ trên xuống dưới | Chia nhỏ thành các hàm/thủ tục | Trích chọn và tương tác giữa các Đối tượng |  
| **Công thức cốt lõi** | Chuỗi câu lệnh nối tiếp | Chương trình = Dữ liệu + Giải thuật | Chương trình = Tập hợp các Đối tượng |  
| **Quản lý dữ liệu** | Biến toàn cục / Đơn giản | Dữ liệu tách rời hàm, nguy cơ đổi ngoài ý muốn | Đóng gói dữ liệu an toàn bên trong Đối tượng |  
| **Tái sử dụng mã** | Không hỗ trợ | Hạn chế (gọi lại hàm trong cùng dự án) | Rất cao (Kế thừa, Đa hình, Thư viện Lớp) |  
| **Khả năng mở rộng** | Rất kém | Trung bình (khó sửa khi thay đổi dữ liệu) | Rất cao, linh hoạt, dễ bảo trì |  
| **Ứng dụng phù hợp** | Bài toán siêu nhỏ, kịch bản ngắn | Ứng dụng vừa, tính toán thuật toán | Ứng dụng doanh nghiệp lớn, phần mềm phức tạp |  
  
---  
  
## PHẦN 4: VÍ DỤ TRỰC QUAN TOÀN DIỆN (CASE STUDY MINH HỌA)  
  
**Bài toán:** Thiết kế hệ thống *"Ứng dụng Đặt xe Công nghệ"* (tương tự Grab / Uber) áp dụng 6 bước OOAD:  
  
> 📌 **Áp dụng 6 bước OOAD vào bài toán Đặt xe:**  
> 1. **Mô tả & Đặc tả yêu cầu:** Khách hàng đặt chuyến xe từ điểm A đến B. Hệ thống tự động tìm Tài xế gần nhất, tính cước phí và xử lý thanh toán.  
> 2. **Trích chọn đối tượng:** Các danh từ chính trong bài toán $\rightarrow$ `KhachHang`, `TaiXe`, `ChuyenDi`, `ThanhToan`.  
> 3. **Mô hình hóa lớp đối tượng:**  
>    - Tạo lớp cha `NguoiDung` chứa thông tin chung: `HoTen`, `SoDienThoai`.  
>    - Lớp `KhachHang` kế thừa `NguoiDung`: Thêm phương thức `datChuyen()`, `danhGia()`.
>    - Lớp `TaiXe` kế thừa `NguoiDung`: Thêm thuộc tính `BienSoXe`, `LoaiXe` và phương thức `nhanChuyen()`.  
>    - Lớp `ChuyenDi`: Đóng gói `DiemBatDau`, `DiemDen`, `GiaTien`, `TrangThai`.  
> 4. **Thiết kế & Luồng tương tác:**  
>    `KhachHang.datChuyen()` $\rightarrow$ `ChuyenDi.timTaiXe()` $\rightarrow$ `TaiXe.nhanChuyen()` $\rightarrow$ `ThanhToan.xuly()`.  
  
**Tóm lại:** Phương pháp Hướng đối tượng giúp bài toán phức tạp trở nên trực quan, bảo mật dữ liệu tốt hơn và cực kỳ dễ mở rộng (ví dụ: muốn mở rộng sang dịch vụ *Giao hàng*, chỉ cần tạo lớp `TaiXeGiaoHang` kế thừa từ `TaiXe` mà không ảnh hưởng đến mã nguồn hiện tại).

