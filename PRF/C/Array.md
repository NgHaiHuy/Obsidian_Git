
---

# 🔰 **1. Khái niệm chung về mảng trong C**

- **Mảng** là tập hợp các phần tử **cùng kiểu dữ liệu**, được lưu **liên tiếp trong bộ nhớ**.
    
- Mỗi phần tử có thể được truy cập thông qua **chỉ số (index)**, bắt đầu từ `0`.
    

---

# 🧱 **2. Khai báo và khởi tạo mảng**

## ➤ **Mảng một chiều:**

```c
int arr[5];                      // Khai báo mảng 5 phần tử kiểu int
int a[] = {1, 2, 3};             // Compiler tự tính kích thước
int b[5] = {1, 2};               // Các phần tử còn lại sẽ là 0
```

## ➤ **Mảng hai chiều:**

```c
int matrix[3][4];                // Ma trận 3 hàng, 4 cột
int m[2][3] = {{1,2,3},{4,5,6}}; // Khởi tạo cụ thể
```

## ➤ **Mảng nhiều chiều:**

```c
int arr[2][3][4];                // Mảng 3 chiều
```

---

# 🔁 **3. Truy cập và duyệt mảng**

```c
for (int i = 0; i < 5; i++) {
    printf("%d\n", arr[i]);
}
```

Mảng 2 chiều:

```c
for (int i = 0; i < 3; i++)
    for (int j = 0; j < 4; j++)
        printf("%d ", matrix[i][j]);
```

---

# 🔍 **4. Mảng và con trỏ**

- Tên mảng là **con trỏ hằng** trỏ tới phần tử đầu tiên:
    

```c
int arr[5] = {1,2,3,4,5};
int *p = arr;            // tương đương với &arr[0]
```

- Có thể truy cập qua con trỏ:
    

```c
printf("%d", *(p + 2));  // → 3
```

## ❗ So sánh con trỏ và mảng:

|Tính chất|Mảng|Con trỏ|
|---|---|---|
|Bộ nhớ|Cấp phát tĩnh|Có thể động hoặc tĩnh|
|Gán con trỏ mới|❌ Không được|✅ Được (`p = q`)|
|`sizeof`|Tổng kích thước mảng|Kích thước con trỏ|

---

# 📤 **5. Truyền mảng vào hàm**

## Một chiều:

```c
void process(int arr[], int size);  // hoặc int *arr
```

- Mảng luôn được truyền theo dạng địa chỉ → **tham chiếu**.
    

## Hai chiều:

```c
void print(int arr[][3], int rows); // PHẢI biết số cột
```

---

# 📦 **6. Mảng ký tự và chuỗi**

```c
char str[] = "Hello";       // tự động thêm '\0'
char str2[6] = {'H','e','l','l','o','\0'}; // tương đương
```

- Có thể dùng hàm trong `<string.h>`: `strlen`, `strcpy`, `strcmp`, ...
    

---

# 🧮 **7. Mảng động với malloc**

## Một chiều:

```c
int *arr = malloc(n * sizeof(int));
arr[0] = 100;
free(arr);
```

## Hai chiều:

```c
int **arr = malloc(rows * sizeof(int*));
for (int i = 0; i < rows; i++)
    arr[i] = malloc(cols * sizeof(int));
// Sử dụng: arr[i][j]
// Đừng quên free từng hàng và rồi free(arr)
```

---

# 🔧 **8. Một số thao tác phổ biến**

|Thao tác|Cách thực hiện|
|---|---|
|**Sao chép mảng**|`memcpy(dest, src, n * sizeof(int));`|
|**So sánh mảng**|`memcmp(arr1, arr2, n * sizeof(int));`|
|**Khởi tạo 0**|`memset(arr, 0, sizeof(arr));`|
|**Tìm kiếm**|Dùng vòng lặp for hoặc các thuật toán tìm|
|**Sắp xếp**|Bubble Sort, Quick Sort, v.v.|

---

# 🧠 **9. Cơ chế hoạt động của mảng trong bộ nhớ**

Ví dụ: `int arr[5] = {1,2,3,4,5};` → mỗi phần tử chiếm 4 byte (giả sử hệ 32-bit)

```
Giả sử bắt đầu từ 0x1000:
arr[0] → 0x1000
arr[1] → 0x1004
arr[2] → 0x1008
...
```

---

# ⚠️ **10. Lỗi phổ biến khi dùng mảng**

|Lỗi|Mô tả|
|---|---|
|Truy cập ngoài phạm vi|Dẫn đến lỗi hoặc crash|
|Gán trực tiếp giữa hai mảng|`a = b;` là **sai**|
|Quên giải phóng mảng động|Rò rỉ bộ nhớ (`memory leak`)|
|Nhầm giữa con trỏ và mảng|`*arr` không bằng `arr[]` trong mọi trường hợp|

---

# ✅ **11. Tổng kết**

|Tình huống|Nên dùng|
|---|---|
|Kích thước cố định|Mảng tĩnh (`int a[100];`)|
|Kích thước linh hoạt|Cấp phát động với `malloc`|
|Chuỗi ký tự|`char str[]` hoặc `char *str`|
|Truyền cho hàm|Dùng `int *arr`, luôn truyền thêm `size`|

---
