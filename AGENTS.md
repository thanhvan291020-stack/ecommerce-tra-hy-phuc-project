# Project Instructions for AI

## 1. Project context

Đây là dự án website thương mại điện tử của Nhóm 8 dành cho thương hiệu Trà Hỷ Phúc, thực hiện trong học phần Phát triển ứng dụng thương mại điện tử.

Website theo mô hình B2C, kinh doanh đồ uống pha sẵn, trà khô đóng gói, món tráng miệng và topping. Mục tiêu là giúp khách nhận diện đúng cửa hàng, tìm hiểu sản phẩm, đặt hàng thuận tiện và hỗ trợ cửa hàng quản lý sản phẩm, đơn hàng.

Phiên bản đầu sử dụng thanh toán khi nhận hàng (COD). Khách đặt hàng không cần tài khoản; cửa hàng xác nhận, chuẩn bị và giao hàng; khách thanh toán khi nhận hàng. Không yêu cầu khách thanh toán trước khi cửa hàng chuẩn bị món.

AI hỗ trợ phân tích, lập trình, kiểm thử và tài liệu. Nhóm sinh viên chịu trách nhiệm đánh giá, xác nhận phương án và kiểm tra kết quả; AI không thay thế quyết định của nhóm.

## 2. Scope

- Chỉ triển khai các chức năng đã được nhóm thống nhất trong `REQUIREMENTS.md`.
- Đọc `README.md` để hiểu dự án và `PROJECT_PLAN.md` để nắm phân công trước khi thực hiện công việc liên quan.
- Ưu tiên chức năng cốt lõi: thông tin cửa hàng, danh mục, chi tiết sản phẩm, tùy chọn món, giỏ hàng, kiểm tra vùng giao, đặt hàng COD và quản trị sản phẩm, đơn hàng.
- Giữ nguyên nguyên tắc phân biệt trạng thái xử lý đơn với trạng thái thanh toán. Đơn đã xác nhận hoặc đang giao vẫn có thể chưa thanh toán; chỉ ghi đã thanh toán khi có xác nhận thu tiền.
- Không tự đưa các chức năng phát triển sau vào phạm vi hiện tại, gồm thanh toán trực tuyến, tài khoản khách hàng, tra cứu đơn trực tuyến, gợi ý món thay thế và các chức năng mở rộng khác được nêu trong `REQUIREMENTS.md`.
- Không tự bổ sung quản lý tồn kho theo nguyên liệu, tích điểm, cá nhân hóa hoặc quản lý nhiều chi nhánh.
- Với chatbot hiện có, chỉ kiểm thử và sửa trong phạm vi nhóm giao. Không tự mở rộng quyền truy cập dữ liệu hoặc khả năng thao tác đơn hàng của chatbot.
- Không tự đặt vùng giao, phí giao, phụ phí, tùy chọn món hay chính sách hủy đơn. Nếu thiếu thông tin, nêu rõ nội dung cần nhóm xác nhận.
- Khi yêu cầu mới mâu thuẫn với tài liệu, chỉ rõ điểm khác biệt, đề xuất cập nhật và chờ nhóm xác nhận trước khi triển khai.

## 3. Coding principles

- Giữ mã nguồn dễ đọc, dễ bảo trì; dùng tên biến, hàm và thành phần thể hiện rõ mục đích.
- Tuân thủ cấu trúc và quy ước của mã nguồn hiện có; không tự chọn hoặc thay đổi nền tảng, framework, cơ sở dữ liệu khi nhóm chưa thống nhất.
- Không thay đổi kiến trúc lớn, bổ sung phụ thuộc quan trọng hoặc thay đổi cấu trúc dữ liệu có ảnh hưởng rộng khi chưa được nhóm đồng ý.
- Không tự ý xóa, vô hiệu hóa hoặc thay thế chức năng đang hoạt động.
- Ưu tiên thay đổi nhỏ, đúng phạm vi, có thể kiểm tra và khôi phục.
- Không chỉnh sửa những phần không liên quan đến nhiệm vụ được giao.
- Kiểm tra dữ liệu đầu vào và các quy tắc nghiệp vụ ở phía xử lý; không chỉ dựa vào kiểm tra trên giao diện.
- Không tin giá hoặc tổng tiền do trình duyệt gửi lên; tính lại theo dữ liệu và quy tắc được nhóm xác nhận.
- Giữ giá tại thời điểm đặt trên đơn đã lưu; cập nhật giá thực đơn không được tự thay đổi giá đơn cũ.
- Tránh tạo đơn trùng khi khách gửi lặp cùng yêu cầu; xử lý lỗi lưu dữ liệu rõ ràng, không báo thành công khi chưa lưu được đơn.
- Không đánh dấu hoàn tất khi chưa xác nhận giao thành công và thu đủ tiền theo quy trình COD đã thống nhất.
- Không che giấu lỗi bằng cách bỏ kiểm tra, bỏ qua ngoại lệ hoặc trả kết quả thành công giả.

## 4. Workflow

### Trước khi sửa mã nguồn

