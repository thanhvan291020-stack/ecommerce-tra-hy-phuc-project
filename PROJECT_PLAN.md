# Project Plan

**Dự án:** Thiết kế và phát triển website thương mại điện tử cho thương hiệu Trà Hỷ Phúc  
**Nhóm thực hiện:** Nhóm 8

Kế hoạch tập trung hoàn thiện quy trình đặt hàng và thanh toán khi nhận hàng (COD). Thanh toán trực tuyến thuộc phạm vi phát triển sau. Kế hoạch không xác nhận website đã hoàn thành các chức năng dự kiến.

## 1. Thành viên và vai trò

| Thành viên | Vai trò | Trách nhiệm |
| --- | --- | --- |
| Nguyễn Thị Thanh Vân | Trưởng nhóm/BA | Quản lý yêu cầu, tiến độ và GitHub Issues; trao đổi với cửa hàng; xác nhận quy tắc giao hàng, tùy chọn và COD; tổng hợp quyết định và cập nhật tài liệu. |
| Nguyễn Minh Đăng | UI/UX và nội dung | Thiết kế các trang chính; chuẩn bị ảnh, mô tả sản phẩm; đối chiếu thực đơn và hỗ trợ kiểm tra hiển thị. |
| Tăng Khánh Tường | Frontend | Xây dựng danh mục, chi tiết, giỏ và đặt hàng; hiển thị lỗi, tổng tiền, mã đơn và thông báo chờ xác nhận trên máy tính, điện thoại. |
| Trần Hoàng Tân | Backend/Database | Xử lý dữ liệu, giá, vùng giao, tình trạng bán; lưu đơn; xây dựng quản trị và kiểm soát truy cập. |
| Nguyễn Phi Long | QA/Integration | Lập kịch bản kiểm thử, ghi lỗi, kiểm thử lại; kiểm tra chatbot hiện có; phối hợp tích hợp và trình diễn. |
| Phạm Ngọc Minh Thư | Phát triển nghiệp vụ COD | Phối hợp xây dựng thông tin COD, số tiền cần thu, trạng thái thanh toán và cập nhật thu tiền; xử lý các trường hợp hủy, giao thất bại. |

### Cách phối hợp

Thanh Vân tổng hợp yêu cầu đã xác nhận và chuyển đến người phụ trách. Minh Đăng bàn giao giao diện, ảnh và nội dung cho Khánh Tường. Khánh Tường phối hợp với Hoàng Tân để thống nhất dữ liệu và thao tác trên giao diện. Minh Thư phối hợp với hai thành viên này để tích hợp COD và ghi nhận thu tiền.

Phi Long kiểm thử toàn bộ quy trình, ghi rõ điều kiện gây lỗi và chuyển cho người phụ trách sửa; sau đó kiểm thử lại. Với chatbot, Phi Long tổng hợp kết quả và phối hợp với thành viên kỹ thuật xử lý lỗi theo phần việc. Mỗi thay đổi được thành viên liên quan kiểm tra trước khi hợp nhất; thay đổi phạm vi phải được nhóm thống nhất và cập nhật tài liệu.

## 2. Các giai đoạn

| Giai đoạn | Nội dung thực hiện | Kết quả cần đạt | Điều kiện chuyển bước |
| --- | --- | --- | --- |
| 1. Khảo sát và xác định yêu cầu | Khảo sát ba website; xác định vấn đề, người dùng; đánh giá AI; chốt phạm vi COD và các điều kiện cần xác minh. | Bản yêu cầu, phân tích website và quy trình nghiệp vụ. | Nhóm thống nhất phạm vi, nhận diện những quy tắc còn thiếu. |
| 2. Thiết kế giao diện | Thiết kế trang chủ, danh mục, chi tiết, giỏ, đặt hàng; chuẩn bị dữ liệu sản phẩm. | Bộ giao diện và nội dung đã đối chiếu. | Các màn hình và dữ liệu đủ để triển khai luồng chính. |
| 3. Xây dựng các chức năng frontend | Xây dựng giao diện và tương tác mua hàng, kiểm tra biểu mẫu, thông báo kết quả. | Luồng thao tác từ xem sản phẩm đến gửi đơn. | Có thể kiểm tra thao tác với dữ liệu mẫu và chuẩn bị kết nối backend. |
| 4. Phát triển backend và cơ sở dữ liệu | Thiết kế dữ liệu; kiểm tra giá và vùng giao; lưu đơn; quản trị sản phẩm, đơn và COD. | Các chức năng nghiệp vụ kết nối với giao diện. | Đơn hợp lệ được lưu; quản trị có thể xác nhận, xử lý và cập nhật thu tiền. |
| 5. Tích hợp và kiểm thử | Kiểm tra toàn bộ luồng, dữ liệu, quyền truy cập, giao diện và chatbot; sửa lỗi. | Bảng kết quả kiểm thử và giới hạn còn tồn tại. | Các tình huống bắt buộc đạt; lỗi cản trở đặt, xử lý đơn được khắc phục. |
| 6. Triển khai và hoàn thiện | Kiểm tra môi trường, cấu hình, tài liệu; chuẩn bị repository và trình diễn. | Phiên bản bàn giao, hướng dẫn và tài liệu thống nhất. | Có thể chạy và trình diễn theo hướng dẫn; kiểm tra quyền truy cập tài liệu nộp. |

