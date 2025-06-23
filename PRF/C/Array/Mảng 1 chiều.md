
---

## 🧠 1. **Khái niệm mảng một chiều**

Mảng một chiều là **tập hợp các phần tử cùng kiểu dữ liệu**, được lưu trữ **liên tiếp trong bộ nhớ** và truy cập bằng **chỉ số (index)** bắt đầu từ 0.

---

## 🧱 2. **Khai báo mảng**

```c
<data_type> array_name[size];
```

### Ví dụ:

```c
int a[5];         // Mảng chứa 5 số nguyên
float b[10];      // Mảng chứa 10 số thực
char name[20];    // Mảng ký tự (chuỗi)
```

---

## 🧪 3. **Khởi tạo mảng**

### Cách 1: Khai báo và khởi tạo cùng lúc

```c
int a[5] = {1, 2, 3, 4, 5};
```

### Cách 2: Không cần khai báo kích thước khi khởi tạo

```c
int a[] = {1, 2, 3}; // tự động xác định size = 3
```

### Cách 3: Khởi tạo một phần tử

```c
int a[5] = {1, 2}; // a = {1, 2, 0, 0, 0}
```

---

## 🔁 4. **Nhập và xuất mảng**

```c
int n, a[100];
scanf("%d", &n);              // nhập số phần tử

for(int i = 0; i < n; i++)    // nhập mảng
    scanf("%d", &a[i]);

for(int i = 0; i < n; i++)    // xuất mảng
    printf("%d ", a[i]);
```

---

## 🔎 5. **Truy cập phần tử**

```c
a[0] = 10;         // Gán giá trị cho phần tử đầu tiên
printf("%d", a[2]); // In phần tử thứ 3
```

---

## 🔧 6. **Một số thao tác phổ biến**

|Thao tác|Gợi ý cách làm|
|---|---|
|Tổng các phần tử|Dùng vòng lặp và biến tổng|
|Tìm max, min|Dùng biến `max`, `min` để so sánh từng phần tử|
|Đếm phần tử chẵn/lẻ|Dùng `if (a[i] % 2 == 0)`|
|Đảo ngược mảng|Hoán đổi `a[i]` và `a[n - i - 1]`|
|Sắp xếp tăng/giảm|Sử dụng thuật toán như Bubble Sort|
|Tìm kiếm giá trị|Duyệt mảng và so sánh từng phần tử|

---

## 🧠 7. **Ví dụ cụ thể**

### a. Tổng các phần tử

```c
int sum = 0;
for (int i = 0; i < n; i++)
    sum += a[i];
printf("Tong = %d", sum);
```

### b. Tìm phần tử lớn nhất

```c
int max = a[0];
for (int i = 1; i < n; i++)
    if (a[i] > max)
        max = a[i];
```

---

## 📌 8. **Giới hạn mảng**

- Không thể thay đổi kích thước mảng sau khi khai báo.
    
- Truy cập ngoài chỉ số `[0, size-1]` gây **lỗi tràn bộ nhớ (undefined behavior)**.
    

---

## 🎯 9. **Truyền mảng vào hàm**

```c
void inMang(int a[], int n) {
    for (int i = 0; i < n; i++)
        printf("%d ", a[i]);
}
```

Gọi hàm:

```c
inMang(a, n);
```

---

## 🧮 10. **Các bài toán luyện tập**

1. Nhập mảng và in ra các phần tử.
    
2. Tính tổng các phần tử.
    
3. Tìm phần tử lớn nhất/nhỏ nhất.
    
4. Đếm số chẵn/lẻ.
    
5. Kiểm tra mảng có tăng dần không.
    
6. Đảo ngược mảng.
    
7. Sắp xếp mảng tăng dần.
    
8. Tìm số xuất hiện nhiều nhất.
    
9. Xóa phần tử tại vị trí `k`.
    
10. Chèn phần tử vào vị trí `k`.
    

---
