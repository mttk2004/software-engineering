# ĐỀ THI VÀ ĐÁP ÁN - BIẾN THỂ 2

## ĐỀ THI

### TRƯỜNG ĐẠI HỌC SÀI GÒN
#### ĐỀ THI KẾT THÚC HỌC PHẦN - BIẾN THỂ 2
**Học phần:** CÔNG NGHỆ PHẦN MỀM
**Mã học phần:** 841047

*Thời gian làm bài: 90 phút, không kể thời gian phát đề*

**Học kì:** I...............................
**Năm học:** 2024-2025.............................
**Trình độ đào tạo:** Đại học ...........................
**Hình thức đào tạo:** Chính quy
**Hệ:** Đại trà
**Họ tên sinh viên:** ......................................
**Mã số sinh viên:** ......................................

*Sinh viên KHÔNG sử dụng tài liệu.*

---

### Câu 1. (3,0 điểm)
**a.** Cho ví dụ cụ thể về dự án phần mềm phù hợp với từng mô hình sau: V-Model, Extreme Programming (XP), Scrum. Giải thích lý do lựa chọn. (1,5 đ)

**b.** So sánh khả năng đáp ứng thay đổi yêu cầu giữa các mô hình Agile, Waterfall và Incremental. Mô hình nào có khả năng đáp ứng thay đổi tốt nhất và tại sao? (1,5 đ)

---

### Câu 2. (3,0 điểm)
So sánh tiến độ phát triển phần mềm giữa mô hình V-Model và mô hình Incremental Development qua các khía cạnh:
- Thời gian phát triển tổng thể
- Thời điểm bàn giao sản phẩm cho khách hàng
- Khả năng phát hiện lỗi sớm
- Quản lý rủi ro dự án

Từ đó, đưa ra nhận xét về ưu điểm của mô hình Incremental khi phát triển các dự án có yêu cầu thay đổi liên tục. (3,0 đ)

---

### Câu 3. (2,0 điểm)
Xét hệ thống đặt vé trực tuyến (cinema booking system) gồm các chức năng: tìm kiếm phim, đặt vé, thanh toán, hủy đặt vé và gửi thông báo.

#### a. Nêu 3-4 use case liên quan đến việc hủy vé của khách hàng. Mô tả ngắn gọn mỗi use case. (1,0 đ)

#### b.  Phân biệt và cho ví dụ cụ thể về quan hệ <<`include`>> và <<`extend`>> trong use case diagram của hệ thống này. (1,0 đ)

#### c. Liệt kê yêu cầu chức năng và yêu cầu phi chức năng của hệ thống này (1,0 đ)
**Yêu cầu chức năng:**
- Tìm kiếm phim theo tên, thể loại, thời gian chiếu
- Đặt vé và chọn chỗ ngồi
- Thanh toán trực tuyến qua nhiều phương thức (thẻ tín dụng, ví điện tử)
- Hủy vé và nhận hoàn tiền
- Gửi thông báo xác nhận và nhắc nhở qua email/SMS

**Yêu cầu phi chức năng:**
- Hiệu năng: Xử lý 1000 truy vấn tìm kiếm/phút
- Bảo mật: Mã hóa dữ liệu người dùng, sử dụng HTTPS
- Khả dụng: Uptime 99.9%, chịu lỗi nút
- Khả năng mở rộng: Hỗ trợ tăng số lượng user đồng thời
- Thời gian phản hồi: <2 giây cho mỗi request

---

### Câu 4. (2,0 điểm)
Thiết kế hệ thống cinema booking với các lớp chính:

**a.** Vẽ các lớp Movie, Customer, Booking, Cinema với các thuộc tính:
- **Movie:** movieID(String), title(String), duration(int), genre(String), showTime(DateTime)
- **Customer:** customerID(String), name(String), email(String), phone(String)
- **Booking:** bookingID(String), bookingDate(DateTime), seatNumber(String), totalAmount(double)
- **Cinema:** cinemaID(String), name(String), location(String), capacity(int)

