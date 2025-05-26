# SƠ ĐỒ HOẠT ĐỘNG (ACTIVITY DIAGRAM)

## Mục lục
1. [Giới thiệu về Activity Diagram](#giới-thiệu-về-activity-diagram)
2. [Các thành phần của Activity Diagram](#các-thành-phần-của-activity-diagram)
   - [Nút khởi đầu (Initial Node)](#nút-khởi-đầu-initial-node)
   - [Hoạt động (Activity/Action)](#hoạt-động-activityaction)
   - [Luồng điều khiển (Control Flow)](#luồng-điều-khiển-control-flow)
   - [Nút quyết định (Decision Node)](#nút-quyết-định-decision-node)
   - [Nút kết hợp (Merge Node)](#nút-kết-hợp-merge-node)
   - [Nút rẽ nhánh (Fork Node)](#nút-rẽ-nhánh-fork-node)
   - [Nút nối (Join Node)](#nút-nối-join-node)
   - [Nút kết thúc (Activity Final Node)](#nút-kết-thúc-activity-final-node)
   - [Nút kết thúc luồng (Flow Final Node)](#nút-kết-thúc-luồng-flow-final-node)
   - [Đối tượng (Object Node)](#đối-tượng-object-node)
   - [Kho dữ liệu (Data Store)](#kho-dữ-liệu-data-store)
   - [Ghi chú (Note)](#ghi-chú-note)
   - [Làn (Swimlane)](#làn-swimlane)
3. [Khi nào nên sử dụng Activity Diagram](#khi-nào-nên-sử-dụng-activity-diagram)
4. [Cách vẽ Activity Diagram](#cách-vẽ-activity-diagram)
5. [Ví dụ về Activity Diagram](#ví-dụ-về-activity-diagram)
   - [Quy trình đăng nhập](#quy-trình-đăng-nhập)
   - [Quy trình mua sắm trực tuyến](#quy-trình-mua-sắm-trực-tuyến)
   - [Quy trình rút tiền từ ATM](#quy-trình-rút-tiền-từ-atm)
   - [Quy trình xử lý đơn hàng](#quy-trình-xử-lý-đơn-hàng)
6. [Sự khác biệt giữa Activity Diagram và Flowchart](#sự-khác-biệt-giữa-activity-diagram-và-flowchart)
7. [Tổng kết](#tổng-kết)
8. [Tham khảo](#tham-khảo)

## Giới thiệu về Activity Diagram

Activity Diagram (Sơ đồ hoạt động) là một trong những biểu đồ hành vi trong UML (Unified Modeling Language) được sử dụng để mô tả các khía cạnh động của hệ thống. Activity Diagram là một phiên bản nâng cao của lưu đồ (flowchart) với ngữ nghĩa phong phú hơn, được sử dụng để mô hình hóa luồng hoạt động từ hoạt động này sang hoạt động khác.

Activity Diagram miêu tả cách các hoạt động được phối hợp để cung cấp một dịch vụ ở các mức trừu tượng khác nhau. Nó mô tả quy trình nghiệp vụ, luồng công việc, và trình tự hoạt động. Điểm mạnh lớn nhất của Activity Diagram là nó hỗ trợ và khuyến khích hành vi song song, làm cho nó trở thành một công cụ tuyệt vời để mô hình hóa quy trình làm việc và trong nguyên tắc, cho lập trình đa luồng.

Activity Diagram có thể được hiểu như một chuỗi các hoạt động được thực hiện bởi hệ thống. Nó không chỉ mô tả những gì xảy ra, mà còn mô tả cách nó xảy ra và ai chịu trách nhiệm thực hiện nó.

## Các thành phần của Activity Diagram

### Nút khởi đầu (Initial Node)

- **Ký hiệu**: Một vòng tròn đen đặc
- **Mục đích**: Biểu thị điểm bắt đầu của một hoạt động
- **Đặc điểm**: Một Activity Diagram chỉ có một nút khởi đầu (trừ khi có các hoạt động lồng nhau)

### Hoạt động (Activity/Action)

- **Ký hiệu**: Hình chữ nhật bo tròn các góc
- **Mục đích**: Biểu thị một hành động hoặc một bước trong quy trình
- **Đặc điểm**: Hoạt động là đơn vị cơ bản của công việc được thực hiện trong quy trình

### Luồng điều khiển (Control Flow)

- **Ký hiệu**: Một mũi tên nét liền
- **Mục đích**: Chỉ ra thứ tự các hoạt động được thực hiện
- **Đặc điểm**: Có thể chứa điều kiện chuyển tiếp (guard condition)

### Nút quyết định (Decision Node)

- **Ký hiệu**: Hình thoi
- **Mục đích**: Biểu thị một quyết định dựa trên điều kiện
- **Đặc điểm**: Có một luồng vào và nhiều luồng ra, mỗi luồng ra được đánh dấu bằng một điều kiện

### Nút kết hợp (Merge Node)

- **Ký hiệu**: Hình thoi
- **Mục đích**: Kết hợp các luồng điều khiển thay thế thành một
- **Đặc điểm**: Có nhiều luồng vào và một luồng ra

### Nút rẽ nhánh (Fork Node)

- **Ký hiệu**: Một thanh ngang đen
- **Mục đích**: Chia một luồng thành nhiều luồng song song
- **Đặc điểm**: Có một luồng vào và nhiều luồng ra được thực hiện đồng thời

### Nút nối (Join Node)

- **Ký hiệu**: Một thanh ngang đen
- **Mục đích**: Kết hợp các luồng song song lại với nhau
- **Đặc điểm**: Có nhiều luồng vào và một luồng ra, tất cả các luồng vào phải hoàn thành trước khi luồng ra được kích hoạt

### Nút kết thúc (Activity Final Node)

- **Ký hiệu**: Một vòng tròn với một vòng tròn đen đặc bên trong (hình như mắt trâu)
- **Mục đích**: Chỉ ra sự kết thúc của tất cả các luồng điều khiển trong hoạt động
- **Đặc điểm**: Khi đạt đến nút kết thúc, toàn bộ hoạt động kết thúc, không phụ thuộc vào trạng thái của các luồng khác

### Nút kết thúc luồng (Flow Final Node)

- **Ký hiệu**: Hình chữ X bên trong một vòng tròn
- **Mục đích**: Kết thúc một luồng điều khiển riêng biệt
- **Đặc điểm**: Chỉ kết thúc luồng điều khiển đi đến nó, không ảnh hưởng đến các luồng khác

### Đối tượng (Object Node)

- **Ký hiệu**: Hình chữ nhật
- **Mục đích**: Biểu thị một đối tượng được sử dụng hoặc tạo ra trong quy trình
- **Đặc điểm**: Có thể chỉ ra trạng thái của đối tượng

### Kho dữ liệu (Data Store)

- **Ký hiệu**: Hình chữ nhật với nhãn <<datastore>>
- **Mục đích**: Biểu thị một kho lưu trữ dữ liệu bền vững
- **Đặc điểm**: Dữ liệu được lưu trữ lâu dài và có thể được truy cập từ nhiều hoạt động khác nhau

### Ghi chú (Note)

- **Ký hiệu**: Hình chữ nhật với góc gấp ở phía trên bên phải
- **Mục đích**: Cung cấp thông tin bổ sung
- **Đặc điểm**: Không có ý nghĩa ngữ nghĩa trong mô hình

### Làn (Swimlane)

- **Ký hiệu**: Các cột hoặc hàng được phân chia bằng các đường thẳng
- **Mục đích**: Phân chia các hoạt động theo người thực hiện, phòng ban, hoặc đơn vị
- **Đặc điểm**: Giúp phân định trách nhiệm và tổ chức các hoạt động

## Khi nào nên sử dụng Activity Diagram

Activity Diagram nên được sử dụng trong các trường hợp sau:

1. **Mô tả quy trình nghiệp vụ**: Khi bạn cần mô tả một quy trình nghiệp vụ phức tạp với nhiều bước và nhiều bên tham gia.

2. **Phân tích use case**: Để hiểu chi tiết về cách thức hoạt động bên trong của một use case, đặc biệt là khi có nhiều luồng xử lý thay thế hoặc ngoại lệ.

3. **Mô tả quy trình làm việc**: Khi cần mô tả quy trình làm việc giữa các bộ phận, phòng ban hoặc các hệ thống khác nhau.

4. **Mô tả thuật toán phức tạp**: Để biểu diễn các thuật toán phức tạp với nhiều quyết định và xử lý song song.

5. **Xác định các use case tiềm năng**: Thông qua việc kiểm tra các quy trình nghiệp vụ.

6. **Xác định các điều kiện tiên quyết và hậu điều kiện**: Cho các use case.

7. **Mô hình hóa quy trình làm việc giữa/trong các use case**: Để hiểu cách các use case phối hợp tạo thành quy trình làm việc.

## Cách vẽ Activity Diagram

### Bước 1: Xác định phạm vi và mục đích

- Xác định quy trình hoặc hoạt động cần mô hình hóa
- Xác định mức độ chi tiết cần thiết
- Xác định các bên liên quan (actors) tham gia vào quy trình

### Bước 2: Xác định các hoạt động và hành động

- Liệt kê tất cả các hoạt động và hành động trong quy trình
- Xác định thứ tự thực hiện các hoạt động

### Bước 3: Xác định các điểm quyết định và điều kiện

- Xác định các điểm trong quy trình mà tại đó cần đưa ra quyết định
- Xác định các điều kiện cho mỗi lựa chọn

### Bước 4: Xác định các hoạt động song song

- Xác định các hoạt động có thể thực hiện đồng thời

### Bước 5: Thêm các làn (swimlanes)

- Nếu cần, thêm các làn để chỉ rõ ai chịu trách nhiệm cho mỗi hoạt động

### Bước 6: Vẽ sơ đồ

1. Đặt nút khởi đầu (initial node) tại điểm bắt đầu của quy trình
2. Vẽ các hoạt động theo thứ tự thực hiện
3. Sử dụng các nút quyết định (decision nodes) và nút kết hợp (merge nodes) để biểu diễn các điều kiện và lựa chọn
4. Sử dụng các nút rẽ nhánh (fork nodes) và nút nối (join nodes) để biểu diễn các hoạt động song song
5. Đặt nút kết thúc (final node) tại điểm kết thúc của quy trình

### Bước 7: Kiểm tra và tinh chỉnh

- Kiểm tra tính đúng đắn và đầy đủ của sơ đồ
- Đảm bảo tất cả các luồng đều bắt đầu từ nút khởi đầu và kết thúc tại nút kết thúc
- Kiểm tra tính nhất quán của các làn (nếu có)

## Ví dụ về Activity Diagram

### Quy trình đăng nhập

Dưới đây là một ví dụ đơn giản về quy trình đăng nhập vào hệ thống:

```
[Nút khởi đầu] --> [Hiển thị màn hình đăng nhập]
[Hiển thị màn hình đăng nhập] --> [Nhập thông tin đăng nhập]
[Nhập thông tin đăng nhập] --> [Kiểm tra thông tin]
[Kiểm tra thông tin] --> [Quyết định: Thông tin hợp lệ?]
[Quyết định: Thông tin hợp lệ?] -- Có --> [Đăng nhập thành công]
[Quyết định: Thông tin hợp lệ?] -- Không --> [Hiển thị thông báo lỗi]
[Hiển thị thông báo lỗi] --> [Hiển thị màn hình đăng nhập]
[Đăng nhập thành công] --> [Hiển thị màn hình chính]
[Hiển thị màn hình chính] --> [Nút kết thúc]
```

### Quy trình mua sắm trực tuyến

Ví dụ về quy trình mua sắm trực tuyến:

```
[Nút khởi đầu] --> [Duyệt sản phẩm]
[Duyệt sản phẩm] --> [Thêm vào giỏ hàng]
[Thêm vào giỏ hàng] --> [Quyết định: Tiếp tục mua sắm?]
[Quyết định: Tiếp tục mua sắm?] -- Có --> [Duyệt sản phẩm]
[Quyết định: Tiếp tục mua sắm?] -- Không --> [Thanh toán]
[Thanh toán] --> [Quyết định: Đã đăng nhập?]
[Quyết định: Đã đăng nhập?] -- Có --> [Chọn phương thức thanh toán]
[Quyết định: Đã đăng nhập?] -- Không --> [Đăng nhập hoặc đăng ký]
[Đăng nhập hoặc đăng ký] --> [Chọn phương thức thanh toán]
[Chọn phương thức thanh toán] --> [Xác nhận đơn hàng]
[Xác nhận đơn hàng] --> [Nút kết thúc]
```

### Quy trình rút tiền từ ATM

Ví dụ về quy trình rút tiền từ máy ATM sử dụng làn (swimlane) để phân biệt trách nhiệm:

**Làn 1: Khách hàng**
```
[Nút khởi đầu] --> [Chèn thẻ ATM]
[Chèn thẻ ATM] --> [Nhập mã PIN]
[Nhập mã PIN] --> [Chọn rút tiền]
[Chọn số tiền] --> [Nhận tiền và biên lai]
[Nhận tiền và biên lai] --> [Quyết định: Giao dịch khác?]
[Quyết định: Giao dịch khác?] -- Có --> [Chọn rút tiền]
[Quyết định: Giao dịch khác?] -- Không --> [Nhận thẻ]
[Nhận thẻ] --> [Nút kết thúc]
```

**Làn 2: ATM**
```
[Xác thực thẻ] --> [Xác minh PIN]
[Xác minh PIN] --> [Hiển thị các tùy chọn]
[Hiển thị các tùy chọn] --> [Hiển thị số tiền có sẵn]
[Hiển thị số tiền có sẵn] --> [Quyết định: Đủ tiền?]
[Quyết định: Đủ tiền?] -- Có --> [Phát tiền]
[Quyết định: Đủ tiền?] -- Không --> [Hiển thị thông báo lỗi]
[Phát tiền] --> [In biên lai]
[In biên lai] --> [Hiển thị tùy chọn giao dịch khác]
[Hiển thị tùy chọn giao dịch khác] --> [Trả thẻ]
```

**Làn 3: Ngân hàng**
```
[Xác minh tài khoản] --> [Kiểm tra số dư]
[Kiểm tra số dư] --> [Ghi nhận giao dịch]
[Ghi nhận giao dịch] --> [Cập nhật số dư]
```

### Quy trình xử lý đơn hàng

Ví dụ về quy trình xử lý đơn hàng với nhiều bên tham gia:

**Làn 1: Khách hàng**
```
[Nút khởi đầu] --> [Đặt hàng]
[Nhận thông báo] --> [Thanh toán]
[Nhận đơn hàng] --> [Nút kết thúc]
```

**Làn 2: Hệ thống**
```
[Xác nhận đơn hàng] --> [Tính toán chi phí]
[Tính toán chi phí] --> [Gửi thông báo]
[Xác nhận thanh toán] --> [Tạo đơn hàng]
[Tạo đơn hàng] --> [Nút rẽ nhánh]
```

**Làn 3: Kho hàng**
```
[Nút rẽ nhánh] --> [Kiểm tra kho]
[Kiểm tra kho] --> [Đóng gói]
[Đóng gói] --> [Nút nối]
```

**Làn 4: Bộ phận vận chuyển**
```
[Nút rẽ nhánh] --> [Lên lịch giao hàng]
[Lên lịch giao hàng] --> [Nút nối]
[Nút nối] --> [Giao hàng]
```

## Sự khác biệt giữa Activity Diagram và Flowchart

Mặc dù Activity Diagram và Flowchart (Lưu đồ) có vẻ tương tự nhau, chúng có một số điểm khác biệt quan trọng:

1. **Phạm vi**: Activity Diagram là một phần của UML, được sử dụng trong phát triển phần mềm. Flowchart có thể được sử dụng trong nhiều lĩnh vực khác nhau.

2. **Mức độ phức tạp**: Activity Diagram có nhiều thành phần phức tạp hơn như làn (swimlanes), rẽ nhánh (fork), nối (join) cho phép mô tả các quy trình phức tạp và song song.

3. **Tiêu chuẩn hóa**: Activity Diagram tuân theo tiêu chuẩn UML, trong khi Flowchart không có tiêu chuẩn cụ thể.

4. **Người thực hiện**: Activity Diagram có thể chỉ rõ ai thực hiện từng hoạt động thông qua làn (swimlanes), trong khi Flowchart thường không thể hiện điều này.

5. **Xử lý song song**: Activity Diagram hỗ trợ mạnh mẽ việc mô tả các hoạt động song song thông qua fork và join, trong khi Flowchart không có các ký hiệu cụ thể cho điều này.

## Tổng kết

Activity Diagram là một công cụ mạnh mẽ trong UML để mô tả các quy trình, luồng công việc, và thuật toán. Nó cung cấp một cách nhìn trực quan về cách các hoạt động được thực hiện, ai thực hiện chúng, và làm thế nào chúng phối hợp với nhau.

Activity Diagram đặc biệt hữu ích trong các tình huống sau:
- Mô tả quy trình nghiệp vụ phức tạp
- Phân tích use case chi tiết
- Mô tả các thuật toán với nhiều quyết định và xử lý song song
- Hiểu quy trình làm việc giữa các bên liên quan khác nhau

Với khả năng mô tả cả hoạt động tuần tự và song song, Activity Diagram là một trong những biểu đồ UML được sử dụng rộng rãi nhất trong thiết kế và phát triển phần mềm.

## Tham khảo

1. Visual Paradigm. (2023). Activity Diagram Tutorial. https://online.visual-paradigm.com/diagrams/tutorials/activity-diagram-tutorial/
2. Visual Paradigm. (2023). What is Activity Diagram? https://www.visual-paradigm.com/guide/uml-unified-modeling-language/what-is-activity-diagram/
3. Creately. (2022). Activity Diagram Tutorial | Easy Guide with Examples. https://creately.com/guides/activity-diagram-tutorial/
4. GeeksforGeeks. (2025). Activity Diagrams - Unified Modeling Language (UML). https://www.geeksforgeeks.org/unified-modeling-language-uml-activity-diagrams/
