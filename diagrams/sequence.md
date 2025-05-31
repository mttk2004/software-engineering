# SƠ ĐỒ TRÌNH TỰ (SEQUENCE DIAGRAM)

## Mục lục
1. [Giới thiệu về Sequence Diagram](#giới-thiệu-về-sequence-diagram)
2. [Các thành phần của Sequence Diagram](#các-thành-phần-của-sequence-diagram)
   - [Đối tượng (Object)](#đối-tượng-object)
   - [Đường đời (Lifeline)](#đường-đời-lifeline)
   - [Thông điệp (Message)](#thông-điệp-message)
   - [Tiêu điểm điều khiển (Focus of Control)](#tiêu-điểm-điều-khiển-focus-of-control)
   - [Tạo và hủy đối tượng](#tạo-và-hủy-đối-tượng)
   - [Phân mảnh kết hợp (Combined Fragment)](#phân-mảnh-kết-hợp-combined-fragment)
3. [Khi nào nên sử dụng Sequence Diagram](#khi-nào-nên-sử-dụng-sequence-diagram)
4. [Cách vẽ Sequence Diagram](#cách-vẽ-sequence-diagram)
5. [Ví dụ về Sequence Diagram](#ví-dụ-về-sequence-diagram)
   - [Quy trình đặt hàng](#quy-trình-đặt-hàng)
   - [Quy trình xác thực người dùng](#quy-trình-xác-thực-người-dùng)
   - [Quy trình rút tiền từ ATM](#quy-trình-rút-tiền-từ-atm)
6. [Sự khác biệt giữa Sequence Diagram và Communication Diagram](#sự-khác-biệt-giữa-sequence-diagram-và-communication-diagram)
7. [Tổng kết](#tổng-kết)
8. [Tham khảo](#tham-khảo)

## Giới thiệu về Sequence Diagram

Sequence Diagram (Sơ đồ trình tự) là một loại sơ đồ tương tác trong UML (Unified Modeling Language) được sử dụng để mô tả các tương tác giữa các đối tượng theo thứ tự thời gian. Sequence Diagram nhấn mạnh vào trình tự của các thông điệp được trao đổi giữa các đối tượng để thực hiện một chức năng cụ thể.

Sequence Diagram miêu tả:
- Các đối tượng và lớp tham gia vào kịch bản
- Trình tự các thông điệp được trao đổi giữa các đối tượng
- Thời gian và thứ tự của các tương tác

Sequence Diagram đặc biệt hữu ích trong việc mô tả hành vi động của một hệ thống bằng cách hiển thị các tương tác giữa các đối tượng theo thời gian. Thông thường, một Sequence Diagram được sử dụng để chỉ định luồng chính của một use case, và các biến thể của sơ đồ đó được sử dụng để chỉ định các luồng ngoại lệ.

## Các thành phần của Sequence Diagram

### Đối tượng (Object)

- **Ký hiệu**: Hình chữ nhật chứa tên của đối tượng, được gạch dưới
- **Mục đích**: Biểu thị các thực thể tham gia vào tương tác
- **Đặc điểm**: Một đối tượng có thể được đặt tên theo một trong ba cách:
  - Tên đối tượng (ví dụ: myAccount)
  - Tên đối tượng và lớp (ví dụ: myAccount:Account)
  - Chỉ tên lớp (đối tượng ẩn danh, ví dụ: :Account)

### Đường đời (Lifeline)

- **Ký hiệu**: Đường đứt nét kéo dài xuống từ đối tượng
- **Mục đích**: Biểu thị sự tồn tại của đối tượng trong thời gian
- **Đặc điểm**: Thời gian trong Sequence Diagram trôi từ trên xuống dưới

### Thông điệp (Message)

- **Ký hiệu**: Mũi tên nối giữa các đường đời của đối tượng
- **Mục đích**: Biểu thị sự giao tiếp giữa các đối tượng
- **Đặc điểm**: Có nhiều loại thông điệp:
  - **Thông điệp đồng bộ (Synchronous Message)**: Mũi tên với đầu đặc, người gửi đợi phản hồi trước khi tiếp tục
  - **Thông điệp trả về (Return Message)**: Mũi tên đứt nét với đầu mở
  - **Thông điệp bất đồng bộ (Asynchronous Message)**: Mũi tên với đầu mở, người gửi tiếp tục thực hiện mà không đợi phản hồi
  - **Thông điệp tạo (Create Message)**: Tạo một đối tượng mới
  - **Thông điệp hủy (Destroy Message)**: Hủy một đối tượng

### Tiêu điểm điều khiển (Focus of Control)

- **Ký hiệu**: Hình chữ nhật dọc trên đường đời
- **Mục đích**: Biểu thị thời gian mà đối tượng đang thực hiện một hoạt động
- **Đặc điểm**: Đỉnh và đáy của hình chữ nhật tương ứng với thời điểm bắt đầu và kết thúc của hoạt động

### Tạo và hủy đối tượng

- **Tạo đối tượng**: Mũi tên với từ khóa `<<create>>` chỉ đến một đối tượng mới
- **Hủy đối tượng**: Mũi tên với từ khóa `<<destroy>>` chỉ đến một đối tượng, hoặc dấu X ở cuối đường đời

### Phân mảnh kết hợp (Combined Fragment)

- **Ký hiệu**: Hình chữ nhật với nhãn ở góc trên bên trái
- **Mục đích**: Biểu thị các cấu trúc điều khiển và các tương tác phức tạp
- **Đặc điểm**: Có nhiều loại phân mảnh:
  - **alt (Alternative)**: Chọn một trong nhiều luồng dựa trên điều kiện
  - **opt (Optional)**: Thực hiện luồng chỉ khi điều kiện đúng
  - **loop (Loop)**: Lặp lại luồng dựa trên điều kiện
  - **par (Parallel)**: Thực hiện các luồng song song
  - **critical (Critical Region)**: Khu vực mà chỉ một luồng có thể thực hiện tại một thời điểm
  - **ref (Reference)**: Tham chiếu đến sơ đồ tương tác khác
  - **neg (Negative)**: Biểu thị tương tác không hợp lệ
  - **sd (Sequence Diagram)**: Bao quanh toàn bộ sơ đồ trình tự

## Khi nào nên sử dụng Sequence Diagram

Sequence Diagram nên được sử dụng trong các trường hợp sau:

1. **Mô tả chi tiết các use case**: Để hiểu rõ cách các đối tượng tương tác với nhau để thực hiện một use case.

2. **Phân tích yêu cầu**: Để xác định các chức năng và thông điệp cần thiết cho hệ thống.

3. **Thiết kế chi tiết**: Để chỉ định cách các đối tượng và thành phần trong hệ thống tương tác với nhau.

4. **Mô tả các giao thức**: Để mô tả cách các thành phần hoặc hệ thống giao tiếp với nhau thông qua các giao thức.

5. **Tài liệu hóa các kịch bản sử dụng**: Để tài liệu hóa các kịch bản sử dụng cụ thể và cách hệ thống xử lý chúng.

6. **Phát hiện các thành phần và hoạt động**: Để phát hiện các thành phần và hoạt động cần thiết trong hệ thống.

7. **Mô tả các tương tác phức tạp**: Đặc biệt là các tương tác có trình tự thời gian quan trọng.

## Cách vẽ Sequence Diagram

### Bước 1: Xác định phạm vi và mục đích

- Xác định kịch bản hoặc use case cần mô hình hóa
- Xác định mức độ chi tiết cần thiết
- Xác định các đối tượng tham gia vào kịch bản

### Bước 2: Xác định các đối tượng tham gia

- Liệt kê tất cả các đối tượng tham gia vào kịch bản
- Sắp xếp các đối tượng theo thứ tự từ trái sang phải, thường bắt đầu với người dùng hoặc hệ thống bên ngoài

### Bước 3: Xác định các tương tác giữa các đối tượng

- Xác định các thông điệp được trao đổi giữa các đối tượng
- Xác định thứ tự thời gian của các thông điệp

### Bước 4: Xác định các điều kiện và luồng điều khiển

- Xác định các điều kiện cho các thông điệp
- Xác định các luồng điều khiển (if-else, loops, parallel) bằng các phân mảnh kết hợp

### Bước 5: Vẽ sơ đồ

1. Vẽ các đối tượng tham gia ở phía trên sơ đồ
2. Vẽ các đường đời xuống từ mỗi đối tượng
3. Vẽ các thông điệp giữa các đường đời theo thứ tự thời gian
4. Thêm các tiêu điểm điều khiển khi cần thiết
5. Thêm các phân mảnh kết hợp để biểu diễn các luồng điều khiển phức tạp

### Bước 6: Kiểm tra và tinh chỉnh

- Kiểm tra tính đúng đắn và đầy đủ của sơ đồ
- Đảm bảo rằng tất cả các thông điệp đều có nguồn gốc và đích rõ ràng
- Đảm bảo rằng các tương tác phản ánh đúng kịch bản

## Ví dụ về Sequence Diagram

### Quy trình đặt hàng

Dưới đây là một ví dụ về quy trình đặt hàng trong một hệ thống thương mại điện tử:

```
Customer          Order           Stock
   |                |               |
   |---create()---->|               |
   |                |               |
   |---addItem()---->               |
   |                |---check()---->|
   |                |<---available--|
   |                |---add()------>|
   |<---added()-----|               |
   |                |               |
   |---save()------>|               |
   |<---saved()-----|               |
   |                |               |
   X                |               |
```

### Quy trình xác thực người dùng

Ví dụ về quy trình xác thực người dùng:

```
User           LoginUI         AuthService      UserDatabase
  |               |                |                |
  |--login()----->|                |                |
  |               |--authenticate->|                |
  |               |                |--findUser()-->|
  |               |                |<--userInfo----|
  |               |                |--validatePwd->|
  |               |                |<--isValid-----|
  |               |<--authResult---|                |
  |<--loginResult-|                |                |
  |               |                |                |
```

### Quy trình rút tiền từ ATM

Ví dụ về quy trình rút tiền từ máy ATM:

```
Customer        ATM            BankServer       Account
   |             |                 |               |
   |--insertCard->|                 |               |
   |             |--validateCard-->|                |
   |             |<--cardValid-----|                |
   |<--requestPIN-|                 |               |
   |--enterPIN-->|                 |               |
   |             |--validatePIN--->|                |
   |             |<--pinValid------|                |
   |<--showOptions|                 |               |
   |--selectWithdraw->|             |               |
   |             |--requestAmount-->|               |
   |<--promptAmount|                |               |
   |--enterAmount->|                |               |
   |             |--withdraw()----->|--debit()----->|
   |             |                 |<--debited-----|
   |             |<--withdrawOK----|                |
   |<--dispenseCash|                |               |
   |<--printReceipt|                |               |
   |<--ejectCard--|                |                |
   |--takeCard-->|                 |               |
   |--takeCash-->|                 |               |
   |             |                 |               |
```

## Sự khác biệt giữa Sequence Diagram và Communication Diagram

Cả Sequence Diagram và Communication Diagram (Collaboration Diagram) đều là các loại sơ đồ tương tác trong UML, nhưng chúng khác nhau ở một số điểm quan trọng:

1. **Trọng tâm**: Sequence Diagram nhấn mạnh vào trình tự thời gian của các thông điệp, trong khi Communication Diagram nhấn mạnh vào cấu trúc tổng thể của các đối tượng và mối quan hệ giữa chúng.

2. **Cách biểu diễn thời gian**: Trong Sequence Diagram, thời gian được biểu diễn trực quan từ trên xuống dưới. Trong Communication Diagram, thời gian được biểu diễn gián tiếp thông qua số thứ tự của các thông điệp.

3. **Bố cục**: Sequence Diagram có bố cục dọc với các đường đời kéo dài xuống, trong khi Communication Diagram có bố cục tự do hơn với các đối tượng được sắp xếp theo cách thể hiện mối quan hệ giữa chúng.

4. **Số lượng đối tượng**: Sequence Diagram có thể trở nên khó đọc khi có nhiều đối tượng, trong khi Communication Diagram có thể xử lý nhiều đối tượng hiệu quả hơn.

5. **Chi tiết tương tác**: Sequence Diagram cung cấp nhiều chi tiết hơn về các tương tác và luồng điều khiển, trong khi Communication Diagram tập trung vào các liên kết giữa các đối tượng.

## Tổng kết

Sequence Diagram là một công cụ mạnh mẽ trong UML để mô tả các tương tác giữa các đối tượng theo thứ tự thời gian. Nó cung cấp một cách trực quan để hiểu cách các đối tượng giao tiếp với nhau để thực hiện một chức năng cụ thể.

Sequence Diagram đặc biệt hữu ích trong các tình huống sau:
- Mô tả chi tiết các use case
- Phân tích yêu cầu và thiết kế chi tiết
- Mô tả các giao thức và tương tác phức tạp
- Tài liệu hóa các kịch bản sử dụng

Với khả năng biểu diễn trình tự thời gian của các tương tác và các cấu trúc điều khiển phức tạp, Sequence Diagram là một trong những sơ đồ UML quan trọng nhất trong thiết kế và phát triển phần mềm hướng đối tượng.

## Tham khảo

1. Visual Paradigm. (2023). Sequence Diagram Tutorial. https://www.visual-paradigm.com/learning/handbooks/software-design-handbook/sequence-diagram.jsp
2. Visual Paradigm. (2023). How to Draw a Sequence Diagram in UML. https://www.visual-paradigm.com/support/documents/vpuserguide/94/2577/7025_drawingseque.html
3. Lucidchart. (2022). UML Sequence Diagram Tutorial. https://www.lucidchart.com/pages/uml-sequence-diagram
4. GeeksforGeeks. (2023). UML Sequence Diagrams. https://www.geeksforgeeks.org/unified-modeling-language-uml-sequence-diagrams/
