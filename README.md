# Thiết kế và phát triển website thương mại điện tử cho thương hiệu Trà Hỷ Phúc

**Nhóm thực hiện:** Nhóm 8 – Đại học Kinh tế TP. Hồ Chí Minh (UEH)  
**Học phần:** Phát triển ứng dụng thương mại điện tử  
**Giảng viên hướng dẫn:** GVC. TS Nguyễn Mạnh Tuấn

## 1. Giới thiệu

Nhóm xây dựng website thương mại điện tử cho Trà Hỷ Phúc theo mô hình B2C, cung cấp sản phẩm trực tiếp đến người tiêu dùng. Danh mục kinh doanh gồm đồ uống pha sẵn, trà khô đóng gói, món tráng miệng và topping.

Theo thông tin ban đầu phục vụ đề tài, khách hàng có thể nhầm Trà Hỷ Phúc với cửa hàng có tên tương tự, chưa tìm thấy đầy đủ sản phẩm trên website hoặc gặp khó khăn khi lựa chọn món do thiếu thông tin về hương vị, thành phần và tùy chọn. Sự khác nhau giữa đồ uống dùng ngay và trà khô cũng đòi hỏi thông tin rõ ràng về quy cách, cách sử dụng, bảo quản và giao nhận.

Website được định hướng giải quyết các vấn đề trên bằng thông tin nhận diện thống nhất, thực đơn đầy đủ, mô tả sản phẩm dễ hiểu và quy trình đặt hàng thuận tiện. Phía cửa hàng có chức năng cập nhật sản phẩm, giá, tình trạng bán và quản lý đơn hàng.

Trong phiên bản đầu, nhóm lựa chọn **thanh toán khi nhận hàng (COD)**. Khách gửi đơn mà không bắt buộc đăng ký tài khoản; cửa hàng xác nhận, chuẩn bị và giao hàng; khách thanh toán khi nhận hàng. Thanh toán trực tuyến thuộc phạm vi phát triển sau. Các chức năng dưới đây là phạm vi dự kiến của dự án, không phải xác nhận mọi chức năng đã hoàn thành.

## 2. Khách hàng mục tiêu

| Nhóm khách hàng | Nhu cầu chính |
| --- | --- |
| Nhân viên văn phòng và người đi làm trong khu vực giao hàng | Xem thực đơn, chọn món và đặt đồ uống thuận tiện. |
| Người mua quan tâm đến nguyên liệu và hương vị | Tìm hiểu thành phần, hương vị và lựa chọn sản phẩm phù hợp với sở thích. |
| Người mua trà khô dùng tại nhà hoặc nơi làm việc | Xem quy cách đóng gói, cách pha và hướng dẫn bảo quản. |
| Khách hàng hiện tại của cửa hàng | Tìm đúng kênh bán hàng, xem thực đơn cập nhật và mua lại món quen thuộc. |
| Người lớn tuổi và người mua cho gia đình | Đọc thông tin dễ hiểu, thao tác đơn giản và có kênh liên hệ hỗ trợ. |

Nhóm ưu tiên khách trong vùng giao của cửa hàng đối với đồ uống pha sẵn và món tráng miệng. Phạm vi giao trà khô được xác định theo điều kiện đóng gói, vận chuyển và phí giao thực tế. Đây là các nhóm khách hàng dự kiến, chưa phải kết quả phân khúc từ khảo sát định lượng.

## 3. Chức năng chính

### 3.1. Chức năng ưu tiên trong phiên bản đầu

**Đối với khách mua hàng:**

- Xem tên thương hiệu, địa chỉ, thông tin liên hệ, giờ hoạt động và hướng dẫn mua hàng.
- Duyệt danh mục, danh sách và chi tiết sản phẩm; xem ảnh, giá, hương vị, thành phần và tình trạng bán.
- Xem quy cách, cách pha và bảo quản đối với trà khô.
- Chọn số lượng, kích cỡ, độ ngọt, lượng đá hoặc topping theo tùy chọn được áp dụng cho từng món; xem phụ phí nếu có.
- Thêm, xóa và thay đổi số lượng sản phẩm trong giỏ hàng.
- Nhập thông tin nhận hàng không cần đăng nhập; kiểm tra vùng giao, phí giao và tổng tiền trước khi gửi đơn.
- Đặt hàng COD và nhận mã đơn, tổng tiền cần thanh toán khi nhận hàng cùng thông báo chờ cửa hàng xác nhận.

