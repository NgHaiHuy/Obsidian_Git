![[Chapter1_V2_Integration.ppt]]

---

## 📘 **Chương 1: TÍCH PHÂN**

---

### 🟢 **1.1 Xấp xỉ diện tích (Approximating Areas)**

- **Mục tiêu:** Tính diện tích dưới đường cong y=f(x)y = f(x) từ aa đến bb.
    
- Chia khoảng [a,b][a, b] thành nn đoạn nhỏ, tính diện tích hình chữ nhật.
    
- **Riemann Sum:**
    
    A≈∑i=1nf(xi∗)ΔxA \approx \sum_{i=1}^n f(x_i^*) \Delta x
    - xi∗x_i^*: điểm đầu trái, đầu phải hoặc trung điểm.
        
- Khi n→∞n \to \infty, tổng này tiệm cận giá trị diện tích thật.
    

---

### 🔵 **1.2 Tích phân xác định (Definite Integral)**

- **Ký hiệu:** ∫abf(x) dx\int_a^b f(x)\, dx
    
- **Ý nghĩa:** Tổng diện tích có dấu từ aa đến bb.
    
- **Thuộc tính:**
    
    - ∫aaf(x) dx=0\int_a^a f(x)\, dx = 0
        
    - ∫abf(x) dx=−∫baf(x) dx\int_a^b f(x)\, dx = -\int_b^a f(x)\, dx
        
    - ∫ab[f(x)±g(x)] dx=∫abf(x) dx±∫abg(x) dx\int_a^b [f(x) \pm g(x)]\, dx = \int_a^b f(x)\, dx \pm \int_a^b g(x)\, dx
        
- **Giá trị trung bình của hàm:**
    
    ftrung bıˋnh=1b−a∫abf(x) dxf_{\text{trung bình}} = \frac{1}{b-a} \int_a^b f(x)\, dx

---

### 🟠 **1.3 Định lý cơ bản của tích phân (FTC)**

- **Phần 1 (FTC1):**
    
    Neˆˊu F(x)=∫axf(t) dt⇒F′(x)=f(x)\text{Nếu } F(x) = \int_a^x f(t)\, dt \Rightarrow F'(x) = f(x)
- **Phần 2 (FTC2):**
    
    ∫abf(x) dx=F(b)−F(a)(với F′(x)=f(x))\int_a^b f(x)\, dx = F(b) - F(a) \quad \text{(với } F'(x) = f(x)\text{)}

---

### 🟣 **1.4 Công thức tích phân & Định lý thay đổi ròng (Net Change)**

- Tích phân của tốc độ thay đổi = Tổng thay đổi:
    
    ∫t1t2v(t) dt=s(t2)−s(t1)\int_{t_1}^{t_2} v(t)\, dt = s(t_2) - s(t_1)
    - Độ dời: ∫v(t) dt\int v(t)\, dt
        
    - Quãng đường: ∫∣v(t)∣ dt\int |v(t)|\, dt
        
- **Áp dụng:** tăng dân số, quãng đường, khối lượng, tốc độ, v.v.
    

---

### 🟤 **1.5 Phép đổi biến (Substitution)**

- **Dùng để tích phân phức tạp dễ hơn.**
    
- Nếu đặt u=g(x)u = g(x), thì:
    
    ∫f(g(x))g′(x) dx=∫f(u) du\int f(g(x))g'(x)\, dx = \int f(u)\, du
- **Tích phân xác định đổi cận:**
    
    ∫abf(g(x))g′(x) dx=∫g(a)g(b)f(u) du\int_a^b f(g(x))g'(x)\, dx = \int_{g(a)}^{g(b)} f(u)\, du

---

### 📌 **Mẹo nhớ công thức cơ bản:**

|Hàm f(x)f(x)|Nguyên hàm ∫f(x)dx\int f(x)dx|
|---|---|
|xnx^n (n ≠ –1)|xn+1n+1+C\frac{x^{n+1}}{n+1} + C|
|1x\frac{1}{x}|( \ln|
|exe^x|ex+Ce^x + C|
|sin⁡x\sin x|−cos⁡x+C-\cos x + C|
|cos⁡x\cos x|sin⁡x+C\sin x + C|

---
