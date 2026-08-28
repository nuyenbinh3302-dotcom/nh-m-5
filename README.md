# nh-m-5
5. Khái niệm kế thừa (Inheritance)
Là cơ chế cho phép lớp con sử dụng lại các thuộc tính và phương thức của lớp cha.

Ví dụ:

class DongVat {
    void an() {
        System.out.println("Đang ăn");
    }
}

class Cho extends DongVat {
    void sua() {
        System.out.println("Gâu gâu");
    }
}

Cho kế thừa DongVat nên có thể sử dụng cả:
Cho cho = new Cho();
cho.an();   // kế thừa từ DongVat
cho.sua();  // riêng của Cho
Mục đích: tái sử dụng code và tạo mối quan hệ “là một” (is-a).

6. Khái niệm đóng gói (Encapsulation)
Là việc gom dữ liệu và các phương thức xử lý dữ liệu vào cùng một lớp, đồng thời hạn chế truy cập trực tiếp vào dữ liệu bên trong.
Ví dụ:

class TaiKhoan {
    private double soDu;

    public double getSoDu() {
        return soDu;
    }

    public void napTien(double tien) {
        if (tien > 0)
            soDu += tien;
    }
}

soDu là private nên bên ngoài không thể tự ý thay đổi:
TaiKhoan tk = new TaiKhoan();
tk.napTien(100000);  // được phép
Lợi ích: bảo vệ dữ liệu, kiểm soát cách dữ liệu được thay đổi và giảm sự phụ thuộc giữa các phần của chương trình.
