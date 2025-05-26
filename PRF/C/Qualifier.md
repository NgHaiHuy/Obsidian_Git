Trong C, **qualifier** là các **từ khóa bổ sung** được dùng để **mô tả cách biến hoặc dữ liệu được truy cập, lưu trữ hoặc sửa đổi**. Chúng không tạo ra biến mới, nhưng **giới hạn hoặc mở rộng quyền sử dụng biến đó**.

---

## ✅ Các loại **qualifier** phổ biến trong C:

|Qualifier|Ý nghĩa chính|
|---|---|
|`const`|Không cho phép thay đổi giá trị biến|
|`volatile`|Báo cho trình biên dịch rằng giá trị có thể thay đổi bất ngờ|
|`restrict`|Gợi ý tối ưu hóa con trỏ (C99 trở lên)|
|`static`|Điều khiển phạm vi và thời gian sống của biến|
|`extern`|Dùng để khai báo biến toàn cục được định nghĩa ở nơi khác|

---

## 🔍 Chi tiết từng qualifier

---

### 1. `const`

- Dùng để khai báo một **hằng số** – không thể thay đổi sau khi gán.
    

```c
const int x = 5;
x = 10;  // ❌ Error: không thể gán lại giá trị cho x
```

---

### 2. `volatile`

- Cho trình biên dịch biết **không được tối ưu hóa biến này**, vì nó có thể **thay đổi bất ngờ** từ bên ngoài chương trình (ví dụ: qua hardware, thread, interrupt).
    

```c
volatile int flag;  // Có thể bị thay đổi bởi phần cứng
```

---

### 3. `restrict` (C99+)

- Dùng với con trỏ, báo rằng **chỉ con trỏ này trỏ tới vùng nhớ đó**, giúp trình biên dịch tối ưu hiệu năng.
    

```c
void add(int * restrict a, int * restrict b);
```

- ⚠️ Dành cho lập trình hiệu năng cao; dùng sai có thể gây lỗi logic.
    

---

### 4. `static`

- Dùng để:
    
    - Trong hàm: biến **giữ giá trị giữa các lần gọi**.
        
    - Ngoài hàm: giới hạn biến/hàm **chỉ dùng trong file đó** (giống private).
        

```c
static int counter = 0;  // Lưu giá trị giữa các lần gọi

static void helper() {}  // Hàm chỉ dùng trong file này
```

---

### 5. `extern`

- Dùng để **khai báo biến toàn cục**, **được định nghĩa ở nơi khác** (thường dùng giữa `.h` và `.c`).
    

```c
extern int count;  // Khai báo
```

---

## 🧠 Tóm tắt cách dùng

|Mục tiêu|Dùng qualifier nào|
|---|---|
|Không cho phép sửa giá trị|`const`|
|Biến có thể thay đổi bất ngờ|`volatile`|
|Tối ưu hóa truy cập con trỏ|`restrict` (C99)|
|Biến dùng nội bộ hoặc giữ giá trị|`static`|
|Khai báo biến ở nơi khác|`extern`|

---

    
