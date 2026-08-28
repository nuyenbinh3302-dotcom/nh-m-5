# nh-m-5
5. Khái niệm kế thừa (Inheritance)

Kế thừa là một đặc điểm quan trọng của lập trình hướng đối tượng, cho phép một lớp mới (lớp con) kế thừa các thuộc tính và phương thức của một lớp đã có (lớp cha).

Lớp con có thể:

Sử dụng lại các thuộc tính và phương thức của lớp cha.
Bổ sung thêm thuộc tính và phương thức mới.
Thay đổi/ghi đè (override) cách thực hiện một phương thức của lớp cha nếu cần.
Ví dụ:
class DongVat {
    String ten;

    void an() {
        System.out.println("Động vật đang ăn");
    }
}

class Cho extends DongVat {
    void sua() {
        System.out.println("Gâu gâu");
    }
}


Trong ví dụ trên:

DongVat là lớp cha.
Cho là lớp con.
Cho kế thừa ten và phương thức an() từ DongVat.
Cho có thêm phương thức riêng là sua().

Có thể sử dụng:

Cho c = new Cho();

c.ten = "Milu";
c.an();
c.sua();

Đặc điểm của kế thừa

1. Tái sử dụng mã nguồn:
Không cần viết lại những thuộc tính và phương thức đã có ở lớp cha.

2. Mở rộng lớp:
Lớp con có thể bổ sung thêm những đặc điểm riêng.

3. Ghi đè phương thức:
Lớp con có thể định nghĩa lại phương thức của lớp cha để phù hợp với đối tượng của mình.

4. Tạo quan hệ giữa các lớp:
Kế thừa thường thể hiện quan hệ “là một” (is-a).
Ví dụ: Cho là một DongVat.

=> Kế thừa giúp tái sử dụng, mở rộng và chuyên biệt hóa các lớp trong chương trình.

6. Khái niệm đóng gói (Encapsulation)

Đóng gói là cơ chế gom các dữ liệu (thuộc tính) và các phương thức xử lý dữ liệu đó vào trong cùng một đối tượng/lớp, đồng thời che giấu và kiểm soát quyền truy cập vào dữ liệu bên trong.

Nói đơn giản, bên ngoài không được tùy ý truy cập và thay đổi dữ liệu nội bộ, mà phải thông qua những phương thức được lớp cung cấp.

Ví dụ:
class TaiKhoan {
    private double soDu;

    public double getSoDu() {
        return soDu;
    }

    public void napTien(double tien) {
        if (tien > 0) {
            soDu += tien;
        }
    }
}


Ở đây:

soDu là dữ liệu của tài khoản.
soDu được khai báo private nên không thể truy cập trực tiếp từ bên ngoài lớp.
getSoDu() cho phép lấy số dư.
napTien() cho phép nạp tiền và đồng thời kiểm tra điều kiện trước khi thay đổi số dư.

Ví dụ:

TaiKhoan tk = new TaiKhoan();

tk.napTien(100000);
System.out.println(tk.getSoDu());


Không thể làm trực tiếp:

tk.soDu = -500000; // Lỗi vì soDu là private

Các mức độ truy cập thường dùng

Trong Java, đóng gói thường được thực hiện bằng các access modifier:

private: chỉ được truy cập bên trong chính lớp đó.
default: truy cập trong cùng package.
protected: truy cập trong cùng package và các lớp con.
public: có thể truy cập từ bên ngoài.

Trong đó, private thường được sử dụng để che giấu dữ liệu.

Lợi ích của đóng gói

1. Bảo vệ dữ liệu:
Ngăn việc thay đổi dữ liệu một cách tùy ý.

2. Kiểm soát việc truy cập:
Có thể quy định dữ liệu được đọc hoặc thay đổi như thế nào.

3. Tăng tính an toàn:
Ví dụ không cho phép số dư tài khoản trở thành giá trị không hợp lệ.

4. Dễ bảo trì chương trình:
Có thể thay đổi cách xử lý bên trong lớp mà không ảnh hưởng nhiều đến phần chương trình bên ngoài.

5. Giảm sự phụ thuộc:
Các phần bên ngoài chỉ cần sử dụng những phương thức mà lớp cung cấp, không cần biết chi tiết cài đặt bên trong.

=> Đóng gói là che giấu dữ liệu bên trong đối tượng và chỉ cho phép truy cập thông qua các phương thức được kiểm soát, giúp chương trình an toàn, dễ quản lý và dễ bảo trì.
