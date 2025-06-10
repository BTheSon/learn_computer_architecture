[Quay lại](README.md)

# 1. Thành phần cơ bản
Các thành phần chính của máy tính bao gồm:

#### 1. **Bộ xử lý trung tâm (CPU):**  
- Là bộ phận thực thi các lệnh.  
- Gồm: **ALU** (Arithmetic And Logic Unit - phần thi hành lệnh) và **CU** (Control Unit - bộ diều khiển) .  
    - Điều phối các hoạt động trong máy tính.

#### 2. **Bộ nhớ trong:**  
- Tập hợp các **ô nhớ** chứa thông tin đã mã hoá thành số nhị phân (**dữ liệu** và **lệnh**).  
- Mỗi ô nhớ có **địa chỉ riêng**.  
- Được truy cập theo kiểu ngẫu nhiên (**RAM** - Random Access Memory).

#### 3. **Hệ thống các bus:**  
- Gồm: **bus địa chỉ**, **bus dữ liệu**, **bus điều khiển**.  
- **Kết nối** các thành phần của máy tính.  
- **Bus địa chỉ** và **bus dữ liệu**: truyền dữ liệu.  
- **Bus điều khiển**: đảm bảo hoạt động theo trình tự.
- **phân biệt**:
    - Bus hệ thống : trao đổi thông tin giữa CPU và bộ nhớ trong
    - Bus vào-ra dùng trao đổi thông tin giữa các bộ phận vào-ra và bộ nhớ trong.

# 2. Tổng quan

## 2.1. Các thành phần cơ bản của một máy tính

### Một bộ máy tính cơ bản bao gồm:
- **CPU**: Bộ xử lý trung tâm.
- **Bộ nhớ trong**: 
- Lưu trữ dữ liệu và chương trình.
- Tập hợp các ô nhớ chứa thông tin mã hóa dưới dạng số nhị phân.
- Mỗi ô nhớ có địa chỉ riêng, hỗ trợ truy cập ngẫu nhiên (RAM).
- **Các bộ phận nhập/xuất**: Giao tiếp với người dùng và thiết bị ngoại vi.
- **Hệ thống bus**:
    - **Bus địa chỉ**: Truyền địa chỉ dữ liệu.
    - **Bus dữ liệu**: Truyền dữ liệu.
    - **Bus điều khiển**: Đồng bộ và điều khiển các bộ phận.

---

## 2.2. Kiến trúc máy tính

- **Kiến trúc máy tính** bao gồm:
    - **Kiến trúc phần mềm**: Tập lệnh, dạng lệnh, kiểu định vị.
    - **Tổ chức máy tính**: Cấu trúc bên trong của bộ xử lý, bus, bộ nhớ.
    - **Lắp đặt phần cứng**: Cách triển khai vật lý.

- **Tập lệnh**:
    - Tập hợp các lệnh mã máy mà CPU có thể hiểu và thực thi.

- **Thi hành lệnh**:
    - Liên quan đến việc chọn số toán hạng, vị trí toán hạng (ngăn xếp, thanh ghi tích lũy, thanh ghi đa dụng) và kiến trúc tương ứng.

---

## 2.3. Các lựa chọn vị trí các toán hạng

- **Kiến trúc ngăn xếp**:
    - **Ưu điểm**: Lệnh ngắn, ít mã máy, dễ tạo bộ biên dịch đơn giản.
    - **Nhược điểm**: Truy cập không ngẫu nhiên, mã không hiệu quả, khó xử lý song song.

- **Kiến trúc thanh ghi tích lũy**:
    - **Ưu điểm**: Lệnh ngắn, tối thiểu trạng thái bên trong, thiết kế dễ dàng.
    - **Nhược điểm**: Lưu giữ tạm thời, khó xử lý song song, trao đổi nhiều với bộ nhớ.

