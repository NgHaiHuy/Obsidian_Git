Trong C, bạn **không thể tạo mảng có kích thước thay đổi sau khi khai báo** nếu dùng kiểu mảng tĩnh truyền thống như:

```c
int arr[100];  // kích thước cố định
```

Tuy nhiên, bạn có thể chọn **một trong hai cách sau** để xác định độ dài mảng **dựa vào giá trị nhập vào từ người dùng**:

---

## ✅ **Cách 1: Dùng mảng động với `malloc` (chuẩn và linh hoạt)**

### ▶️ Ví dụ:

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n;
    printf("Nhap so phan tu cua mang: ");
    scanf("%d", &n);

    // Cấp phát mảng động
    int *arr = (int *)malloc(n * sizeof(int));

    if (arr == NULL) {
        printf("Khong the cap phat bo nho!\n");
        return 1;
    }

    // Nhập giá trị cho mảng
    for (int i = 0; i < n; i++) {
        printf("arr[%d] = ", i);
        scanf("%d", &arr[i]);
    }

    // In mảng
    printf("Mang vua nhap: ");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }

    // Giải phóng bộ nhớ
    free(arr);

    return 0;
}
```

✅ **Ưu điểm:** Dễ mở rộng, không giới hạn kích thước  
⚠️ **Nhược điểm:** Cần hiểu về con trỏ và cấp phát bộ nhớ động

---

## ✅ **Cách 2: Dùng Variable Length Array (VLA – mảng có độ dài biến đổi)**

Áp dụng được nếu bạn dùng chuẩn C99 hoặc mới hơn.

### ▶️ Ví dụ:

```c
#include <stdio.h>

int main() {
    int n;
    printf("Nhap so phan tu cua mang: ");
    scanf("%d", &n);

    int arr[n];  // VLA - mảng độ dài do người dùng nhập

    // Nhập mảng
    for (int i = 0; i < n; i++) {
        printf("arr[%d] = ", i);
        scanf("%d", &arr[i]);
    }

    // In mảng
    printf("Mang vua nhap: ");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }

    return 0;
}
```

✅ **Ưu điểm:** Đơn giản, không cần con trỏ  
⚠️ **Nhược điểm:** Không tương thích với tất cả trình biên dịch cũ (C89 không hỗ trợ)

---

### 🔍 Khi nào dùng cách nào?

|Tình huống|Nên dùng cách|
|---|---|
|Bạn học cơ bản, dùng GCC hoặc Clang|Cách 2 (VLA)|
|Cần cấp phát lớn, mềm dẻo hơn|Cách 1 (malloc)|

---

Bạn muốn mình hướng dẫn cách viết hàm nhập mảng & tính tổng/giá trị lớn nhất từ đầu vào không?