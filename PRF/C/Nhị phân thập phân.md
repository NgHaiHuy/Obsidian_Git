
---

## 🧠 Số nhị phân là gì?

- Là **số chỉ gồm số 0 và 1**.
    
- Mỗi chữ số gọi là **bit**.
    
- Ví dụ: `1011`, `110`, `10001` là số nhị phân.
    

---

## 🎯 Mục tiêu: Đổi số nhị phân sang thập phân

### Bước 1️⃣: Ghi vị trí của từng số từ **phải sang trái**, bắt đầu từ **0**

Ví dụ: `1011`

|Vị trí|Số nhị phân|
|---|---|
|3|1|
|2|0|
|1|1|
|0|1|

---

### Bước 2️⃣: Mỗi số nhân với **2 mũ vị trí**

```
1 × 2³ = 8  
0 × 2² = 0  
1 × 2¹ = 2  
1 × 2⁰ = 1  
```

---

### Bước 3️⃣: Cộng lại kết quả

```
8 + 0 + 2 + 1 = 11
```

✅ Vậy: `1011` trong hệ nhị phân = **11 trong hệ thập phân**

---

## 💡 Mẹo nhớ:

|Nhị phân|Thập phân|
|---|---|
|0001|1|
|0010|2|
|0100|4|
|1000|8|

Cứ **thêm một số 0** thì giá trị nhân **gấp đôi**.

---

## 🎯 Còn nếu muốn đổi **thập phân → nhị phân**?

### Ví dụ: Đổi `13` sang nhị phân

👉 Làm như sau:

1. 13 chia 2 → được 6 dư **1**
    
2. 6 chia 2 → được 3 dư **0**
    
3. 3 chia 2 → được 1 dư **1**
    
4. 1 chia 2 → được 0 dư **1**
    

👉 Viết ngược các số dư lại: **1101**

✅ Vậy: `13` → `1101` trong nhị phân

---

## 🎮 Tóm gọn:

- **Đổi nhị phân → thập phân**: lấy từng số × 2^vị trí, rồi cộng.
    
- **Đổi thập phân → nhị phân**: chia 2 liên tục, lấy dư, viết ngược lại.
    

---

Nếu bạn muốn mình **giải giúp 1 số cụ thể**, bạn chỉ cần gửi số đó (nhị phân hoặc thập phân), mình sẽ làm giúp bạn luôn!