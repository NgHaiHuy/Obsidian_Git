

---

## 🧠 1. **Khái niệm mảng nhiều chiều**

- **Mảng nhiều chiều** là mảng trong đó mỗi phần tử của nó lại là một mảng.
    
- Phổ biến nhất là **mảng hai chiều** (giống như ma trận).
    
- Mảng nhiều chiều có thể mở rộng thành 3 chiều, 4 chiều,...
    

---

## 📏 2. **Khai báo mảng nhiều chiều**

### Mảng 2 chiều:

```c
<data_type> array_name[rows][cols];
```

### Ví dụ:

```c
int a[3][4];     // Mảng 3 dòng, 4 cột (3x4)
float b[2][5];   // Mảng 2 dòng, 5 cột
char c[2][10];   // Mảng ký tự 2 dòng, mỗi dòng 10 ký tự
```

---

## 🧪 3. **Khởi tạo mảng nhiều chiều**

### Cách 1: Khai báo và khởi tạo cùng lúc

```c
int a[2][3] = {
    {1, 2, 3},
    {4, 5, 6}
};
```

### Cách 2: Dòng duy nhất

```c
int a[2][3] = {1, 2, 3, 4, 5, 6};
```

---

## 🧾 4. **Truy cập phần tử**

Cú pháp:

```c
a[i][j]   // truy cập dòng i, cột j
```

Ví dụ:

```c
a[1][2] = 10;       // gán giá trị cho phần tử dòng 1, cột 2
printf("%d", a[0][0]);
```

---

## 🔁 5. **Nhập – Xuất mảng 2 chiều**

```c
int a[100][100], m, n;
scanf("%d%d", &m, &n); // nhập số dòng và cột

// Nhập mảng
for(int i = 0; i < m; i++)
    for(int j = 0; j < n; j++)
        scanf("%d", &a[i][j]);

// Xuất mảng
for(int i = 0; i < m; i++) {
    for(int j = 0; j < n; j++)
        printf("%d ", a[i][j]);
    printf("\n");
}
```

---

## 🔧 6. **Một số thao tác phổ biến**

|Bài toán|Gợi ý cách làm|
|---|---|
|Tổng tất cả phần tử|Duyệt 2 vòng lặp|
|Tìm max, min|Tạo biến `max`, `min` để so sánh|
|Tổng từng dòng|Duyệt từng dòng, cộng theo cột|
|Tổng từng cột|Duyệt từng cột, cộng theo dòng|
|Tìm dòng có tổng lớn nhất|Tính tổng từng dòng|
|Ma trận đối xứng|So sánh `a[i][j] == a[j][i]`|
|Ma trận tam giác trên/dưới|Kiểm tra điều kiện `i < j`, `i > j`|

---

## 🧮 7. **Ví dụ cụ thể**

### a. Tổng tất cả phần tử

```c
int sum = 0;
for(int i = 0; i < m; i++)
    for(int j = 0; j < n; j++)
        sum += a[i][j];
```

### b. Tìm phần tử lớn nhất

```c
int max = a[0][0];
for(int i = 0; i < m; i++)
    for(int j = 0; j < n; j++)
        if (a[i][j] > max)
            max = a[i][j];
```

---

## 📦 8. **Truyền mảng nhiều chiều vào hàm**

### Cần chỉ rõ số cột

```c
void inMaTran(int a[][100], int m, int n) {
    for(int i = 0; i < m; i++) {
        for(int j = 0; j < n; j++)
            printf("%d ", a[i][j]);
        printf("\n");
    }
}
```

Gọi:

```c
inMaTran(a, m, n);
```

---

## 🔢 9. **Mảng 3 chiều trở lên**

### Ví dụ:

```c
int b[2][3][4]; // Mảng 3 chiều: 2 khối, 3 dòng, 4 cột

b[1][2][3] = 100;  // phần tử tại khối 1, dòng 2, cột 3
```

### Truy cập:

```c
for(int i = 0; i < 2; i++)
  for(int j = 0; j < 3; j++)
    for(int k = 0; k < 4; k++)
      printf("%d ", b[i][j][k]);
```

> ❗ Lưu ý: Mảng nhiều chiều hơn 3 rất hiếm khi dùng và dễ gây rối. Hãy cân nhắc dùng struct hoặc cấp phát động với con trỏ.

---

## 📘 10. **Bài tập luyện tập**

1. Nhập ma trận m x n và in ra.
    
2. Tính tổng từng dòng, từng cột.
    
3. Tìm dòng có tổng lớn nhất.
    
4. Kiểm tra ma trận có phải ma trận vuông.
    
5. Kiểm tra ma trận có đối xứng qua đường chéo chính.
    
6. Sắp xếp từng dòng tăng dần.
    
7. Tìm phần tử nhỏ nhất trong từng cột.
    
8. Ma trận tam giác trên/dưới.
    
9. Nhập 2 ma trận vuông A và B, tính ma trận C = A + B.
    
10. Nhân 2 ma trận.
    

---