Các phần frontend, backend và chuẩn bị kiểm thử có thể phối hợp song song sau khi thống nhất cấu trúc dữ liệu và nghiệp vụ. Việc mở rộng chức năng không được làm gián đoạn luồng COD cốt lõi.

## 3. Công việc

Trạng thái trong bảng phản ánh thông tin có thể xác nhận từ tài liệu, không suy diễn tiến độ triển khai. Các mục chưa có bằng chứng hoàn thành được ghi **Chưa xác nhận tiến độ**. Khi thực hiện, nhóm cập nhật thành **Chưa bắt đầu**, **Đang thực hiện**, **Chờ kiểm tra** hoặc **Hoàn thành** theo thực tế.

| Mã công việc | Công việc | Người phụ trách chính | Kết quả cần đạt | Trạng thái |
| --- | --- | --- | --- | --- |
| CV01 | Rà soát vấn đề kinh doanh và yêu cầu | Nguyễn Thị Thanh Vân | Yêu cầu nhất quán với COD, có danh sách nội dung cần xác minh. | Đã có bản thảo |
| CV02 | Hoàn thiện khảo sát ba website | Nguyễn Minh Đăng | Bảng so sánh, đường dẫn, minh chứng và lý do lựa chọn tính năng. | Đã có nội dung; cần rà soát minh chứng |
| CV03 | Xác nhận quy tắc với cửa hàng | Nguyễn Thị Thanh Vân | Vùng giao, phí, tùy chọn, đơn hỗn hợp, xác nhận và hủy đơn được ghi rõ. | Cần xác minh |
| CV04 | Thống nhất công nghệ và cấu trúc dự án | Trần Hoàng Tân | Phương án frontend, backend, dữ liệu và triển khai được nhóm thống nhất. | Chưa xác nhận |
| CV05 | Thiết kế giao diện | Nguyễn Minh Đăng | Các trang chính và trạng thái lỗi, trống, tạm hết, đặt thành công. | Chưa xác nhận tiến độ |
| CV06 | Chuẩn hóa nội dung sản phẩm | Nguyễn Minh Đăng | Ảnh, giá, mô tả, thành phần, quy cách và tùy chọn được đối chiếu. | Chưa xác nhận tiến độ |
| CV07 | Xây dựng trang danh mục và chi tiết | Tăng Khánh Tường | Giao diện hiển thị đúng dữ liệu và trạng thái bán. | Chưa xác nhận tiến độ |
| CV08 | Xây dựng giỏ và biểu mẫu đặt hàng | Tăng Khánh Tường | Thao tác thêm, sửa, xóa; nhập thông tin; xem tổng tiền và kết quả gửi đơn. | Chưa xác nhận tiến độ |
| CV09 | Thiết kế dữ liệu sản phẩm và đơn | Trần Hoàng Tân | Cấu trúc dữ liệu lưu tùy chọn, giá tại thời điểm đặt và trạng thái riêng biệt. | Chưa xác nhận tiến độ |
| CV10 | Xử lý kiểm tra và lưu đơn | Trần Hoàng Tân | Kiểm tra giá, vùng giao, tình trạng bán; chống đơn trùng; lưu đơn nhất quán. | Chưa xác nhận tiến độ |
| CV11 | Xây dựng quản trị và quyền truy cập | Trần Hoàng Tân | Đăng nhập, cập nhật sản phẩm và xử lý đơn trong quyền quản trị. | Chưa xác nhận tiến độ |
| CV12 | Tích hợp phương thức COD | Phạm Ngọc Minh Thư | Ghi nhận COD, số tiền cần thu; không yêu cầu thanh toán trước khi chuẩn bị. | Chưa xác nhận tiến độ |
| CV13 | Xử lý thu tiền và tình huống phát sinh | Phạm Ngọc Minh Thư | Cập nhật thu tiền; phân biệt hủy, giao thất bại và hoàn tất; có hướng dẫn thao tác. | Chưa xác nhận tiến độ |
| CV14 | Lập kịch bản nghiệm thu | Nguyễn Phi Long | Kịch bản theo F01–F11 và yêu cầu phi chức năng, có dữ liệu và kết quả mong đợi. | Chưa xác nhận tiến độ |
| CV15 | Kiểm thử chatbot hiện có | Nguyễn Phi Long | Bảng kết quả, lỗi và đề xuất phạm vi bàn giao; phối hợp người liên quan sửa lỗi. | Chatbot đã có theo ghi nhận; chưa xác nhận kết quả kiểm thử |
| CV16 | Kiểm thử tích hợp và theo dõi sửa lỗi | Nguyễn Phi Long | Kiểm tra luồng COD, lỗi nhập liệu, món hết, vùng giao, giá, đơn trùng và thu tiền. | Chưa xác nhận tiến độ |
| CV17 | Hoàn thiện tài liệu và GitHub Issues | Nguyễn Thị Thanh Vân | Tài liệu nhất quán; mỗi công việc có người phụ trách và tiêu chí kiểm tra. | Đã có bản thảo tài liệu; chưa xác nhận repository |
| CV18 | Chuẩn bị môi trường triển khai | Trần Hoàng Tân | Cấu hình chạy được, bảo vệ bí mật, kiểm tra luồng trên môi trường bàn giao. | Chưa xác nhận tiến độ |
| CV19 | Chuẩn bị kịch bản trình diễn | Nguyễn Phi Long | Dữ liệu giả lập, thao tác minh họa thành công và tình huống lỗi; các thành viên giải thích phần phụ trách. | Chưa xác nhận tiến độ |
| CV20 | Rà soát và chốt bàn giao | Nguyễn Thị Thanh Vân | Đối chiếu kết quả với yêu cầu; ghi giới hạn còn lại; kiểm tra liên kết tài liệu nộp. | Chưa xác nhận tiến độ |

