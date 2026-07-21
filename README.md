# Phân tích và thiết kế Hệ thống Quản lý Thư viện

Repository lưu trữ bộ hồ sơ phân tích nghiệp vụ, đặc tả yêu cầu và thiết kế cho **Hệ thống Quản lý Thư viện**. Nội dung được xây dựng trong khuôn khổ học phần **Phân tích thiết kế phần mềm** tại Khoa Công nghệ Thông tin, Trường Đại học Ngoại ngữ – Tin học Thành phố Hồ Chí Minh (HUFLIT).

Tài liệu trong repository tạo thành cơ sở thống nhất để trao đổi yêu cầu, kiểm soát phạm vi, thiết kế hệ thống, xây dựng cơ sở dữ liệu, phát triển phần mềm và tổ chức kiểm thử chấp nhận người dùng.

## Tổng quan dự án

Hệ thống được đề xuất nhằm số hóa các nghiệp vụ chính của thư viện, thay thế việc theo dõi thủ công bằng một nguồn dữ liệu tập trung và nhất quán. Giải pháp phục vụ hai nhóm người dùng chính:

- **Độc giả:** đăng ký và đăng nhập tài khoản, đăng ký thẻ thư viện, tra cứu sách, đăng ký mượn sách, xem thông tin cá nhân và lịch sử mượn – trả.
- **Thủ thư:** quản lý tài khoản, thẻ thư viện, thể loại, đầu sách, bản sao sách, phiếu mượn, phiếu trả và tra cứu dữ liệu vận hành.

Phiên bản hiện tại tập trung vào giai đoạn phân tích và thiết kế. Repository chưa bao gồm mã nguồn của ứng dụng hoàn chỉnh.

## Mục tiêu

- Chuẩn hóa quy trình quản lý tài khoản, thẻ thư viện và danh mục sách.
- Quản lý riêng thông tin đầu sách và từng bản sao vật lý.
- Kiểm soát toàn bộ vòng đời của giao dịch mượn – trả.
- Hỗ trợ độc giả tra cứu và sử dụng các dịch vụ thư viện trực tuyến.
- Xác định rõ yêu cầu chức năng, yêu cầu phi chức năng và quy tắc nghiệp vụ.
- Bảo đảm khả năng truy vết từ mục tiêu nghiệp vụ đến yêu cầu và kịch bản kiểm thử.
- Cung cấp nền tảng tài liệu cho các giai đoạn thiết kế, phát triển, kiểm thử và nghiệm thu.

## Phạm vi nghiệp vụ

### Trong phạm vi

- Đăng ký, đăng nhập, đăng xuất và quản lý hồ sơ người dùng.
- Phân quyền giữa Độc giả và Thủ thư.
- Đăng ký, phê duyệt, cập nhật và quản lý trạng thái thẻ thư viện.
- Quản lý thể loại, đầu sách và bản sao sách.
- Tra cứu sách theo từ khóa, tựa sách, tác giả, thể loại và trạng thái.
- Đăng ký mượn, lập phiếu mượn và ghi nhận trả sách.
- Theo dõi hạn trả, tình trạng sách và phí phạt.
- Tra cứu lịch sử mượn – trả và dữ liệu vận hành.
- Ghi nhận nhật ký đối với các thao tác quản trị quan trọng.

### Ngoài phạm vi phiên bản 1.0

- Mua sắm và quản lý nhà cung cấp sách.
- Thanh toán trực tuyến và nghiệp vụ kế toán.
- RFID, cổng từ và thiết bị kiểm kê tự động.
- Liên thông dữ liệu với thư viện bên ngoài.
- Quản lý sách điện tử có DRM.
- Ứng dụng di động native và hệ thống gợi ý sách.

## Tài liệu trọng tâm

