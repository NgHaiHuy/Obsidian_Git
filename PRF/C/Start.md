

---

## 🔰 Giai đoạn 1: Làm quen với C (Tương đương JS cơ bản)

### 🧱 1. Cấu trúc chương trình C

```c
#include <stdio.h>

int main() {
    printf("Hello, world!\n");
    return 0;
}
```

- `#include <stdio.h>`: dùng để nhập thư viện I/O
    
- `main()`: hàm chính bắt buộc
    
- `printf()`: tương tự `console.log()`
    

👉 **So sánh JS:**

```javascript
console.log("Hello, world!");
```

---

### 🧮 2. Kiểu dữ liệu và biến

- `int`, `float`, `double`, `char`
    
- Khai báo bắt buộc phải rõ ràng:
    

```c
int age = 25;
float weight = 70.5;
char grade = 'A';
```

👉 Trong JS bạn có `let x = 5`, còn C phải là `int x = 5;`

---

### 🔁 3. Câu lệnh điều kiện và vòng lặp

- Tương tự JavaScript về cú pháp:
    

```c
if (age > 18) {
    printf("Adult");
} else {
    printf("Minor");
}

for (int i = 0; i < 5; i++) {
    printf("%d\n", i);
}
```

👉 Gần giống JS, nhưng lưu ý là không có `let`, `var`, `const`.

---

## ⚙️ Giai đoạn 2: Đi sâu vào C (Cấu trúc dữ liệu và con trỏ)

### 📦 4. Mảng và chuỗi

```c
int nums[5] = {1, 2, 3, 4, 5};
char name[] = "John"; // giống như mảng char: {'J','o','h','n','\0'}
```

- Không có kiểu `string` như trong JS.
    
- Xử lý chuỗi dùng thư viện `<string.h>`: `strcpy`, `strlen`, `strcmp`, ...
    

---

### 🧠 5. Hàm

```c
int sum(int a, int b) {
    return a + b;
}
```

- Trong JS bạn viết `function sum(a, b) { return a + b; }`
    
- Trong C: phải khai báo kiểu trả về và kiểu tham số
    

---

### 🧭 6. Con trỏ (quan trọng nhất trong C)

```c
int x = 10;
int *p = &x;
printf("%d", *p); // in ra 10
```

- `*` là toán tử giải tham chiếu (dereference)
    
- `&` là lấy địa chỉ của biến
    
- JS không có khái niệm con trỏ ⇒ bạn sẽ cần luyện kỹ
    

---

### 🧱 7. Cấp phát động bộ nhớ

```c
int *arr = (int *)malloc(5 * sizeof(int));
arr[0] = 10;
free(arr); // tránh rò rỉ bộ nhớ
```

- C tương đương JS dùng mảng động nhưng phải quản lý bộ nhớ thủ công
    

---

## 🧰 Giai đoạn 3: Kỹ thuật nâng cao

### 📂 8. Struct – giống như object trong JS

```c
struct Person {
    char name[50];
    int age;
};

struct Person p1 = {"Alice", 25};
```

---

### 📁 9. Quản lý file

```c
FILE *f = fopen("data.txt", "r");
char line[100];
fgets(line, 100, f);
fclose(f);
```

- Trong JS có thể dùng `fs` module hoặc Web API để xử lý file
    

---

### 🧪 10. Tự làm các bài tập JS quen thuộc bằng C:

|Bài tập JS quen thuộc|Viết lại bằng C|
|---|---|
|In bảng cửu chương|Sử dụng `for` và `printf`|
|Tính tổng 1..n|Hàm `int sumTo(int n)`|
|Kiểm tra số nguyên tố|Dùng `for` và `if`|
|Viết máy tính đơn giản|Dùng `switch-case`|
|Xử lý chuỗi|Dùng mảng `char[]` và `string.h`|

---

## 📘 Tài nguyên cụ thể

### Khóa học tương tác:

- [Learn-C.org](https://www.learn-c.org/)
    
- [CS50x – Harvard](https://cs50.harvard.edu/x/)
    

### Video tiếng Việt:

- [Lập trình C cơ bản - Kteam](https://www.youtube.com/playlist?list=PL33lvabfss1z4hYmn_Fk4VZ4F7r0EXzhl)
    
- [HowKteam – học C](https://www.howkteam.vn/course/ngon-ngu-lap-trinh-c-28)
    

### Sách đề xuất:

- _The C Programming Language_ – K&R (rất nên đọc nếu muốn học nghiêm túc)
    
- _Head First C_ – học theo kiểu dễ hiểu, có hình ảnh
    

---

## 📌 Gợi ý luyện tập từng bước

|Giai đoạn|Chủ đề|Bài tập gợi ý|
|---|---|---|
|Cơ bản|biến, if, vòng lặp|in số lẻ, in bảng cửu chương|
|Mảng & hàm|xử lý mảng, viết hàm|đảo ngược mảng, tìm max|
|Chuỗi|`char[]`, thao tác chuỗi|đếm ký tự, đảo chuỗi|
|Con trỏ|`*`, `&`, `malloc`|swap 2 số, truyền mảng qua con trỏ|
|Struct|đối tượng|danh sách sinh viên|
|File|lưu/trích xuất dữ liệu|đọc/ghi từ file|

---

👉 **Bạn muốn mình gửi bộ bài tập cụ thể + lời giải mẫu cho từng phần không?**  
(Mỗi bài sẽ có đề + hướng dẫn từng bước chuyển từ JS sang C nếu bạn cần)