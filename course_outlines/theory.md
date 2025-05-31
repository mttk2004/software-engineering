# BỘ CÂU HỎI - TRẢ LỜI ÔN TẬP CÔNG NGHỆ PHẦN MỀM

## MỤC LỤC

1. [Mô hình quy trình phần mềm cơ bản](#1-mô-hình-quy-trình-phần-mềm-cơ-bản)
2. [Khả năng đáp ứng thay đổi yêu cầu](#2-khả-năng-đáp-ứng-thay-đổi-yêu-cầu)
3. [So sánh tiến độ phát triển](#3-so-sánh-tiến-độ-phát-triển)
4. [Ưu điểm trong môi trường thay đổi](#4-ưu-điểm-trong-môi-trường-thay-đổi)
5. [Câu hỏi tình huống và phân tích](#5-câu-hỏi-tình-huống-và-phân-tích)

---

## 1. MÔ HÌNH QUY TRÌNH PHẦN MỀM CƠ BẢN

### Câu 1: Mô hình V-Model là gì? Cho ví dụ minh họa?
**Trả lời:**
- **Định nghĩa:** V-Model là một biến thể của mô hình Waterfall, trong đó các giai đoạn phát triển và kiểm thử được tổ chức theo hình chữ V
- **Cấu trúc:**
  - **Nhánh trái (Development):** Requirements → System Design → Module Design → Coding
  - **Nhánh phải (Testing):** Unit Testing → Integration Testing → System Testing → Acceptance Testing
- **Đặc điểm:** Mỗi giai đoạn phát triển có một giai đoạn kiểm thử tương ứng
- **Ví dụ:** Phát triển hệ thống quản lý bệnh viện - khi viết yêu cầu hệ thống, đồng thời thiết kế test case cho kiểm thử chấp nhận

### Câu 2: Mô hình Incremental là gì? Cho ví dụ cụ thể?
**Trả lời:**
- **Định nghĩa:** Mô hình phát triển gia tăng chia hệ thống thành nhiều increment, mỗi increment cung cấp một phần chức năng hoàn chỉnh
- **Quy trình:**
  1. Phân tích toàn bộ yêu cầu
  2. Chia thành các increment theo độ ưu tiên
  3. Phát triển từng increment độc lập
  4. Tích hợp và giao hàng liên tục
- **Ví dụ:** Phát triển ứng dụng e-commerce:
  - Increment 1: Đăng ký/đăng nhập người dùng
  - Increment 2: Xem sản phẩm và tìm kiếm
  - Increment 3: Giỏ hàng và thanh toán
  - Increment 4: Quản lý đơn hàng

### Câu 3: Extreme Programming (XP) là gì? Cho ví dụ các thực hành chính?
**Trả lời:**
- **Định nghĩa:** XP là một phương pháp phát triển phần mềm Agile tập trung vào chất lượng mã nguồn và khả năng đáp ứng thay đổi
- **12 thực hành chính:**
  1. **Planning Game:** Khách hàng và dev cùng lập kế hoạch
  2. **Small Releases:** Phát hành phiên bản nhỏ thường xuyên
  3. **Pair Programming:** 2 người lập trình cùng 1 máy
  4. **Test-Driven Development:** Viết test trước khi code
- **Ví dụ áp dụng:** Team startup phát triển app mobile - làm việc theo sprint 1-2 tuần, pair programming cho code quan trọng, release beta hàng tuần

### Câu 4: Scrum là gì? Mô tả các thành phần chính với ví dụ?
**Trả lời:**
- **Định nghĩa:** Scrum là framework Agile để quản lý phát triển sản phẩm phức tạp
- **3 Roles chính:**
  - **Product Owner:** Đại diện khách hàng, quản lý Product Backlog
  - **Scrum Master:** Hỗ trợ team, loại bỏ trở ngại
  - **Development Team:** Nhóm phát triển tự tổ chức
- **Events:**
  - **Sprint:** Chu kỳ phát triển 1-4 tuần
  - **Sprint Planning:** Lập kế hoạch sprint
  - **Daily Scrum:** Họp hàng ngày 15 phút
  - **Sprint Review:** Demo sản phẩm cuối sprint
  - **Sprint Retrospective:** Đánh giá và cải tiến
- **Ví dụ:** Team 5 người phát triển website bán hàng, Sprint 2 tuần, PO là manager marketing, Scrum Master là senior developer

---

## 2. KHẢ NĂNG ĐÁP ỨNG THAY ĐỔI YÊU CẦU

### Câu 5: Đánh giá khả năng đáp ứng thay đổi của mô hình Agile?
**Trả lời:**
- **Khả năng đáp ứng: Rất cao (9/10)**
- **Lý do:**
  - **Lặp ngắn:** Sprint 1-4 tuần cho phép điều chỉnh nhanh
  - **Phản hồi liên tục:** Khách hàng tham gia suốt quá trình
  - **Thiết kế tiến hóa:** Cấu trúc code được refactor liên tục
  - **Ưu tiên linh hoạt:** Product Backlog thay đổi theo nhu cầu
- **Ví dụ:** Trong pandemic, app giao đồ ăn nhanh chóng thêm tính năng "contactless delivery" chỉ trong 1 sprint

### Câu 6: Đánh giá khả năng đáp ứng thay đổi của mô hình Waterfall?
**Trả lời:**
- **Khả năng đáp ứng: Thấp (2/10)**
- **Lý do:**
  - **Giai đoạn cứng nhắc:** Phải hoàn thành giai đoạn trước mới chuyển tiếp
  - **Chi phí thay đổi cao:** Thay đổi yêu cầu có thể làm lại từ đầu
  - **Phản hồi muộn:** Chỉ nhận phản hồi ở cuối dự án
  - **Tài liệu nặng:** Nhiều tài liệu cần cập nhật khi thay đổi
- **Ví dụ:** Hệ thống ERP doanh nghiệp - nếu thay đổi quy trình nghiệp vụ giữa chừng, có thể phải thiết kế lại toàn bộ

### Câu 7: Đánh giá khả năng đáp ứng thay đổi của mô hình Incremental?
**Trả lời:**
- **Khả năng đáp ứng: Trung bình cao (7/10)**
- **Lý do:**
  - **Phản hồi sớm:** Nhận feedback từ increment đầu tiên
  - **Điều chỉnh increment tiếp theo:** Có thể thay đổi thiết kế cho các increment sau
  - **Rủi ro giảm:** Phát hiện vấn đề sớm qua từng increment
  - **Hạn chế:** Kiến trúc tổng thể khó thay đổi sau khi định hình
- **Ví dụ:** Website thương mại điện tử - sau increment 1 (đăng ký user), nhận feedback cần thêm đăng nhập social media, có thể bổ sung vào increment 2

### Câu 8: So sánh khả năng thích ứng của ba mô hình trong bối cảnh COVID-19?
**Trả lời:**
**Tình huống:** Công ty phần mềm cần chuyển đổi từ làm việc tại văn phòng sang remote work

- **Agile/Scrum:**
  - ✅ Nhanh chóng chuyển Daily Scrum sang online
  - ✅ Điều chỉnh Definition of Done cho remote work
  - ✅ Thêm tools collaboration vào Sprint Backlog
  - **Thời gian thích ứng:** 1-2 tuần

- **Incremental:**
  - ✅ Có thể điều chỉnh increment đang phát triển
  - ⚠️ Cần review lại kế hoạch các increment tiếp theo
  - ⚠️ Kiến trúc đã định có thể không phù hợp với remote
  - **Thời gian thích ứng:** 3-4 tuần

- **Waterfall:**
  - ❌ Nếu đang ở giai đoạn design, phải dừng để re-plan
  - ❌ Tài liệu và quy trình phải viết lại
  - ❌ Timeline toàn dự án bị ảnh hưởng
  - **Thời gian thích ứng:** 2-3 tháng

---

## 3. SO SÁNH TIẾN ĐỘ PHÁT TRIỂN

### Câu 9: So sánh tiến độ phát triển giữa V-Model và Incremental Model?
**Trả lời:**

**V-Model:**
- **Giai đoạn đầu:** Chậm (phân tích và thiết kế chi tiết)
- **Giai đoạn giữa:** Tăng tốc (coding song song nhiều module)
- **Giai đoạn cuối:** Giảm tốc (integration và system testing)
- **Giao hàng:** Một lần duy nhất ở cuối dự án
- **Timeline:** ████████████████████████████████████████ (100% cuối dự án)

**Incremental Model:**
- **Giai đoạn đầu:** Vừa phải (phân tích tổng thể + thiết kế increment 1)
- **Các increment:** Ổn định và đều (mỗi increment có giá trị)
- **Giao hàng:** Liên tục sau mỗi increment
- **Timeline:**
  - Increment 1: ████████ (25% sau 3 tháng)
  - Increment 2: ████████ (50% sau 6 tháng)
  - Increment 3: ████████ (75% sau 9 tháng)
  - Increment 4: ████████ (100% sau 12 tháng)

### Câu 10: Phân tích đường cong giá trị theo thời gian của hai mô hình?
**Trả lời:**

**V-Model - Đường cong "J":**
```
Giá trị |
cho     |                                    ████
khách   |                                ████
hàng    |                            ████
        |                        ████
        |________________________
        |________________________
        |________________________ (Không có giá trị 80% thời gian)
        +--------------------------------> Thời gian
```

**Incremental Model - Đường cong "Bậc thang":**
```
Giá trị |████████████████████████████████
cho     |████████████████████████
khách   |████████████████
hàng    |████████
        |
        +--------------------------------> Thời gian
```

**Phân tích:**
- **V-Model:** Khách hàng chờ đợi lâu, nhận giá trị muộn nhưng lớn
- **Incremental:** Khách hàng nhận giá trị sớm và tăng dần, giảm rủi ro

### Câu 11: So sánh effort distribution (phân bổ công sức) giữa hai mô hình?
**Trả lời:**

**V-Model - Effort Distribution:**
- **Requirements & Analysis:** 20%
- **System Design:** 15%
- **Module Design:** 10%
- **Coding:** 25%
- **Unit Testing:** 10%
- **Integration Testing:** 10%
- **System Testing:** 5%
- **Acceptance Testing:** 5%

**Incremental Model - Effort Distribution (mỗi increment):**
- **Requirements Analysis:** 15% (giảm từ increment 2+)
- **Design:** 20%
- **Coding:** 35%
- **Testing:** 20%
- **Integration:** 10%

**Đặc điểm:**
- **V-Model:** Front-load effort vào analysis/design
- **Incremental:** Effort phân bổ đều, linh hoạt điều chỉnh

### Câu 12: Trong dự án 12 tháng, mô hình nào giao hàng nhanh hơn?
**Trả lời:**

**Kịch bản: Phát triển hệ thống quản lý thư viện**

**V-Model (12 tháng):**
- Tháng 1-3: Requirements & System Design
- Tháng 4-6: Module Design & Coding
- Tháng 7-9: Testing & Integration
- Tháng 10-12: System Testing & Deployment
- **Sản phẩm khả dụng:** Tháng 12 (100% chức năng)

**Incremental Model (12 tháng):**
- **Increment 1 (Tháng 1-3):** Quản lý sách và tìm kiếm → 30% giá trị
- **Increment 2 (Tháng 4-6):** Quản lý thành viên → 60% giá trị
- **Increment 3 (Tháng 7-9):** Mượn/trả sách → 85% giá trị
- **Increment 4 (Tháng 10-12):** Báo cáo thống kê → 100% giá trị

**Kết luận:**
- **Time to Market:** Incremental nhanh hơn (3 tháng vs 12 tháng)
- **ROI sớm:** Incremental cho phép thu lợi từ tháng thứ 3
- **Risk:** Incremental giảm rủi ro nhờ feedback sớm

---

## 4. ƯU ĐIỂM TRONG MÔI TRƯỜNG THAY ĐỔI

### Câu 13: Ưu điểm của mô hình Agile khi phát triển dự án có yêu cầu thay đổi liên tục?
**Trả lời:**

**Ưu điểm chính:**

1. **Phản hồi nhanh (Rapid Feedback):**
   - Demo working software mỗi 1-4 tuần
   - Khách hàng thấy và sử dụng được sản phẩm sớm
   - Điều chỉnh direction dựa trên phản hồi thực tế

2. **Embracing Change:**
   - "Responding to change over following a plan"
   - Backlog linh hoạt, priority thay đổi theo business needs
   - Technical debt được quản lý qua refactoring liên tục

3. **Reduced Risk:**
   - Fail fast, learn fast
   - Phát hiện vấn đề sớm khi cost of change còn thấp
   - Validate giả định business sớm

4. **Team Collaboration:**
   - Self-organizing teams thích ứng nhanh
   - Daily communication giải quyết blockers
   - Cross-functional teams giảm dependencies

**Ví dụ thực tế:**
Spotify thay đổi thuật toán recommendation dựa trên user behavior - với Agile, họ có thể A/B test và deploy thay đổi trong vòng 1-2 tuần.

### Câu 14: Ưu điểm của mô hình Spiral khi yêu cầu thay đổi liên tục?
**Trả lời:**

**Ưu điểm chính:**

1. **Risk-Driven Approach:**
   - Identify risks sớm trong mỗi spiral
   - Prototype để validate technical feasibility
   - Risk mitigation strategies cho từng iteration

2. **Flexibility in Process:**
   - Mỗi spiral có thể dùng process model khác nhau
   - Waterfall cho well-understood parts
   - Agile cho uncertain requirements

3. **Stakeholder Involvement:**
   - Regular review và approval tại mỗi spiral
   - Continuous validation với business goals
   - Early detection của requirement misalignment

4. **Incremental Progress:**
   - Mỗi spiral tạo ra refined version
   - Learning from previous spirals
   - Gradual increase trong system completeness

**Ví dụ thực tế:**
NASA phát triển Mars Rover - requirements thay đổi dựa trên scientific discoveries và technological advances. Spiral model cho phép re-evaluate risks và adjust approach sau mỗi phase.

### Câu 15: Ưu điểm của mô hình RAD khi yêu cầu thay đổi liên tục?
**Trả lời:**

**Ưu điểm chính:**

1. **Rapid Prototyping:**
   - Visual prototypes trong vài ngày/tuần
   - User testing ngay trên mockups
   - Quick validation của UI/UX concepts

2. **Reusability Focus:**
   - Component-based development
   - Reuse existing libraries và frameworks
   - Rapid assembly từ pre-built components

3. **User-Centric Design:**
   - Intensive user involvement trong design phase
   - Iterative refinement dựa trên user feedback
   - Joint Application Development (JAD) sessions

4. **Time-Boxing:**
   - Fixed timeline cho mỗi phase
   - Force decision making
   - Prevent over-engineering

**RAD Phases:**
1. **Business Modeling:** Understand business context
2. **Data Modeling:** Define data structures
3. **Process Modeling:** Design application flow
4. **Application Generation:** Build using RAD tools
5. **Testing & Turnover:** Deploy và transfer

**Ví dụ thực tế:**
Startup fintech cần MVP trong 3 tháng để demo cho investors - RAD cho phép build prototype với low-code tools, validate với users, và iterate nhanh chóng.

### Câu 16: So sánh hiệu quả của 3 mô hình trong môi trường startup vs enterprise?
**Trả lời:**

**Startup Environment (high uncertainty, limited resources):**

| Mô hình | Hiệu quả | Lý do |
|---------|----------|--------|
| **Agile** | 9/10 | ✅ Fast iteration, MVP approach, team flexibility |
| **Spiral** | 6/10 | ⚠️ Too heavyweight, unnecessary for small scale |
| **RAD** | 8/10 | ✅ Quick prototypes, but limited by available components |

**Enterprise Environment (complex requirements, multiple stakeholders):**

| Mô hình | Hiệu quả | Lý do |
|---------|----------|--------|
| **Agile** | 7/10 | ✅ Good for development, ⚠️ challenges in coordination |
| **Spiral** | 9/10 | ✅ Excellent risk management, stakeholder alignment |
| **RAD** | 5/10 | ❌ Limited scalability, integration complexity |

**Key Factors:**
- **Team Size:** Agile < 10, Spiral any size, RAD < 5
- **Timeline:** RAD fastest, Agile fast, Spiral moderate
- **Risk Tolerance:** Spiral lowest risk, Agile moderate, RAD highest
- **Budget:** RAD cheapest, Agile moderate, Spiral expensive

---

## 5. CÂU HỎI TÌNH HUỐNG VÀ PHÂN TÍCH

### Câu 17: Tình huống 1 - Startup phát triển app food delivery
**Đề bài:** Một startup với 5 developers cần phát triển app food delivery. Requirements thay đổi thường xuyên dựa trên market feedback. Budget hạn chế, cần launch nhanh để compete. Nên chọn mô hình nào?

**Trả lời:**
**Khuyến nghị: Agile (Scrum)**

**Phân tích SWOT:**

**Strengths phù hợp:**
- Team nhỏ → Self-organizing dễ dàng
- Budget hạn chế → Agile cost-effective
- Market competition → Need for speed

**Weaknesses được giải quyết:**
- Changing requirements → Agile embraces change
- Uncertain market → Frequent validation through sprints

**Implementation Plan:**
1. **Sprint 0:** Setup development environment, define MVP scope
2. **Sprint 1-2:** Core features (user registration, restaurant listing)
3. **Sprint 3-4:** Ordering và payment
4. **Sprint 5-6:** Delivery tracking
5. **Continuous:** Marketing feedback integration

**Success Metrics:**
- Time to Market: 3-4 months vs 8-12 months traditional
- User Satisfaction: Weekly feedback incorporation
- Development Cost: 30-40% lower than waterfall

### Câu 18: Tình huống 2 - Ngân hàng phát triển core banking system
**Đề bài:** Ngân hàng lớn cần modernize core banking system. High security requirements, regulatory compliance, 50+ developers, budget $10M, timeline 2 năm. Chọn mô hình nào?

**Trả lời:**
**Khuyến nghị: Spiral Model với V-Model components**

**Lý do lựa chọn:**

1. **Risk Management Critical:**
   - Financial data security risks
   - Regulatory compliance risks
   - Integration với legacy systems
   - Performance và scalability risks

2. **Spiral Phases:**
   - **Spiral 1:** Risk analysis, architecture design, proof of concept
   - **Spiral 2:** Core modules development với V-Model
   - **Spiral 3:** Integration testing và security validation
   - **Spiral 4:** Full system testing và deployment prep

3. **Stakeholder Management:**
   - Regulatory bodies approval tại mỗi spiral
   - Business units feedback và sign-off
   - IT security team continuous involvement

**Timeline:**
- Spiral 1 (6 months): Architecture + POC
- Spiral 2 (9 months): Core development
- Spiral 3 (6 months): Integration + Security
- Spiral 4 (3 months): Deployment + Training

### Câu 19: Tình huống 3 - Game studio phát triển mobile game
**Đề bài:** Game studio với 8 developers phát triển RPG mobile game. Gameplay cần test với users liên tục, monetization model chưa rõ, cần soft launch sau 6 tháng. Chọn mô hình nào?

**Trả lời:**
**Khuyến nghị: Incremental với RAD elements**

**Strategy:**

**Increment 1 (2 tháng): Core Gameplay**
- Character creation và basic combat
- 2-3 levels hoàn chỉnh
- RAD approach: Rapid prototyping với Unity tools

**Increment 2 (2 tháng): Content & Features**
- 10+ levels, story progression
- Character progression system
- Social features (friends, leaderboard)

**Increment 3 (2 tháng): Monetization & Polish**
- In-app purchases integration
- Ad system implementation
- UI/UX polish, performance optimization

**Benefits của approach này:**
- **Early User Testing:** Soft launch với Increment 1
- **Monetization Validation:** Test different models từ Increment 2
- **Risk Mitigation:** Pivot nếu gameplay không hit với users
- **Team Motivation:** Playable game sớm boost morale

### Câu 20: So sánh chi phí thay đổi requirements giữa các mô hình
**Trả lời:**

**Cost of Change Analysis:**

```
Chi phí thay đổi
        |
        |     ████ Waterfall
        |    ████
        |   ████
        |  ████
        | ████               ▓▓▓▓ Spiral
        |████                ▓▓▓▓
        |                   ▓▓▓▓
        |░░░░░░░░░░░░░░░░░░░░░░░░░░ Agile
        +-------------------------> Thời gian trong dự án
```

**Waterfall:**
- Early phase change: 1x cost
- Design phase change: 5x cost
- Implementation phase: 20x cost
- Testing phase: 100x cost

**Agile:**
- Constant low cost: 1-2x throughout project
- Architecture change: 3-5x cost (higher than normal)

**Spiral:**
- Within spiral: 2-3x cost
- Between spirals: 1x cost (planned change points)
- Major architecture change: 10-15x cost

**Real Example:**
E-commerce project cần thêm cryptocurrency payment:
- **Waterfall (month 8/12):** $50,000 (redesign payment system)
- **Agile (any sprint):** $5,000 (new payment provider integration)
- **Spiral (between spirals):** $10,000 (planned extension point)

### Câu 21: Phân tích team productivity qua các mô hình
**Trả lời:**

**Team Productivity Factors:**

**Agile Teams:**
- **Tốc độ phát triển:** Tăng dần qua các sprints (đường cong học tập)
- **Động lực:** Cao (phần mềm hoạt động tốt, tự chủ trong nhóm)
- **Giao tiếp:** Xuất sắc (họp hàng ngày, làm việc cùng địa điểm)
- **Nợ kỹ thuật:** Được kiểm soát (refactoring thường xuyên)

**Waterfall Teams:**
- **Giai đoạn đầu:** Chậm (phân tích quá mức)
- **Giai đoạn lập trình:** Bùng nổ năng suất cao
- **Giai đoạn cuối:** Giảm (khó khăn tích hợp, sửa lỗi)
- **Tổng thể:** Phân bố không đều

**Spiral Teams:**
- **Giai đoạn phân tích rủi ro:** Chậm nhưng kỹ lưỡng
- **Giai đoạn phát triển:** Tiến độ ổn định
- **Giai đoạn đánh giá:** Chi phí quản lý cao
- **Tổng thể:** Nhất quán nhưng ở mức trung bình

**Chỉ số năng suất (Dòng mã/Người phát triển/Ngày):**

| Giai đoạn | Waterfall | Agile | Spiral |
|-------|-----------|--------|--------|
| Tháng 1-3 | 10 | 25 | 15 |
| Tháng 4-6 | 50 | 35 | 30 |
| Tháng 7-9 | 30 | 40 | 35 |
| Tháng 10-12 | 15 | 42 | 38 |
| **Trung bình** | **26** | **36** | **30** |

### Câu 22: Quản lý chất lượng trong các mô hình khác nhau
**Trả lời:**

**Các phương pháp đảm bảo chất lượng:**

**Quản lý chất lượng theo V-Model:**
- **Tập trung phòng ngừa:** Thiết kế cổng chất lượng
- **Chiến lược kiểm thử:** Lập kế hoạch kiểm thử toàn diện từ yêu cầu
- **Tài liệu:** Tài liệu kiểm thử chi tiết
- **Chỉ số đo lường:** Mật độ lỗi, độ bao phủ kiểm thử
- **Lợi ích:** Chất lượng dự đoán được, xác minh chính thức

**Quản lý chất lượng theo Agile:**
- **Chất lượng tích hợp:** Phát triển hướng kiểm thử, lập trình cặp
- **Tích hợp liên tục:** Đường ống kiểm thử tự động
- **Định nghĩa hoàn thành:** Tiêu chí chất lượng cho mỗi user story
- **Chỉ số đo lường:** Tốc độ, burn-down, sự hài lòng của khách hàng
- **Lợi ích:** Phản hồi nhanh, chất lượng thích ứng

**Quản lý chất lượng theo Incremental:**
- **Chất lượng tiến triển:** Chất lượng cải thiện qua từng increment
- **Chấp nhận người dùng:** Kiểm thử người dùng thực cho mỗi increment
- **Kiểm thử hồi quy:** Đảm bảo các increment trước vẫn hoạt động tốt
- **Chỉ số đo lường:** Tỷ lệ chấp nhận increment, lỗi tích lũy
- **Lợi ích:** Chất lượng được xác nhận bởi người dùng, phát hiện sớm vấn đề

**So sánh chất lượng:**

| Khía cạnh | V-Model | Agile | Incremental |
|--------|---------|-------|-------------|
| **Phòng ngừa lỗi** | Xuất sắc | Tốt | Tốt |
| **Phát hiện sớm** | Kém | Xuất sắc | Tốt |
| **Sự hài lòng của người dùng** | Rủi ro | Cao | Cao |
| **Tuân thủ quy định** | Xuất sắc | Trung bình | Tốt |

### Câu 23: Tình huống crisis management - COVID-19 impact
**Đề bài:** Dự án phát triển hệ thống quản lý sự kiện đang ở giữa chừng khi COVID-19 bùng phát. Yêu cầu chuyển từ sự kiện offline sang online/hybrid. Team phải work from home. Mô hình nào handle tốt nhất?

**Trả lời:**

**Phân tích tình huống:**

**Trạng thái trước COVID:**
- Dự án 6 tháng, đã hoàn thành 3 tháng
- Yêu cầu: Quản lý sự kiện vật lý
- Nhóm: 10 developers, co-located
- Công nghệ: Web-based, designed for on-site check-in

**Tác động của COVID:**
- ❌ Sự kiện vật lý bị hủy/hoãn
- ❌ Nhóm phân tán (work from home)
- ✅ Cơ hội mới: Bùng nổ sự kiện trực tuyến
- ⚡ Nhu cầu khẩn cấp: Chuyển hướng nhanh hoặc mất thị trường

**So sánh mô hình:**

**Nếu sử dụng Waterfall:**
- ❌ **Vấn đề lớn:** Giai đoạn yêu cầu đã hoàn thành, thiết kế đã khóa
- ❌ **Chi phí thay đổi:** 50-100x (thiết kế lại hoàn toàn)
- ❌ **Thời gian:** 6+ tháng để chuyển hướng
- ❌ **Vấn đề nhóm:** Nặng tài liệu, khó phối hợp từ xa

**Nếu sử dụng Incremental:**
- ✅ **Ưu điểm:** Có thể chuyển hướng các increment sắp tới
- ⚠️ **Thách thức:** Kiến trúc có thể không hỗ trợ sự kiện ảo
- ✅ **Thời gian:** 2-3 tháng để chuyển hướng
- ✅ **Nhóm:** Các increment có thể được phát triển độc lập

**Nếu sử dụng Agile:**
- ✅ **Phản ứng tốt nhất:** Chấp nhận thay đổi là nguyên tắc cốt lõi
- ✅ **Ưu tiên lại:** Product backlog được sắp xếp lại ngay lập tức
- ✅ **Thời gian:** 2-4 sprint (1-2 tháng) cho MVP chuyển hướng
- ✅ **Nhóm:** Các buổi họp hàng ngày hoạt động tốt từ xa

**Kế hoạch hành động khuyến nghị (Agile):**
1. **Lập kế hoạch Sprint khẩn cấp:** Xác định lại tầm nhìn sản phẩm
2. **Spike Stories:** Nghiên cứu nền tảng sự kiện ảo
3. **Sprint chuyển hướng 1:** Tạo sự kiện ảo cơ bản
4. **Sprint chuyển hướng 2:** Tích hợp phát trực tuyến
5. **Sprint chuyển hướng 3:** Tính năng tương tác người tham dự

**Kết quả thành công:** Nhiều công ty chuyển hướng nhanh chóng sang sự kiện ảo (như Zoom, Microsoft Teams) đã chứng kiến sự tăng trưởng bùng nổ trong đại dịch.

### Câu 24: Phân tích ROI - Mô hình nào có ROI tốt nhất?
**Trả lời:**

**Khung tính toán ROI:**

**Thành phần đầu tư:**
- Chi phí phát triển
- Chi phí đào tạo
- Chi phí công cụ/hạ tầng
- Chi phí rủi ro/làm lại

**Thành phần lợi nhuận:**
- Giá trị thời gian ra thị trường
- Lợi ích chất lượng
- Tiết kiệm bảo trì
- Sự hài lòng của khách hàng

**Nghiên cứu tình huống: Nền tảng E-learning (ngân sách $500K)**

**ROI Waterfall:**
```
Đầu tư: $500K + $100K (công cụ) + $50K (làm lại) = $650K
Lợi nhuận:
- Thời gian ra thị trường: 12 tháng (phạt do ra thị trường muộn: -$200K)
- Chất lượng: Chất lượng ban đầu cao (+$100K)
- Bảo trì: Chi phí cao (-$50K/năm)
ROI Năm 1: ($500K - $650K) / $650K = -23%
```

**ROI Agile:**
```
Đầu tư: $500K + $30K (đào tạo) + $20K (công cụ) = $550K
Lợi nhuận:
- Thời gian ra thị trường: 6 tháng (lợi thế thị trường sớm: +$300K)
- Chất lượng: Tốt với các lần lặp (+$150K)
- Bảo trì: Chi phí trung bình (-$30K/năm)
ROI Năm 1: ($750K - $550K) / $550K = +36%
```

**ROI Incremental:**
```
Đầu tư: $500K + $40K (phối hợp) + $30K (tích hợp) = $570K
Lợi nhuận:
- Thời gian ra thị trường: 3 tháng cho increment đầu tiên (+$200K)
- Chất lượng: Cải thiện tiến triển (+$120K)
- Bảo trì: Chi phí thấp-trung bình (-$35K/năm)
ROI Năm 1: ($650K - $570K) / $570K = +14%
```

**Xếp hạng ROI:**
1. **Agile: +36%** (Tốt nhất cho thị trường không chắc chắn)
2. **Incremental: +14%** (Lợi nhuận ổn định)
3. **Waterfall: -23%** (Rủi ro cao, lợi nhuận muộn)

### Câu 25: Tổng hợp - Ma trận quyết định cho lựa chọn mô hình
**Trả lời:**

**Ma trận quyết định đa tiêu chí:**

| Tiêu chí (Trọng số) | Waterfall | Incremental | Agile | Spiral | RAD |
|-------------------|-----------|-------------|-------|--------|-----|
| **Độ ổn định yêu cầu (20%)** | 9 | 6 | 3 | 5 | 4 |
| **Thời gian ra thị trường (25%)** | 2 | 7 | 9 | 4 | 8 |
| **Khả năng mở rộng quy mô nhóm (15%)** | 8 | 6 | 4 | 9 | 3 |
| **Khả năng thích ứng thay đổi (20%)** | 2 | 7 | 9 | 6 | 7 |
| **Quản lý rủi ro (10%)** | 6 | 5 | 4 | 9 | 3 |
| **Hiệu quả tài nguyên (10%)** | 5 | 7 | 8 | 4 | 9 |

**Điểm số có trọng số:**
- **Agile:** (3×0.2) + (9×0.25) + (4×0.15) + (9×0.2) + (4×0.1) + (8×0.1) = **6.95**
- **Incremental:** (6×0.2) + (7×0.25) + (6×0.15) + (7×0.2) + (5×0.1) + (7×0.1) = **6.55**
- **Spiral:** (5×0.2) + (4×0.25) + (9×0.15) + (6×0.2) + (9×0.1) + (4×0.1) = **5.85**
- **RAD:** (4×0.2) + (8×0.25) + (3×0.15) + (7×0.2) + (3×0.1) + (9×0.1) = **6.25**
- **Waterfall:** (9×0.2) + (2×0.25) + (8×0.15) + (2×0.2) + (6×0.1) + (5×0.1) = **4.90**

**Khuyến nghị theo ngữ cảnh:**

**Dự án Startup/Đổi mới:** → **Agile** (Điểm: 6.95)
- Khả năng thích ứng thay đổi cao
- Thời gian ra thị trường nhanh
- Hiệu quả tài nguyên

**Doanh nghiệp/Quy mô lớn:** → **Incremental** (Điểm: 6.55)
- Cân bằng giữa kiểm soát và linh hoạt
- Khả năng mở rộng tốt
- Quản lý rủi ro hợp lý

**Rủi ro cao/Môi trường được quy định:** → **Spiral** (Điểm: 5.85)
- Quản lý rủi ro xuất sắc
- Phù hợp với nhóm lớn
- Xử lý tốt sự không chắc chắn

**Prototype/Chứng minh khái niệm:** → **RAD** (Điểm: 6.25)
- Phát triển nhanh nhất
- Hiệu quả tài nguyên
- Phù hợp với phạm vi nhỏ

**Yêu cầu ổn định/Nhiệm vụ quan trọng:** → **Waterfall** (Điểm: 4.90)
- Tốt nhất khi yêu cầu ổn định
- Kết quả dự đoán được
- Tài liệu chính thức

---

## KẾT LUẬN

Việc lựa chọn mô hình quy trình phần mềm phù hợp là yếu tố quyết định thành công của dự án. Không có mô hình nào hoàn hảo cho mọi tình huống, mà cần phân tích:

### Yếu tố quyết định chính:
1. **Tính chất yêu cầu:** Stable vs Changing
2. **Áp lực thời gian:** Khẩn cấp vs Linh hoạt
3. **Bối cảnh nhóm:** Quy mô, kinh nghiệm, vị trí
4. **Khả năng chịu rủi ro:** Cao vs Thấp
5. **Hạn chế ngân sách:** Tài nguyên hạn chế vs Dồi dào

### Xu hướng hiện tại:
- **Agile** trở thành xu hướng chính cho phần lớn dự án
- **Phương pháp kết hợp** tận dụng ưu điểm nhiều mô hình
- **DevOps** tích hợp development và operations
- **Giao hàng liên tục** là tiêu chuẩn mới

### Lời khuyên thực tiễn:
1. **Bắt đầu đơn giản:** Khởi đầu với mô hình đơn giản, phát triển theo nhu cầu
2. **Đo lường và thích ứng:** Sử dụng các chỉ số để đánh giá và cải tiến
3. **Con người hơn quy trình:** Quy trình phục vụ con người, không ngược lại
4. **Giá trị khách hàng:** Tập trung vào việc mang lại giá trị cho khách hàng sớm nhất

**Chúc các bạn ôn tập tốt và thành công trong kỳ thi!** 🚀
