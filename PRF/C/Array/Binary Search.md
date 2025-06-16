Dưới đây là **toàn bộ thông tin đầy đủ về thuật toán Binary Search (Tìm kiếm nhị phân)** – từ định nghĩa, điều kiện sử dụng, cách hoạt động, ví dụ minh họa, code thực tế, đến các biến thể:

---

## 📘 1. Binary Search là gì?

**Binary Search** là thuật toán **tìm kiếm phần tử trong một mảng đã sắp xếp** bằng cách:

- So sánh phần tử ở giữa với giá trị cần tìm
    
- Rút gọn phạm vi tìm kiếm còn một nửa mỗi lần lặp lại
    

---

## ⚙️ 2. Điều kiện sử dụng

- **Mảng hoặc danh sách phải được sắp xếp trước** (tăng dần hoặc giảm dần).
    
- Không dùng được nếu mảng chưa sắp xếp.
    

---

## ⏱️ 3. Độ phức tạp

|Trường hợp|Độ phức tạp|
|---|---|
|Tốt nhất (Best case)|O(1) — tìm thấy ngay ở giữa|
|Trung bình / Tệ nhất|**O(log n)**|
|Bộ nhớ|O(1) (phiên bản lặp) hoặc O(log n) (đệ quy do ngăn xếp gọi hàm)|

---

## 🔄 4. Cách hoạt động của thuật toán

### Bước 1:

Xác định 2 vị trí:

- `left` (bắt đầu mảng)
    
- `right` (kết thúc mảng)
    

### Bước 2:

Tính vị trí giữa:

```c
int mid = (left + right) / 2;
```

### Bước 3:

- Nếu `arr[mid] == target` → ✅ Tìm thấy → Trả về vị trí `mid`
    
- Nếu `arr[mid] < target` → Tìm **nửa bên phải** → `left = mid + 1`
    
- Nếu `arr[mid] > target` → Tìm **nửa bên trái** → `right = mid - 1`
    

### Bước 4:

Lặp lại bước 2-3 cho đến khi tìm thấy hoặc `left > right`.

---

## 🧮 5. Ví dụ minh họa

Tìm `10` trong mảng `{2, 4, 6, 8, 10, 12, 14}`:

- `left = 0`, `right = 6`
    
- `mid = 3` → `arr[3] = 8` → 10 > 8 → tìm bên phải
    
- `left = 4`, `right = 6`
    
- `mid = 5` → `arr[5] = 12` → 10 < 12 → tìm bên trái
    
- `left = 4`, `right = 4`
    
- `mid = 4` → `arr[4] = 10` → ✅ tìm thấy tại vị trí 4
    

---

## 💻 6. Code C: **Dạng lặp**

```c
#include <stdio.h>

int binarySearch(int arr[], int n, int target) {
    int left = 0, right = n - 1;

    while (left <= right) {
        int mid = (left + right) / 2;

        if (arr[mid] == target)
            return mid;
        else if (arr[mid] < target)
            left = mid + 1;
        else
            right = mid - 1;
    }

    return -1;
}

int main() {
    int arr[] = {2, 4, 6, 8, 10, 12, 14};
    int n = sizeof(arr) / sizeof(arr[0]);
    int target = 10;

    int result = binarySearch(arr, n, target);
    if (result != -1)
        printf("Tim thay %d tai vi tri %d\n", target, result);
    else
        printf("Khong tim thay %d\n", target);

    return 0;
}
```

---

## 🔁 7. Code C: **Dạng đệ quy**

```c
int binarySearchRecursive(int arr[], int left, int right, int target) {
    if (left > right)
        return -1;

    int mid = (left + right) / 2;

    if (arr[mid] == target)
        return mid;
    else if (arr[mid] < target)
        return binarySearchRecursive(arr, mid + 1, right, target);
    else
        return binarySearchRecursive(arr, left, mid - 1, target);
}
```

---

## 🔄 8. Biến thể của Binary Search

- **Tìm vị trí xuất hiện đầu tiên / cuối cùng** của phần tử trùng lặp
    
- **Tìm vị trí chèn** (dành cho các cấu trúc như set, map)
    
- **Tìm mốc (boundaries)**: Ví dụ phần tử đầu tiên lớn hơn hoặc bằng `x`
    
- **Tìm nghiệm trong khoảng (dạng bài toán nhị phân hóa đáp án)**
    

---

## 🧠 9. Khi nào không nên dùng Binary Search?

- Dữ liệu không sắp xếp
    
- Dữ liệu thay đổi liên tục (phải sắp xếp lại sau mỗi thay đổi)
    

---

## 📌 10. Tổng kết

|Thuật toán|Binary Search|
|---|---|
|Tác dụng|Tìm kiếm nhanh trong mảng sắp xếp|
|Độ phức tạp|O(log n)|
|Loại|Thuật toán chia để trị|
|Dạng|Lặp hoặc đệ quy|
|Yêu cầu|Mảng **phải sắp xếp**|

---