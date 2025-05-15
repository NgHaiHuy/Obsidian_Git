Trong ngôn ngữ lập trình C, **biến (variable)** là vùng nhớ dùng để lưu trữ dữ liệu, và mỗi biến sẽ có **tên**, **kiểu dữ liệu**, và có thể có **giá trị**. Biến được dùng để lưu tạm dữ liệu trong quá trình chương trình chạy.

---

### 🧱 Cú pháp khai báo biến trong C:

```c
<kiểu_dữ_liệu> <tên_biến>;
```

Ví dụ:

```c
int age;          // biến kiểu int
float score;      // biến kiểu float
char letter;      // biến kiểu ký tự
```

Bạn cũng có thể **khởi tạo giá trị ngay khi khai báo**:

```c
int age = 20;
float score = 8.5;
char letter = 'A';
```

---

### 📦 Các kiểu dữ liệu cơ bản:

|Kiểu|Mô tả|Ví dụ|
|---|---|---|
|`int`|Số nguyên|1, 25, -10|
|`float`|Số thực, dấu phẩy động|3.14, -0.5|
|`double`|Số thực chính xác cao hơn|3.1415926|
|`char`|Một ký tự|'A', 'z', '9'|

---

### ⚠️ Lưu ý khi dùng biến trong C:

1. **Phải khai báo trước khi sử dụng.**
    
2. **Tên biến không được trùng từ khóa C** (ví dụ: `int`, `return`, `if`).
    
3. **Tên biến phân biệt chữ hoa và chữ thường** (`age` khác `Age`).
    
4. Tên biến nên rõ ràng, dễ hiểu (`score` tốt hơn `s`).
    

---

### 🧪 Ví dụ đơn giản:

```c
#include <stdio.h>

int main() {
    int age = 18;
    float height = 1.75;
    char grade = 'A';

    printf("Age: %d\n", age);
    printf("Height: %.2f\n", height);
    printf("Grade: %c\n", grade);

    return 0;
}
```

Kết quả:

```
Age: 18
Height: 1.75
Grade: A
```

---