| Tài liệu | Nội dung |
| --- | --- |
| [Software Requirements Specification](Requirements/Software%20Requirements%20Specification.pdf) | Đặc tả yêu cầu phần mềm, phạm vi, stakeholder, quy tắc nghiệp vụ, yêu cầu chức năng và phi chức năng, dữ liệu, tiêu chí nghiệm thu, rủi ro và ma trận truy vết. |
| [Mã nguồn LaTeX của SRS](Requirements/SRS.tex) | Nguồn biên soạn tài liệu SRS, hỗ trợ chỉnh sửa và phát hành các phiên bản tiếp theo. |
| [Business Requirement Document](Requirements/Business%20Requirement%20Document.pdf) | Bối cảnh, mục tiêu và yêu cầu nghiệp vụ cấp cao. |
| [User Stories & Acceptance Criteria](Requirements/User%20Stories%20%26%20Acceptance%20Criteria.pdf) | User story và tiêu chí chấp nhận cho các luồng chức năng. |
| [Báo cáo phân tích và thiết kế](Report/Analysis%20And%20Design%20Library%20Management%20System.docx) | Báo cáo gốc tổng hợp quá trình phân tích và thiết kế hệ thống. |

## Mô hình và bản thiết kế

| Nhóm | Tài liệu | Mục đích |
| --- | --- | --- |
| Quy trình | [Business Process Model and Notation](Diagrams/Business%20Process%20Model%20and%20Notation.pdf) | Mô tả quy trình nghiệp vụ và sự phối hợp giữa các bên. |
| Chức năng | [Use Case Diagram](Diagrams/Use%20Case%20Diagram.docx) | Xác định actor, chức năng và quan hệ giữa các use case. |
| Hành vi | [Activity Diagram](Diagrams/Activity%20Diagram.docx) | Thể hiện luồng xử lý, nhánh điều kiện và trình tự hoạt động. |
| Tương tác | [Sequence Diagram](Diagrams/Sequence%20Diagram.docx) | Mô tả trao đổi giữa người dùng, giao diện, nghiệp vụ và dữ liệu. |
| Dữ liệu | [Entity Relationship Diagram](Database/ERD%20%28Entity%20Relationship%20Diagram%29.pdf) | Trình bày thực thể, thuộc tính và quan hệ trong cơ sở dữ liệu. |
| Giao diện | [Figma Wireframes](Wireframes/Figma.pdf) | Minh họa bố cục và luồng thao tác trên các màn hình chính. |

## Cấu trúc repository

```text
.
├── Database/
│   └── ERD (Entity Relationship Diagram).pdf
├── Diagrams/
│   ├── Activity Diagram.docx
│   ├── Business Process Model and Notation.pdf
│   ├── Sequence Diagram.docx
│   └── Use Case Diagram.docx
├── Report/
│   └── Analysis And Design Library Management System.docx
├── Requirements/
│   ├── assets/
│   │   └── huflit-logo.png
│   ├── Business Requirement Document.pdf
│   ├── Software Requirements Specification.pdf
│   ├── SRS.tex
│   └── User Stories & Acceptance Criteria.pdf
├── Wireframes/
│   └── Figma.pdf
├── LICENSE
└── README.md
```

## Nội dung của SRS

Tài liệu SRS được tổ chức thành các nhóm nội dung chính:

1. Giới thiệu, mục đích, phạm vi và thuật ngữ.
2. Bối cảnh nghiệp vụ, mục tiêu và stakeholder.
3. Business requirements và business rules.
4. Yêu cầu chức năng theo từng phân hệ.
5. Yêu cầu phi chức năng có tiêu chí đo lường.
6. Mô hình dữ liệu logic và quy tắc dữ liệu.
7. Giao diện người dùng, giao diện phần mềm và truyền thông.
8. Use case trọng yếu và tiêu chí chấp nhận.
9. Ma trận truy vết yêu cầu.
10. Điều kiện UAT, kịch bản nghiệm thu và quản trị rủi ro.
11. Quản lý thay đổi, các quyết định còn mở, Definition of Ready và Definition of Done.

Các yêu cầu được định danh theo nhóm như `BR`, `RULE`, `FR` và `NFR` để thuận tiện cho việc quản lý phiên bản, thiết kế test case và truy vết thay đổi.

## Mô hình dữ liệu cốt lõi

Hệ thống sử dụng mô hình dữ liệu quan hệ với các thực thể chính:

