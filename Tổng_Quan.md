[Quay lại](README.md)

# Tổng quan

## 1. Khái niệm

- Kiến trúc máy tính là việc xây dựng sản phẩm từ các thành phần có sẵn theo phương thức nhất định, ví dụ: kiến trúc chip, kiến trúc mạng Internet.
- Sự phát triển kiến trúc máy tính là mấu chốt cho các lĩnh vực tính toán khác.
- Máy tính có các chức năng chính: xử lý dữ liệu, lưu trữ dữ liệu, chuyển dữ liệu, điều khiển.

## 2. Các thế hệ máy tính

- **Thế hệ 1 (1946-1957):** Bóng chân không, máy lớn, lập trình bằng thẻ đục lỗ.
- **Thế hệ 2 (1958-1964):** Transistor, nhỏ hơn, dùng ngôn ngữ cấp cao (FORTRAN, COBOL).
- **Thế hệ 3 (1965-1971):** Mạch tích hợp (IC), tốc độ tăng, đa nhiệm.
- **Thế hệ 4 (1971 trở đi):** VLSI, tích hợp hàng triệu linh kiện, máy nhỏ, mạnh, đa phương tiện, xử lý song song.
- **Thế hệ 5 (từ 1978):** VLSI nâng cao, hệ phân tán, AI, tương tác đa dạng, tốc độ cao.

## 3. Phân loại máy tính

- **Siêu máy tính (Super Computer):** Mạnh nhất, tính toán khoa học, mô phỏng phức tạp, nhiều bộ xử lý song song.
- **Máy tính lớn (Mainframe):** Đa dụng, quản lý và ứng dụng khoa học lớn.
- **Máy tính mini (Minicomputer):** Trung bình, cho doanh nghiệp và ứng dụng vừa.
- **Máy vi tính (Microcomputer):** Cá nhân, dùng vi xử lý, phổ biến.

## 4. Hệ số

### 🎯 Các hệ số thường gặp

| Tên hệ đếm    | Cơ số | Ký hiệu dùng                       |
| ------------- | ----- | ---------------------------------- |
| Nhị phân      | 2     | `0, 1`                             |
| Bát phân      | 8     | `0 → 7`                            |
| Thập phân     | 10    | `0 → 9`                            |
| Thập lục phân | 16    | `0 → 9`, `A → F` (A=10, ..., F=15) |

---

### 🧠 Cách chuyển đổi giữa các hệ số

#### 1. Hệ bất kỳ → Thập phân

> **Công thức:** Số = chữ số × cơ số^vị trí

**Ví dụ:** `1011₂` sang thập phân:
```
= 1×2³ + 0×2² + 1×2¹ + 1×2⁰  
= 8 + 0 + 2 + 1 = 11₁₀
```

---

#### 2. Thập phân → Hệ khác

> **Cách:** Chia liên tiếp cho cơ số, ghi phần dư (đọc từ dưới lên)

**Ví dụ:** `156₁₀` sang nhị phân:
```
156 ÷ 2 = 78 dư 0  
78 ÷ 2 = 39 dư 0  
39 ÷ 2 = 19 dư 1  
19 ÷ 2 = 9 dư 1  
9 ÷ 2 = 4 dư 1  
4 ÷ 2 = 2 dư 0  
2 ÷ 2 = 1 dư 0  
1 ÷ 2 = 0 dư 1  
→ đọc ngược: 10011100₂
```

---

#### 3. Nhị phân ↔ Bát phân

> Nhóm 3 bit từ phải sang trái, mỗi nhóm là 1 chữ số bát phân

**Ví dụ:** `1101011₂` → bát phân:
```
Tách nhóm 3-bit: 001 101 011
→ 1   5   3 → 153₈
```

---

#### 4. Nhị phân ↔ Thập lục phân

> Nhóm 4 bit từ phải sang trái, mỗi nhóm là 1 chữ số hex

**Ví dụ:** `11101110₂` → thập lục phân:
```
Tách nhóm 4-bit: 1110 1110
→ 14   14 → EE₁₆
```

