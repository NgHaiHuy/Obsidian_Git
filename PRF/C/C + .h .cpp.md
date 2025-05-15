Trong lập trình C/C++, **.h** và **.cpp** là hai loại tệp (file) quan trọng với mục đích khác nhau:

---

### **1. File Header (.h hoặc .hpp)**
- **Mục đích**: Chứa **khai báo** (declarations) nhưng không chứa định nghĩa chi tiết (implementation).
- **Nội dung thường có**:
  - Khai báo hàm (function prototypes).
  - Khai báo lớp (class declarations).
  - Các macro (`#define`).
  - Include thư viện (`#include`).
  - Biến toàn cục (`extern`).
- **Ví dụ**:
  ```cpp
  // File: MathUtils.h
  #ifndef MATH_UTILS_H  // Header guard tránh include nhiều lần
  #define MATH_UTILS_H

  int add(int a, int b);  // Khai báo hàm
  class Calculator {      // Khai báo lớp
  public:
      int multiply(int x, int y);
  };

  #endif
  ```

---

### **2. File Source (.cpp)**
- **Mục đích**: Chứa **định nghĩa** (implementation) của các hàm/class đã khai báo trong file header.
- **Nội dung thường có**:
  - Code thực thi chi tiết của hàm.
  - Logic chương trình.
  - Hàm `main()` (nếu là file chính).
- **Ví dụ**:
  ```cpp
  // File: MathUtils.cpp
  #include "MathUtils.h"  // Include header tương ứng

  // Định nghĩa hàm add()
  int add(int a, int b) {
      return a + b;
  }

  // Định nghĩa phương thức của class Calculator
  int Calculator::multiply(int x, int y) {
      return x * y;
  }
  ```

---

### **Tại sao phải tách .h và .cpp?**
1. **Tách biệt khai báo và định nghĩa**:
   - File header (.h) giống như bản **mô tả** (có gì), file .cpp là **cách làm** (như thế nào).
   - Giúp code dễ đọc, dễ bảo trì.

2. **Tái sử dụng code**:
   - Nhiều file .cpp khác nhau có thể `#include` chung một header để dùng cùng hàm/class.

3. **Tối ưu thời gian biên dịch**:
   - Khi thay đổi file .cpp, chỉ cần biên dịch lại file đó thay vì toàn bộ chương trình.

4. **Tránh lỗi liên kết**:
   - Nếu định nghĩa hàm trong header mà không dùng `inline`, có thể gây lỗi **multiple definitions** khi include nhiều lần.

---

### **Ví dụ thực tế**
- **File header**: `Student.h`  
  ```cpp
  #pragma once
  class Student {
  private:
      int id;
  public:
      void setID(int newID);
      int getID();
  };
  ```

- **File source**: `Student.cpp`  
  ```cpp
  #include "Student.h"
  void Student::setID(int newID) {
      id = newID;
  }
  int Student::getID() {
      return id;
  }
  ```

- **File main**: `main.cpp`  
  ```cpp
  #include "Student.h"
  int main() {
      Student s;
      s.setID(123);
      return 0;
  }
  ```

---

### **Khi nào dùng .h/.cpp?**
- **Tạo file .h**: Khi cần khai báo hàm/class dùng chung.
- **Tạo file .cpp**: Khi cần viết code thực thi hoặc hàm `main()`.
- **Tạo C++ Class (IDE hỗ trợ)**: Khi cần cả hai file .h và .cpp cho một class (tiện hơn).