

---

## 📌 1. Cú pháp của `switch case` trong C

```c
switch (biểu_thức) {
    case hằng_số_1:
        // khối lệnh 1
        break;
    case hằng_số_2:
        // khối lệnh 2
        break;
    ...
    default:
        // khối lệnh mặc định
}
```

### ✅ Giải thích:

- `biểu_thức`: phải là kiểu **nguyên thủy** như `int` hoặc `char`.
    
- `case`: mỗi `case` là một giá trị **hằng số duy nhất**.
    
- `break`: kết thúc `case`. Nếu **không có `break`**, chương trình sẽ **rơi qua các case tiếp theo** (gọi là **fall-through**).
    
- `default`: khối mặc định, chạy khi **không có case nào khớp**.
    

---

## 📘 2. Ví dụ đơn giản

```c
#include <stdio.h>

int main() {
    int number = 2;

    switch (number) {
        case 1:
            printf("One\n");
            break;
        case 2:
            printf("Two\n");
            break;
        case 3:
            printf("Three\n");
            break;
        default:
            printf("Not 1, 2, or 3\n");
    }

    return 0;
}
```

📤 **Kết quả:**

```
Two
```

---

## 🔍 3. Ví dụ với fall-through (không có `break`)

```c
int x = 1;

switch (x) {
    case 1:
        printf("Case 1\n");
    case 2:
        printf("Case 2\n");
    case 3:
        printf("Case 3\n");
        break;
    default:
        printf("Default case\n");
}
```

📤 **Kết quả:**

```
Case 1  
Case 2  
Case 3
```

➡️ Vì **không có `break` sau case 1 và 2**, nên lệnh sẽ chạy tiếp qua case tiếp theo.

---

## ⚠️ 4. Những lưu ý quan trọng

|Nội dung|Mô tả|
|---|---|
|`biểu_thức` chỉ nhận kiểu|`int`, `char`, `enum`|
|Không hỗ trợ kiểu `float`|❌ Không thể dùng `switch(float)`|
|`case` phải là hằng số|❌ Không dùng biến trong `case`|
|`break` là tùy chọn|Nhưng nên dùng để tránh **fall-through** trừ khi có chủ đích|
|`default` là tùy chọn|Nhưng nên có để xử lý các trường hợp khác|

---

## 🧠 5. Ứng dụng thực tế – Chuyển ngày sang tên thứ

```c
#include <stdio.h>

int main() {
    int day;

    printf("Nhap so ngay (1-7): ");
    scanf("%d", &day);

    switch (day) {
        case 1:
            printf("Chu Nhat\n");
            break;
        case 2:
            printf("Thu Hai\n");
            break;
        case 3:
            printf("Thu Ba\n");
            break;
        case 4:
            printf("Thu Tu\n");
            break;
        case 5:
            printf("Thu Nam\n");
            break;
        case 6:
            printf("Thu Sau\n");
            break;
        case 7:
            printf("Thu Bay\n");
            break;
        default:
            printf("Gia tri khong hop le\n");
    }

    return 0;
}
```

---

## 🧪 6. So sánh với `if else`

|Tiêu chí|`switch`|`if-else`|
|---|---|---|
|Dễ đọc|✅ (với nhiều case)|❌ (nhiều `else if`)|
|Hỗ trợ so sánh|`==`|Mọi loại biểu thức (`<`, `>`, `!=`, ...)|
|Kiểu dữ liệu|Chỉ hỗ trợ số nguyên và `char`|Hỗ trợ mọi kiểu|

---

## ✅ 7. Tổng kết

- `switch case` dùng để chọn giữa **nhiều nhánh có giá trị cụ thể**.
    
- Giúp mã dễ đọc hơn so với nhiều `if else`.
    
- Luôn nhớ dùng `break` nếu không muốn rơi vào nhánh tiếp theo.
    
- Hữu ích khi có nhiều lựa chọn theo giá trị số nguyên hoặc ký tự.
    

---
