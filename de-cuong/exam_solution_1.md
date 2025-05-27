# ĐỀ THI VÀ ĐÁP ÁN - BIẾN THỂ 1

## ĐỀ THI

### TRƯỜNG ĐẠI HỌC SÀI GÒN
#### ĐỀ THI KẾT THÚC HỌC PHẦN
**Học phần:** CÔNG NGHỆ PHẦN MẠM
**Mã học phần:** 841047
*Thời gian làm bài: 90 phút, không kể thời gian phát đề*

**Học kì:** I............................... **Năm học:** 2024-2025.............................
**Trình độ đào tạo:** Đại học ........................... **Hình thức đào tạo:** Chính quy **Hệ:** Đại trà
**Họ tên sinh viên:** ...................................... **Mã số sinh viên:** ......................................

*Sinh viên KHÔNG sử dụng tài liệu.*

---

### Câu 1. (3,0 điểm)
**a.** So sánh ưu nhược điểm của mô hình Waterfall và mô hình Incremental Development. Khi nào nên sử dụng từng mô hình? (1,5 đ)

**b.** Trong quá trình phát triển phần mềm, tại sao việc "Coping with Change" lại quan trọng? Nêu 2 kỹ thuật chính để đối phó với sự thay đổi yêu cầu. (1,5 đ)

---

### Câu 2. (3,0 điểm)
Một công ty muốn phát triển hệ thống quản lý thư viện trực tuyến với các yêu cầu sau:
- Hệ thống cần phải hoạt động ổn định với hiệu suất cao
- Yêu cầu rõ ràng và ít thay đổi trong quá trình phát triển
- Dự án có quy mô lớn với nhiều nhóm phát triển ở các địa điểm khác nhau
- Cần tài liệu chi tiết để quản lý dự án

**a.** Đề xuất mô hình quy trình phần mềm phù hợp và giải thích lý do lựa chọn. (1,5 đ)

**b.** Mô tả 4 hoạt động cơ bản (Process Activities) sẽ được thực hiện trong dự án này. (1,5 đ)

---

### Câu 3. (2,0 điểm)
Xét hệ thống đặt vé máy bay trực tuyến với các chức năng chính: tìm kiếm chuyến bay, đặt vé, thanh toán, hủy vé, và gửi thông báo.

**a.** Liệt kê các actor chính tương tác với hệ thống và mô tả ngắn gọn vai trò của từng actor. (1,0 đ)

**b.** Viết 3 user story cho chức năng "Đặt vé máy bay". (1,0 đ)

---

### Câu 4. (2,0 điểm)
Trong hệ thống đặt vé máy bay ở câu 3, hãy thiết kế các lớp chính của hệ thống:

**a.** Vẽ Class Diagram bao gồm các lớp: Customer, Flight, Booking, Payment với các thuộc tính cơ bản và mối quan hệ giữa chúng. (1,0 đ)

**b.** Mô tả ý nghĩa của các mối quan hệ trong Class Diagram vừa vẽ. (1,0 đ)

---

*Cán bộ coi thi không giải thích gì thêm.*
*Trang 1/1*

---

## ĐÁP ÁN

### Câu 1. (3,0 điểm)

#### a. So sánh ưu nhược điểm của mô hình Waterfall và Incremental Development (1,5 đ)

##### Mô hình Waterfall:
**Ưu điểm:**
- Cấu trúc rõ ràng, dễ quản lý và theo dõi tiến độ
- Tài liệu hóa đầy đủ cho từng giai đoạn
- Phù hợp với các dự án lớn, đa địa điểm
- Kế hoạch chi tiết, dễ ước lượng chi phí và thời gian

**Nhược điểm:**
- Khó thích ứng với thay đổi yêu cầu
- Khách hàng chỉ thấy sản phẩm cuối cùng
- Rủi ro cao nếu có lỗi ở giai đoạn đầu
- Thời gian phát triển dài

##### Mô hình Incremental Development:
**Ưu điểm:**
- Linh hoạt với thay đổi yêu cầu
- Khách hàng có thể đánh giá sớm
- Giảm rủi ro dự án
- Phân phối sản phẩm nhanh hơn

**Nhược điểm:**
- Khó quản lý tiến độ tổng thể
- Cấu trúc hệ thống có thể suy giảm
- Tài liệu không đầy đủ
- Chi phí refactoring cao

##### Khi nào sử dụng:
- **Waterfall:** Yêu cầu ổn định, dự án lớn, nhiều bên tham gia
- **Incremental:** Yêu cầu thay đổi thường xuyên, cần phản hồi sớm từ khách hàng

#### b. Tầm quan trọng của "Coping with Change" và 2 kỹ thuật chính (1,5 đ)

##### Tầm quan trọng:
- Thay đổi là không thể tránh khỏi trong mọi dự án phần mềm lớn
- Môi trường kinh doanh thay đổi liên tục
- Công nghệ mới xuất hiện
- Nền tảng phát triển thay đổi
- Thay đổi dẫn đến việc làm lại (rework) và tăng chi phí

##### 2 kỹ thuật chính:
1. **Software Prototyping:**
   - Tạo phiên bản ban đầu để thử nghiệm ý tưởng
   - Giúp xác định yêu cầu chính xác hơn
   - Cải thiện thiết kế giao diện người dùng
   - Giảm rủi ro phát triển

2. **Incremental Delivery:**
   - Chia nhỏ phát triển thành các increment
   - Ưu tiên yêu cầu quan trọng nhất
   - Phản hồi sớm từ người dùng
   - Giảm rủi ro thất bại dự án

---

### Câu 2. (3,0 điểm)

#### a. Đề xuất mô hình quy trình phù hợp (1,5 đ)

**Mô hình đề xuất: Waterfall Model**

