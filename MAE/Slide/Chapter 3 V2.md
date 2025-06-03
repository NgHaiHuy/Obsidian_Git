![[Chapter 3_V2_Techniquse Of Integration.ppt]]

---

## 📘 **CHƯƠNG 3: KỸ THUẬT TÍNH TÍCH PHÂN**

---

### 🟢 **3.1 Phép tích phân từng phần (Integration by Parts)**

- **Công thức**:
    
    ∫u dv=uv−∫v du\int u\, dv = uv - \int v\, du
- **Cách chọn uu và dvdv** theo thứ tự **LIATE**:
    
    - **L**: Logarithmic
        
    - **I**: Inverse trig
        
    - **A**: Algebra (đa thức, phân thức…)
        
    - **T**: Trig
        
    - **E**: Exponential
        
- **Ví dụ quan trọng**:
    
    - ∫xsin⁡x dx\int x \sin x \, dx
        
    - ∫exsin⁡x dx\int e^x \sin x \, dx: cần làm **2 lần** rồi giải phương trình.
        

---

### 🔵 **3.6 Tích phân số (Numerical Integration)**

#### 📏 Các phương pháp gần đúng:

|Phương pháp|Công thức/Ý tưởng|
|---|---|
|Left Endpoint|Lấy giá trị đầu trái mỗi đoạn nhỏ|
|Right Endpoint|Lấy giá trị đầu phải mỗi đoạn nhỏ|
|Midpoint|Lấy trung điểm mỗi đoạn nhỏ|
|**Trapezoidal**|Dùng hình thang thay vì hình chữ nhật|
|**Simpson’s Rule**|Dùng parabol để xấp xỉ đường cong (n chẵn)|

#### ✅ **Lỗi (Error) của các phương pháp**:

- Trapezoid/Midpoint: lỗi phụ thuộc ∣f′′(x)∣|f''(x)|
    
- Simpson: lỗi phụ thuộc ∣f(4)(x)∣|f^{(4)}(x)|
    

---

### 🟣 **3.7 Tích phân không đúng (Improper Integrals)**

#### 🔸 **Loại I** – **Cận vô hạn**:

∫a∞f(x) dx=lim⁡t→∞∫atf(x) dx\int_a^{\infty} f(x)\, dx = \lim_{t \to \infty} \int_a^t f(x)\, dx

#### 🔹 **Loại II** – **Hàm không liên tục** (vô hạn tại cận):

∫abf(x) dx=lim⁡t→b−∫atf(x) dxneˆˊu f→∞ khi x→b\int_a^b f(x)\, dx = \lim_{t \to b^-} \int_a^t f(x)\, dx \quad \text{nếu } f \to \infty \text{ khi } x \to b

#### ✅ **Hội tụ (Convergent)**: Nếu giới hạn tồn tại hữu hạn

#### ❌ **Phân kỳ (Divergent)**: Nếu giới hạn không tồn tại

---

### 📐 **Tiêu chí hội tụ cơ bản**:

- ∫1∞1xpdx\int_1^\infty \frac{1}{x^p} dx:
    
    - Hội tụ nếu p>1p > 1
        
    - Phân kỳ nếu p≤1p \le 1
        

---

### 🧠 **Định lý so sánh (Comparison Theorem)**:

- Nếu 0≤g(x)≤f(x)0 \leq g(x) \leq f(x):
    
    - Nếu ∫f(x)\int f(x) hội tụ ⇒ ∫g(x)\int g(x) hội tụ.
        
    - Nếu ∫g(x)\int g(x) phân kỳ ⇒ ∫f(x)\int f(x) phân kỳ.
        

---

## ✅ **Ghi nhớ nhanh công thức quan trọng**

|Công thức|Ý nghĩa|
|---|---|
|∫u dv=uv−∫v du\int u\, dv = uv - \int v\, du|Tích phân từng phần|
|∫abf(x) dx≈Trapezoid/Midpoint/Simpson\int_a^b f(x)\, dx \approx \text{Trapezoid/Midpoint/Simpson}|Tích phân số|
|∫1∞1xpdx\int_1^\infty \frac{1}{x^p} dx|Xét hội tụ theo p|
|Error≤K(b−a)312n2\text{Error} \leq \frac{K(b - a)^3}{12n^2}|Sai số Trapezoid|
|Error≤K(b−a)5180n4\text{Error} \leq \frac{K(b - a)^5}{180n^4}|Sai số Simpson|

---
	