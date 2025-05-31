# ĐỀ THI VÀ ĐÁP ÁN - BIẾN THỂ 3

## ĐỀ THI

### TRƯỜNG ĐẠI HỌC SÀI GÒN
#### ĐỀ THI KẾT THÚC HỌC PHẦN - BIẾN THỂ 3
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
a. Hãy mô tả mô hình V-Model và cho ví dụ một dự án phần mềm phù hợp để áp dụng mô hình này. (1,5 đ)

b. So sánh tiến độ phát triển phần mềm giữa mô hình V-Model và mô hình Incremental. Mô hình nào phù hợp khi yêu cầu thường xuyên thay đổi? (1,5 đ)

### Câu 2. (3,0 điểm)
Cho hệ thống đặt vé trực tuyến gồm các chức năng: tìm kiếm, đặt vé, thanh toán, hủy đặt vé và gửi thông báo.

a. Liệt kê các actor chính tương tác với hệ thống và mô tả ngắn gọn vai trò của từng actor. (1,0 đ)

b. Nêu 3 use case liên quan đến hủy vé của khách hàng và phân biệt quan hệ <<`include`>>, <<`extend`>> trong use case. (0,5 đ)

c. Liệt kê yêu cầu chức năng và yêu cầu phi chức năng của hệ thống này. (0,5 đ)

### Câu 3. (2,0 điểm)
a. Vẽ sơ đồ lớp (Class Diagram) cho hệ thống đặt vé với các lớp: Customer, Booking, Ticket, Payment. Bao gồm thuộc tính và biểu diễn quan hệ giữa các lớp. (1,0 đ)

b. Nêu các ràng buộc hợp lệ (constraint) cho lớp Ticket với các thuộc tính: ticketID, price, seatNumber, flightDate. (1,0 đ)

### Câu 4. (2,0 điểm)
a. Mô tả trình tự xử lý khi khách hàng đặt vé trong hệ thống đặt vé trực tuyến. (1,0 đ)

b. Viết 2 test case để kiểm thử chức năng "Hủy vé" (bao gồm input và output mong đợi). (0,5 đ)

c. Mô tả quy trình CI/CD cho việc phát triển hệ thống đặt vé trực tuyến này. (0,5 đ)

---

## ĐÁP ÁN

### Câu 1. (3,0 điểm)

#### a. Mô hình V-Model và ví dụ (1,5 đ)

**Mô tả mô hình V-Model:**
- Mô hình V-Model là mở rộng của mô hình Waterfall, có hình dạng chữ V
- Mỗi giai đoạn phát triển (bên trái) có giai đoạn kiểm thử tương ứng (bên phải)
- Đặc điểm: kiểm thử được lên kế hoạch song song với từng giai đoạn phát triển

**Cấu trúc V-Model:**
```
Requirements ←→ Acceptance Testing
System Design ←→ System Testing
Architecture ←→ Integration Testing
Module Design ←→ Unit Testing
     ↓           ↑
    Implementation
```

**Ví dụ dự án phù hợp:**
- **Hệ thống ngân hàng:** Yêu cầu rõ ràng, ít thay đổi, cần kiểm thử kỹ lưỡng
- **Phần mềm y tế:** Cần tuân thủ nghiêm ngặt quy chuẩn, kiểm thử toàn diện
- **Hệ thống hàng không:** Yêu cầu độ tin cậy cao, quy trình kiểm thử nghiêm ngặt

#### b. So sánh tiến độ phát triển (1,5 đ)

| Tiêu chí | V-Model | Incremental |
|----------|---------|-------------|
| **Tiến độ** | Tuyến tính, tuần tự | Song song, lặp lại |
| **Thời gian ra sản phẩm** | Cuối dự án | Sớm (sau increment đầu) |
| **Phản hồi khách hàng** | Cuối dự án | Thường xuyên |
| **Khả năng thay đổi** | Khó, tốn kém | Dễ dàng, linh hoạt |
| **Rủi ro** | Cao (phát hiện muộn) | Thấp (phát hiện sớm) |

**Kết luận:** Mô hình Incremental phù hợp hơn khi yêu cầu thường xuyên thay đổi vì:
- Cho phép điều chỉnh trong quá trình phát triển
- Nhận phản hồi sớm từ khách hàng
- Giảm rủi ro do phát hiện vấn đề sớm

