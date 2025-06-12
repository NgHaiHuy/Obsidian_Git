
---

## 🗂️ **1. Khái niệm cơ bản về File trong C**

Trong C, file là cách để **đọc/ghi dữ liệu từ/đến bộ nhớ ngoài (như ổ cứng)**. C sử dụng con trỏ kiểu `FILE *` để thao tác với tệp.

```c
FILE *fp;
```

---

## 📂 **2. Mở và đóng file: `fopen`, `fclose`**

### 📌 `FILE *fopen(const char *filename, const char *mode);`

|Chế độ|Ý nghĩa|
|---|---|
|`"r"`|Mở file để đọc. File phải tồn tại.|
|`"w"`|Mở file để ghi. Nếu file tồn tại, xóa trắng; nếu không, tạo mới.|
|`"a"`|Mở file để ghi nối vào cuối. Nếu không tồn tại, tạo mới.|
|`"r+"`|Đọc/ghi. File phải tồn tại.|
|`"w+"`|Đọc/ghi. Tạo mới hoặc xóa trắng file cũ.|
|`"a+"`|Đọc/ghi. Ghi nối vào cuối file.|

### ✅ Ví dụ:

```c
FILE *fp = fopen("data.txt", "r");
if (fp == NULL) {
    printf("Không mở được file!\n");
}
```

---

### 🔚 `int fclose(FILE *stream);`

- Đóng file đang mở. **Luôn nên gọi `fclose()`** sau khi làm việc với file.
    

```c
fclose(fp);
```

---

## 🔍 **3. Đọc file**

### ✅ `int fgetc(FILE *stream);`

- Đọc **1 ký tự** từ file.
    
- Trả về `EOF` nếu hết file hoặc lỗi.
    

```c
int ch;
while ((ch = fgetc(fp)) != EOF) {
    putchar(ch);
}
```

---

### ✅ `char *fgets(char *str, int n, FILE *stream);`

- Đọc **1 dòng** (tối đa `n-1` ký tự) từ file.
    
- Kết thúc bằng `\n` hoặc EOF.
    

```c
char line[100];
while (fgets(line, sizeof(line), fp)) {
    printf("%s", line);
}
```

---

### ✅ `size_t fread(void *ptr, size_t size, size_t count, FILE *stream);`

- Đọc **nhiều khối dữ liệu nhị phân** từ file.
    

```c
char buffer[10];
fread(buffer, sizeof(char), 10, fp);
```

---

## ✍️ **4. Ghi vào file**

### ✅ `int fputc(int char, FILE *stream);`

- Ghi 1 ký tự vào file.
    

```c
fputc('A', fp);
```

---

### ✅ `int fprintf(FILE *stream, const char *format, ...)`

- Ghi dữ liệu định dạng giống như `printf` vào file.
    

```c
fprintf(fp, "Name: %s, Age: %d\n", name, age);
```

---

### ✅ `size_t fwrite(const void *ptr, size_t size, size_t count, FILE *stream);`

- Ghi **dữ liệu nhị phân** vào file.
    

```c
fwrite(buffer, sizeof(char), strlen(buffer), fp);
```

---

## 🔁 **5. Kiểm tra kết thúc file & lỗi**

### ✅ `int feof(FILE *stream);`

- Trả về **true (khác 0)** nếu đã đọc đến cuối file (EOF).
    

```c
while (!feof(fp)) {
    ch = fgetc(fp);
    putchar(ch);
}
```

> ⚠️ `feof()` chỉ nên dùng **sau khi lệnh đọc thất bại**, không nên dùng làm điều kiện lặp trực tiếp!

---

### ✅ `int ferror(FILE *stream);`

- Trả về **true nếu có lỗi** khi thao tác với file.
    

```c
if (ferror(fp)) {
    printf("Lỗi khi đọc file!\n");
}
```

---

## ⚠️ **6. Hằng số đặc biệt: `EOF`**

- `EOF` = **End Of File**, thường là `-1`.
    
- Dùng để biết **đã kết thúc khi đọc**, ví dụ với `fgetc()`.
    

```c
int ch;
while ((ch = fgetc(fp)) != EOF) {
    // xử lý ch
}
```

---

## 🧪 **7. Tổng hợp ví dụ đọc từng dòng từ file:**

```c
#include <stdio.h>

int main() {
    FILE *fp = fopen("data.txt", "r");
    char line[100];

    if (fp == NULL) {
        printf("Không mở được file!\n");
        return 1;
    }

    while (fgets(line, sizeof(line), fp)) {
        printf("%s", line);
    }

    fclose(fp);
    return 0;
}
```

---

## 🧰 **8. Các hàm file khác hữu ích**

|Hàm|Mô tả|
|---|---|
|`rewind(fp)`|Đưa con trỏ file về đầu.|
|`fseek(fp, offset, origin)`|Di chuyển con trỏ file.|
|`ftell(fp)`|Lấy vị trí hiện tại của con trỏ file.|
|`remove("file.txt")`|Xóa file.|
|`rename("old.txt", "new.txt")`|Đổi tên file.|

---

## 🧠 **Ghi nhớ:**

- Luôn kiểm tra `NULL` khi mở file.
    
- Luôn `fclose()` sau khi dùng.
    
- Không đọc quá giới hạn file (dùng `feof`, `ferror`).
    
- Dùng đúng kiểu hàm: `fgets` cho chuỗi, `fread` cho nhị phân...