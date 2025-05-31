# SƠ ĐỒ USE CASE (USE CASE DIAGRAM)

## Mục lục
1. [Giới thiệu về Use Case Diagram](#giới-thiệu-về-use-case-diagram)
2. [Các thành phần của Use Case Diagram](#các-thành-phần-của-use-case-diagram)
   - [Actor (Tác nhân)](#actor-tác-nhân)
   - [Use Case (Trường hợp sử dụng)](#use-case-trường-hợp-sử-dụng)
   - [Relationship (Mối quan hệ)](#relationship-mối-quan-hệ)
   - [System Boundary (Ranh giới hệ thống)](#system-boundary-ranh-giới-hệ-thống)
3. [Các loại mối quan hệ trong Use Case Diagram](#các-loại-mối-quan-hệ-trong-use-case-diagram)
   - [Association (Kết hợp)](#association-kết-hợp)
   - [Include (Bao gồm)](#include-bao-gồm)
   - [Extend (Mở rộng)](#extend-mở-rộng)
   - [Generalization (Tổng quát hóa)](#generalization-tổng-quát-hóa)
4. [Cách vẽ Use Case Diagram](#cách-vẽ-use-case-diagram)
5. [Lợi ích của Use Case Diagram](#lợi-ích-của-use-case-diagram)
6. [Business Use Case vs System Use Case](#business-use-case-vs-system-use-case)
7. [Các ví dụ về Use Case Diagram](#các-ví-dụ-về-use-case-diagram)
8. [Các lỗi thường gặp khi vẽ Use Case Diagram](#các-lỗi-thường-gặp-khi-vẽ-use-case-diagram)
9. [Các công cụ vẽ Use Case Diagram](#các-công-cụ-vẽ-use-case-diagram)
10. [Tổng kết](#tổng-kết)

## Giới thiệu về Use Case Diagram

Use Case Diagram (Sơ đồ trường hợp sử dụng) là một loại sơ đồ trong Ngôn ngữ Mô hình hóa Thống nhất (UML - Unified Modeling Language) được sử dụng để mô tả các tương tác giữa người dùng (actors) và hệ thống. Use Case Diagram cung cấp một cái nhìn tổng quan về các chức năng của hệ thống từ góc độ người dùng.

Use Case Diagram mô tả:
- **Hệ thống đang được mô tả là gì?** (system)
- **Ai đang sử dụng hệ thống?** (actors)
- **Người dùng muốn đạt được điều gì?** (use cases)

Use Case Diagram giúp đảm bảo rằng hệ thống đúng đắn được phát triển bằng cách nắm bắt các yêu cầu từ góc nhìn của người dùng.

Một Use Case là danh sách các hành động hoặc các bước sự kiện thường xác định các tương tác giữa một vai trò của actor và hệ thống để đạt được một mục tiêu. Use Case là một kỹ thuật hữu ích để xác định, làm rõ và tổ chức các yêu cầu hệ thống.

## Các thành phần của Use Case Diagram

Use Case Diagram bao gồm bốn thành phần chính:

### Actor (Tác nhân)

Actors là các thực thể bên ngoài tương tác với hệ thống. Actors có thể là:
- Con người (người dùng, khách hàng, quản trị viên...)
- Hệ thống bên ngoài khác
- Thiết bị phần cứng
- Thời gian (khi một sự kiện xảy ra tại một thời điểm cụ thể)

Actors được biểu diễn bằng biểu tượng hình người que (stick figure) với tên của actor bên dưới.

```
    O
   /|\
   / \
  Actor
```

### Use Case (Trường hợp sử dụng)

Use Case mô tả cách actors sử dụng hệ thống để hoàn thành một mục tiêu cụ thể. Use Case thường được khởi tạo bởi người dùng để đáp ứng các mục tiêu, mô tả các hoạt động và các biến thể liên quan đến việc đạt được mục tiêu.

Use Case được biểu diễn bằng hình elip với tên use case bên trong.

```
  ____________
 /            \
|   Use Case   |
 \____________/
```

### Relationship (Mối quan hệ)

Các mối quan hệ giữa actors và use cases, hoặc giữa các use cases với nhau.

### System Boundary (Ranh giới hệ thống)

Ranh giới hệ thống xác định hệ thống đang được quan tâm trong mối quan hệ với thế giới xung quanh nó. Nó được biểu diễn bằng một hình chữ nhật bao quanh các use case, với tên của hệ thống ở phía trên.

```
 ________________________
|      Tên Hệ Thống      |
|  ____________          |
| /            \         |
||   Use Case   |        |
| \____________/         |
|                        |
|________________________|
```

## Các loại mối quan hệ trong Use Case Diagram

### Association (Kết hợp)

Mối quan hệ Association là mối quan hệ cơ bản giữa actor và use case, cho biết actor tham gia vào use case đó. Nó được biểu diễn bằng một đường thẳng nối actor và use case.

```
   O
  /|\    ____________
  / \---/            \
 Actor  |   Use Case   |
        \____________/
```

### Include (Bao gồm)

Mối quan hệ Include được sử dụng khi một use case bao gồm chức năng của một use case khác như một phần của luồng cơ bản của nó. Nó được biểu diễn bằng một mũi tên nét đứt với nhãn `<<include>>`.

```
  ____________           ____________
 /            \         /            \
|   Use Case   |------>|  Use Case B  |
 \____________/<<include>>\____________/
```

Khi nào sử dụng Include:
- Khi bạn có một phần chức năng chung được sử dụng bởi nhiều use case
- Để tránh lặp lại mô tả trong nhiều use case
- Khi luồng bao gồm luôn được thực hiện

### Extend (Mở rộng)

Mối quan hệ Extend được sử dụng khi một use case mở rộng chức năng của use case khác bằng cách thêm các bước hoặc hành động vào luồng cơ bản. Nó được biểu diễn bằng một mũi tên nét đứt với nhãn `<<extend>>`.

```
  ____________           ____________
 /            \         /            \
|   Use Case   |<------|  Use Case B  |
 \____________/<<extend>>\____________/
```

Khi nào sử dụng Extend:
- Khi bạn có một luồng tùy chọn hoặc điều kiện
- Khi luồng mở rộng chỉ được thực hiện trong một số trường hợp cụ thể
- Để mô tả các biến thể hoặc ngoại lệ của use case cơ bản

### Generalization (Tổng quát hóa)

Mối quan hệ Generalization thể hiện quan hệ kế thừa giữa các use case hoặc giữa các actor. Use case con kế thừa hành vi và ý nghĩa của use case cha, và có thể thêm hoặc ghi đè hành vi. Nó được biểu diễn bằng một mũi tên rỗng từ use case con đến use case cha.

```
  ____________           ____________
 /            \         /            \
|  Use Case A  |--------|  Use Case B  |
 \____________/         \____________/
       ^                       ^
       |                       |
  ____________           ____________
 /            \         /            \
|  Use Case C  |        |  Use Case D  |
 \____________/         \____________/
```

## Cách vẽ Use Case Diagram

Để vẽ một Use Case Diagram hiệu quả, hãy tuân theo các bước sau:

1. **Xác định ranh giới hệ thống**: Vẽ một hình chữ nhật đại diện cho hệ thống của bạn và đặt tên cho nó.

2. **Xác định các actors**: Xác định tất cả các actors (người dùng hoặc hệ thống bên ngoài) tương tác với hệ thống của bạn.
   - Đối với mỗi loại người dùng, xác định tất cả các vai trò được đóng bởi người dùng liên quan đến hệ thống.

3. **Xác định các use cases**: Xác định những gì người dùng yêu cầu hệ thống thực hiện để đạt được các mục tiêu của họ.
   - Tạo use case cho mỗi mục tiêu.
   - Đặt tên cho use case bằng động từ + danh từ (ví dụ: "Đặt hàng", "Thanh toán hóa đơn").

4. **Xây dựng cấu trúc use cases**:
   - Xác định các mối quan hệ giữa use cases (include, extend, generalization).
   - Sắp xếp các use case theo nhóm logic nếu cần thiết.

5. **Ưu tiên, đánh giá và xác thực**: Ưu tiên các use cases, đánh giá và xác thực chúng với người dùng.

Lưu ý: Để làm cho phương pháp use case trở nên "Agile" hơn, đừng chi tiết hóa tất cả các use cases, mà hãy ưu tiên chúng trong product backlog. Bạn nên tinh chỉnh use case ở các mức độ chi tiết khác nhau theo giai đoạn phát triển với cách tiếp cận "vừa đủ, đúng lúc".

## Lợi ích của Use Case Diagram

1. Use cases là một kỹ thuật mạnh mẽ để thu thập và tài liệu hóa các yêu cầu chức năng black-box.

2. Use cases dễ hiểu và cung cấp một cách tuyệt vời để giao tiếp với khách hàng và người dùng vì chúng được viết bằng ngôn ngữ tự nhiên.

3. Use cases có thể giúp quản lý độ phức tạp của các dự án lớn bằng cách phân chia vấn đề thành các tính năng người dùng chính (tức là use cases) và bằng cách chỉ định ứng dụng từ góc độ người dùng.

4. Một kịch bản use case, thường được biểu diễn bằng sequence diagram, liên quan đến sự cộng tác của nhiều đối tượng và lớp. Use cases giúp xác định các thông điệp (các hoạt động và thông tin hoặc dữ liệu cần thiết - tham số) kết nối các đối tượng và lớp lại với nhau.

5. Use cases cung cấp cơ sở tốt để liên kết giữa việc xác minh các mô hình cấp cao hơn (tức là tương tác giữa actors và một tập hợp các đối tượng cộng tác), và sau đó, để xác thực các yêu cầu chức năng (tức là bản thiết kế của white-box test).

6. Phương pháp tiếp cận dựa trên use case cung cấp các liên kết có thể theo dõi cho việc theo dõi dự án, trong đó các hoạt động phát triển chính như các use cases được triển khai, kiểm thử và giao hàng đáp ứng các mục tiêu và mục đích từ quan điểm của người dùng.

## Business Use Case vs System Use Case

### Business Use Case

Business Use Case được mô tả bằng **thuật ngữ không liên quan đến công nghệ** xem quy trình kinh doanh như một hộp đen và mô tả quy trình kinh doanh được sử dụng bởi các business actors. Business Use Case đại diện cho cách thức công việc được thực hiện theo cách thủ công trong tình huống hiện tại và không nhất thiết phải được thực hiện bởi hệ thống hoặc có ý định tự động hóa trong phạm vi của hệ thống mục tiêu.

### System Use Case

System Use Case thường được mô tả ở **cấp độ chức năng hệ thống** và chỉ định chức năng hoặc dịch vụ mà hệ thống cung cấp cho người dùng. System Use Case tập trung vào các chức năng cụ thể mà hệ thống phần mềm sẽ thực hiện.

## Các ví dụ về Use Case Diagram

### Ví dụ 1: Hệ thống ATM

```
 _______________________________
|          Hệ thống ATM         |
|                               |
|   ____________                |
|  /            \               |
| | Rút tiền     |              |
|  \____________/<------\       |
|                       |       |
|   ____________        |       |
|  /            \       |       |
| | Kiểm tra số |       |       |
| |    dư       |       |       |
|  \____________/       |       |
|                       |       |
|   ____________        |       |
|  /            \       |       |
| | Chuyển tiền |       |       |
|  \____________/       |       |
|                       |       |
|   ____________        |       |
|  /            \       |       |
| | Đổi mật khẩu|       |       |
|  \____________/       |       |
|                       |       |
|_______________________|       |
          ^                     |
          |                     |
          |                     |
     O    |                     |
    /|\---/                     |
    / \                         |
 Khách hàng                     |
                                |
     O                          |
    /|\-------------------------|
    / \                         |
  Ngân hàng                     |
```

### Ví dụ 2: Hệ thống Quản lý Đặt Hàng Trực Tuyến

```
 _______________________________________
|    Hệ thống Quản lý Đặt Hàng Trực Tuyến|
|                                       |
|   ____________        ____________    |
|  /            \      /            \   |
| | Đăng ký     |     | Đăng nhập   |   |
|  \____________/      \____________/   |
|                                       |
|   ____________        ____________    |
|  /            \      /            \   |
| | Tìm kiếm    |     | Xem chi tiết|   |
| | sản phẩm    |---->| sản phẩm    |   |
|  \____________/      \____________/   |
|                                       |
|   ____________        ____________    |
|  /            \      /            \   |
| | Thêm vào    |     | Thanh toán  |   |
| | giỏ hàng    |---->|             |   |
|  \____________/      \____________/   |
|         |               ^             |
|         |               |             |
|         v               |             |
|   ____________        ____________    |
|  /            \      /            \   |
| | Quản lý     |     | Xác nhận    |   |
| | giỏ hàng    |---->| đơn hàng    |   |
|  \____________/      \____________/   |
|                                       |
|_______________________________________|
          ^                 ^
          |                 |
          |                 |
     O    |                 |
    /|\---/                 |
    / \                     |
  Khách hàng                |
                            |
     O                      |
    /|\---------------------/
    / \
  Quản trị viên
```

## Các lỗi thường gặp khi vẽ Use Case Diagram

1. **Quá chi tiết**: Use Case Diagram nên cung cấp cái nhìn tổng quan về chức năng hệ thống, không nên đi vào chi tiết triển khai.

2. **Thiếu actors**: Đảm bảo xác định tất cả các actors liên quan đến hệ thống, bao gồm cả hệ thống bên ngoài.

3. **Use case không đúng**: Use case nên mô tả một mục tiêu của người dùng, không phải một chức năng hệ thống. Ví dụ, "Đăng nhập" là một use case tốt, nhưng "Kiểm tra thông tin đăng nhập" không phải.

4. **Lạm dụng mối quan hệ**: Chỉ sử dụng các mối quan hệ include, extend và generalization khi thực sự cần thiết.

5. **Thiếu ranh giới hệ thống**: Ranh giới hệ thống giúp xác định phạm vi của hệ thống và nên được bao gồm trong sơ đồ.

6. **Đặt tên không rõ ràng**: Tên của use case nên rõ ràng và mô tả mục tiêu của người dùng.

## Các công cụ vẽ Use Case Diagram

Có nhiều công cụ có thể được sử dụng để vẽ Use Case Diagram:

1. **Visual Paradigm**: Một công cụ UML mạnh mẽ với phiên bản miễn phí cho mục đích phi thương mại.

2. **Lucidchart**: Công cụ vẽ sơ đồ trực tuyến với các mẫu Use Case Diagram.

3. **Draw.io**: Công cụ vẽ sơ đồ miễn phí với nhiều mẫu UML.

4. **StarUML**: Công cụ mô hình hóa UML mã nguồn mở.

5. **Microsoft Visio**: Công cụ vẽ sơ đồ chuyên nghiệp từ Microsoft.

6. **Enterprise Architect**: Công cụ mô hình hóa UML chuyên nghiệp cho doanh nghiệp.

## Tổng kết

Use Case Diagram là một công cụ mạnh mẽ để hiểu và truyền đạt các yêu cầu hệ thống từ góc độ người dùng. Bằng cách xác định actors, use cases và mối quan hệ giữa chúng, Use Case Diagram cung cấp một cái nhìn tổng quan về chức năng của hệ thống và cách nó tương tác với người dùng và các hệ thống bên ngoài.

Khi tạo Use Case Diagram, hãy nhớ giữ cho nó đơn giản, tập trung vào mục tiêu của người dùng và sử dụng các mối quan hệ một cách thích hợp. Use Case Diagram là bước đầu tiên trong quá trình phát triển phần mềm và nên được bổ sung bằng các mô tả chi tiết hơn về từng use case.