**Đối với quản trị viên:**

- Đăng nhập để truy cập chức năng quản trị.
- Quản lý danh mục, nội dung sản phẩm, giá, tùy chọn và trạng thái còn bán hoặc tạm hết.
- Xem, xác nhận và cập nhật quá trình chuẩn bị, giao hàng, hoàn tất hoặc hủy đơn.
- Ghi nhận kết quả thu tiền COD và lý do phát sinh trong quá trình xử lý đơn.

Nhóm tách trạng thái xử lý đơn khỏi trạng thái thanh toán: đơn đã xác nhận hoặc đang giao vẫn có thể chưa thanh toán. Việc ghi nhận đã thanh toán chỉ thực hiện sau khi xác nhận đã thu tiền. Giá trên đơn được lưu tại thời điểm đặt và không tự thay đổi khi cửa hàng cập nhật thực đơn.

### 3.2. Chức năng hiện có cần kiểm thử

Website đã có chatbot hỗ trợ thông tin và lựa chọn sản phẩm theo ghi nhận của nhóm. Nhóm kiểm tra tính chính xác của phản hồi, khả năng thực hiện thao tác và giới hạn hoạt động trước khi quyết định phạm vi bàn giao.

### 3.3. Chức năng phát triển sau và giới hạn phạm vi

- Đăng ký, đăng nhập tài khoản khách hàng và lịch sử mua hàng.
- Tra cứu trạng thái các đơn thuộc tài khoản của khách.
- Tìm kiếm, bộ lọc nâng cao và gợi ý món thay thế.
- Thanh toán trực tuyến; blog và mã giảm giá được xem xét theo tiến độ.

Quản lý tồn kho theo nguyên liệu, gợi ý cá nhân hóa, tích điểm và quản lý nhiều chi nhánh chưa thuộc phạm vi đồ án hiện tại. Vùng giao, phí giao, tùy chọn từng món và quy tắc giao chung trà khô với đồ uống cần được xác nhận với cửa hàng trước khi triển khai.

## 4. Thành viên

| Thành viên | Vai trò | Trách nhiệm chính |
| --- | --- | --- |
| Nguyễn Thị Thanh Vân | Trưởng nhóm/BA | Quản lý tiến độ, yêu cầu và GitHub Issues; xác nhận nghiệp vụ với cửa hàng; tổng hợp quyết định và cập nhật tài liệu. |
| Nguyễn Minh Đăng | UI/UX và nội dung | Thiết kế giao diện; chuẩn bị ảnh, mô tả sản phẩm và đối chiếu thông tin thực đơn. |
| Tăng Khánh Tường | Frontend | Xây dựng giao diện danh mục, chi tiết, giỏ hàng và đặt hàng; hiển thị lỗi, tổng tiền và thông báo nhận đơn. |
| Trần Hoàng Tân | Backend/Database | Xử lý dữ liệu, kiểm tra giá, vùng giao, tình trạng bán; lưu đơn và xây dựng chức năng quản trị. |
| Nguyễn Phi Long | QA/Integration | Lập kịch bản kiểm thử, ghi nhận lỗi, kiểm thử lại, kiểm tra chatbot hiện có và phối hợp trình diễn. |
| Phạm Ngọc Minh Thư | Phát triển nghiệp vụ COD | Phối hợp xây dựng thông tin COD, số tiền cần thu và thao tác cập nhật thu tiền; kiểm tra giao thất bại và hủy đơn. |

Mỗi thành viên chịu trách nhiệm về kết quả bàn giao của mình, phối hợp tích hợp và kiểm thử. Nội dung hoặc mã nguồn do AI hỗ trợ phải được thành viên phụ trách kiểm tra trước khi sử dụng.

## 5. Công nghệ dự kiến

