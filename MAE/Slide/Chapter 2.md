![[Chapter 2_Limits.ppt]]

---

## 📘 **CHƯƠNG 2: GIỚI HẠN (LIMITS)**

---

### 🟢 **2.1 Mở đầu – Tầm quan trọng của giới hạn**

- **Giới hạn** giúp hiểu các khái niệm như: tiếp tuyến, vận tốc tức thời, diện tích dưới đường cong.
    
- Ví dụ:
    
    - **Tiếp tuyến**: tìm giới hạn của hệ số góc tiếp tuyến.
        
    - **Vận tốc tức thời**: là giới hạn của vận tốc trung bình khi khoảng thời gian → 0.
        
    - **Diện tích**: là giới hạn của tổng diện tích các hình chữ nhật nhỏ.
        

---

### 🔵 **2.2 Khái niệm giới hạn**

- **Giới hạn tại điểm aa**:
    
    lim⁡x→af(x)=L⇒f(x) tieˆˊn gaˆˋn L khi x→a\lim_{x \to a} f(x) = L \Rightarrow f(x) \text{ tiến gần } L \text{ khi } x \to a
- **Giới hạn một phía**:
    
    - Từ trái: lim⁡x→a−f(x)\lim_{x \to a^-} f(x)
        
    - Từ phải: lim⁡x→a+f(x)\lim_{x \to a^+} f(x)
        
- **Giới hạn vô cực**:
    
    - lim⁡x→af(x)=∞\lim_{x \to a} f(x) = \infty: hàm tăng không giới hạn khi x gần a.
        
    - → Đây là dấu hiệu của **tiệm cận đứng** tại x=ax = a.
        

---

### 🟠 **2.3 Các quy tắc tính giới hạn (Limit Laws)**

- Nếu lim⁡x→af(x)=L\lim_{x \to a} f(x) = L, lim⁡x→ag(x)=M\lim_{x \to a} g(x) = M, thì:
    

|Biểu thức|Kết quả|
|---|---|
|lim⁡[f(x)±g(x)]\lim [f(x) \pm g(x)]|L±ML \pm M|
|lim⁡[f(x)g(x)]\lim [f(x)g(x)]|LMLM|
|lim⁡[f(x)g(x)]\lim \left[\frac{f(x)}{g(x)}\right]|LM\frac{L}{M} nếu M≠0M \ne 0|
|lim⁡[c⋅f(x)]\lim [c \cdot f(x)]|cLcL|

- **Định lý kẹp (Squeeze Theorem)**:  
    Nếu:
    
    f(x)≤g(x)≤h(x),vaˋ lim⁡f(x)=lim⁡h(x)=L⇒lim⁡g(x)=Lf(x) \leq g(x) \leq h(x), \quad \text{và } \lim f(x) = \lim h(x) = L \Rightarrow \lim g(x) = L

---

### 🟣 **2.4 Tính liên tục (Continuity)**

- **Hàm liên tục tại aa** nếu:
    
    lim⁡x→af(x)=f(a)\lim_{x \to a} f(x) = f(a)
- **Các loại gián đoạn**:
    
    1. **Gián đoạn có thể loại bỏ**: lim⁡f(x)\lim f(x) tồn tại nhưng khác f(a)f(a).
        
    2. **Gián đoạn kiểu nhảy**: giới hạn trái và phải khác nhau.
        
    3. **Gián đoạn vô hạn**: lim⁡f(x)=±∞\lim f(x) = \pm \infty
        
- **Tính chất của hàm liên tục**:
    
    - Các hàm sau **luôn liên tục** trên miền xác định:
        
        - Đa thức, phân thức, căn bậc chẵn, lượng giác, log, mũ.
            
    - Tính liên tục được bảo toàn khi cộng, trừ, nhân, chia (nếu mẫu ≠ 0), hàm hợp.
        

---

### 🟤 **2.5 Định lý giá trị trung gian (Intermediate Value Theorem - IVT)**

- Nếu hàm ff **liên tục trên** [a,b][a, b], và f(a)<N<f(b)f(a) < N < f(b), thì tồn tại c∈(a,b)c \in (a, b) sao cho f(c)=Nf(c) = N.
    
- 👉 Dùng để **chứng minh phương trình có nghiệm** trong khoảng.
    

---

### 🟡 **2.6 Giới hạn tại vô cực & tiệm cận ngang**

- Nếu lim⁡x→∞f(x)=L\lim_{x \to \infty} f(x) = L ⇒ đường thẳng y=Ly = L là **tiệm cận ngang**.
    
- Tương tự khi x→−∞x \to -\infty.
    

---

## ✅ Tổng kết từ khóa:

|Từ khóa|Ý nghĩa|
|---|---|
|Limit (Giới hạn)|Giá trị hàm tiến tới khi x→ax \to a|
|Continuity (Liên tục)|Hàm không bị “nhảy” hay “đứt đoạn”|
|Asymptote (Tiệm cận)|Đường mà đồ thị tiệm cận đến|
|Squeeze Theorem|Định lý kẹp, dùng khi hàm bị kẹp giữa 2 hàm|
|Intermediate Value|Định lý giá trị trung gian, dùng để tìm nghiệm|

---
