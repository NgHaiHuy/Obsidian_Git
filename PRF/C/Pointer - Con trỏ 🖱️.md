
---

## 📌 1. **Con trỏ là gì?**

Con trỏ là biến dùng để lưu **địa chỉ bộ nhớ** của một biến khác.

```c
int x = 10;
int *ptr = &x;
```

- `x`: biến bình thường chứa giá trị `10`.
    
- `&x`: địa chỉ của `x`.
    
- `ptr`: biến con trỏ trỏ tới `x`.
    
- `*ptr`: giá trị tại địa chỉ mà `ptr` trỏ tới (chính là `10`).
    

---

## 📌 2. **Khai báo và khởi tạo con trỏ**

```c
int *p;        // con trỏ tới int
char *c;       // con trỏ tới char
float *f = NULL; // khởi tạo bằng NULL để tránh lỗi
```

---

## 📌 3. **Toán tử liên quan đến con trỏ**

|Toán tử|Ý nghĩa|Ví dụ|
|---|---|---|
|`*`|Truy cập giá trị tại địa chỉ (dereference)|`*ptr = 5;`|
|`&`|Lấy địa chỉ của biến|`&a`|

---

## 📌 4. **Ví dụ cơ bản**

```c
#include <stdio.h>

int main() {
    int x = 5;
    int *ptr = &x;

    printf("Giá trị x: %d\n", x);
    printf("Địa chỉ x: %p\n", &x);
    printf("Giá trị ptr: %p\n", ptr);
    printf("Giá trị tại ptr: %d\n", *ptr);

    return 0;
}
```

---

## 📌 5. **Truyền con trỏ vào hàm (truyền tham chiếu)**

```c
void tangGiaTri(int *n) {
    (*n)++;
}

int main() {
    int a = 10;
    tangGiaTri(&a);
    printf("%d\n", a); // 11
}
```

---

## 📌 6. **Con trỏ và mảng**

Mảng thực chất là con trỏ trỏ đến phần tử đầu tiên.

```c
int a[3] = {1, 2, 3};
int *p = a;

printf("%d\n", *(p + 1)); // 2
```

Bạn có thể duyệt mảng bằng con trỏ:

```c
for (int i = 0; i < 3; i++) {
    printf("%d ", *(p + i));
}
```

---

## 📌 7. **Con trỏ và chuỗi**

```c
char *str = "Hello";
printf("%c\n", *(str + 1)); // 'e'
```

---

## 📌 8. **Cấp phát bộ nhớ động (malloc, free)**

```c
#include <stdlib.h>

int *arr = malloc(5 * sizeof(int));
arr[0] = 10;
// ...
free(arr); // Giải phóng bộ nhớ
```

---

## 📌 9. **Con trỏ tới con trỏ (double pointer)**

```c
int x = 5;
int *p = &x;
int **pp = &p;

printf("%d\n", **pp); // 5
```

---

## 📌 10. **Con trỏ tới hàm**

```c
void hello() {
    printf("Xin chào!\n");
}

int main() {
    void (*func_ptr)() = hello;
    func_ptr(); // Gọi hàm thông qua con trỏ
}
```

---

## 📌 11. **Con trỏ trong cấu trúc dữ liệu**

Dùng con trỏ để tạo:

- Danh sách liên kết (linked list)
    
- Cây nhị phân (binary tree)
    
- Stack, queue,...
    

🔍 Ví dụ node đơn giản:

```c
struct Node {
    int data;
    struct Node *next;
};
```

---

## 📌 12. **Lỗi thường gặp với con trỏ**

|Lỗi|Nguyên nhân|
|---|---|
|Dùng con trỏ chưa khởi tạo|`int *p; *p = 5;` → chưa có địa chỉ|
|Truy cập con trỏ NULL|`int *p = NULL; *p = 1;` → lỗi|
|Quên giải phóng `malloc`|Dẫn đến rò rỉ bộ nhớ|

---

## ✅ Tổng kết

| Tính năng của con trỏ               | Lợi ích                           |
| ----------------------------------- | --------------------------------- |
| Truy cập biến qua địa chỉ           | Truyền tham chiếu vào hàm         |
| Duyệt mảng/chuỗi hiệu quả           | Tối ưu xử lý dữ liệu              |
| Cấp phát bộ nhớ động                | Quản lý bộ nhớ linh hoạt          |
| Xây dựng cấu trúc dữ liệu linh hoạt | Linked list, tree, graph...       |
| Gọi hàm qua con trỏ                 | Lập trình động (function pointer) |

---