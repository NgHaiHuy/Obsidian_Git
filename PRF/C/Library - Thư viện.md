Dưới đây là bản **tổng hợp đầy đủ tất cả các thư viện chuẩn C cơ bản**, bao gồm:  
📁 Nhập/xuất (`<stdio.h>`), chuỗi (`<string.h>`), toán học (`<math.h>`), xử lý bộ nhớ & hệ thống (`<stdlib.h>`), xử lý ký tự (`<ctype.h>`), thời gian (`<time.h>`), boolean (`<stdbool.h>`), giới hạn kiểu dữ liệu (`<limits.h>`, `<float.h>`), và các thư viện tiện ích khác.

---

## 📘 `<stdio.h>` – Nhập xuất chuẩn

|Hàm|Mô tả|Ví dụ|
|---|---|---|
|`printf()`|In ra màn hình|`printf("Hello %d", 5);`|
|`scanf()`|Nhập từ bàn phím|`int x; scanf("%d", &x);`|
|`putchar()`|In ký tự|`putchar('A');`|
|`getchar()`|Nhập ký tự|`char c = getchar();`|
|`puts()`|In chuỗi + xuống dòng|`puts("Xin chào");`|
|`gets()` _(không an toàn)_|Nhập chuỗi|`gets(s);`|
|`fopen()` / `fclose()`|Mở/đóng file|`FILE *f = fopen("a.txt", "r");`|
|`fgetc()` / `fputc()`|Đọc/ghi ký tự|`fputc('A', f);`|
|`fgets()` / `fputs()`|Đọc/ghi dòng|`fgets(buf, 100, f);`|
|`fprintf()` / `fscanf()`|Đọc/ghi có định dạng|`fprintf(f, "%d", x);`|
|`fseek()` / `ftell()` / `rewind()`|Điều hướng con trỏ file|`fseek(f, 0, SEEK_SET);`|
|`remove()` / `rename()`|Xoá hoặc đổi tên file|`remove("a.txt");`|

---

## 📗 `<stdlib.h>` – Thư viện chuẩn

|Hàm|Mô tả|Ví dụ|
|---|---|---|
|`malloc()` / `calloc()` / `realloc()` / `free()`|Quản lý bộ nhớ|`int *p = malloc(10*sizeof(int));`|
|`exit()`|Thoát chương trình|`exit(1);`|
|`atoi()` / `atof()`|Chuỗi → số|`atoi("123");`|
|`rand()` / `srand()`|Số ngẫu nhiên|`srand(time(NULL)); rand();`|
|`abs()`|Giá trị tuyệt đối nguyên|`abs(-10);`|
|`system()`|Gọi lệnh hệ thống|`system("cls");`|
|`qsort()` / `bsearch()`|Sắp xếp và tìm kiếm|`qsort(arr, n, sz, cmp);`|

---

## 📙 `<string.h>` – Xử lý chuỗi

| Hàm                      | Mô tả             | Ví dụ                  |
| ------------------------ | ----------------- | ---------------------- |
| `strlen()`               | Độ dài chuỗi      | `strlen("abc");`       |
| `strcpy()` / `strncpy()` | Sao chép chuỗi    | `strcpy(dest, src);`   |
| `strcat()` / `strncat()` | Nối chuỗi         | `strcat(s1, s2);`      |
| `strcmp()` / `strncmp()` | So sánh chuỗi     | `strcmp(a, b);`        |
| `strchr()` / `strrchr()` | Tìm ký tự         | `strchr(s, 'a');`      |
| `strstr()`               | Tìm chuỗi con     | `strstr(s, "abc");`    |
| `strtok()`               | Tách chuỗi        | `strtok(s, " ,");`     |
| `memcpy()` / `memmove()` | Sao chép vùng nhớ | `memcpy(d, s, n);`     |
| `memset()`               | Gán vùng nhớ      | `memset(arr, 0, 100);` |

---

## 📐 `<math.h>` – Hàm toán học

|Hàm|Mô tả|Ví dụ|
|---|---|---|
|`sqrt()`|Căn bậc hai|`sqrt(9.0);`|
|`pow()`|Lũy thừa|`pow(2, 3);`|
|`sin()` / `cos()` / `tan()`|Lượng giác|`sin(PI);`|
|`log()` / `log10()` / `exp()`|Logarit và mũ|`log(10);`|
|`fabs()`|Giá trị tuyệt đối|`fabs(-3.5);`|
|`ceil()` / `floor()` / `round()`|Làm tròn|`ceil(2.3);`|
|`fmod()`|Phần dư số thực|`fmod(5.3, 2);`|

---

## 🔤 `<ctype.h>` – Xử lý ký tự

|Hàm|Mô tả|Ví dụ|
|---|---|---|
|`isalpha()`|Là chữ cái|`isalpha('A');`|
|`isdigit()`|Là chữ số|`isdigit('7');`|
|`isalnum()`|Là chữ hoặc số|`isalnum('a');`|
|`islower()` / `isupper()`|Thường/in hoa|`islower('c');`|
|`isspace()`|Khoảng trắng|`isspace(' ');`|
|`isprint()`|In được|`isprint('#');`|
|`ispunct()`|Ký hiệu|`ispunct('.');`|
|`isxdigit()`|Hex|`isxdigit('F');`|
|`toupper()` / `tolower()`|Đổi hoa/thường|`toupper('a');`|

---

## ⏰ `<time.h>` – Làm việc với thời gian

|Hàm|Mô tả|Ví dụ|
|---|---|---|
|`time()`|Lấy thời gian hiện tại|`time_t now = time(NULL);`|
|`clock()`|Thời gian CPU đã dùng|`clock_t t = clock();`|
|`localtime()`|Chuyển `time_t` → `struct tm`|`localtime(&now);`|
|`difftime()`|Tính khoảng cách thời gian|`difftime(t2, t1);`|
|`strftime()`|Định dạng thời gian|`strftime(buf, 100, "%H:%M", tm);`|

---

## ✅ `<stdbool.h>` – Kiểu boolean (chuẩn từ C99)

|Thành phần|Mô tả|
|---|---|
|`bool`|Kiểu logic|
|`true`|Giá trị đúng|
|`false`|Giá trị sai|

**Ví dụ:**

```c
#include <stdbool.h>
bool isEven = true;
if (isEven) printf("Chẵn");
```

---

## 📏 `<limits.h>` và `<float.h>` – Giới hạn kiểu dữ liệu

|Macro|Ý nghĩa|
|---|---|
|`INT_MAX`, `INT_MIN`|Giới hạn int|
|`LONG_MAX`, `LONG_MIN`|Giới hạn long|
|`FLT_MAX`, `FLT_MIN`|Giới hạn float|
|`DBL_MAX`, `DBL_MIN`|Giới hạn double|

**Ví dụ:**

```c
#include <limits.h>
#include <float.h>
printf("%d\n", INT_MAX);
printf("%f\n", FLT_MIN);
```

---

## 🧩 Một số thư viện khác hữu ích

|Thư viện|Mô tả|
|---|---|
|`<errno.h>`|Xử lý mã lỗi toàn cục|
|`<assert.h>`|Kiểm tra điều kiện khi debug (`assert()`)|
|`<stdarg.h>`|Xử lý hàm có số tham số không cố định|
|`<stddef.h>`|Định nghĩa kiểu `size_t`, `NULL`, `offsetof()`|

---
