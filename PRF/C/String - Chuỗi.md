
---

### ✅ **1. Chuỗi là gì trong C?**

Trong C, **chuỗi (string)** là một **mảng các ký tự** (`char[]`) được **kết thúc bằng ký tự null** `'\0'`.  
Ví dụ:

```c
char s[] = "Hello";  // Thực chất là {'H', 'e', 'l', 'l', 'o', '\0'}
```

---

### ✅ **2. Khai báo và Khởi tạo String**

```c
char str1[10];                      // Khai báo, chưa gán giá trị
char str2[] = "Hello";             // Tự động thêm '\0'
char str3[6] = {'H','e','l','l','o','\0'};  // Rõ ràng
```

📌 **Lưu ý:**

- Ký tự `'\0'` rất quan trọng, dùng để đánh dấu kết thúc chuỗi.
    
- Nếu không có `'\0'`, các hàm thao tác chuỗi sẽ bị lỗi hoặc đọc vượt giới hạn.
    

---

### ✅ **3. Nhập / Xuất Chuỗi**

#### Dùng `scanf` (không đọc được khoảng trắng):

```c
char name[20];
scanf("%s", name);
```

#### Dùng `fgets` (đọc được cả dòng có khoảng trắng):

```c
fgets(name, sizeof(name), stdin);
name[strcspn(name, "\n")] = '\0';  // Xoá ký tự newline nếu có
```

📌 **Lưu ý:**

- `scanf` không giới hạn độ dài → dễ gây tràn bộ nhớ
    
- `fgets` an toàn hơn, nên dùng trong hầu hết trường hợp
    

---

### ✅ **4. Các hàm xử lý chuỗi – `#include <string.h>`**

|Hàm|Mô tả|
|---|---|
|`strcpy(dest, src)`|Sao chép chuỗi|
|`strncpy(dest, src, n)`|Sao chép n ký tự|
|`strcat(dest, src)`|Nối chuỗi|
|`strncat(dest, src, n)`|Nối n ký tự|
|`strcmp(s1, s2)`|So sánh hai chuỗi|
|`strncmp(s1, s2, n)`|So sánh n ký tự|
|`strlen(s)`|Trả về độ dài chuỗi (không tính `'\0'`)|
|`strchr(s, ch)`|Tìm ký tự đầu tiên xuất hiện|
|`strstr(s1, s2)`|Tìm chuỗi con|

---

### ✅ **5. Các hàm kiểm tra ký tự – `#include <ctype.h>`**

|Hàm|Chức năng|
|---|---|
|`isalpha(c)`|Kiểm tra có phải chữ cái không (a-zA-Z)|
|`isdigit(c)`|Kiểm tra có phải chữ số không (0-9)|
|`isspace(c)`|Kiểm tra có phải khoảng trắng (space, tab, newline)|
|`islower(c)`|Kiểm tra chữ thường|
|`isupper(c)`|Kiểm tra chữ hoa|
|`isalnum(c)`|Kiểm tra là chữ cái hoặc số|
|`ispunct(c)`|Kiểm tra là ký tự đặc biệt|
|`tolower(c)`|Chuyển ký tự sang chữ thường|
|`toupper(c)`|Chuyển ký tự sang chữ hoa|

📌 **Ví dụ phân loại ký tự trong chuỗi**:

```c
for (int i = 0; str[i] != '\0'; i++) {
    if (isalpha(str[i])) printf("Chữ cái\n");
    else if (isdigit(str[i])) printf("Chữ số\n");
    else if (isspace(str[i])) printf("Khoảng trắng\n");
    else printf("Ký tự đặc biệt\n");
}
```

---

### ✅ **6. Mảng chuỗi (mảng 2 chiều)**

```c
char names[3][20] = {"Alice", "Bob", "Charlie"};
printf("Tên thứ hai: %s\n", names[1]);  // In ra "Bob"
```

📌 Mỗi hàng là một chuỗi riêng biệt. Có thể dùng vòng lặp để duyệt từng chuỗi.

---

### ✅ **7. Con trỏ và chuỗi**

```c
char *s = "Hello";  // trỏ tới chuỗi hằng
printf("%s\n", s);
```

🔒 Không thể thay đổi nội dung nếu chuỗi là hằng.

```c
char arr[] = "Hello";
arr[0] = 'h';  // ✅ Hợp lệ
```

---

### ✅ **8. Lỗi thường gặp**

|Lỗi|Giải thích|
|---|---|
|**Thiếu `'\0'`**|Gây lỗi khi in hoặc thao tác chuỗi|
|**Dùng `scanf` không an toàn**|Có thể nhập vượt giới hạn mảng|
|**Gán chuỗi bằng phép gán**|Không thể `str1 = str2` (dùng `strcpy`)|
|**So sánh chuỗi bằng `==`**|So sánh địa chỉ, không so sánh nội dung|

---

### ✅ **9. Ví dụ tổng hợp**

```c
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char str[100];
    int chu = 0, so = 0, dacbiet = 0;

    printf("Nhập chuỗi: ");
    fgets(str, sizeof(str), stdin);

    for (int i = 0; str[i] != '\0'; i++) {
        if (isalpha(str[i]))
            chu++;
        else if (isdigit(str[i]))
            so++;
        else if (!isspace(str[i]))
            dacbiet++;
    }

    printf("Chữ cái: %d\n", chu);
    printf("Chữ số: %d\n", so);
    printf("Ký tự đặc biệt: %d\n", dacbiet);
    printf("Độ dài chuỗi: %zu\n", strlen(str));
    return 0;
}
```

---

### ✅ **10. Tóm tắt**

|Chủ đề|Nội dung|
|---|---|
|Kiểu dữ liệu|`char[]`, kết thúc bằng `'\0'`|
|Nhập|Dùng `fgets` để an toàn|
|Xử lý|Dùng `<string.h>` và `<ctype.h>`|
|Cần tránh|So sánh bằng `==`, gán trực tiếp, thiếu `'\0'`|

---
