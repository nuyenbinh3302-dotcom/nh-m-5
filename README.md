# GIỚI THIỆU VỀ LẬP TRÌNH HƯỚNG ĐỐI TƯỢNG
## GIỚI THIỆU THÀNH VIÊN NHÓM 5:
1.Lục Bình Nguyên
2.Nguyễn Nam Khánh
3.Phạm Bách Minh
4.Nguyễn Huyền Trang
5.Vũ Đức Bình
## PHÂN CÔNG NHIỆM VỤ
1. Phương pháp tiếp cận hướng đối tượng:  Nguyễn Huyền Trang
2. Các khái niệm cơ bản:
     + Đối tượng, lớp đối tượng: Vũ Đức Bình
     + Trừu tượng hóa đối tượng theo chức năng và theo dữ liệu: Phạm Bách Minh
     + Khái niệm kế thừa và đóng gói: Nguyễn Nam Khánh
     + Khái niệm đa hình: Lục Bình Nguyên
## NỘI DUNG
PHẦN 1: CÁC PHƯƠNG PHÁP TIẾP CẬN LẬP TRÌNH TRUYỀN THỐNG
1.1. Lập trình tuyến tính (Linear Programming Approach)
Khái niệm: Lập trình tuyến tính là phương pháp lập trình sơ khai nhất, nơi toàn bộ chương trình được viết thành một chuỗi các câu lệnh nối tiếp nhau từ đầu đến cuối.
•	Tư duy thiết kế: Tư duy theo lối tuần tự: Các dòng lệnh được thực thi lần lượt từ trên xuống dưới theo đúng thứ tự xuất hiện.
•	Đặc trưng 1: Đơn giản: Không có sự phân chia hàm, cấu trúc hay lớp phức tạp.
•	Đặc trưng 2: Đơn luồng (Single-thread): Xử lý một luồng thực thi duy nhất.
Tính chất của Lập trình tuyến tính:
•	Ưu điểm: Chương trình đơn giản, dễ viết, dễ hiểu đối với người mới bắt đầu hoặc các bài toán siêu nhỏ.
•	Nhược điểm: Không thể dùng để giải quyết các ứng dụng phức tạp. Mã nguồn dễ bị lặp lại, cực kỳ khó bảo trì và mở rộng.
📌 Ví dụ trực quan - Lập trình tuyến tính
Ví dụ thực tế: Giống như danh sách việc cần làm (To-Do List) của một quán cà phê đơn giản:
1. Mở cửa quán -> 2. Bật đèn -> 3. Pha cà phê -> 4. Tính tiền cho khách hàng.
Nếu muốn thay đổi cách tính tiền hay thêm món mới, người quản lý phải viết lại hoặc sửa trực tiếp vào dòng lệnh cụ thể trong danh sách từ trên xuống.

1.2. Lập trình cấu trúc (Structured Programming Approach)
Khái niệm: Lập trình cấu trúc ra đời để giải quyết bài toán phình to mã nguồn của lập trình tuyến tính bằng cách chia nhỏ chương trình thành các chương trình con (hàm / thủ tục / module).
•	Đặc trưng cốt lõi: Chương trình = Cấu trúc dữ liệu + Giải thuật
•	Tính chất 1: Mỗi chương trình con (hàm/thủ tục) có thể được gọi thực hiện nhiều lần từ các vị trí khác nhau trong chương trình.
•	Tính chất 2: Cung cấp các cấu trúc điều khiển chuẩn hóa: Rẽ nhánh (if-else, switch-case), Vòng lặp (for, while, do-while).
Tính chất của Lập trình cấu trúc:
•	Ưu điểm: Chương trình dễ hiểu, dễ theo dõi, tư duy giải thuật rõ ràng, module hóa công việc.
•	Nhược điểm: Không hỗ trợ việc sử dụng lại mã nguồn (Code Reusability) giữa các dự án khác nhau. Dữ liệu và giải thuật bị tách rời, dữ liệu toàn cục dễ bị thay đổi ngoài ý muốn.
📌 Ví dụ trực quan - Lập trình cấu trúc
Ví dụ thực tế: Giống như một xưởng sản xuất được chia thành các phòng ban riêng biệt:
• Hàm NhanDonHang(), Hàm KiemTraKho(), Hàm TinhTien().
Dữ liệu (thông tin đơn hàng, số lượng tồn kho) được truyền tự do qua lại giữa các hàm. Nếu cấu trúc dữ liệu đơn hàng thay đổi (ví dụ: thêm mã giảm giá), tất cả các hàm liên quan đều phải điều chỉnh lại mã nguồn.