1. Đọc các tài liệu liên quan, đặc biệt `REQUIREMENTS.md`, `PROJECT_PLAN.md`, hướng dẫn chạy và mã nguồn của chức năng cần sửa.
2. Phân tích hiện trạng: chức năng đang hoạt động thế nào, vấn đề cần giải quyết, dữ liệu và thành phần có thể bị ảnh hưởng.
3. Đề xuất phương án, nêu mục tiêu, các file dự kiến sửa, tác động và cách kiểm thử. Phân biệt nội dung đã xác minh với giả định.
4. Chờ nhóm xác nhận phương án trước khi sửa mã nguồn. Nếu nhóm đã xác nhận một phương án cụ thể trong cùng nhiệm vụ, thực hiện trong phạm vi đó; thay đổi vượt phương án phải được xác nhận bổ sung.

Trong lúc chờ xác nhận, AI có thể tiếp tục đọc và phân tích tài liệu hoặc mã nguồn liên quan, nhưng không thực hiện thay đổi mã nguồn hay dữ liệu vận hành.

### Trong quá trình thực hiện

- Chỉ sửa những nội dung thuộc phương án được xác nhận.
- Giữ nguyên thay đổi của thành viên khác; không tự ghi đè hoặc hoàn tác phần việc chưa được giao.
- Nếu phát hiện vấn đề làm thay đổi phạm vi hoặc có nguy cơ ảnh hưởng dữ liệu, dừng phần liên quan và báo nhóm để thống nhất cách xử lý.
- Kiểm thử phù hợp với thay đổi, gồm tình huống hợp lệ và tình huống lỗi liên quan.
- Không dùng dữ liệu khách hàng thật hoặc tạo giao dịch thật để kiểm thử khi chưa được phép.

### Sau khi sửa mã nguồn

1. Giải thích nội dung đã thay đổi và lý do thay đổi.
2. Liệt kê các file đã sửa, nêu vai trò của từng thay đổi chính.
3. Hướng dẫn cách chạy và kiểm thử; ghi rõ kiểm thử đã thực hiện, kết quả và phần chưa thể kiểm tra.
4. Báo cáo giới hạn còn tồn tại, lỗi chưa xử lý và điều kiện cần nhóm xác nhận.
5. Đề xuất cập nhật tài liệu nếu hành vi hoặc cách vận hành thay đổi; ghi nhận việc sử dụng AI trong `AI_USAGE_LOG.md` khi được giao cập nhật nhật ký.

Không tự đánh dấu công việc hoàn thành nếu chưa có căn cứ đáp ứng tiêu chí nghiệm thu. Khi môi trường không cho phép chạy kiểm thử, nêu rõ giới hạn thay vì khẳng định chức năng đã hoạt động đúng.

## 5. Security

- Không đưa mật khẩu, API key, token hoặc thông tin kết nối thật vào mã nguồn, tài liệu, nhật ký công khai hay repository.
- Không in hoặc sao chép giá trị bí mật vào phản hồi, ảnh minh họa hoặc kết quả kiểm thử.
- Dùng cấu hình môi trường hoặc cơ chế quản lý bí mật phù hợp với công nghệ đã thống nhất; file cấu hình mẫu chỉ chứa giá trị giả lập.
- Không tự ý vô hiệu hóa xác thực, phân quyền hoặc kiểm tra bảo mật để làm chức năng chạy được.
- Các trang và thao tác quản trị phải được kiểm soát quyền; không chỉ ẩn nút trên giao diện.
- Không cho khách truy cập hoặc chỉnh sửa dữ liệu đơn của người khác bằng cách thay mã đơn hay tham số yêu cầu.
- Không sử dụng dữ liệu cá nhân thật khi chưa được phép; bản trình diễn và kiểm thử sử dụng dữ liệu giả lập.
- Chỉ thu thập thông tin cần thiết cho nghiệp vụ đã thống nhất; không tự bổ sung trường dữ liệu cá nhân.
- Không gửi thông tin khách hàng, bí mật hệ thống hoặc dữ liệu đơn hàng cho dịch vụ AI bên ngoài khi chưa được nhóm cho phép.
- Không tự xóa dữ liệu, đặt lại cơ sở dữ liệu, thay đổi quyền truy cập hoặc triển khai lên hệ thống đang vận hành khi chưa được nhóm xác nhận.
- Nếu phát hiện thông tin bí mật bị lộ, báo vị trí và loại thông tin cho nhóm; không nhắc lại giá trị bí mật trong phản hồi.

## 6. Communication

- Trao đổi với nhóm bằng tiếng Việt, diễn đạt rõ ràng và dễ hiểu; chỉ dùng thuật ngữ kỹ thuật khi cần thiết.
- Nếu yêu cầu chưa rõ hoặc thiếu thông tin ảnh hưởng cách triển khai, hỏi lại trước khi thực hiện phần phụ thuộc vào thông tin đó.
- Phân biệt rõ đề xuất của AI, yêu cầu đã được nhóm xác nhận và kết quả kiểm tra thực tế.
- Không trình bày đề xuất mới như quyết định đã được nhóm thông qua.
- Không tự tạo dữ liệu khảo sát, kết quả kiểm thử, phản hồi của công cụ AI khác hoặc xác nhận của cửa hàng.
- Khi có nhiều phương án, giải thích ngắn gọn tác động đến phạm vi, độ phức tạp, khả năng kiểm thử và bảo trì để nhóm lựa chọn.
- Khi gặp trở ngại, nêu vấn đề, phần việc bị ảnh hưởng và hướng xử lý đề xuất; không che giấu giới hạn.
- Báo cáo kết quả theo mục tiêu và tiêu chí nghiệm thu, giúp thành viên phụ trách hiểu và giải thích được phần việc.

