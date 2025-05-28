
---

### 🟢 **Cấp độ Cơ Bản (1–10)**

1. **Nhập và in chuỗi**
    
    - Viết chương trình yêu cầu người dùng nhập một chuỗi (có khoảng trắng), sau đó in lại chuỗi đó ra màn hình.
        
2. **Tính độ dài chuỗi**
    
    - Nhập một chuỗi từ bàn phím. Sử dụng hàm `strlen` để tính và in ra độ dài của chuỗi (không tính ký tự `'\0'`).
        
3. **Sao chép chuỗi**
    
    - Nhập một chuỗi từ bàn phím, sao chép nó vào một biến khác và in chuỗi mới ra màn hình (dùng `strcpy`).
        
4. **Nối hai chuỗi**
    
    - Nhập hai chuỗi từ bàn phím, dùng `strcat` để nối chúng lại thành một chuỗi duy nhất, sau đó in kết quả ra.
        
5. **So sánh hai chuỗi**
    
    - Nhập hai chuỗi và sử dụng `strcmp` để so sánh. In thông báo: "Chuỗi 1 lớn hơn", "Chuỗi 2 lớn hơn" hoặc "Hai chuỗi bằng nhau".
        
6. **In từng ký tự trong chuỗi**
    
    - Nhập chuỗi và in từng ký tự trên một dòng riêng biệt, kèm theo vị trí của nó.
        
7. **Đếm số ký tự chữ cái, số, ký tự đặc biệt**
    
    - Phân loại và đếm: chữ cái, chữ số, ký tự khác. In ra từng loại và số lượng tương ứng.
        
8. **Chuyển chuỗi sang chữ in hoa**
    
    - Nhập chuỗi, chuyển tất cả ký tự thường sang in hoa. (Dùng `toupper()` từng ký tự).
        
9. **Chuyển chuỗi sang chữ thường**
    
    - Nhập chuỗi, chuyển tất cả ký tự hoa sang thường. (Dùng `tolower()` từng ký tự).
        
10. **Đếm số lần xuất hiện của một ký tự**
    

- Nhập chuỗi và một ký tự bất kỳ, đếm số lần ký tự đó xuất hiện trong chuỗi.
    

---

### 🟡 **Cấp độ Trung Bình (11–20)**

11. **Đảo ngược chuỗi**
    

- Nhập chuỗi và in ra chuỗi bị đảo ngược hoàn toàn. (Ví dụ: `"hello"` → `"olleh"`)
    

12. **Kiểm tra chuỗi đối xứng (Palindrome)**
    

- Nhập chuỗi, kiểm tra xem chuỗi có giống nhau khi đọc xuôi và ngược không. (Không phân biệt hoa thường)
    

13. **Tách chuỗi thành từ (tokenize)**
    

- Nhập chuỗi chứa nhiều từ, sử dụng `strtok` để tách và in từng từ trên một dòng.
    

14. **Đếm số từ trong chuỗi**
    

- Đếm số lượng từ trong chuỗi (các từ cách nhau bằng khoảng trắng).
    

15. **Tìm từ dài nhất trong chuỗi**
    

- Tách từng từ và tìm từ có số ký tự dài nhất. In ra từ đó và độ dài của nó.
    

16. **Tìm từ ngắn nhất trong chuỗi**
    

- Tương tự bài 15 nhưng tìm từ ngắn nhất.
    

17. **Đếm số nguyên âm và phụ âm**
    

- Duyệt chuỗi, đếm số lượng nguyên âm (`a, e, i, o, u`) và phụ âm.
    

18. **Xoá khoảng trắng thừa giữa các từ**
    

- Ví dụ: `" Toi la sinh vien "` → `"Toi la sinh vien"`
    

19. **Chuyển chữ cái đầu mỗi từ thành in hoa**
    

- Ví dụ: `"nguyen van a"` → `"Nguyen Van A"`
    

20. **Xoá tất cả khoảng trắng trong chuỗi**
    

- Nhập chuỗi và xoá hết ký tự khoảng trắng.
    

---

### 🔴 **Cấp độ Nâng Cao (21–30)**

21. **Viết lại hàm `strlen`**
    

- Không dùng thư viện, viết hàm đếm số ký tự trong chuỗi thủ công.
    

22. **Viết lại hàm `strcpy`**
    

- Viết hàm sao chép chuỗi nguồn sang chuỗi đích mà không dùng `strcpy`.
    

23. **Viết lại hàm `strcmp`**
    

- So sánh hai chuỗi thủ công (trả về 0 nếu bằng nhau, >0 nếu chuỗi 1 lớn hơn,...).
    

24. **Đếm số lần xuất hiện của một từ**
    

- Nhập đoạn văn và từ khóa. Đếm xem từ đó xuất hiện bao nhiêu lần.
    

25. **Tìm và thay thế từ**
    

- Nhập đoạn văn, từ cần tìm và từ thay thế. In chuỗi sau khi thay thế tất cả.
    

26. **Loại bỏ ký tự trùng lặp**
    

- Ví dụ: `"programming"` → `"progamin"` (giữ lại ký tự đầu tiên, xoá trùng lặp sau)
    

27. **Mã hóa chuỗi kiểu Caesar**
    

- Mỗi ký tự chữ cái được dịch tiến thêm `k` vị trí trong bảng chữ cái. (Ví dụ: `"abc"` với k=2 → `"cde"`)
    

28. **Tách câu trong đoạn văn**
    

- Nhập đoạn văn và tách từng câu kết thúc bằng `.`, `?`, `!`
    

29. **Chuyển số dạng chuỗi thành số nguyên**
    

- Viết hàm chuyển chuỗi `"1234"` thành số nguyên `1234` (không dùng `atoi`).
    

30. **Chuẩn hoá tên người**
    

- Nhập chuỗi là tên người có định dạng sai (thừa khoảng trắng, sai hoa/thường). Xuất tên chuẩn.  
    → `" nGUyen vaN aN "` → `"Nguyen Van An"`
    

---