### Câu 2. (3,0 điểm)

#### a. Các actor chính (1,0 đ)

1. **Khách hàng (Customer):**
   - Tìm kiếm vé máy bay
   - Đặt vé và thanh toán
   - Hủy vé khi cần thiết
   - Nhận thông báo xác nhận

2. **Quản trị viên (Administrator):**
   - Quản lý thông tin chuyến bay
   - Xử lý các giao dịch đặc biệt
   - Giám sát hệ thống

3. **Hệ thống thanh toán (Payment System):**
   - Xử lý giao dịch thanh toán
   - Xác thực thông tin thẻ tín dụng

4. **Hệ thống thông báo (Notification System):**
   - Gửi email xác nhận
   - Gửi SMS thông báo

#### b. Use case hủy vé và quan hệ (0,5 đ)

**3 Use case liên quan đến hủy vé:**
1. **Kiểm tra điều kiện hủy vé**
2. **Tính phí hủy vé**
3. **Hoàn tiền**

**Quan hệ:**
- "Hủy vé" <<`include`>> "Kiểm tra điều kiện hủy vé" (bắt buộc)
- "Hủy vé" <<`extend`>> "Tính phí hủy vé" (tùy điều kiện thời gian hủy)

**Phân biệt quan hệ:**
- **<<`include`>>:** Quan hệ bắt buộc, luôn thực hiện
- **<<`extend`>>:** Quan hệ tùy chọn, thực hiện khi có điều kiện

#### c. Yêu cầu hệ thống (0,5 đ)

**Yêu cầu chức năng:**
- Tìm kiếm vé theo điểm đi, điểm đến, ngày bay
- Đặt vé và chọn chỗ ngồi
- Thanh toán trực tuyến
- Hủy vé và hoàn tiền
- Gửi thông báo xác nhận

**Yêu cầu phi chức năng:**
- **Hiệu năng:** Xử lý 1000 user đồng thời
- **Bảo mật:** Mã hóa thông tin thanh toán
- **Khả dụng:** Hoạt động 24/7, uptime 99.9%
- **Thời gian phản hồi:** < 3 giây
- **Tương thích:** Hỗ trợ nhiều trình duyệt

### Câu 3. (2,0 điểm)

#### a. Sơ đồ lớp (Class Diagram) (1,0 đ)

```
┌─────────────────┐       ┌─────────────────┐
│    Customer     │       │     Booking     │
├─────────────────┤       ├─────────────────┤
│- customerID: String│ 1 ─→ │- bookingID: String│
│- name: String   │   *   │- bookingDate: Date│
│- email: String  │       │- status: String │
│- phone: String  │       │- totalAmount: double│
└─────────────────┘       └─────────────────┘
                                    │ 1
                                    │
                                    ↓ *
                          ┌─────────────────┐
                          │     Ticket      │
                          ├─────────────────┤
                          │- ticketID: String│
                          │- price: double  │
                          │- seatNumber: String│
                          │- flightDate: Date│
                          └─────────────────┘
                                    │ 1
                                    │
                                    ↓ 1
                          ┌─────────────────┐
                          │    Payment      │
                          ├─────────────────┤
                          │- paymentID: String│
                          │- amount: double │
                          │- method: String │
                          │- paymentDate: Date│
                          │- status: String │
                          └─────────────────┘
```

**Quan hệ:**
- Customer (1) → Booking (*): Một khách hàng có thể có nhiều booking
- Booking (1) → Ticket (*): Một booking có thể có nhiều vé
- Ticket (1) → Payment (1): Mỗi vé có một thanh toán

#### b. Ràng buộc hợp lệ cho lớp Ticket (1,0 đ)

**Constraints cho lớp Ticket:**
1. **ticketID:**
   - Không được null hoặc rỗng
   - Phải duy nhất trong hệ thống
   - Định dạng: "TK" + 8 chữ số

2. **price:**
   - Phải > 0
   - Không vượt quá 50,000,000 VND
   - Là số thực dương

3. **seatNumber:**
   - Không được null
   - Định dạng: [A-F][1-50] (ví dụ: A12, B05)
   - Phải duy nhất trong cùng chuyến bay

4. **flightDate:**
   - Không được null
   - Phải >= ngày hiện tại
   - Không quá 1 năm từ ngày đặt

### Câu 4. (2,0 điểm)