PHẦN 2: PHƯƠNG PHÁP TIẾP CẬN HƯỚNG ĐỐI TƯỢNG (OBJECT-ORIENTED APPROACH)
2.1. Phương pháp Lập trình Hướng đối tượng (OOP)
Khái niệm: Phương pháp lập trình hướng đối tượng (OOP) ra đời nhằm khắc phục hoàn toàn những hạn chế của lập trình cấu trúc, lấy 'đối tượng' làm trung tâm của mọi thao tác xử lý.
Các đặc trưng ưu việt của OOP:
•	Đóng gói dữ liệu (Encapsulation): Gộp dữ liệu (thuộc tính) và các thao tác trên dữ liệu đó (phương thức) vào trong một đơn vị duy nhất (Lớp/Đối tượng). Dữ liệu nội bộ được bảo vệ, tránh sự can thiệp trực tiếp từ bên ngoài.
•	Sử dụng lại mã nguồn (Code Reusability): Cho phép lớp con kế thừa lại các thuộc tính và phương thức của lớp cha, giúp tái sử dụng mã nguồn tối đa mà không cần viết lại.
•	Trừu tượng hóa (Abstraction): Ẩn đi sự phức tạp bên trong và chỉ cung cấp các giao diện đơn giản cần thiết cho người dùng sử dụng đối tượng.
•	Tính đa hình (Polymorphism): Cho phép các đối tượng thuộc các lớp khác nhau phản ứng khác nhau trước cùng một thông điệp (gọi hàm).
2.2. Phương pháp Phân tích và Thiết kế Hướng đối tượng (OOAD)
Quy trình chuẩn hóa: Để xây dựng một hệ thống hướng đối tượng thành công, người phát triển cần tuân theo quy trình Phân tích và Thiết kế Hướng đối tượng (OOAD) gồm 6 bước bài bản sau:
•	Bước 1: Mô tả bài toán (Problem Description): Viết lại bài toán phát biểu bằng ngôn ngữ tự nhiên, làm rõ bối cảnh, phạm vi và mục tiêu của ứng dụng cần phát triển.
•	Bước 2: Đặc tả yêu cầu (Requirements Specification): Thu thập và làm rõ các yêu cầu chức năng (hệ thống phải làm gì) và phi chức năng (hiệu năng, bảo mật, giao diện). Xây dựng danh sách Use Case.
•	Bước 3: Trích chọn đối tượng (Object Identification): Phân tích các từ ngữ (đặc biệt là danh từ) trong bản đặc tả để tìm ra các thực thể/đối tượng tồn tại trong miền bài toán.
•	Bước 4: Mô hình hóa lớp đối tượng (Class Modeling): Xác định các thuộc tính, phương thức cho từng lớp và thiết lập mối quan hệ giữa các lớp (Kế thừa, Nối kết, Thành phần). Xây dựng sơ đồ lớp (Class Diagram).
•	Bước 5: Thiết kế tổng quan (High-Level / Architectural Design): Xác định kiến trúc phần mềm (3 lớp, MVC, Microservices), phân chia hệ thống thành các phân hệ/package và quy định chuẩn giao tiếp.
•	Bước 6: Thiết kế chi tiết (Detailed Design): Thiết kế chi tiết nội bộ từng lớp, thuật toán cụ thể cho từng phương thức, thiết kế cơ sở dữ liệu và sơ đồ tương tác tuần tự (Sequence Diagram).
PHẦN 3: BẢNG SO SÁNH TỔNG HỢP CÁC PHƯƠNG PHÁP TIẾP CẬN
Tiêu chí so sánh	Lập trình Tuyến tính	Lập trình Cấu trúc	Lập trình Hướng đối tượng (OOP)
Tư duy tiếp cận	Tuần tự từ trên xuống dưới	Chia nhỏ thành các hàm/thủ tục	Trích chọn và tương tác giữa các Đối tượng
Công thức cốt lõi	Chuỗi câu lệnh nối tiếp	Chương trình = Dữ liệu + Giải thuật	Chương trình = Tập hợp các Đối tượng tương tác
Quản lý dữ liệu	Biến toàn cục / Đơn giản	Dữ liệu tách rời hàm, dùng toàn cục/cục bộ	Đóng gói dữ liệu an toàn bên trong Đối tượng
Tái sử dụng mã	Không hỗ trợ	Hạn chế (gọi lại hàm trong cùng dự án)	Rất cao (Kế thừa, Đa hình, Thư viện Lớp)
Khả năng mở rộng	Rất kém	Trung bình (khó sửa khi thay đổi dữ liệu)	Rất cao, linh hoạt, dễ bảo trì
Ứng dụng phù hợp	Bài toán siêu nhỏ, kịch bản ngắn	Ứng dụng vừa, tính toán thuật toán	Ứng dụng doanh nghiệp lớn, phần mềm phức tạp

