Trong ngôn ngữ lập trình C, **struct** (cấu trúc) là một kiểu dữ liệu do người dùng định nghĩa, cho phép nhóm các biến có kiểu dữ liệu khác nhau lại với nhau dưới một tên duy nhất. Dưới đây là tất cả thông tin quan trọng về **struct** trong C:

---

### **1. Khai báo struct**
```c
struct TenStruct {
    kieudulieu1 tenBien1;
    kieudulieu2 tenBien2;
    // ...
};
```
**Ví dụ:**
```c
struct SinhVien {
    char ten[50];
    int tuoi;
    float diem;
};
```

---

### **2. Khởi tạo struct**
- Có thể khởi tạo ngay khi khai báo:
```c
struct SinhVien sv1 = {"Nguyen Van A", 20, 8.5};
```
- Hoặc khởi tạo từng thành phần sau:
```c
struct SinhVien sv2;
strcpy(sv2.ten, "Tran Thi B");
sv2.tuoi = 21;
sv2.diem = 7.5;
```

---

### **3. Truy cập thành phần struct**
Sử dụng toán tử `.` (dot) để truy cập các biến thành viên:
```c
printf("Ten: %s\n", sv1.ten);
printf("Tuoi: %d\n", sv1.tuoi);
```

---

### **4. Con trỏ struct**
- Dùng toán tử `->` để truy cập thành phần qua con trỏ:
```c
struct SinhVien *ptr = &sv1;
printf("Ten: %s\n", ptr->ten); // Tương đương (*ptr).ten
```

---

### **5. Typedef với struct**
Để đơn giản hóa tên struct, dùng `typedef`:
```c
typedef struct SinhVien {
    char ten[50];
    int tuoi;
} SV;

// Khai báo ngắn gọn hơn
SV sv3;
```

---

### **6. Struct lồng nhau**
Một struct có thể chứa struct khác:
```c
struct DiaChi {
    char soNha[20];
    char duong[50];
};

struct NhanVien {
    char ten[50];
    struct DiaChi diaChi;
};
```

---

### **7. Kích thước struct (Size of struct)**
- Kích thước struct không nhất thiết bằng tổng kích thước các thành phần do **padding** (cơ chế alignment để tối ưu hóa truy cập bộ nhớ).
- Dùng `sizeof` để kiểm tra:
```c
printf("Size of SinhVien: %d bytes\n", sizeof(struct SinhVien));
```

---

### **8. Sao chép struct**
Có thể gán trực tiếp 2 struct cùng kiểu:
```c
struct SinhVien sv3 = sv1; // Sao chép toàn bộ dữ liệu từ sv1 sang sv3
```

---

### **9. Mảng struct**
```c
struct SinhVien lopHoc[30];
lopHoc[0].tuoi = 20; // Truy cập phần tử đầu tiên
```

---

### **10. Hàm với struct**
- Truyền struct vào hàm (theo giá trị hoặc tham chiếu):
```c
void inThongTin(struct SinhVien sv) {
    printf("Ten: %s\n", sv.ten);
}

// Truyền tham chiếu
void thayDoiTuoi(struct SinhVien *sv, int tuoiMoi) {
    sv->tuoi = tuoiMoi;
}
```

---

### **11. So sánh struct**
- **Không thể** dùng toán tử `==` để so sánh 2 struct. Phải so sánh từng thành phần:
```c
if (strcmp(sv1.ten, sv2.ten) == 0 && sv1.tuoi == sv2.tuoi) {
    printf("Hai sinh vien giong nhau.\n");
}
```

---

### **12. Bit Fields trong struct**
Dùng để tiết kiệm bộ nhớ khi cần lưu các biến nhỏ:
```c
struct {
    unsigned int isActive : 1; // 1 bit
    unsigned int age : 7;      // 7 bit
} status;
```

---

### **Ưu điểm của struct**
- Nhóm dữ liệu liên quan lại với nhau.
- Truyền nhiều tham số vào hàm một cách gọn gàng.
- Cơ sở để xây dựng các kiểu dữ liệu phức tạp (như danh sách liên kết, cây...).

---

### **Nhược điểm**
- Truyền struct theo giá trị (pass by value) có thể tốn bộ nhớ nếu struct lớn.
- Không hỗ trợ các phương thức như trong C++ (OOP).

---