Biểu diễn quan hệ giữa các lớp và trình bày ý nghĩa của từng mối quan hệ. (1,5 đ)

**b.** Nêu 2 ràng buộc hợp lệ (constraint) cho lớp Booking. (0,5 đ)

#### c. Mô tả quy trình triển khai CI/CD cho hệ thống này (0,5 đ)
- Quản lý mã nguồn với Git, nhánh `main` và `develop`
- Thiết lập GitLab CI/GitHub Actions với các stage: build, test, deploy
- Stage build: build code, tạo Docker image
- Stage test: chạy unit test, integration test, đảm bảo coverage >=80%
- Stage deploy: deploy tự động lên môi trường staging và production
- Sử dụng Kubernetes để quản lý container và rollback tự động khi gặp lỗi
- Tích hợp monitoring (Prometheus, Grafana) và alert khi có sự cố

---

*Cán bộ coi thi không giải thích gì thêm.*
*Trang 1/1*

---

## ĐÁP ÁN

### Câu 1. (3,0 điểm)

#### a. Ví dụ cụ thể cho từng mô hình (1,5 đ)

##### V-Model:
**Ví dụ:** Phát triển phần mềm điều khiển máy bay tự động (autopilot system)
**Lý do lựa chọn:**
- Yêu cầu về độ tin cậy và an toàn cực cao
- Cần kiểm thử kỹ lưỡng từng cấp độ (unit → integration → system → acceptance)
- Tài liệu hóa chi tiết cho việc chứng nhận an toàn
- Yêu cầu ổn định, ít thay đổi trong quá trình phát triển

##### Extreme Programming (XP):
**Ví dụ:** Phát triển ứng dụng mobile startup cho việc chia sẻ ảnh
**Lý do lựa chọn:**
- Yêu cầu thay đổi liên tục dựa trên phản hồi người dùng
- Đội ngũ nhỏ, giao tiếp trực tiếp với khách hàng
- Cần phát triển nhanh để ra thị trường sớm
- Sử dụng pair programming và test-driven development

##### Scrum:
**Ví dụ:** Phát triển hệ thống quản lý học tập trực tuyến (LMS)
**Lý do lựa chọn:**
- Dự án trung bình với yêu cầu rõ ràng nhưng có thể thay đổi
- Cần phản hồi định kỳ từ giáo viên và học sinh
- Phát triển theo sprint 2-4 tuần
- Đội ngũ có kinh nghiệm làm việc theo Agile

#### b. So sánh khả năng đáp ứng thay đổi yêu cầu (1,5 đ)

##### Xếp hạng khả năng đáp ứng thay đổi (từ cao đến thấp):

1. **Agile (Cao nhất):**
   - Thiết kế để thích ứng với thay đổi
   - Phản hồi liên tục từ khách hàng
   - Sprint ngắn, điều chỉnh nhanh
   - Tài liệu tối thiểu, tập trung vào code

2. **Incremental (Trung bình):**
   - Có thể thay đổi giữa các increment
   - Phản hồi sớm từ khách hàng
   - Tuy nhiên cần lập kế hoạch trước cho từng increment
   - Thay đổi lớn vẫn khó khăn

3. **Waterfall (Thấp nhất):**
   - Rất khó thay đổi sau khi hoàn thành một phase
   - Chi phí thay đổi tăng theo cấp số nhân
   - Cần tài liệu hóa lại toàn bộ
   - Chỉ phù hợp khi yêu cầu rất ổn định

**Kết luận:** Agile có khả năng đáp ứng thay đổi tốt nhất vì được thiết kế dựa trên nguyên tắc "Responding to change over following a plan".

---

### Câu 2. (3,0 điểm)

#### So sánh V-Model và Incremental Development:

