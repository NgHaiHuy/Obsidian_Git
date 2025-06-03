
---

### 1. `=` (Gán)

- **Ví dụ:** `x = 5;`
    
- **Giải thích:** Gán giá trị 5 cho biến `x`.
    

---

### 2. `+=` (Cộng rồi gán)

- **Ví dụ:** `x += 3;` tương đương `x = x + 3;`
    
- **Giải thích:** Cộng 3 vào giá trị hiện tại của `x`, rồi gán lại cho `x`.
    

---

### 3. `-=` (Trừ rồi gán)

- **Ví dụ:** `x -= 3;` tương đương `x = x - 3;`
    
- **Giải thích:** Trừ 3 khỏi giá trị hiện tại của `x`, rồi gán lại cho `x`.
    

---

### 4. `*=` (Nhân rồi gán)

- **Ví dụ:** `x *= 3;` tương đương `x = x * 3;`
    
- **Giải thích:** Nhân giá trị của `x` với 3, rồi gán lại cho `x`.
    

---

### 5. `/=` (Chia rồi gán)

- **Ví dụ:** `x /= 3;` tương đương `x = x / 3;`
    
- **Giải thích:** Chia `x` cho 3 (nếu là số nguyên thì chia lấy phần nguyên), rồi gán lại cho `x`.
    

---

### 6. `%=` (Chia lấy dư rồi gán)

- **Ví dụ:** `x %= 3;` tương đương `x = x % 3;`
    
- **Giải thích:** Lấy phần dư khi `x` chia cho 3, rồi gán lại cho `x`.
    

---

### 7. `&=` (AND bit rồi gán)

- **Ví dụ:** `x &= 3;` tương đương `x = x & 3;`
    
- **Giải thích:** Thực hiện phép AND bit giữa `x` và 3, rồi gán lại cho `x`.  
    Ví dụ:  
    `x = 6` (110), `3 = 011`  
    `x & 3 = 010` → `x = 2`
    

---

### 8. `|=` (OR bit rồi gán)

- **Ví dụ:** `x |= 3;` tương đương `x = x | 3;`
    
- **Giải thích:** Thực hiện phép OR bit giữa `x` và 3, rồi gán lại cho `x`.  
    Ví dụ:  
    `x = 4` (100), `3 = 011`  
    `x | 3 = 111` → `x = 7`
    

---

### 9. `^=` (XOR bit rồi gán)

- **Ví dụ:** `x ^= 3;` tương đương `x = x ^ 3;`
    
- **Giải thích:** Thực hiện phép XOR bit giữa `x` và 3, rồi gán lại cho `x`.  
    Ví dụ:  
    `x = 6` (110), `3 = 011`  
    `x ^ 3 = 101` → `x = 5`
    

---

### 10. `>>=` (Dịch phải rồi gán)

- **Ví dụ:** `x >>= 3;` tương đương `x = x >> 3;`
    
- **Giải thích:** Dịch các bit của `x` sang phải 3 vị trí (chia cho 2^3), rồi gán lại cho `x`.  
    Ví dụ:  
    `x = 16` (10000), `x >> 3 = 00010` → `x = 2`
    

---

### 11. `<<=` (Dịch trái rồi gán)

- **Ví dụ:** `x <<= 3;` tương đương `x = x << 3;`
    
- **Giải thích:** Dịch các bit của `x` sang trái 3 vị trí (nhân với 2^3), rồi gán lại cho `x`.  
    Ví dụ:  
    `x = 2` (00010), `x << 3 = 10000` → `x = 16`
    

---
