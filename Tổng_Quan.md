[Quay lại](README.md)

# Tổng quan

## 1. Khái niệm 
- Kiến trúc máy tính hướng đến việc xây dựng sản phẩm từ các thành phần có sẵn theo một phương thức nhất định, ví dụ như kiến trúc chip, kiến trúc mạng Internet.

- Sự phát triển của kiến trúc máy tính được xem là mấu chốt cho sự phát triển của những lĩnh vực tính toán khác.

- Máy tính có các chức năng chính: xử lý dữ liệu, lưu trữ dữ liệu, chuyển dữ liệu và điều khiển.

## 2. Các thế hệ máy tính

- **Thế hệ thứ nhất** (1946-1957): Sử dụng bóng chân không, máy lớn, lập trình bằng thẻ đục lỗ.

- **Thế hệ thứ hai** (1958-1964): Thay transistor, kích thước nhỏ hơn, dùng ngôn ngữ cấp cao như FORTRAN, COBOL.

- **Thế hệ thứ ba** (1965-1971): Sử dụng mạch tích hợp (IC), tăng tốc độ, đa nhiệm.

- **Thế hệ thứ tư** (1971 trở đi): Công nghệ VLSI, tích hợp hàng triệu linh kiện, máy nhỏ, mạnh, hỗ trợ đa phương tiện và xử lý song song.

- **Thế hệ thứ năm** (từ 1978): Tăng cường công nghệ VLSI, phát triển hệ phân tác, trí tuệ nhân tạo, tương tác đa dạng, tốc độ xử lý cao hơn.


## 3. Phân loại máy tính

Phân loại máy tính dựa trên tính năng kỹ thuật và giá tiền như sau:

- **Siêu máy tính** (Super Computer): Mạnh nhất, dùng để tính toán khoa học, mô phỏng phức tạp, tích hợp nhiều bộ xử lý theo kỹ thuật song song.

- **Máy tính lớn** (Mainframe): Đa dụng, dùng cho quản lý và các ứng dụng khoa học lớn.

- **Máy tính mini** (Minicomputer): Cỡ trung, phù hợp cho doanh nghiệp và các ứng dụng trung bình.

- **Máy vi tính** (Microcomputer): Máy tính cá nhân, dùng bộ vi xử lý, phổ biến rộng rãi.

## 4. Mã hóa 
Tuyệt! Bạn đang nói đến **các hệ đếm (cơ số)** như nhị phân (cơ số 2), thập phân (cơ số 10), thập lục phân (cơ số 16), bát phân (cơ số 8)... đúng không? Nếu vậy thì tôi sẽ giải thích rõ ràng cách **chuyển đổi qua lại giữa các hệ số** với ví dụ dễ hiểu.

---

## 🎯 Các hệ số thường gặp

| Tên hệ đếm    | Cơ số | Ký hiệu dùng                       |
| ------------- | ----- | ---------------------------------- |
| Nhị phân      | 2     | `0, 1`                             |
| Bát phân      | 8     | `0 → 7`                            |
| Thập phân     | 10    | `0 → 9`                            |
| Thập lục phân | 16    | `0 → 9`, `A → F` (A=10, ..., F=15) |

---

## 🧠 Cách chuyển đổi giữa các hệ số

---

### 1. **Từ hệ bất kỳ → thập phân (cơ số 10)**

> Dùng công thức:
> **Số = chữ số × cơ số^vị trí**

**Ví dụ:** `1011₂` sang thập phân:

```
= 1×2³ + 0×2² + 1×2¹ + 1×2⁰  
= 8 + 0 + 2 + 1 = 11₁₀
```

---

### 2. **Từ thập phân → hệ khác (nhị phân, bát phân, thập lục phân,...)**

> Dùng cách **chia liên tiếp cho cơ số**, ghi lại phần dư (đọc từ dưới lên)

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

→ đọc ngược: **10011100₂**
```

---

### 3. **Nhị phân ↔ Bát phân**

> Nhóm **3 bit** từ phải sang trái
> mỗi nhóm tương ứng với **1 chữ số bát phân**

**Ví dụ:** `1101011₂` → bát phân:

```
Tách nhóm 3-bit: 
  001 101 011
→ 1   5   3 → 153₈
```

---

### 4. **Nhị phân ↔ Thập lục phân**

> Nhóm **4 bit** từ phải sang trái
> mỗi nhóm tương ứng với **1 chữ số hex**

**Ví dụ:** `11101110₂` → thập lục phân:

```
Tách nhóm 4-bit: 
  1110 1110
→ 14   14 → EE₁₆
```

---

### 5. **Bát phân ↔ Nhị phân** (ngược lại của phần 3)

> Mỗi chữ số bát phân → 3 bit nhị phân.

**Ví dụ:** `57₈` → nhị phân:

```
5 = 101, 7 = 111 → 101111₂
```

---

### 6. **Thập lục phân ↔ Nhị phân** (ngược lại của phần 4)

**Ví dụ:** `3F₁₆` → nhị phân:

```
3 = 0011, F = 1111 → 00111111₂
```

---

## 🔁 Tổng kết công thức chuyển đổi

| Từ → Đến            | Cách làm           |
| ------------------- | ------------------ |
| Bất kỳ → Thập phân  | Công thức lũy thừa |
| Thập phân → Bất kỳ  | Chia lấy dư        |
| Nhị phân ↔ Bát phân | Nhóm 3 bit         |
| Nhị phân ↔ Hex      | Nhóm 4 bit         |