**Lý do lựa chọn:**
- **Yêu cầu ổn định:** Hệ thống thư viện có yêu cầu rõ ràng và ít thay đổi
- **Quy mô lớn đa địa điểm:** Waterfall giúp phối hợp tốt giữa các nhóm phát triển
- **Tài liệu chi tiết:** Mô hình này tạo ra tài liệu đầy đủ cho quản lý dự án
- **Hiệu suất cao:** Thiết kế kỹ lưỡng từ đầu đảm bảo hiệu suất hệ thống
- **Quản lý dễ dàng:** Cấu trúc rõ ràng giúp quản lý tiến độ và nguồn lực

#### b. 4 hoạt động cơ bản (Process Activities) (1,5 đ)

1. **Software Specification (Đặc tả phần mềm):**
   - Xác định yêu cầu chức năng: quản lý sách, độc giả, mượn/trả sách
   - Xác định yêu cầu phi chức năng: hiệu suất, bảo mật, khả năng mở rộng
   - Tạo tài liệu SRS (Software Requirements Specification)

2. **Design and Implementation (Thiết kế và triển khai):**
   - Thiết kế kiến trúc hệ thống: 3-tier architecture
   - Thiết kế cơ sở dữ liệu: ERD, schema
   - Lập trình các module theo thiết kế

3. **Software Validation (Xác thực phần mềm):**
   - Unit testing: kiểm thử từng module
   - Integration testing: kiểm thử tích hợp
   - System testing: kiểm thử toàn hệ thống
   - User acceptance testing: kiểm thử chấp nhận

4. **Software Evolution (Tiến hóa phần mềm):**
   - Bảo trì và sửa lỗi
   - Cập nhật tính năng mới
   - Nâng cấp công nghệ
   - Tối ưu hóa hiệu suất

---

### Câu 3. (2,0 điểm)

#### a. Các actor chính và vai trò (1,0 đ)

1. **Customer (Khách hàng):**
   - Tìm kiếm chuyến bay
   - Đặt vé và thanh toán
   - Hủy vé khi cần thiết
   - Nhận thông báo về chuyến bay

2. **Airline Staff (Nhân viên hàng không):**
   - Quản lý thông tin chuyến bay
   - Xử lý yêu cầu hủy/đổi vé
   - Hỗ trợ khách hàng
   - Cập nhật trạng thái chuyến bay

3. **System Administrator:**
   - Quản lý hệ thống
   - Backup và restore dữ liệu
   - Bảo trì hệ thống
   - Quản lý tài khoản người dùng

4. **Payment Gateway:**
   - Xử lý giao dịch thanh toán
   - Xác thực thông tin thẻ
   - Gửi kết quả thanh toán

#### b. 3 User Story cho chức năng "Đặt vé máy bay" (1,0 đ)

1. **User Story 1:**
   - **Như một** khách hàng
   - **Tôi muốn** tìm kiếm chuyến bay theo điểm đi, điểm đến và ngày bay
   - **Để** có thể chọn chuyến bay phù hợp với lịch trình của mình

2. **User Story 2:**
   - **Như một** khách hàng
   - **Tôi muốn** chọn chỗ ngồi và nhập thông tin hành khách
   - **Để** hoàn tất thông tin đặt vé trước khi thanh toán

3. **User Story 3:**
   - **Như một** khách hàng
   - **Tôi muốn** thanh toán trực tuyến bằng thẻ tín dụng/debit
   - **Để** hoàn tất việc đặt vé và nhận xác nhận booking

---

### Câu 4. (2,0 điểm)

#### a. Class Diagram (1,0 đ)

```
┌─────────────────┐         ┌─────────────────┐
│    Customer     │         │     Flight      │
├─────────────────┤         ├─────────────────┤
│ - customerID    │         │ - flightID      │
│ - name          │         │ - flightNumber  │
│ - email         │    1    │ - departure     │
│ - phone         │────────▶│ - destination   │
│ - address       │    *    │ - departureTime │
└─────────────────┘         │ - arrivalTime   │
         │                  │ - availableSeats│
         │ 1                │ - price         │
         │                  └─────────────────┘
         │                           │
         ▼                           │ *
┌─────────────────┐                  │
│    Booking      │                  │
├─────────────────┤                  │
│ - bookingID     │                  │
│ - bookingDate   │◀─────────────────┘
│ - seatNumber    │ 1
│ - status        │
│ - totalAmount   │
└─────────────────┘
         │ 1
         │
         ▼
┌─────────────────┐
│    Payment      │
├─────────────────┤
│ - paymentID     │
│ - amount        │
│ - paymentDate   │
│ - paymentMethod │
│ - status        │
└─────────────────┘
```

#### b. Ý nghĩa các mối quan hệ (1,0 đ)

1. **Customer - Booking (1:*):**
   - Một khách hàng có thể có nhiều booking
   - Mỗi booking chỉ thuộc về một khách hàng
   - Quan hệ composition: booking phụ thuộc vào customer

2. **Flight - Booking (*:*):**
   - Một chuyến bay có thể có nhiều booking
   - Một booking chỉ cho một chuyến bay cụ thể
   - Quan hệ association: liên kết giữa chuyến bay và đặt chỗ

3. **Booking - Payment (1:1):**
   - Mỗi booking có một payment tương ứng
   - Mỗi payment chỉ thuộc về một booking
   - Quan hệ composition: payment phụ thuộc hoàn toàn vào booking

**Giải thích thêm:**
- **Multiplicity (1, *, 1:1, 1:*)** thể hiện số lượng đối tượng tham gia vào quan hệ
- **Composition** (◆): đối tượng con không thể tồn tại độc lập khi đối tượng cha bị xóa
- **Association** (──): mối quan hệ lỏng lẻo giữa các đối tượng
</rewritten_file>