Tại thời điểm lập README, tài liệu dự án chưa ghi rõ công nghệ đã thống nhất cho frontend, backend, cơ sở dữ liệu và môi trường triển khai. Nhóm sẽ cập nhật các lựa chọn này sau khi thống nhất; chưa xác định nền tảng hoặc ngôn ngữ cụ thể trong README.

| Hạng mục | Công nghệ hoặc công cụ | Trạng thái |
| --- | --- | --- |
| Frontend | Chưa xác định trong tài liệu hiện tại | Cần bổ sung lựa chọn của nhóm |
| Backend | Chưa xác định trong tài liệu hiện tại | Cần bổ sung lựa chọn của nhóm |
| Cơ sở dữ liệu | Chưa xác định trong tài liệu hiện tại | Cần bổ sung lựa chọn của nhóm |
| Môi trường triển khai | Chưa xác định trong tài liệu hiện tại | Cần bổ sung lựa chọn của nhóm |
| Quản lý mã nguồn và công việc | GitHub, GitHub Issues | Được sử dụng trong phương án phối hợp của nhóm |
| Hỗ trợ phân tích yêu cầu và phản biện | ChatGPT, Gemini | Công cụ hỗ trợ thực hiện bài tập; kết quả do nhóm đánh giá |

COD là phương thức thanh toán trong phạm vi nghiệp vụ, không phải công nghệ tích hợp cổng thanh toán trực tuyến. Công nghệ của chatbot hiện có được ghi nhận riêng sau khi nhóm xác minh cấu hình thực tế.

## 6. Kế hoạch thực hiện

Thời gian dự kiến theo thông tin dự án: **11/11/2026–03/01/2027**. Nhóm tổ chức công việc theo các giai đoạn dưới đây; thời hạn chi tiết và người phụ trách từng công việc được cập nhật trong kế hoạch dự án.

| Giai đoạn | Công việc chính | Kết quả dự kiến |
| --- | --- | --- |
| 1. Khảo sát và xác định yêu cầu | Xác định vấn đề kinh doanh, khách hàng; khảo sát ba website; phân tích và phản biện bằng AI; chốt phạm vi COD. | Bản yêu cầu, bảng khảo sát và danh sách nội dung cần xác minh. |
| 2. Thiết kế giao diện và chuẩn bị dữ liệu | Thiết kế các trang chính; chuẩn hóa ảnh, nội dung, giá và tùy chọn sản phẩm. | Thiết kế giao diện và bộ dữ liệu sản phẩm. |
| 3. Xây dựng frontend | Triển khai danh mục, chi tiết, giỏ hàng và biểu mẫu đặt hàng trên máy tính, điện thoại. | Luồng thao tác mua hàng và thông báo kết quả. |
| 4. Phát triển backend và nghiệp vụ COD | Xây dựng dữ liệu, kiểm tra vùng giao và giá, lưu đơn, quản trị sản phẩm, trạng thái đơn và thu tiền. | Chức năng xử lý đơn COD và quản trị tích hợp. |
| 5. Tích hợp và kiểm thử | Kiểm thử luồng mua hàng, giá, gửi trùng, món hết, ngoài vùng giao, giao thất bại; đánh giá chatbot và sửa lỗi. | Bảng kết quả kiểm thử, lỗi đã xử lý và giới hạn còn tồn tại. |
| 6. Triển khai và hoàn thiện | Kiểm tra môi trường triển khai, hoàn thiện tài liệu, repository và kịch bản trình diễn. | Phiên bản bàn giao và tài liệu phục vụ đánh giá. |

Nhóm ưu tiên luồng bán hàng cốt lõi trước các chức năng mở rộng. Kết quả kiểm thử được ghi nhận theo thực tế; bản trình diễn sử dụng dữ liệu khách hàng giả lập.

## 7. Liên kết

- Bảng yêu cầu: [REQUIREMENTS.md](REQUIREMENTS.md)
- Kế hoạch: [PROJECT_PLAN.md](PROJECT_PLAN.md)
- Phân tích website: [docs/competitor-analysis.md](docs/competitor-analysis.md)

Các liên kết tương đối trên trỏ đến tài liệu dự kiến trong cùng repository. Nhóm cần bổ sung các tệp tương ứng để sử dụng đầy đủ các liên kết.