##### 1. Thời gian phát triển tổng thể:
- **V-Model:** Thời gian dài, tuần tự từ đầu đến cuối
- **Incremental:** Có thể ngắn hơn do song song hóa và tái sử dụng code

##### 2. Thời điểm bàn giao sản phẩm:
- **V-Model:** Chỉ bàn giao khi hoàn thành toàn bộ dự án (100%)
- **Incremental:** Bàn giao từng phần chức năng sau mỗi increment (20%, 40%, 60%...)

##### 3. Khả năng phát hiện lỗi sớm:
- **V-Model:** Phát hiện lỗi muộn, chủ yếu trong giai đoạn testing
- **Incremental:** Phát hiện lỗi sớm sau mỗi increment, dễ sửa chữa

##### 4. Quản lý rủi ro dự án:
- **V-Model:** Rủi ro cao, tập trung vào cuối dự án
- **Incremental:** Rủi ro thấp, phân tán đều qua các increment

#### Ưu điểm của Incremental với dự án thay đổi liên tục:

1. **Thích ứng nhanh:** Có thể điều chỉnh yêu cầu giữa các increment
2. **Phản hồi sớm:** Khách hàng thấy kết quả ngay và góp ý
3. **Giảm rủi ro:** Phát hiện vấn đề sớm, tránh thất bại lớn
4. **Tăng giá trị:** Chức năng quan trọng được phát triển trước
5. **Cải thiện chất lượng:** Học hỏi từ increment trước để cải thiện increment sau

---

### Câu 3. (2,0 điểm)

#### a. 3-4 Use case liên quan đến hủy vé (1,0 đ)

1. **Cancel Booking Before Payment:**
   - Mô tả: Khách hàng hủy đặt vé trước khi thanh toán
   - Actor: Customer
   - Kết quả: Booking bị xóa, ghế được giải phóng

2. **Cancel Paid Booking with Refund:**
   - Mô tả: Khách hàng hủy vé đã thanh toán và yêu cầu hoàn tiền
   - Actor: Customer, Payment System
   - Kết quả: Booking bị hủy, tiền được hoàn lại theo chính sách

3. **Cancel Booking Due to Movie Cancellation:**
   - Mô tả: Hệ thống tự động hủy vé khi phim bị hủy chiếu
   - Actor: System, Customer (receive notification)
   - Kết quả: Tất cả booking của phim bị hủy, hoàn tiền tự động

4. **Staff Cancel Customer Booking:**
   - Mô tả: Nhân viên hủy booking của khách hàng (trường hợp đặc biệt)
   - Actor: Cinema Staff
   - Kết quả: Booking bị hủy, thông báo được gửi đến khách hàng

#### b. Phân biệt quan hệ <<`include`>> và <<`extend`>> (1,0 đ)

##### Quan hệ <<`include`>>:
**Định nghĩa:** Use case con luôn được thực hiện khi use case cha được thực hiện

**Ví dụ trong hệ thống cinema:**
```
"Book Movie Ticket" <<include>> "Verify Customer Login"
```
- Khi đặt vé, hệ thống luôn phải kiểm tra đăng nhập
- Không thể đặt vé mà không xác thực

##### Quan hệ <<`extend`>>:
**Định nghĩa:** Use case con chỉ được thực hiện trong điều kiện nhất định

**Ví dụ trong hệ thống cinema:**
```
"Apply Discount Code" <<extend>> "Book Movie Ticket"
```

**Sự khác biệt:**
- **Include:** Bắt buộc, luôn xảy ra
- **Extend:** Tùy chọn, chỉ xảy ra trong điều kiện đặc biệt

#### c. Liệt kê yêu cầu chức năng và yêu cầu phi chức năng của hệ thống này (1,0 đ)
**Yêu cầu chức năng:**
- Tìm kiếm phim theo tên, thể loại, thời gian chiếu
- Đặt vé và chọn chỗ ngồi
- Thanh toán trực tuyến qua nhiều phương thức (thẻ tín dụng, ví điện tử)
- Hủy vé và nhận hoàn tiền
- Gửi thông báo xác nhận và nhắc nhở qua email/SMS

