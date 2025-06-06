

---

## 🔁 **1. Khái niệm vòng lặp**

Vòng lặp dùng để **thực hiện một khối lệnh lặp đi lặp lại** nhiều lần, đến khi một điều kiện không còn đúng.

---

## 🌀 **2. Các loại vòng lặp trong C**

|Tên vòng lặp|Khi nào dùng?|
|---|---|
|`for`|Biết số lần lặp trước|
|`while`|Không biết trước số lần lặp|
|`do...while`|Muốn chạy ít nhất một lần|

---

## ✅ **3. Vòng lặp `for`**

### 📌 Cú pháp:

```c
for (khởi tạo; điều kiện; cập nhật) {
    // khối lệnh
}
```

### 🧪 Ví dụ:

```c
for (int i = 1; i <= 5; i++) {
    printf("%d ", i);  // In ra 1 2 3 4 5
}
```

---

## ✅ **4. Vòng lặp `while`**

### 📌 Cú pháp:

```c
while (điều kiện) {
    // khối lệnh
}
```

### 🧪 Ví dụ:

```c
int i = 1;
while (i <= 5) {
    printf("%d ", i);
    i++;
}
```

---

## ✅ **5. Vòng lặp `do...while`**

### 📌 Cú pháp:

```c
do {
    // khối lệnh
} while (điều kiện);
```

### 🧪 Ví dụ:

```c
int i = 1;
do {
    printf("%d ", i);
    i++;
} while (i <= 5);
```

> Ưu điểm: **Luôn chạy ít nhất 1 lần**, dù điều kiện sai ngay từ đầu.

---

## 🚀 **6. Từ khóa trong vòng lặp**

|Từ khóa|Ý nghĩa|
|---|---|
|`break`|Thoát khỏi vòng lặp ngay lập tức|
|`continue`|Bỏ qua lần lặp hiện tại và tiếp tục vòng kế tiếp|

### 🔍 Ví dụ `break`:

```c
for (int i = 1; i <= 10; i++) {
    if (i == 5) break;
    printf("%d ", i);  // In ra 1 2 3 4
}
```

### 🔍 Ví dụ `continue`:

```c
for (int i = 1; i <= 5; i++) {
    if (i == 3) continue;
    printf("%d ", i);  // In ra 1 2 4 5
}
```

---

## ⚠️ **7. Lỗi thường gặp với vòng lặp**

|Lỗi|Ví dụ|Ghi chú|
|---|---|---|
|Vòng lặp vô hạn|`while (1) {...}`|Phải có `break` để thoát|
|Không cập nhật biến lặp|`for (int i = 0; i < 5;)`|Quên `i++`, lặp mãi|
|Điều kiện sai|`for (int i = 10; i < 5; i++)`|Không chạy lần nào|

---

## 📚 **8. Bài tập gợi ý**

1. In các số từ 1 đến 100.
    
2. Tính tổng từ 1 đến n.
    
3. In bảng cửu chương.
    
4. Đếm số lượng chữ số của một số.
    
5. In dãy Fibonacci.
    

---

## 🧠 **9. So sánh 3 loại vòng lặp**

|Đặc điểm|`for`|`while`|`do...while`|
|---|---|---|---|
|Biết số lần lặp|✅|❌|❌|
|Có thể không chạy lần nào|✅|✅|❌ (luôn chạy 1 lần)|
|Cấu trúc gọn|✅|❌|❌|

---

## ✨ **10. Mẹo dùng vòng lặp**

- Dùng `for` khi lặp theo chỉ số.
    
- Dùng `while` khi chờ một điều kiện xảy ra (vd: nhập đúng mật khẩu).
    
- Dùng `do...while` khi cần kiểm tra điều kiện **sau khi thực hiện lệnh**.