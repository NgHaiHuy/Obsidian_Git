Trong ngôn ngữ lập trình C, có nhiều **thư viện chuẩn** (standard libraries) cung cấp sẵn các hàm giúp bạn xử lý các công việc thường gặp như nhập xuất, xử lý chuỗi, toán học, làm việc với tệp tin, v.v.

Dưới đây là một số **thư viện phổ biến nhất trong C**:

---

### 📌 1. `#include <stdio.h>`

**(Standard Input Output)**  
Dùng để nhập và xuất dữ liệu.  
🔹 Các hàm tiêu biểu:

- `printf()` – in ra màn hình
    
- `scanf()` – đọc dữ liệu từ bàn phím
    
- `fopen(), fclose(), fread(), fwrite()` – thao tác với file
    

---

### 📌 2. `#include <stdlib.h>`

**(Standard Library)**  
Chứa các hàm tiện ích tổng quát.  
🔹 Các hàm tiêu biểu:

- `malloc(), calloc(), free()` – cấp phát/buông bộ nhớ
    
- `atoi(), atof()` – chuyển đổi chuỗi thành số
    
- `rand(), srand()` – sinh số ngẫu nhiên
    
- `exit()` – thoát chương trình
    

---

### 📌 3. `#include <string.h>`

**(String handling)**  
Xử lý chuỗi ký tự (mảng `char[]`).  
🔹 Các hàm tiêu biểu:

- `strcpy(), strncpy()` – sao chép chuỗi
    
- `strlen()` – độ dài chuỗi
    
- `strcmp()` – so sánh chuỗi
    
- `strcat()` – nối chuỗi
    

---

### 📌 4. `#include <math.h>`

**(Math functions)**  
Các hàm toán học.  
🔹 Các hàm tiêu biểu:

- `sqrt()` – căn bậc hai
    
- `pow(a, b)` – lũy thừa a^b
    
- `sin(), cos(), tan()` – lượng giác
    
- `fabs()` – trị tuyệt đối
    

📝 Lưu ý: Khi dùng `math.h`, biên dịch với `-lm` nếu dùng GCC:

```bash
gcc mycode.c -lm
```

---

### 📌 5. `#include <ctype.h>`

**(Character type)**  
Xử lý ký tự đơn lẻ.  
🔹 Các hàm tiêu biểu:

- `isalpha(), isdigit()` – kiểm tra loại ký tự
    
- `toupper(), tolower()` – đổi chữ hoa/thường
    

---

### 📌 6. `#include <time.h>`

**(Time and date)**  
Làm việc với thời gian.  
🔹 Các hàm tiêu biểu:

- `time()` – lấy thời gian hiện tại
    
- `clock()` – đếm thời gian CPU sử dụng
    
- `localtime()` – chuyển thời gian thành dạng `struct tm`
    

---

### 📌 7. `#include <stdbool.h>`

**(Boolean type)**  
Giúp dùng kiểu `bool`, `true`, `false` (chuẩn từ C99).

---

### 📌 8. `#include <limits.h>` và `#include <float.h>`

Chứa giá trị giới hạn của kiểu số nguyên và số thực như:

- `INT_MAX`, `INT_MIN`
    
- `FLT_MAX`, `DBL_MIN`
    

---

### 📌 Một số thư viện khác:

- `<errno.h>` – xử lý mã lỗi
    
- `<assert.h>` – kiểm tra điều kiện trong khi chạy (debug)
    
- `<stdarg.h>` – xử lý hàm có số lượng tham số không cố định (như `printf`)
    
- `<stddef.h>` – định nghĩa các kiểu như `size_t`, `NULL`
    

---
