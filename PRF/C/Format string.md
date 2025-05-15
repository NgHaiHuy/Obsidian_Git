

---

# 📘 Chuỗi định dạng trong C (Format Strings) — Đầy đủ

Chuỗi định dạng trong C là chuỗi chứa các **specifier** (ký hiệu định dạng) dùng với các hàm như `printf()`, `sprintf()`… để **hiển thị dữ liệu theo định dạng mong muốn**.

---

## ✅ Cấu trúc tổng quát

```
%[flags][width][.precision][length]specifier
```

---

## 🔠 Các **specifier** thường dùng (kèm ví dụ)

|Specifier|Ý nghĩa|Ví dụ|
|---|---|---|
|`%d`|Số nguyên có dấu (int)|`printf("%d", -123);`|
|`%i`|Giống `%d`, thường dùng thay thế|`printf("%i", 42);`|
|`%u`|Số nguyên không dấu (unsigned int)|`printf("%u", 300);`|
|`%ld`|`long int`|`printf("%ld", 100000L);`|
|`%lu`|`unsigned long int`|`printf("%lu", 4000000000);`|
|`%f`|Số thực (float, double)|`printf("%.2f", 3.14159);`|
|`%e` / `%E`|Khoa học (số mũ, exponential)|`printf("%e", 1000.0);`|
|`%g` / `%G`|Gọn gàng giữa `%f` và `%e`|`printf("%g", 123456.0);`|
|`%c`|Ký tự đơn|`printf("%c", 'A');`|
|`%s`|Chuỗi ký tự|`printf("%s", "Hi");`|
|`%x` / `%X`|Số hệ 16 (hex)|`printf("%x", 255);` → `ff`|
|`%o`|Số hệ 8 (octal)|`printf("%o", 10);` → `12`|
|`%p`|Con trỏ (địa chỉ bộ nhớ)|`printf("%p", ptr);`|
|`%%`|In ra dấu phần trăm `%`|`printf("%%");`|
|`\n`|**Xuống dòng**|`printf("Hello\nWorld");`|
|`\t`|**Tab ngang**|`printf("A\tB");`|

📝 **Lưu ý**: `\n`, `\t` là **ký tự đặc biệt (escape sequences)**, không phải specifier theo kiểu `%`, nhưng thường dùng trong format string nên mình liệt kê luôn.

---

## 🎛️ Giải thích các phần khác của định dạng

### 1. **Width**: Độ rộng tối thiểu

```c
printf("|%10d|\n", 123);   // |       123|
```

### 2. **Precision (`.precision`)**

- Với số thực: số chữ số sau dấu phẩy
    
- Với chuỗi: độ dài tối đa được in ra
    

```c
printf("%.2f\n", 3.14159);     // 3.14
printf("%.3s\n", "abcdef");    // abc
```

### 3. **Flags (cờ định dạng)**

|Cờ|Tác dụng|Ví dụ|
|---|---|---|
|`-`|Căn trái|`%-10s`|
|`0`|Đệm bằng số 0|`%05d` → `00042`|
|`+`|In dấu `+` với số dương|`%+d` → `+42`|
|(space)|Thêm khoảng trắng nếu số dương|`% d` → `42`|
|`#`|In thêm tiền tố (0x, 0, ...)|`%#x` → `0xff`|

---

## 🧪 Ví dụ tổng hợp

```c
#include <stdio.h>

int main() {
    int num = 42;
    float pi = 3.141592;
    char ch = 'A';
    char *str = "OpenAI";
    void *ptr = &num;

    printf("1. Số nguyên:         |%5d|\n", num);
    printf("2. Căn trái:          |%-5d|\n", num);
    printf("3. Đệm bằng 0:        |%05d|\n", num);
    printf("4. Có dấu +:          |%+d|\n", num);
    printf("5. Số thực:           |%.3f|\n", pi);
    printf("6. Số dạng mũ:        |%e|\n", pi);
    printf("7. Chuỗi rút gọn:     |%.3s|\n", str);
    printf("8. Hex + tiền tố:     |%#x|\n", 255);
    printf("9. In con trỏ:        |%p|\n", ptr);
    printf("10. Ký tự:            |%c|\n", ch);
    printf("11. In dấu %%:         |%%|\n");
    printf("12. Tab và newline:   |A\tB\n");
    
    return 0;
}
```

---

## 📌 Bảng tóm tắt

|Mục đích|Format|Ghi chú|
|---|---|---|
|Số nguyên|`%d`, `%i`, `%u`|Có dấu, không dấu|
|Số thực|`%f`, `%.2f`, `%e`|Có thập phân, dạng mũ|
|Căn trái/phải|`%-10d`, `%10s`|Dài ít nhất 10 ký tự|
|Đệm bằng số 0|`%05d`|`00042`|
|Dấu cộng/dấu cách|`%+d`, `% d`|`+42`, `42`|
|Số hệ 16/8|`%x`, `%#x`, `%o`|`ff`, `0xff`, `12`|
|Chuỗi rút gọn|`%.4s`|In n ký tự đầu chuỗi|
|In con trỏ|`%p`|Địa chỉ ô nhớ|
|In ký tự đặc biệt|`%%`, `\n`, `\t`|Phần trăm, xuống dòng, tab|

---
