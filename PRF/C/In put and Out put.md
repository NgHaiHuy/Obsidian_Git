Trong ngôn ngữ lập trình **C**, bạn có thể nhập và xuất **chữ**, **số nguyên**, **số thực**, hoặc **chuỗi** bằng cách sử dụng các hàm trong thư viện chuẩn như `scanf()` và `printf()`.

---

## ✅ 1. **Input / Output số nguyên**

### 📌 Ví dụ:

```c
#include <stdio.h>

int main() {
    int a;
    printf("Nhap so nguyen a: ");
    scanf("%d", &a);  // %d để nhập số nguyên

    printf("Gia tri a = %d\n", a);
    return 0;
}
```

---

## ✅ 2. **Input / Output số thực (float, double)**

```c
#include <stdio.h>

int main() {
    float x;
    printf("Nhap so thuc x: ");
    scanf("%f", &x);  // %f để nhập float

    printf("Gia tri x = %.2f\n", x);  // in 2 chữ số thập phân
    return 0;
}
```

> Dùng `%.2f` để in 2 số sau dấu phẩy, có thể đổi thành `%.1f`, `%.3f`, v.v.

---

## ✅ 3. **Input / Output 1 ký tự**

```c
#include <stdio.h>

int main() {
    char ch;
    printf("Nhap mot ky tu: ");
    scanf(" %c", &ch);  // khoảng trắng trước %c để tránh lỗi khi đọc ký tự sau số

    printf("Ky tu vua nhap: %c\n", ch);
    return 0;
}
```

---

## ✅ 4. **Input / Output chuỗi (xâu ký tự)**

```c
#include <stdio.h>

int main() {
    char name[50];
    printf("Nhap ten: ");
    scanf("%s", name);  // lưu ý: không đọc được chuỗi có khoảng trắng

    printf("Xin chao %s!\n", name);
    return 0;
}
```

> Nếu bạn muốn nhập cả **chuỗi có khoảng trắng**, thì dùng `fgets()` thay vì `scanf("%s")`.

---

## 🔁 Tổng hợp định dạng trong `scanf()` / `printf()`:

|Kiểu dữ liệu|`scanf`|`printf`|
|---|---|---|
|int|`%d`|`%d`|
|float|`%f`|`%f`|
|double|`%lf`|`%lf`|
|char|`%c`|`%c`|
|string|`%s`|`%s`|

---

Nếu bạn muốn mình tạo ví dụ cụ thể cho một bài toán (cộng 2 số, nhập tên, v.v.) thì cứ nói nhé!