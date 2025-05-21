Dưới đây là **10 bài tập về mảng và vòng lặp** giúp bạn làm quen và thành thạo từ cơ bản đến nâng cao. Mỗi bài tập đều kèm ví dụ minh họa để bạn dễ hình dung.  

---

### **📌 Bài tập cơ bản**
#### **1. Tính tổng các phần tử trong mảng**  
**Yêu cầu:** Viết chương trình tính tổng các phần tử của mảng `int arr[] = {1, 2, 3, 4, 5}`.  
**Ví dụ:**  
```c
Tổng các phần tử: 15
```

#### **2. Tìm giá trị lớn nhất/nhỏ nhất trong mảng**  
**Yêu cầu:** Cho mảng `int arr[] = {10, 5, 20, 3, 15}`, tìm giá trị lớn nhất và nhỏ nhất.  
**Ví dụ:**  
```c
Max = 20, Min = 3
```

#### **3. Đếm số phần tử chẵn/lẻ trong mảng**  
**Yêu cầu:** Đếm số phần tử chẵn và lẻ trong mảng `int arr[] = {2, 7, 4, 9, 6}`.  
**Ví dụ:**  
```c
Số chẵn: 3, Số lẻ: 2
```

#### **4. In mảng theo chiều ngược lại**  
**Yêu cầu:** Cho mảng `int arr[] = {1, 2, 3, 4, 5}`, in các phần tử theo thứ tự đảo ngược.  
**Ví dụ:**  
```c
5 4 3 2 1
```

#### **5. Tính trung bình cộng các phần tử**  
**Yêu cầu:** Tính trung bình cộng của mảng `float arr[] = {1.5, 2.5, 3.5, 4.5}`.  
**Ví dụ:**  
```c
Trung bình: 3.0
```

---

### **📌 Bài tập nâng cao**
#### **6. Tìm phần tử xuất hiện nhiều nhất trong mảng**  
**Yêu cầu:** Cho mảng `int arr[] = {1, 2, 2, 3, 3, 3, 4}`, tìm phần tử xuất hiện nhiều nhất.  
**Ví dụ:**  
```c
Phần tử xuất hiện nhiều nhất: 3 (3 lần)
```

#### **7. Kiểm tra mảng có phải là mảng tăng dần không**  
**Yêu cầu:** Kiểm tra xem mảng `int arr[] = {1, 3, 5, 7, 9}` có tăng dần không.  
**Ví dụ:**  
```c
Mảng tăng dần: Có
```

#### **8. Xóa một phần tử khỏi mảng**  
**Yêu cầu:** Cho mảng `int arr[] = {10, 20, 30, 40, 50}`, xóa phần tử `30` và in mảng sau khi xóa.  
**Ví dụ:**  
```c
Mảng sau khi xóa: 10 20 40 50
```

#### **9. Gộp hai mảng thành một mảng**  
**Yêu cầu:** Cho 2 mảng `int a[] = {1, 2, 3}` và `int b[] = {4, 5, 6}`, gộp thành mảng `c` và in ra.  
**Ví dụ:**  
```c
Mảng gộp: 1 2 3 4 5 6
```

#### **10. Tìm vị trí của một phần tử trong mảng**  
**Yêu cầu:** Cho mảng `int arr[] = {5, 10, 15, 20}`, nhập một số từ bàn phím và tìm vị trí của nó trong mảng.  
**Ví dụ:**  
```c
Nhập số: 15
Vị trí: 2 (chỉ số bắt đầu từ 0)
```

---

### **📌 Gợi ý cách làm**
- Dùng **vòng lặp `for` hoặc `while`** để duyệt mảng.  
- Dùng **`if`** để kiểm tra điều kiện (chẵn/lẻ, lớn nhất/nhỏ nhất).  
- Với bài xóa/gộp mảng, cần **dịch chuyển phần tử** hoặc **tạo mảng mới**. 