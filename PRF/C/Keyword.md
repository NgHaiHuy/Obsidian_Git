Dưới đây là **tên**, **ý nghĩa**, và **ví dụ** cho từng **32 từ khóa trong ngôn ngữ lập trình C** :

---

### 1. `int`

- **Ý nghĩa**: Kiểu dữ liệu số nguyên.
    
- **Ví dụ**: `int age = 25;`
    

### 2. `char`

- **Ý nghĩa**: Kiểu dữ liệu ký tự (1 byte).
    
- **Ví dụ**: `char letter = 'A';`
    

### 3. `float`

- **Ý nghĩa**: Kiểu dữ liệu thực (độ chính xác đơn).
    
- **Ví dụ**: `float pi = 3.14;`
    

### 4. `double`

- **Ý nghĩa**: Kiểu dữ liệu thực (độ chính xác kép).
    
- **Ví dụ**: `double balance = 12345.67;`
    

### 5. `void`

- **Ý nghĩa**: Không có giá trị trả về.
    
- **Ví dụ**: `void sayHello() { printf("Hello!"); }`
    

### 6. `auto`

- **Ý nghĩa**: Khai báo biến cục bộ (tự động), mặc định trong C.
    
- **Ví dụ**: `auto int x = 10;`
    

### 7. `static`

- **Ý nghĩa**: Giữ giá trị giữa các lần gọi hàm.
    
- **Ví dụ**:
    

```c
void counter() {
    static int count = 0;
    count++;
    printf("%d\n", count);
}
```

### 8. `extern`

- **Ý nghĩa**: Khai báo biến/hàm từ file khác.
    
- **Ví dụ**: `extern int total;`
    

### 9. `register`

- **Ý nghĩa**: Yêu cầu lưu biến vào thanh ghi (gợi ý).
    
- **Ví dụ**: `register int i;`
    

### 10. `break`

- **Ý nghĩa**: Thoát khỏi vòng lặp hoặc switch.
    
- **Ví dụ**:
    

```c
for (int i = 0; i < 10; i++) {
    if (i == 5) break;
}
```

### 11. `switch`

- **Ý nghĩa**: Rẽ nhánh nhiều điều kiện.
    
- **Ví dụ**:
    

```c
switch (x) {
    case 1: printf("One"); break;
}
```

### 12. `case`

- **Ý nghĩa**: Trường hợp cụ thể trong switch.
    
- **Ví dụ**: `case 2: printf("Two"); break;`
    

### 13. `if`

- **Ý nghĩa**: Câu lệnh điều kiện.
    
- **Ví dụ**: `if (x > 0) printf("Positive");`
    

### 14. `else`

- **Ý nghĩa**: Nếu điều kiện if sai.
    
- **Ví dụ**:
    

```c
if (x > 0) printf("Positive");
else printf("Non-positive");
```

### 15. `const`

- **Ý nghĩa**: Hằng số (không thay đổi).
    
- **Ví dụ**: `const int MAX = 100;`
    

### 16. `default`

- **Ý nghĩa**: Trường hợp mặc định trong switch.
    
- **Ví dụ**:
    

```c
default: printf("Unknown");
```

### 17. `for`

- **Ý nghĩa**: Vòng lặp có điều kiện rõ ràng.
    
- **Ví dụ**: `for (int i = 0; i < 5; i++) printf("%d", i);`
    

### 18. `do`

- **Ý nghĩa**: Phần đầu vòng lặp do-while.
    
- **Ví dụ**:
    

```c
do {
    printf("Run once");
} while (0);
```

### 19. `while`

- **Ý nghĩa**: Vòng lặp khi điều kiện đúng.
    
- **Ví dụ**:
    

```c
while (x > 0) {
    x--;
}
```

### 20. `return`

- **Ý nghĩa**: Trả giá trị về từ hàm.
    
- **Ví dụ**: `return 0;`
    

### 21. `continue`

- **Ý nghĩa**: Bỏ qua phần còn lại vòng lặp.
    
- **Ví dụ**:
    

```c
for (int i = 0; i < 10; i++) {
    if (i % 2 == 0) continue;
    printf("%d", i);
}
```

### 22. `goto`

- **Ý nghĩa**: Nhảy đến nhãn (không khuyến khích).
    
- **Ví dụ**:
    

```c
goto label;
label: printf("Jumped!");
```

### 23. `long`

- **Ý nghĩa**: Kiểu số nguyên dài.
    
- **Ví dụ**: `long distance = 100000L;`
    

### 24. `short`

- **Ý nghĩa**: Kiểu số nguyên ngắn.
    
- **Ví dụ**: `short smallNumber = 5;`
    

### 25. `signed`

- **Ý nghĩa**: Số nguyên có dấu.
    
- **Ví dụ**: `signed int a = -10;`
    

### 26. `unsigned`

- **Ý nghĩa**: Số nguyên không dấu.
    
- **Ví dụ**: `unsigned int b = 10;`
    

### 27. `sizeof`

- **Ý nghĩa**: Trả về kích thước (byte).
    
- **Ví dụ**: `printf("%zu", sizeof(int));`
    

### 28. `struct`

- **Ý nghĩa**: Cấu trúc dữ liệu.
    
- **Ví dụ**:
    

```c
struct Point {
    int x, y;
};
```

### 29. `typeof` _(không phải chuẩn C89/C99 mà là phần mở rộng của GCC)_

- **Ý nghĩa**: Lấy kiểu dữ liệu của biến (GCC extension).
    
- **Ví dụ**: `typeof(x) y = 10;`
    

### 30. `volatile`

- **Ý nghĩa**: Không tối ưu biến vì có thể thay đổi ngoài chương trình.
    
- **Ví dụ**: `volatile int flag;`
    

### 31. `union`

- **Ý nghĩa**: Cấu trúc lưu nhiều kiểu tại cùng một vùng nhớ.
    
- **Ví dụ**:
    

```c
union Data {
    int i;
    float f;
};
```

### 32. `enum`

- **Ý nghĩa**: Tập hợp hằng số.
    
- **Ví dụ**:
    

```c
enum Color { RED, GREEN, BLUE };
```

---