Người phụ trách chính điều phối và chịu trách nhiệm kết quả; các thành viên vẫn hỗ trợ nhau. Việc sửa lỗi do thành viên phụ trách chức năng thực hiện, QA chịu trách nhiệm kiểm thử lại. Không giao toàn bộ việc lập trình hoặc quyết định yêu cầu cho AI.

## 4. Rủi ro

| Rủi ro | Tác động | Phương án xử lý | Người theo dõi chính |
| --- | --- | --- | --- |
| Mở rộng quá nhiều chức năng | Phân tán nguồn lực, luồng chính chưa hoàn thiện. | Ưu tiên F01–F11; chỉ mở rộng khi nhóm thống nhất và các chức năng cốt lõi ổn định. | Nguyễn Thị Thanh Vân |
| Công nghệ chưa thống nhất | Khó tích hợp và tổ chức mã nguồn. | Chốt phương án trước khi xây dựng phụ thuộc kỹ thuật; cập nhật tài liệu và hướng dẫn. | Trần Hoàng Tân |
| Thiếu quy tắc giao hàng hoặc phụ phí | Nhận sai vùng, tính sai tổng tiền. | Xác nhận với cửa hàng; chưa nhận đơn khi chưa xác định phí hoặc khả năng giao. | Nguyễn Thị Thanh Vân |
| Thông tin sản phẩm không chính xác | Khách hiểu sai món và tùy chọn. | Đối chiếu thực đơn, giá, thành phần và nội dung trước khi cập nhật. | Nguyễn Minh Đăng |
| Giao diện và backend không thống nhất | Mất tùy chọn, sai giá hoặc không lưu đơn. | Thống nhất dữ liệu và thông báo; kiểm thử tích hợp từng phần. | Tăng Khánh Tường |
| Đơn trùng, đơn rác hoặc khách không nhận COD | Tốn nguyên liệu và chi phí giao. | Chống gửi trùng, giới hạn gửi phù hợp; xác nhận đơn trước khi chuẩn bị; ghi nhận giao thất bại. | Phạm Ngọc Minh Thư |
| Ghi đã thanh toán khi chưa thu tiền | Sai dữ liệu và đối soát. | Tách trạng thái đơn và thanh toán; chỉ cập nhật thu tiền theo xác nhận thực tế; kiểm thử tình huống hủy. | Phạm Ngọc Minh Thư |
| Lộ dữ liệu hoặc khóa dịch vụ | Ảnh hưởng thông tin khách và hệ thống. | Kiểm tra quyền, dùng dữ liệu giả lập, không đưa bí mật vào mã công khai hoặc trình duyệt. | Trần Hoàng Tân |
| Chatbot trả lời sai hoặc thao tác không đúng | Gây hiểu nhầm về sản phẩm, đơn hàng. | Kiểm thử riêng; giới hạn khả năng bàn giao; bảo đảm luồng mua hàng không phụ thuộc chatbot. | Nguyễn Phi Long |
| Xung đột khi cùng sửa mã hoặc tài liệu | Mất nội dung và khó tích hợp. | Phân người phụ trách, dùng nhánh công việc và kiểm tra trước khi hợp nhất. | Nguyễn Thị Thanh Vân |
| Nội dung AI không đúng thực tế | Sai yêu cầu hoặc báo cáo không có minh chứng. | Lưu prompt, kết quả và quyết định riêng; đối chiếu tài liệu; thành viên phụ trách kiểm tra. | Nguyễn Thị Thanh Vân |
| Môi trường bàn giao khác môi trường phát triển | Không chạy được hoặc phát sinh lỗi. | Ghi hướng dẫn cấu hình; thử luồng đầy đủ trên môi trường bàn giao trước trình diễn. | Trần Hoàng Tân |

