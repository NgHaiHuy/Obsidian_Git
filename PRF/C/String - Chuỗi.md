Trong ngôn ngữ C, **string** (chuỗi) là một mảng các ký tự (`char`) kết thúc bằng ký tự **null** (`'\0'`). Dưới đây là phân tích chi tiết về string trong C, bao gồm khai báo, cách sử dụng, và các hàm thư viện phổ biến.

---

### **1. Khai báo và Khởi tạo String**
- **String là mảng ký tự**:  
  ```c
  char str1[10];          // Khai báo mảng 10 ký tự (chưa khởi tạo)
  char str2[] = "Hello";  // Khởi tạo với giá trị "Hello" (tự động thêm '\0')
  char str3[6] = {'H', 'e', 'l', 'l', 'o', '\0'};  // Khởi tạo từng ký tự
  ```

- **Lưu ý**:
  - Ký tự `'\0'` đánh dấu kết thúc chuỗi. Nếu thiếu, các hàm xử lý chuỗi có thể gặp lỗi.
  - Kích thước mảng phải đủ lớn để chứa chuỗi + `'\0'`. Ví dụ: `"Hello"` cần mảng tối thiểu 6 phần tử.

---

### **2. Nhập/Xuất String**
- **Sử dụng `scanf` và `printf`**:
  ```c
  char name[20];
  printf("Nhập tên: ");
  scanf("%s", name);      // Dừng khi gặp khoảng trắng
  printf("Tên: %s\n", name);
  ```

- **Nhập chuỗi có khoảng trắng** (dùng `fgets`):
  ```c
  fgets(name, sizeof(name), stdin);  // Đọc cả dòng (kể cả khoảng trắng)
  ```

- **Lưu ý**:
  - `scanf` không an toàn với chuỗi dài hơn kích thước mảng. Có thể dùng `%19s` để giới hạn.
  - `fgets` lưu cả ký tự `\n` (xuống dòng), cần xóa nếu không mong muốn.

---

### **3. Các Hàm Thư Viện `<string.h>`**
#### **a. Sao chép chuỗi: `strcpy`, `strncpy`**
- **`strcpy`**:
  ```c
  char src[] = "Source";
  char dest[10];
  strcpy(dest, src);  // dest = "Source"
  ```
  - **Lưu ý**: Kiểm tra kích thước mảng đích để tránh tràn bộ nhớ.

- **`strncpy`** (an toàn hơn):
  ```c
  strncpy(dest, src, sizeof(dest) - 1);  // Sao chép tối đa (kích thước đích - 1)
  dest[sizeof(dest) - 1] = '\0';         // Đảm bảo kết thúc chuỗi
  ```

#### **b. Nối chuỗi: `strcat`, `strncat`**
- **`strcat`**:
  ```c
  char str1[20] = "Hello";
  char str2[] = " World";
  strcat(str1, str2);  // str1 = "Hello World"
  ```
  - **Lưu ý**: Đảm bảo mảng đích đủ lớn.

#### **c. So sánh chuỗi: `strcmp`, `strncmp`**
- **`strcmp`**:
  ```c
  if (strcmp(str1, str2) == 0) {
      printf("Hai chuỗi giống nhau.\n");
  }
  ```
  - Trả về `0` nếu giống nhau, giá trị âm/dương nếu khác nhau.

#### **d. Độ dài chuỗi: `strlen`**
- **Ví dụ**:
  ```c
  int len = strlen("Hello");  // len = 5
  ```

---

### **4. Mảng String (Mảng 2 chiều)**
- **Khai báo**:
  ```c
  char names[3][20] = {"Alice", "Bob", "Charlie"};
  ```
- **Truy cập**:
  ```c
  printf("Tên thứ 2: %s\n", names[1]);  // "Bob"
  ```

---

### **5. Con trỏ và String**
- **String có thể được truy cập qua con trỏ**:
  ```c
  char *ptr = "Hello";  // Con trỏ trỏ đến chuỗi hằng (không thể thay đổi nội dung)
  printf("%s\n", ptr);  // In ra "Hello"
  ```

- **Lưu ý**:
  - Chuỗi hằng (`"Hello"`) lưu trong bộ nhớ chỉ đọc (segmentation fault nếu cố ghi).
  - Để thay đổi nội dung, dùng mảng:
    ```c
    char arr[] = "Hello";
    arr[0] = 'h';  // Hợp lệ
    ```

---

### **6. Ví dụ Tổng Hợp**
```c
#include <stdio.h>
#include <string.h>

int main() {
    char s1[20] = "Hello";
    char s2[20];

    // Sao chép và nối chuỗi
    strcpy(s2, s1);
    strcat(s2, " World!");
    printf("s2: %s\n", s2);  // "Hello World!"

    // So sánh
    if (strcmp(s1, s2) != 0) {
        printf("s1 và s2 khác nhau.\n");
    }

    // Độ dài
    printf("Độ dài s2: %zu\n", strlen(s2));  // 12
    return 0;
}
```

---

### **7. Lỗi Thường Gặp**
1. **Quên `'\0'`**:
   ```c
   char s[3] = {'A', 'B', 'C'};  // Không phải string hợp lệ (thiếu '\0')
   ```
2. **Tràn bộ nhớ**:
   ```c
   char s[5];
   strcpy(s, "Hello World");  // Lỗi tràn
   ```
3. **Nhập với `scanf` không giới hạn**:
   ```c
   scanf("%s", s);  // Nguy hiểm nếu người dùng nhập quá dài
   ```

---

### **Tóm tắt**
- **String trong C** là mảng ký tự kết thúc bằng `'\0'`.
- **Thư viện `<string.h>`** cung cấp các hàm xử lý chuỗi như `strcpy`, `strcat`, `strcmp`, `strlen`.
- **Luôn kiểm tra kích thước mảng** để tránh tràn bộ nhớ.
- **Sử dụng `fgets` thay vì `scanf`** để nhập chuỗi có khoảng trắng an toàn.