![[Chapter 3_Derivatives.ppt]]

---

## 📘 **CHƯƠNG 3: ĐẠO HÀM (DERIVATIVES)**

---

### 🟢 **3.1 Định nghĩa đạo hàm**

- **Đạo hàm tại điểm aa**:
    
    f′(a)=lim⁡h→0f(a+h)−f(a)hf'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h}
    
    → là **tốc độ thay đổi tức thời** hay **hệ số góc tiếp tuyến**.
    
- **Ý nghĩa hình học**: là **độ dốc tiếp tuyến** của đồ thị tại điểm (a,f(a))(a, f(a)).
    
- **Ứng dụng**:
    
    - Tìm vận tốc tức thời v(t)=s′(t)v(t) = s'(t)
        
    - Tìm tiếp tuyến: y−f(a)=f′(a)(x−a)y - f(a) = f'(a)(x - a)
        

---

### 🔵 **3.2 Đạo hàm là một hàm số**

- Khi biến aa trở thành biến xx, ta có **đạo hàm của hàm số**:
    
    f′(x)=lim⁡h→0f(x+h)−f(x)hf'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}
- **Ký hiệu khác**:
    
    - f′(x),dydx,Df(x),y′f'(x), \frac{dy}{dx}, Df(x), y'
        
- **Không khả vi** nếu:
    
    - Hàm không liên tục tại điểm.
        
    - Có “góc nhọn” (như ∣x∣|x| tại x=0x = 0).
        
- **Đạo hàm bậc cao**:
    
    f′′(x)=đạo haˋm bậc hai,f(n)(x)=đạo haˋm bậc nf''(x) = \text{đạo hàm bậc hai},\quad f^{(n)}(x) = \text{đạo hàm bậc n}

---

### 🟠 **3.3 Quy tắc đạo hàm**

|Tên quy tắc|Công thức|
|---|---|
|Hằng số|(c)′=0(c)' = 0|
|Lũy thừa|(xn)′=nxn−1(x^n)' = nx^{n-1}|
|Tổng/Hiệu|(f±g)′=f′±g′(f \pm g)' = f' \pm g'|
|Tích|(fg)′=f′g+fg′(fg)' = f'g + fg'|
|Thương|(fg)′=f′g−fg′g2\left(\frac{f}{g}\right)' = \frac{f'g - fg'}{g^2}|

---

### 🟣 **3.5 Đạo hàm hàm lượng giác**

|Hàm f(x)f(x)|Đạo hàm f′(x)f'(x)|
|---|---|
|sin⁡x\sin x|cos⁡x\cos x|
|cos⁡x\cos x|−sin⁡x-\sin x|
|tan⁡x\tan x|sec⁡2x\sec^2 x|
|cot⁡x\cot x|−csc⁡2x-\csc^2 x|
|sec⁡x\sec x|sec⁡xtan⁡x\sec x \tan x|
|csc⁡x\csc x|−csc⁡xcot⁡x-\csc x \cot x|

---

### 🟡 **3.9 Đạo hàm hàm mũ & log**

|Hàm f(x)f(x)|Đạo hàm f′(x)f'(x)|
|---|---|
|exe^x|exe^x|
|axa^x|axln⁡aa^x \ln a|
|ln⁡x\ln x|1x\frac{1}{x}|
|log⁡ax\log_a x|1xln⁡a\frac{1}{x \ln a}|

---

### 🟤 **3.4 Đạo hàm & tốc độ thay đổi**

- Đạo hàm thể hiện **tốc độ thay đổi** trong vật lý, kinh tế,...
    
- Ví dụ: nếu D(t)D(t) là nợ quốc gia theo năm tt, thì:
    
    D′(1990)=toˆˊc độ ta˘ng nợ na˘m 1990D'(1990) = \text{tốc độ tăng nợ năm 1990}

---

### 🟢 **3.6 Quy tắc chuỗi (Chain Rule)**

- Nếu y=f(u),u=g(x)y = f(u), u = g(x), thì:
    
    dydx=dydu⋅dudx\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}
- Ví dụ: f(x)=sin⁡(3x)⇒f′(x)=3cos⁡(3x)f(x) = \sin(3x) \Rightarrow f'(x) = 3\cos(3x)
    

---

### 🔵 **3.6 Phép vi phân ẩn (Implicit Differentiation)**

- Khi yy không tách được khỏi xx, ta đạo hàm hai vế:
    
    VD: x2+y2=25⇒2x+2yy′=0⇒y′=−xy\text{VD: } x^2 + y^2 = 25 \Rightarrow 2x + 2yy' = 0 \Rightarrow y' = -\frac{x}{y}

---

📌 **Ghi nhớ nhanh:**

|Khái niệm|Biểu diễn|
|---|---|
|Đạo hàm|f′(x),dydxf'(x), \frac{dy}{dx}|
|Đạo hàm tiếp tuyến|y−f(a)=f′(a)(x−a)y - f(a) = f'(a)(x - a)|
|Vận tốc tức thời|v(t)=s′(t)v(t) = s'(t)|
|Gia tốc|a(t)=s′′(t)a(t) = s''(t)|

---
