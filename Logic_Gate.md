[Quay lại](README.md)
# Định nghĩa
Một mạng logic hay một mạng các cổng là một hệ thống có dạng:
- input: x1, x2, ... là các biến bool
- output: f(x1, x2, ..) là hàm bool

# Các cổng logic cơ bản:
![Các ký hiệu cổng logic bao gồm AND, NAND, OR, NOR, BUFFER, NOT, XOR và XNOR. Mỗi cổng được biểu diễn bằng ký hiệu sơ đồ mạch chuẩn của nó, được sắp xếp thành hai hàng. Hàng trên cùng hiển thị các cổng AND, NAND, OR và NOR. Hàng dưới cùng hiển thị các cổng BUFFER, NOT, XOR và XNOR. Mỗi ký hiệu được dán nhãn với tên cổng tương ứng bên dưới. Hình ảnh có tông màu giáo dục rõ ràng với các đường màu đen rõ nét trên nền trắng. Tiêu đề ở trên cùng có nội dung KÝ HIỆU CỔNG LOGIC bằng chữ in hoa đậm.](asset/image.png)

- gồm 4 cổng chính: AND, OR, NOT, XOR

# Mạch trừ 1 bit

## 1. **Thiết lập bảng chân trị**

| A | B | D (A−B) | Borrow |
| - | - | ------- | ------ |
| 0 | 0 | 0       | 0      |
| 0 | 1 | 1       | 1      |
| 1 | 0 | 1       | 0      |
| 1 | 1 | 0       | 0      |

---

## 2. **Thiết lập biểu thức logic từ bảng chân trị**

### a. Hiệu (D):

Nhìn vào bảng, ta thấy D = 1 tại các hàng:

* A = 0, B = 1
* A = 1, B = 0

Ta viết minterms tương ứng:

```
D = (-A * B) + (A * -B)
```

---

### b. Borrow:

Chỉ có một trường hợp Borrow = 1:

* A = 0, B = 1

Biểu thức:

```
Borrow = -A * B
```

---

## 3. **Rút gọn biểu thức**

### a. Hiệu (D):

Không thể rút gọn thêm — đây **chính là dạng tối giản** rồi.
Vì D là **XOR**, và biểu thức:

```
D = (-A * B) + (A * -B)
```

là biểu diễn XOR bằng các cổng cơ bản.

### b. Borrow:

Biểu thức đã tối giản:

```
Borrow = -A * B
```

---

## 4. **Vẽ mạch logic (mô tả bằng chữ)**

### a. Hiệu (D):

* Tạo `-A` và `-B` (cổng NOT)
* Tạo hai cổng AND:

  * AND1: `-A * B`
  * AND2: `A * -B`
* Dùng OR để cộng đầu ra của AND1 và AND2

### b. Borrow:

* Dùng lại `-A`
* Dùng AND: `-A * B`

---

## 🎯 **Sơ đồ logic mô tả bằng chữ (cho mạch trừ 1 bit)**

![mạch logic](asset/machtru.png)

---

## ✅ **Tổng kết bài làm**

| Đầu ra            | Biểu thức logic tối giản |
| ----------------- | ------------------------ |
| **Hiệu (D)**      | `(-A * B) + (A * -B)`    |
| **Mượn (Borrow)** | `-A * B`                 |

---