- `TaiKhoan`: thông tin đăng nhập, hồ sơ và vai trò người dùng.
- `TheThuVien`: trạng thái, hạng và thời hạn thẻ của độc giả.
- `TheLoai`: danh mục phân loại sách.
- `DauSach`: thông tin thư mục chung của một tựa sách.
- `Sach`: từng bản sao vật lý cùng vị trí và trạng thái riêng.
- `PhieuMuon` và chi tiết mượn: thông tin giao dịch, sách mượn và hạn trả.
- `PhieuTra`: ngày trả, tình trạng sách và phí phạt.
- `AuditLog`: lịch sử các thay đổi và thao tác quản trị quan trọng.

## Hướng dẫn sử dụng tài liệu

### Đối với Business Analyst

1. Bắt đầu từ BRD để nắm bối cảnh và mục tiêu nghiệp vụ.
2. Dùng SRS làm baseline khi làm rõ phạm vi và quản lý thay đổi.
3. Đối chiếu user story, use case và ma trận truy vết để phát hiện yêu cầu còn thiếu.
4. Ghi nhận các quyết định nghiệp vụ còn mở trước khi chuyển yêu cầu sang trạng thái sẵn sàng phát triển.

### Đối với nhóm phát triển

1. Đọc yêu cầu chức năng, business rules và mô hình dữ liệu trong SRS.
2. Tham khảo sequence diagram, activity diagram và wireframe cho từng luồng xử lý.
3. Bảo đảm các ràng buộc dữ liệu và yêu cầu phi chức năng được phản ánh trong thiết kế kỹ thuật.

### Đối với nhóm kiểm thử

1. Xây dựng test scenario từ tiêu chí chấp nhận và các luồng thay thế của use case.
2. Dùng mã yêu cầu trong SRS để liên kết test case và defect.
3. Kiểm tra đầy đủ các business rules, trường hợp lỗi, phân quyền và yêu cầu phi chức năng.
4. Sử dụng các kịch bản UAT trong SRS làm bộ kiểm thử nghiệm thu tối thiểu.

## Biên dịch tài liệu SRS

Tài liệu SRS sử dụng XeLaTeX để hỗ trợ tiếng Việt và font Unicode. Có thể biên dịch bằng một trong các công cụ tương thích như XeLaTeX hoặc Tectonic.

Ví dụ với XeLaTeX:

```bash
cd Requirements
xelatex -jobname="Software Requirements Specification" SRS.tex
xelatex -jobname="Software Requirements Specification" SRS.tex
```

Khi biên dịch cần giữ nguyên đường dẫn `Requirements/assets/huflit-logo.png` để logo trên trang bìa được hiển thị chính xác.

## Quy ước cập nhật tài liệu

- Không thay đổi yêu cầu đã được baseline nếu chưa có đánh giá tác động.
- Mỗi yêu cầu mới phải có mã duy nhất, mô tả rõ ràng và tiêu chí kiểm chứng.
- Thay đổi phạm vi phải được cập nhật đồng thời trong SRS, ma trận truy vết và tài liệu kiểm thử.
- Sơ đồ và wireframe phải phản ánh cùng phiên bản nghiệp vụ với tài liệu yêu cầu.
- Tài liệu phát hành cần cập nhật lịch sử phiên bản và trạng thái phê duyệt.

## Người thực hiện

| Họ và tên | Mã số sinh viên |
| --- | --- |
| Huỳnh Phúc Bảo | 22DH110240 |

**Giảng viên hướng dẫn:** TS/ThS Đặng Thị Kim Giao<br>
**Đơn vị:** Khoa Công nghệ Thông tin, Trường Đại học Ngoại ngữ – Tin học Thành phố Hồ Chí Minh

## Liên hệ

- GitHub: [PhucBaogithub](https://github.com/PhucBaogithub)
- Email: [baominecraft12344@gmail.com](mailto:baominecraft12344@gmail.com)

## Giấy phép

Dự án được phát hành theo [MIT License](LICENSE). Các biểu trưng, tên tổ chức và tài liệu học thuật đi kèm được sử dụng trong phạm vi của dự án môn học.
