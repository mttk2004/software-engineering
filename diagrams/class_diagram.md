# SƠ ĐỒ LỚP (CLASS DIAGRAM)

## Mục lục
1. [Giới thiệu về Class Diagram](#giới-thiệu-về-class-diagram)
2. [Lớp (Class) là gì?](#lớp-class-là-gì)
3. [Ký hiệu trong Class Diagram](#ký-hiệu-trong-class-diagram)
   - [Lớp (Class)](#lớp-class)
   - [Thuộc tính (Attribute)](#thuộc-tính-attribute)
   - [Phương thức (Operation/Method)](#phương-thức-operationmethod)
   - [Phạm vi truy cập (Visibility)](#phạm-vi-truy-cập-visibility)
4. [Các mối quan hệ trong Class Diagram](#các-mối-quan-hệ-trong-class-diagram)
   - [Kế thừa (Inheritance/Generalization)](#kế-thừa-inheritancegeneralization)
   - [Liên kết (Association)](#liên-kết-association)
   - [Tập hợp (Aggregation)](#tập-hợp-aggregation)
   - [Hợp thành (Composition)](#hợp-thành-composition)
   - [Phụ thuộc (Dependency)](#phụ-thuộc-dependency)
   - [Hiện thực hóa (Realization)](#hiện-thực-hóa-realization)
5. [Bội số (Multiplicity)](#bội-số-multiplicity)
6. [Góc nhìn của Class Diagram](#góc-nhìn-của-class-diagram)
7. [Khi nào nên sử dụng Class Diagram?](#khi-nào-nên-sử-dụng-class-diagram)
8. [Cách vẽ Class Diagram](#cách-vẽ-class-diagram)
9. [Các ví dụ về Class Diagram](#các-ví-dụ-về-class-diagram)
   - [Ví dụ 1: Hệ thống đặt hàng](#ví-dụ-1-hệ-thống-đặt-hàng)
   - [Ví dụ 2: Mô hình xe hơi](#ví-dụ-2-mô-hình-xe-hơi)
10. [Các lỗi thường gặp khi vẽ Class Diagram](#các-lỗi-thường-gặp-khi-vẽ-class-diagram)
11. [Công cụ vẽ Class Diagram](#công-cụ-vẽ-class-diagram)
12. [Tổng kết](#tổng-kết)

## Giới thiệu về Class Diagram

Class Diagram (Sơ đồ lớp) là một loại sơ đồ cấu trúc tĩnh trong Ngôn ngữ Mô hình hóa Thống nhất (UML - Unified Modeling Language), được sử dụng để mô tả cấu trúc của một hệ thống bằng cách hiển thị:

- Các lớp trong hệ thống
- Thuộc tính của các lớp
- Phương thức (hoạt động) của các lớp
- Mối quan hệ giữa các lớp

Class Diagram là một công cụ quan trọng trong thiết kế hướng đối tượng và được sử dụng rộng rãi trong quá trình phát triển phần mềm. Nó giúp các nhà phát triển và các bên liên quan hiểu cấu trúc của hệ thống và cách các thành phần khác nhau tương tác với nhau.

## Lớp (Class) là gì?

Một lớp (class) là một bản thiết kế (blueprint) cho một đối tượng. Lớp và đối tượng luôn đi đôi với nhau. Chúng ta không thể nói về cái này mà không đề cập đến cái kia. Toàn bộ điểm của Thiết kế Hướng Đối tượng không phải là về đối tượng, mà là về lớp, bởi vì chúng ta sử dụng lớp để tạo ra đối tượng. Vì vậy, một lớp mô tả đối tượng sẽ là gì, nhưng nó không phải là bản thân đối tượng.

Trên thực tế, các lớp mô tả kiểu của đối tượng, trong khi đối tượng là các thể hiện (instances) có thể sử dụng của lớp. Mỗi đối tượng được xây dựng từ cùng một bộ bản thiết kế và do đó chứa các thành phần giống nhau (thuộc tính và phương thức). Ý nghĩa tiêu chuẩn là một đối tượng là một thể hiện của một lớp và đối tượng có trạng thái và hành vi.

### Ví dụ:

Một con chó có các trạng thái - màu sắc, tên, giống, cũng như các hành vi - vẫy đuôi, sủa, ăn. Một đối tượng là một thể hiện của một lớp.

```
Lớp: Dog (Chó)
- Thuộc tính: color, name, breed
- Phương thức: wag(), bark(), eat()

Đối tượng: myDog (một thể hiện cụ thể của lớp Dog)
- color = "Nâu"
- name = "Rex"
- breed = "Labrador"
```

## Ký hiệu trong Class Diagram

### Lớp (Class)

Trong UML, một lớp được biểu diễn bằng một hình chữ nhật chia thành ba phần:

```
┌───────────────────┐
│     Class Name    │ <- Tên lớp
├───────────────────┤
│    attributes     │ <- Thuộc tính
├───────────────────┤
│    operations     │ <- Phương thức
└───────────────────┘
```

**Tên lớp:**
- Tên của lớp xuất hiện ở phần đầu tiên.
- Tên lớp thường được viết hoa chữ cái đầu và in đậm.
- Tên của lớp trừu tượng (abstract class) được hiển thị bằng chữ nghiêng.

### Thuộc tính (Attribute)

Thuộc tính được hiển thị trong phần thứ hai của hình chữ nhật. Mỗi thuộc tính được liệt kê trên một dòng riêng biệt theo định dạng:

```
[phạm vi truy cập] tên : kiểu dữ liệu [= giá trị mặc định] [các ràng buộc]
```

Ví dụ:
```
+ name: String
- age: Integer = 0
# height: Float
```

### Phương thức (Operation/Method)

Phương thức được hiển thị trong phần thứ ba của hình chữ nhật. Mỗi phương thức được liệt kê trên một dòng riêng biệt theo định dạng:

```
[phạm vi truy cập] tên(danh sách tham số) : kiểu trả về
```

Ví dụ:
```
+ getName(): String
- calculateAge(): Integer
# setHeight(h: Float): void
```

### Phạm vi truy cập (Visibility)

Phạm vi truy cập được biểu thị bằng các ký hiệu đặt trước tên thuộc tính hoặc phương thức:

- `+`: Public - Có thể truy cập từ bất kỳ đâu
- `-`: Private - Chỉ có thể truy cập từ bên trong lớp
- `#`: Protected - Chỉ có thể truy cập từ bên trong lớp và các lớp con
- `~`: Package/Default - Có thể truy cập từ các lớp trong cùng gói

## Các mối quan hệ trong Class Diagram

### Kế thừa (Inheritance/Generalization)

Kế thừa là mối quan hệ phân loại giữa một phân loại chung hơn (lớp cha) và một phân loại cụ thể hơn (lớp con). Mỗi thể hiện của lớp con cũng là một thể hiện gián tiếp của lớp cha. Do đó, lớp con kế thừa các đặc điểm của lớp cha.

- Biểu diễn mối quan hệ "is-a" (là một).
- Tên của lớp trừu tượng được hiển thị bằng chữ nghiêng.
- SubClass1 và SubClass2 là các đặc biệt hóa của SuperClass.

Kế thừa được biểu diễn bằng một đường liền với một mũi tên rỗng chỉ từ lớp con đến lớp cha.

```
    ┌─────────┐
    │SuperClass│
    └─────────┘
        ▲
        │
  ┌─────┴─────┐
  │           │
┌─┴──┐     ┌──┴─┐
│Sub1│     │Sub2│
└────┘     └────┘
```

### Liên kết (Association)

Liên kết là mối quan hệ giữa các lớp trong Class Diagram. Chúng được biểu diễn bằng một đường thẳng giữa các lớp. Liên kết thường được đặt tên bằng một động từ hoặc cụm động từ phản ánh miền vấn đề thực tế.

#### Liên kết đơn giản

- Một liên kết cấu trúc giữa hai lớp ngang hàng.
- Có một liên kết giữa Class1 và Class2.

Liên kết đơn giản được biểu diễn bằng một đường thẳng kết nối hai lớp.

```
┌────────┐         ┌────────┐
│ Class1 │─────────│ Class2 │
└────────┘         └────────┘
```

### Tập hợp (Aggregation)

Tập hợp là một loại liên kết đặc biệt.

- Nó biểu diễn mối quan hệ "một phần của" (part-of).
- Class2 là một phần của Class1.
- Nhiều thể hiện (được ký hiệu bởi *) của Class2 có thể được liên kết với Class1.
- Các đối tượng của Class1 và Class2 có vòng đời riêng biệt.

Tập hợp được biểu diễn bằng một đường liền với một hình thoi rỗng ở đầu liên kết, kết nối với lớp đại diện cho tập hợp.

```
┌────────┐         ┌────────┐
│ Class1 │◇────────│ Class2 │
└────────┘         └────────┘
```

### Hợp thành (Composition)

- Một loại tập hợp đặc biệt trong đó các phần bị hủy khi tổng thể bị hủy.
- Các đối tượng của Class2 sống và chết cùng với Class1.
- Class2 không thể tồn tại độc lập.

Hợp thành được biểu diễn bằng một đường liền với một hình thoi đặc ở đầu liên kết, kết nối với lớp đại diện cho tổng thể hoặc hợp thành.

```
┌────────┐         ┌────────┐
│ Class1 │◆────────│ Class2 │
└────────┘         └────────┘
```

### Phụ thuộc (Dependency)

Một đối tượng của một lớp có thể sử dụng một đối tượng của lớp khác trong mã của một phương thức. Nếu đối tượng không được lưu trữ trong bất kỳ trường nào, thì điều này được mô hình hóa như một mối quan hệ phụ thuộc.

- Một loại liên kết đặc biệt.
- Tồn tại giữa hai lớp nếu thay đổi định nghĩa của một lớp có thể gây ra thay đổi cho lớp kia (nhưng không theo chiều ngược lại).
- Class1 phụ thuộc vào Class2.

Phụ thuộc được biểu diễn bằng một đường đứt nét với một mũi tên mở.

```
┌────────┐         ┌────────┐
│ Class1 │- - - - >│ Class2 │
└────────┘         └────────┘
```

### Hiện thực hóa (Realization)

Hiện thực hóa là mối quan hệ giữa lớp bản thiết kế và đối tượng chứa các chi tiết cấp triển khai tương ứng của nó. Đối tượng này được gọi là hiện thực hóa lớp bản thiết kế. Nói cách khác, bạn có thể hiểu điều này như mối quan hệ giữa giao diện và lớp triển khai.

Ví dụ, giao diện Owner có thể chỉ định các phương thức để mua tài sản và bán tài sản. Các lớp Person và Corporation cần triển khai các phương thức này, có thể theo những cách rất khác nhau.

Hiện thực hóa được biểu diễn bằng một đường đứt nét với một mũi tên rỗng chỉ đến giao diện.

```
┌────────┐         ┌────────┐
│Interface│<- - - -│  Class │
└────────┘         └────────┘
```

## Bội số (Multiplicity)

Bội số chỉ định số lượng thể hiện của một lớp có thể liên quan đến một thể hiện của lớp khác. Bội số được đặt gần các đầu của liên kết. Các ký hiệu này cho biết số lượng thể hiện của một lớp được liên kết với một thể hiện của lớp khác.

Ví dụ, một công ty sẽ có một hoặc nhiều nhân viên, nhưng mỗi nhân viên chỉ làm việc cho một công ty.

Các ký hiệu bội số phổ biến:
- `1`: Chính xác một
- `0..1`: Không hoặc một
- `*`: Không hoặc nhiều
- `1..*`: Một hoặc nhiều
- `5..10`: Từ 5 đến 10

```
┌────────┐         ┌────────┐
│ Company│1────1..*│Employee│
└────────┘         └────────┘
```

## Góc nhìn của Class Diagram

Lựa chọn góc nhìn phụ thuộc vào việc bạn đã tiến xa đến đâu trong quá trình phát triển. Trong quá trình xây dựng mô hình miền (domain model), ví dụ, bạn hiếm khi vượt qua góc nhìn khái niệm. Các mô hình phân tích (analysis models) thường có sự kết hợp giữa góc nhìn khái niệm và đặc tả. Phát triển mô hình thiết kế (design model) thường bắt đầu với sự nhấn mạnh vào góc nhìn đặc tả, và phát triển thành góc nhìn triển khai.

Một sơ đồ có thể được diễn giải từ nhiều góc nhìn:

- **Khái niệm (Conceptual)**: đại diện cho các khái niệm trong miền
- **Đặc tả (Specification)**: tập trung vào các giao diện của Kiểu Dữ liệu Trừu tượng (ADTs) trong phần mềm
- **Triển khai (Implementation)**: mô tả cách các lớp sẽ triển khai giao diện của chúng

Góc nhìn ảnh hưởng đến lượng chi tiết cần cung cấp và các loại mối quan hệ đáng trình bày. Như đã đề cập ở trên, tên lớp là thông tin bắt buộc duy nhất.

## Khi nào nên sử dụng Class Diagram?

Hầu hết các sơ đồ UML không thể được ánh xạ trực tiếp với bất kỳ ngôn ngữ lập trình hướng đối tượng nào ngoại trừ class diagram. Nói cách khác, class diagram lý tưởng có thể có ánh xạ một-một với các sơ đồ lớp UML. Ngoài ra, class diagram hữu ích trong các tình huống sau:

1. Mô tả cái nhìn tĩnh của hệ thống.
2. Mô hình hóa sự hợp tác giữa các phần tử của cái nhìn tĩnh.
3. Mô tả các chức năng được thực hiện bởi hệ thống.
4. Xây dựng các ứng dụng phần mềm bằng các ngôn ngữ hướng đối tượng.
5. Thực hiện kỹ thuật chuyển tiếp mã cho các hệ thống mục tiêu.
6. Phân loại các lớp hoặc thành phần như thư viện để tái sử dụng trong tương lai.

## Cách vẽ Class Diagram

1. **Xác định các lớp trong miền vấn đề**: Xác định các đối tượng trong miền vấn đề và tạo các lớp cho mỗi đối tượng đó. (ví dụ: Teacher, Student, Course cho một hệ thống đăng ký khóa học)

2. **Thêm thuộc tính cho các lớp**: Thêm thuộc tính cho các lớp đó (ví dụ: name, address, telephone cho lớp Student)

3. **Thêm phương thức cho các lớp**: Thêm các phương thức cho các lớp đó (ví dụ: addStudent(student) cho lớp Course)

4. **Kết nối các lớp với các mối quan hệ thích hợp**: Kết nối các lớp bằng các mối quan hệ thích hợp (ví dụ: Liên kết Teacher và Course với một liên kết)

5. **Chỉ định bội số cho các đầu kết nối liên kết**: Tùy chọn chỉ định bội số cho các đầu kết nối liên kết (ví dụ: Nhập 0..3 cho phía Course của liên kết kết nối Teacher và Course, để biểu thị rằng một giáo viên có thể dạy nhiều khóa học lên đến ba khóa học)

Bạn cũng có thể:

6. **Vẽ các gói cho phân loại logic của các lớp**: Nhóm các lớp liên quan vào các gói logic

## Các ví dụ về Class Diagram

### Ví dụ 1: Hệ thống đặt hàng

```
┌───────────┐       ┌───────────┐
│  Customer │       │   Order   │
├───────────┤       ├───────────┤
│ name      │       │ date      │
│ address   │       │ status    │
│ email     │       ├───────────┤
├───────────┤       │ cancel()  │
│ register()│       │ dispatch()│
│ login()   │       └─────┬─────┘
└─────┬─────┘             │
      │ 1                 │ *
      │                   │
      │ places            │
      └───────────────────┘
                ▲
                │
        ┌───────┴────────┐
        │                │
┌───────┴─────┐  ┌───────┴─────┐
│ OnlineOrder │  │ StoreOrder  │
├─────────────┤  ├─────────────┤
│ webRefNo    │  │ storeID     │
├─────────────┤  ├─────────────┤
│ validate()  │  │ process()   │
└─────────────┘  └─────────────┘
        │                │
        │ 1...*          │ 1
        │                │
┌───────┴─────┐  ┌───────┴─────┐
│  OrderItem  │  │  Payment    │
├─────────────┤  ├─────────────┤
│ quantity    │  │ amount      │
│ price       │  │ date        │
├─────────────┤  │ status      │
│ calculate() │  ├─────────────┤
└─────────────┘  │ authorize() │
                 └─────────────┘
```

### Ví dụ 2: Mô hình xe hơi

```
┌───────────┐
│  Vehicle  │
├───────────┤
│ brand     │
│ model     │
│ year      │
├───────────┤
│ start()   │
│ stop()    │
└─────┬─────┘
      │
      │
┌─────┴─────┐
│    Car    │
├───────────┤
│ numDoors  │
│ fuelType  │
├───────────┤
│ refuel()  │
└─────┬─────┘
      │
      │
┌─────┴─────┐       ┌───────────┐
│   Engine  │◆──────│   Wheel   │
├───────────┤ 1   4 ├───────────┤
│ horsepower│       │ size      │
│ cylinders │       │ type      │
├───────────┤       ├───────────┤
│ rev()     │       │ rotate()  │
└───────────┘       └───────────┘
```

## Các lỗi thường gặp khi vẽ Class Diagram

1. **Quá nhiều chi tiết**: Đưa quá nhiều chi tiết vào sơ đồ, khiến nó trở nên phức tạp và khó hiểu.

2. **Thiếu mối quan hệ**: Không xác định đầy đủ các mối quan hệ giữa các lớp.

3. **Sử dụng sai mối quan hệ**: Sử dụng không đúng các mối quan hệ như kế thừa, tập hợp, hợp thành, v.v.

4. **Không chỉ định bội số**: Quên chỉ định bội số cho các mối quan hệ.

5. **Thiếu thuộc tính và phương thức**: Không bao gồm các thuộc tính và phương thức quan trọng trong các lớp.

6. **Lạm dụng kế thừa**: Sử dụng kế thừa khi không cần thiết hoặc không phù hợp.

7. **Không tuân theo quy ước đặt tên**: Không tuân theo các quy ước đặt tên tiêu chuẩn cho lớp, thuộc tính và phương thức.

## Công cụ vẽ Class Diagram

Có nhiều công cụ có thể được sử dụng để vẽ Class Diagram:

1. **Visual Paradigm**: Một công cụ UML mạnh mẽ với phiên bản miễn phí cho mục đích phi thương mại.

2. **Lucidchart**: Công cụ vẽ sơ đồ trực tuyến với các mẫu Class Diagram.

3. **Draw.io**: Công cụ vẽ sơ đồ miễn phí với nhiều mẫu UML.

4. **StarUML**: Công cụ mô hình hóa UML mã nguồn mở.

5. **Microsoft Visio**: Công cụ vẽ sơ đồ chuyên nghiệp từ Microsoft.

6. **Enterprise Architect**: Công cụ mô hình hóa UML chuyên nghiệp cho doanh nghiệp.

## Tổng kết

Class Diagram là một công cụ mạnh mẽ trong thiết kế hướng đối tượng, giúp các nhà phát triển và các bên liên quan hiểu cấu trúc của hệ thống và cách các thành phần khác nhau tương tác với nhau. Bằng cách hiển thị các lớp, thuộc tính, phương thức và mối quan hệ, Class Diagram cung cấp một cái nhìn tổng quan về thiết kế của hệ thống.

Khi tạo Class Diagram, điều quan trọng là phải xem xét mục đích của sơ đồ và đảm bảo rằng nó chứa đủ chi tiết để hữu ích nhưng không quá phức tạp đến mức khó hiểu. Class Diagram nên được sử dụng kết hợp với các sơ đồ UML khác để cung cấp một cái nhìn toàn diện về hệ thống.

Cuối cùng, hãy nhớ rằng Class Diagram chỉ là một công cụ trong bộ công cụ thiết kế phần mềm của bạn. Nó nên được sử dụng khi phù hợp và kết hợp với các kỹ thuật thiết kế và mô hình hóa khác để tạo ra các hệ thống phần mềm chất lượng cao.