PHẦN 4: VÍ DỤ TRỰC QUAN TOÀN DIỆN (CASE STUDY MINH HỌA)
Bài toán thực tế: Để thấy rõ sự khác biệt và hiệu quả của Phương pháp Hướng đối tượng, chúng ta hãy cùng phân tích bài toán xây dựng 'Ứng dụng Đặt xe Công nghệ' (tương tự Grab / Gojek):
📌 Minh họa quy trình OOAD 6 bước cho Hệ thống Đặt xe
📌 BƯỚC 1 & 2: MÔ TẢ & ĐẶC TẢ YÊU CẦU
Hệ thống cho phép Khách hàng đặt chuyến xe từ vị trí A đến B. Hệ thống tự động tìm Tài xế gần nhất, tính cước phí chuyến đi và thực hiện thanh toán.

📌 BƯỚC 3: TRÍCH CHỌN ĐỐI TƯỢNG (Dựa trên các danh từ)
• KhachHang, TaiXe, ChuyenDi, ThanhToan, ViTri.

📌 BƯỚC 4: MÔ HÌNH HÓA LỚP ĐỐI TƯỢNG (Áp dụng Đóng gói & Kế thừa)
• Lớp cha `NguoiDung`: Có thuộc tính (HoTen, SoDienThoai).
• Lớp `KhachHang` kế thừa `NguoiDung`: Thêm phương thức `datChuyen()`, `danhGia()`.
• Lớp `TaiXe` kế thừa `NguoiDung`: Thêm thuộc tính (BienSoXe, LoaiXe) và phương thức `nhanChuyen()`.
• Lớp `ChuyenDi`: Đóng gói thông tin (DiemBatDau, DiemDen, GiaTien, TrangThai).

📌 BƯỚC 5 & 6: THIẾT KẾ TỔNG QUAN VÀ CHI TIẾT
• Luồng tương tác: KhachHang.datChuyen() -> ChuyenDi.timTaiXe() -> TaiXe.nhanChuyen() -> ThanhToan.xuly().

Tóm lại: Kết luận: Phương pháp Hướng đối tượng giúp bài toán phức tạp trở nên trực quan, dễ quản lý, bảo mật dữ liệu tốt hơn và cực kỳ dễ mở rộng (ví dụ: muốn thêm loại hình 'Giao hàng' chỉ cần tạo thêm lớp `TaiXeGiaoHang` kế thừa từ `TaiXe` mà không làm hỏng mã nguồn cũ).