**Yêu cầu phi chức năng:**
- Hiệu năng: Xử lý 1000 truy vấn tìm kiếm/phút
- Bảo mật: Mã hóa dữ liệu người dùng, sử dụng HTTPS
- Khả dụng: Uptime 99.9%, chịu lỗi nút
- Khả năng mở rộng: Hỗ trợ tăng số lượng user đồng thời
- Thời gian phản hồi: <2 giây cho mỗi request

---

### Câu 4. (2,0 điểm)

#### a. Class Diagram và mối quan hệ (1,5 đ)

```
┌─────────────────┐         ┌─────────────────┐
│    Customer     │         │     Cinema      │
├─────────────────┤         ├─────────────────┤
│ - customerID    │         │ - cinemaID      │
│ - name          │         │ - name          │
│ - email         │    1    │ - location      │
│ - phone         │────────▶│ - capacity      │
└─────────────────┘    *    └─────────────────┘
         │                           │
         │ 1                         │ 1
         │                           │
         ▼                           ▼
┌─────────────────┐         ┌─────────────────┐
│    Booking      │    *    │     Movie       │
├─────────────────┤◀────────├─────────────────┤
│ - bookingID     │    1    │ - movieID       │
│ - bookingDate   │         │ - title         │
│ - seatNumber    │         │ - duration      │
│ - totalAmount   │         │ - genre         │
└─────────────────┘         │ - showTime      │
                            └─────────────────┘
```

##### Ý nghĩa các mối quan hệ:

1. **Customer - Booking (1:*):**
   - Một khách hàng có thể có nhiều booking
   - Mỗi booking thuộc về duy nhất một khách hàng
   - Quan hệ composition: booking phụ thuộc vào customer

2. **Movie - Booking (1:*):**
   - Một phim có thể có nhiều booking (nhiều người đặt)
   - Mỗi booking chỉ cho một phim cụ thể
   - Quan hệ association: liên kết giữa phim và đặt vé

3. **Cinema - Movie (1:*):**
   - Một rạp chiếu có thể chiếu nhiều phim
   - Mỗi suất chiếu thuộc về một rạp cụ thể
   - Quan hệ aggregation: rạp chứa các suất chiếu

#### b. Ràng buộc hợp lệ cho lớp Booking (0,5 đ)

1. **Constraint về thời gian:**
   ```
   {bookingDate >= currentDate AND bookingDate <= showTime - 30 minutes}
   ```
   - Chỉ được đặt vé từ hiện tại đến trước giờ chiếu 30 phút

2. **Constraint về số ghế:**
   ```
   {seatNumber NOT IN (SELECT seatNumber FROM Booking WHERE movieID = this.movieID AND showTime = this.showTime)}
   ```
   - Một ghế chỉ được đặt bởi một booking cho cùng suất chiếu

**Giải thích thêm:**
- Constraints đảm bảo tính nhất quán và logic nghiệp vụ
- Ngăn chặn việc đặt vé không hợp lệ (quá muộn, ghế đã được đặt)
- Có thể implement ở database level hoặc application level

#### c. Mô tả quy trình triển khai CI/CD cho hệ thống này (0,5 đ)
- Quản lý mã nguồn với Git, nhánh `main` và `develop`
- Thiết lập GitLab CI/GitHub Actions với các stage: build, test, deploy
- Stage build: build code, tạo Docker image
- Stage test: chạy unit test, integration test, đảm bảo coverage >=80%
- Stage deploy: deploy tự động lên môi trường staging và production
- Sử dụng Kubernetes để quản lý container và rollback tự động khi gặp lỗi
- Tích hợp monitoring (Prometheus, Grafana) và alert khi có sự cố
