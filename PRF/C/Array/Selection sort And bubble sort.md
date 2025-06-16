Dưới đây là **tất cả thông tin chi tiết về Selection Sort và Bubble Sort**, bao gồm **khái niệm, cách hoạt động, giải thích thuật toán, độ phức tạp, ưu nhược điểm và ví dụ minh họa bằng C**.

---

## 🔷 1. **Selection Sort (Sắp xếp chọn)**

### 🧠 Khái niệm:

- Selection Sort hoạt động bằng cách **chọn phần tử nhỏ nhất (hoặc lớn nhất)** trong dãy chưa được sắp xếp và **đưa nó về đúng vị trí** trong dãy đã sắp xếp.
    

### ⚙️ Cách hoạt động:

Giả sử sắp xếp tăng dần:

1. Bắt đầu từ phần tử đầu tiên.
    
2. Tìm phần tử nhỏ nhất trong dãy chưa được sắp xếp.
    
3. Đổi chỗ nó với phần tử hiện tại.
    
4. Lặp lại với phần tử tiếp theo.
    

### 📊 Độ phức tạp:

|Trường hợp|Độ phức tạp|
|---|---|
|Tốt nhất (Best)|O(n²)|
|Trung bình (Avg)|O(n²)|
|Xấu nhất (Worst)|O(n²)|
|Bộ nhớ phụ|O(1)|
|Ổn định không?|❌ Không ổn định|

---

### 💡 Ví dụ C - Selection Sort:

```c
#include <stdio.h>

void selectionSort(int arr[], int n) {
    int i, j, min_idx, temp;

    for (i = 0; i < n - 1; i++) {
        min_idx = i;

        for (j = i + 1; j < n; j++) {
            if (arr[j] < arr[min_idx])
                min_idx = j;
        }

        // Đổi chỗ phần tử nhỏ nhất với arr[i]
        temp = arr[i];
        arr[i] = arr[min_idx];
        arr[min_idx] = temp;
    }
}

void printArray(int arr[], int n) {
    for (int i = 0; i < n; i++)
        printf("%d ", arr[i]);
}

int main() {
    int arr[] = {64, 25, 12, 22, 11};
    int n = sizeof(arr) / sizeof(arr[0]);
    selectionSort(arr, n);
    printArray(arr, n);
    return 0;
}
```

---

## 🔷 2. **Bubble Sort (Sắp xếp nổi bọt)**

### 🧠 Khái niệm:

- Bubble Sort hoạt động bằng cách **so sánh từng cặp phần tử kề nhau** và **đổi chỗ nếu sai thứ tự**. Phần tử lớn nhất sẽ "nổi" lên cuối dãy sau mỗi vòng lặp.
    

### ⚙️ Cách hoạt động:

1. So sánh từng cặp `arr[i]` và `arr[i+1]`.
    
2. Nếu `arr[i] > arr[i+1]`, thì hoán đổi.
    
3. Sau mỗi vòng lặp, phần tử lớn nhất được đưa về cuối.
    
4. Tiếp tục lặp lại cho đến khi không còn sự hoán đổi nào.
    

### 📊 Độ phức tạp:

|Trường hợp|Độ phức tạp|
|---|---|
|Tốt nhất (Best)|O(n) (nếu tối ưu)|
|Trung bình (Avg)|O(n²)|
|Xấu nhất (Worst)|O(n²)|
|Bộ nhớ phụ|O(1)|
|Ổn định không?|✅ Ổn định|

---

### 💡 Ví dụ C - Bubble Sort (đã tối ưu):

```c
#include <stdio.h>
#include <stdbool.h>

void bubbleSort(int arr[], int n) {
    bool swapped;
    for (int i = 0; i < n - 1; i++) {
        swapped = false;

        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                // Đổi chỗ
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
                swapped = true;
            }
        }

        // Nếu không có hoán đổi nào, dừng sớm
        if (!swapped)
            break;
    }
}

void printArray(int arr[], int n) {
    for (int i = 0; i < n; i++)
        printf("%d ", arr[i]);
}

int main() {
    int arr[] = {5, 1, 4, 2, 8};
    int n = sizeof(arr) / sizeof(arr[0]);
    bubbleSort(arr, n);
    printArray(arr, n);
    return 0;
}
```

---

## 🔍 So sánh Selection Sort và Bubble Sort

|Tiêu chí|Selection Sort|Bubble Sort|
|---|---|---|
|Ý tưởng chính|Chọn phần tử nhỏ nhất|Hoán đổi phần tử kề sai thứ tự|
|Độ ổn định|❌ Không ổn định|✅ Ổn định|
|Hiệu quả tốt nhất|O(n²)|✅ O(n) nếu tối ưu|
|Sử dụng|Khi thao tác ghi đè ít|Khi cần thuật toán ổn định|

---