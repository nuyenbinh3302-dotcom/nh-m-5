
TRỪU TƯỢNG HÓA ĐỐI TƯỢNG THEO CHỨC NĂNG VÀ THEO DỮ LIỆU
1. Trừu tượng hóa theo chức năng

Trừu tượng hóa theo chức năng là việc tập trung vào những gì một đối tượng có thể thực hiện, đồng thời che giấu cách thức thực hiện bên trong.

Nói đơn giản, người sử dụng chỉ cần biết đối tượng làm được gì, không cần biết nó thực hiện như thế nào.

Ví dụ, một tài khoản ngân hàng có chức năng rutTien(). Người dùng chỉ cần sử dụng chức năng rút tiền mà không cần biết hệ thống thực hiện các bước kiểm tra số dư, kiểm tra số tiền và cập nhật tài khoản như thế nào.

Ví dụ bằng Java:

class TaiKhoan {

    private double soDu;

    public void rutTien(double soTien) {
        if (soTien > 0 && soTien <= soDu) {
            soDu -= soTien;
            System.out.println("Rút tiền thành công");
        }
    }
}


Khi sử dụng:

TaiKhoan taiKhoan = new TaiKhoan();

taiKhoan.rutTien(500000);


Người sử dụng chỉ cần biết và gọi:

taiKhoan.rutTien(500000);


mà không cần quan tâm đến các bước xử lý bên trong phương thức rutTien(). Đây chính là trừu tượng hóa theo chức năng.

2. Trừu tượng hóa theo dữ liệu

Trừu tượng hóa theo dữ liệu là việc tập trung vào những dữ liệu cần thiết của một đối tượng, đồng thời che giấu và kiểm soát cách dữ liệu đó được truy cập hoặc thay đổi.

Trong ví dụ trên, biến:

private double soDu;


là dữ liệu được che giấu bên trong lớp TaiKhoan. Từ khóa private giúp ngăn việc truy cập và thay đổi trực tiếp từ bên ngoài.

Ví dụ, bên ngoài không thể tùy ý thực hiện:

taiKhoan.soDu = -1000000;


Thay vào đó, dữ liệu phải được quản lý thông qua các phương thức được cung cấp bởi lớp như rutTien() hoặc napTien().

Nhờ vậy, chương trình có thể kiểm soát dữ liệu, tránh những giá trị không hợp lệ và đảm bảo tính an toàn của đối tượng.

3. Mối quan hệ giữa hai hình thức trừu tượng hóa

Trừu tượng hóa theo chức năng và trừu tượng hóa theo dữ liệu thường được sử dụng kết hợp với nhau.

Trong đối tượng TaiKhoan:

soDu là dữ liệu của đối tượng và được bảo vệ bằng private.
rutTien() là chức năng mà đối tượng cung cấp cho bên ngoài.
Người sử dụng chỉ cần biết những chức năng cần thiết và không cần quan tâm đến cách dữ liệu được xử lý bên trong.

Có thể hiểu ngắn gọn:

Trừu tượng hóa theo chức năng: Đối tượng làm được gì?

Trừu tượng hóa theo dữ liệu: Đối tượng có dữ liệu gì và dữ liệu được quản lý như thế nào?

4. Kết luận

Trừu tượng hóa giúp che giấu những chi tiết không cần thiết và chỉ cung cấp cho người sử dụng những thông tin, chức năng cần thiết. Điều này giúp chương trình dễ sử dụng, dễ quản lý, an toàn hơn và dễ bảo trì.

Trong lập trình hướng đối tượng, việc kết hợp trừu tượng hóa theo chức năng và theo dữ liệu giúp xây dựng các đối tượng có cấu trúc rõ ràng, hạn chế sự phụ thuộc giữa các thành phần của chương trình.