- **Kiến trúc thanh ghi đa dụng**:
    - **Ưu điểm**: Tốc độ xử lý nhanh, định vị đơn giản, tạo mã hiệu quả.
    - **Nhược điểm**: Lệnh dài, số lượng thanh ghi giới hạn.

---

## 2.4. Tập lệnh

- **Cấu trúc**:
    - Mỗi lệnh ngôn ngữ cấp cao được xây dựng từ một hoặc nhiều lệnh mã máy.
    - Bao gồm:
    - **Lệnh bộ nhớ**: LOAD, STORE.
    - **Lệnh tính toán số học**: ADD, SUB, MUL, DIV.
    - **Lệnh logic**: AND, OR, XOR, NEG.
    - **Lệnh dịch chuyển**: SHIFT.

- **Lệnh có điều kiện**:
    - Dạng: `Nếu <điều kiện> thì <chuỗi lệnh 1> nếu không <chuỗi lệnh 2>`.
    - Sử dụng các bit trạng thái để ghi nhớ điều kiện.

---

## 2.5. Lệnh có điều kiện

- **Bit trạng thái**:
    - Được cung cấp bởi ALU (Arithmetic Logic Unit).
    - Lưu trữ kết quả dưới dạng các bit trạng thái.

- **Kỹ thuật ghi nhớ bit trạng thái**:
    - Ghi vào thanh ghi đa dụng.
    - Sử dụng thanh ghi trạng thái đặc biệt.

- **Lệnh nhảy có điều kiện**:
    - Chỉ thực hiện khi điều kiện thỏa mãn.
    - Có thể cải tiến bằng lệnh di chuyển có điều kiện (ví dụ: MGT).

---

## 2.6. Các kiểu định vị

- **Định nghĩa**:
    - Xác định cách truy cập toán hạng (bộ nhớ hoặc thanh ghi).

- **Sắp xếp địa chỉ trong ô nhớ**:
    - **Big-Endian**: Byte thấp nhất ở địa chỉ cao nhất.
    - **Little-Endian**: Byte thấp nhất ở địa chỉ thấp nhất.

- **Kiểu định vị trong kiến trúc thanh ghi đa dụng**:
    - Bao gồm nhiều kiểu khác nhau (không nêu chi tiết).

---

## 2.7. Kiến trúc RISC

- **Khái niệm**:
    - RISC (Reduced Instruction Set Computer) ra đời từ thập niên 1980.
    - Trái ngược với CISC (Complex Instruction Set Computer) từ thập niên 1960.

- **Đặc điểm**:
    - Số lượng lệnh ít, kiểu định vị và dạng lệnh đơn giản.
    - Lệnh có chiều dài cố định.
    - Chỉ lệnh đọc/ghi ô nhớ mới truy cập bộ nhớ.

- **Thiết kế**:
    - Sử dụng mạch điện tạo tín hiệu điều khiển.
    - Nhiều thanh ghi để giảm truy cập bộ nhớ.

---

## 2.8. Lợi điểm và bất lợi của RISC

- **Lợi điểm**:
    - Diện tích bộ xử lý nhỏ.
    - Tốc độ tính toán cao.
    - Thời gian thiết kế ngắn, ít rủi ro sai sót.

- **Bất lợi**:
    - Chương trình dài hơn.
    - Cần tính địa chỉ hiệu dụng.
    - Tập lệnh ít lệnh, gây khó khăn cho chương trình dịch.

---

## 2.9. Kiểu định vị và ngôn ngữ

- **Kiểu định vị trong RISC**:
    - Thanh ghi.
    - Tức thì.
    - Trực tiếp.
    - Gián tiếp bằng thanh ghi + độ dời.
    - Tự tăng.

- **Ngôn ngữ cấp cao**:
    - Gần với ngôn ngữ thông thường, cô đọng, độc lập với bộ xử lý.
    - Sử dụng chương trình dịch để chuyển sang ngôn ngữ máy.

---