#### a. Trình tự xử lý đặt vé (1,0 đ)

**Sequence Diagram - Đặt vé:**

1. **Khách hàng → Hệ thống:** Tìm kiếm chuyến bay
2. **Hệ thống → Database:** Truy vấn thông tin chuyến bay
3. **Database → Hệ thống:** Trả về danh sách chuyến bay
4. **Hệ thống → Khách hàng:** Hiển thị kết quả tìm kiếm
5. **Khách hàng → Hệ thống:** Chọn chuyến bay và chỗ ngồi
6. **Hệ thống → Database:** Kiểm tra tình trạng chỗ ngồi
7. **Database → Hệ thống:** Xác nhận chỗ ngồi available
8. **Hệ thống → Khách hàng:** Yêu cầu thông tin thanh toán
9. **Khách hàng → Hệ thống:** Nhập thông tin thanh toán
10. **Hệ thống → Payment Gateway:** Xử lý thanh toán
11. **Payment Gateway → Hệ thống:** Xác nhận thanh toán thành công
12. **Hệ thống → Database:** Lưu thông tin booking và ticket
13. **Hệ thống → Notification Service:** Gửi email xác nhận
14. **Hệ thống → Khách hàng:** Hiển thị thông tin vé đã đặt

#### b. Test case cho chức năng "Hủy vé" (0,5 đ)

**Test Case 1: Hủy vé thành công**
- **Input:**
  - Ticket ID: "TK12345678"
  - Customer ID: "CUS001"
  - Thời gian hủy: 2 ngày trước ngày bay
- **Expected Output:**
  - Trạng thái vé: "Cancelled"
  - Phí hủy: 10% tổng giá vé
  - Số tiền hoàn: 90% tổng giá vé
  - Thông báo: "Hủy vé thành công. Số tiền hoàn sẽ được chuyển trong 3-5 ngày làm việc."

**Test Case 2: Hủy vé thất bại - Quá hạn**
- **Input:**
  - Ticket ID: "TK12345679"
  - Customer ID: "CUS002"
  - Thời gian hủy: 30 phút trước giờ bay
- **Expected Output:**
  - Trạng thái vé: Không thay đổi
  - Lỗi: "Không thể hủy vé. Đã quá thời hạn cho phép hủy vé (2 giờ trước giờ bay)."
  - Gợi ý: "Vui lòng liên hệ tổng đài để được hỗ trợ."

**Test Case 3: Hủy vé thất bại - Vé không tồn tại**
- **Input:**
  - Ticket ID: "TK99999999"
  - Customer ID: "CUS003"
- **Expected Output:**
  - Lỗi: "Không tìm thấy thông tin vé với mã TK99999999"
  - Gợi ý: "Vui lòng kiểm tra lại mã vé hoặc liên hệ hỗ trợ."

#### c. Quy trình CI/CD cho hệ thống đặt vé (0,5 đ)

**Continuous Integration (CI):**
- **Source Control Management:** Sử dụng Git với nhánh phát triển (develop) và nhánh chính (main)
- **Automated Build:** Mỗi khi có code mới được push lên repository, hệ thống tự động build ứng dụng
- **Unit Testing:** Thực hiện kiểm thử tự động cho từng đơn vị code
- **Code Quality Analysis:** Sử dụng SonarQube để kiểm tra chất lượng mã nguồn
- **Security Testing:** Kiểm tra lỗ hổng bảo mật với công cụ OWASP ZAP

**Continuous Delivery/Deployment (CD):**
- **Automated Deployment:** Tự động triển khai đến môi trường test, staging và production
- **Infrastructure as Code:** Sử dụng Docker và Kubernetes để đóng gói và quản lý ứng dụng
- **Canary Deployment:** Triển khai dần dần để giảm thiểu rủi ro
- **Rollback Strategy:** Khả năng quay lại phiên bản trước nếu phát hiện lỗi

**Tools và Platforms:**
- **CI/CD Tools:** Jenkins, GitLab CI/CD hoặc GitHub Actions
- **Monitoring:** Prometheus và Grafana để giám sát hiệu suất hệ thống
- **Logging:** ELK Stack (Elasticsearch, Logstash, Kibana) để thu thập và phân tích log
- **Notification:** Tự động thông báo qua Slack/Email khi có build thất bại hoặc vấn đề triển khai