---

#### 5. Bát phân ↔ Nhị phân

> Mỗi chữ số bát phân → 3 bit nhị phân

**Ví dụ:** `57₈` → nhị phân:
```
5 = 101, 7 = 111 → 101111₂
```

---

#### 6. Thập lục phân ↔ Nhị phân

**Ví dụ:** `3F₁₆` → nhị phân:
```
3 = 0011, F = 1111 → 00111111₂
```

---

### 🔁 Tổng kết công thức chuyển đổi

| Từ → Đến            | Cách làm           |
| ------------------- | ------------------ |
| Bất kỳ → Thập phân  | Công thức lũy thừa |
| Thập phân → Bất kỳ  | Chia lấy dư        |
| Nhị phân ↔ Bát phân | Nhóm 3 bit         |
| Nhị phân ↔ Hex      | Nhóm 4 bit         |

## 5. Mã hóa

### Số nguyên âm

1. Nếu **bit đầu là 0** → số dương → chuyển bình thường
2. Nếu **bit đầu là 1** → số âm:
    - Đảo tất cả các bit
    - Cộng 1
    - Chuyển kết quả sang thập phân, thêm dấu âm

**Ví dụ:** `11111011₂` (8 bit)
1. Bit đầu = 1 → số âm
2. Đảo bit: `00000100`
3. Cộng 1: `00000101` = 5
4. Vậy số là **-5**

---

### Số thực 32 bit (IEEE 754)

#### 📏 Cấu trúc số thực 32-bit

```
| S |  Exponent (8 bit) |   Fraction / Mantissa (23 bit)   |
```
- **S:** Bit dấu (0 = dương, 1 = âm)
- **Exponent:** Số mũ lệch (biased exponent)
- **Fraction:** Phần thập phân của 1.xxx

---

#### 🔢 Các bước mã hóa số thực

1. **Xác định dấu (S):**
    - S = 0 nếu số dương, S = 1 nếu số âm
2. **Chuyển trị tuyệt đối sang nhị phân chuẩn hóa:**  
    Dạng: 1.mantissa × 2^e  
    VD: 5.75₁₀ → 101.11₂ = 1.0111 × 2²  
    Mantissa = 0111, Exponent thật = 2
3. **Tính exponent bị lệch:**  
    E = e + 127  
    VD: e = 2 → E = 129 → 10000001₂
4. **Ghi mantissa (23 bit):**  
    Bỏ số 1 trước dấu phẩy, bổ sung 0 nếu thiếu bit
5. **Ghép lại 32 bit**

---

#### ✅ Ví dụ chuẩn

`5.75₁₀`:
1. Dấu S = 0
2. Nhị phân = 101.11 → 1.0111 × 2^2
3. Exponent = 2 + 127 = 129 = 10000001
4. Mantissa = 01110000000000000000000
5. Kết quả:
```
0 10000001 01110000000000000000000
```

---

#### ⚠️ Các trường hợp đặc biệt

| Loại                          | Dấu      | Exponent   | Mantissa  | Ý nghĩa                               |
| ----------------------------- | -------- | ---------- | --------- | ------------------------------------- |
| **0**                         | 0/1      | 00000000   | 000...0   | Số 0 (âm hoặc dương)                  |
| **Số rất nhỏ (denormalized)** | 0/1      | 00000000   | ≠ 0       | Không chuẩn hóa (không có số 1 ẩn)    |
| **Vô cùng (±∞)**              | 0/1      | 11111111   | 000...0   | Dương / âm vô cực                     |
| **NaN (Not a Number)**        | 0/1      | 11111111   | ≠ 0       | Kết quả vô nghĩa (chia 0, sqrt âm...) |

---

#### ✅ Ví dụ đặc biệt

- `-0` → `1 00000000 00000000000000000000000`
- `+∞` → `0 11111111 00000000000000000000000`
- `NaN` → `x 11111111 mantissa ≠ 0` (bit dấu bất kỳ)
