# Requirements

**Dự án:** Thiết kế và phát triển website thương mại điện tử cho thương hiệu Trà Hỷ Phúc  
**Nhóm thực hiện:** Nhóm 8

Tài liệu xác định phạm vi và yêu cầu dự kiến do nhóm lựa chọn. Tiêu chí nghiệm thu là căn cứ để kiểm thử, không phải xác nhận các chức năng đã hoàn thành.

## 1. Mục tiêu dự án

Nhóm xây dựng website B2C cho Trà Hỷ Phúc để hỗ trợ khách hàng nhận diện đúng cửa hàng, tiếp cận thực đơn đầy đủ và đặt mua thuận tiện. Website phục vụ đồ uống pha sẵn, trà khô đóng gói, món tráng miệng và topping.

Các mục tiêu chính gồm:

- Thống nhất tên, địa chỉ và thông tin liên hệ để hạn chế nhầm lẫn với cửa hàng có tên tương tự.
- Cung cấp ảnh, giá, thành phần, hương vị và tùy chọn rõ ràng để khách dễ lựa chọn món.
- Phân biệt sản phẩm dùng ngay với trà khô tự pha, cung cấp quy cách và hướng dẫn phù hợp.
- Cho phép đặt hàng không cần tài khoản và thanh toán khi nhận hàng (COD).
- Giúp cửa hàng cập nhật thực đơn, tình trạng bán và quản lý quá trình xử lý đơn, giao hàng, thu tiền.

Giá trị dành cho khách hàng là giảm thao tác hỏi thông tin, biết tổng tiền trước khi đặt và lựa chọn sản phẩm phù hợp. Giá trị dành cho cửa hàng là tập trung dữ liệu sản phẩm và đơn hàng, hạn chế tiếp nhận món tạm hết hoặc đơn ngoài vùng phục vụ.

## 2. Phạm vi

### Trong phạm vi

- Thông tin cửa hàng, danh mục và chi tiết sản phẩm.
- Tùy chọn món được cửa hàng xác nhận và phụ phí tương ứng.
- Giỏ hàng, kiểm tra vùng giao và tổng tiền.
- Đặt hàng không cần đăng nhập, ghi nhận đơn COD và hiển thị mã đơn.
- Đăng nhập quản trị, quản lý sản phẩm, trạng thái bán và đơn hàng.
- Theo dõi trạng thái xử lý đơn và kết quả thu tiền COD riêng biệt.
- Kiểm thử giao diện, dữ liệu, quyền quản trị và quy trình mua hàng.
- Kiểm thử chatbot đã có để xác định phạm vi bàn giao. Chatbot không phải điều kiện bắt buộc để hoàn tất luồng đặt hàng.

### Ngoài phạm vi

Các chức năng sau chưa thuộc phạm vi bắt buộc của phiên bản đầu:

- Thanh toán trực tuyến, kết nối tự động đơn vị vận chuyển và đối soát thu hộ.
- Tài khoản khách hàng, lịch sử mua hàng và tra cứu đơn trực tuyến.
- Gợi ý món thay thế, tìm kiếm và bộ lọc nâng cao.
- Blog, mã giảm giá, tích điểm và gợi ý cá nhân hóa.
- Quản lý tồn kho theo định lượng nguyên liệu, nhiều chi nhánh và tài khoản riêng cho người giao hàng.

Các mã F12–F14 và F16 được giữ để thống nhất với báo cáo; đây là yêu cầu phát triển sau. Chỉ đưa vào triển khai khi nhóm cập nhật phạm vi và tiêu chí tương ứng.

## 3. Người dùng

| Vai trò | Quyền hạn | Giới hạn |
| --- | --- | --- |
| Khách chưa đăng nhập | Xem thông tin công khai; chọn món, sửa giỏ; nhập thông tin nhận hàng; gửi đơn COD và nhận mã đơn. | Không truy cập trang quản trị hoặc xem đơn của người khác; chưa có tra cứu đơn trực tuyến. |
| Quản trị viên | Quản lý danh mục, sản phẩm, tùy chọn và giá; xem đơn, xác nhận đơn; cập nhật giao hàng, hủy và thu tiền. | Phải đăng nhập bằng tài khoản được cấp quyền. |
| Khách hàng có tài khoản — phát triển sau | Mua hàng, cập nhật thông tin và xem lịch sử, trạng thái các đơn thuộc tài khoản. | Chưa triển khai trong phiên bản đầu; không được xem đơn thuộc tài khoản khác. |

Người giao hàng thực hiện giao và thu tiền bên ngoài website. Quản trị viên ghi nhận kết quả dựa trên thông tin xác nhận từ người giao hàng. Khách chưa có tài khoản sử dụng mã đơn khi liên hệ cửa hàng.

## 4. Yêu cầu chức năng

Mức ưu tiên gồm **Bắt buộc**, **Phát triển sau** và **Hiện có, cần kiểm thử**. Việc cần xác minh dữ liệu hoặc quy tắc không đồng nghĩa chức năng đã được triển khai.

### F01 — Xem thông tin cửa hàng

- **Mô tả:** Hiển thị tên, địa chỉ, liên hệ, giờ hoạt động, vùng giao và hướng dẫn mua hàng.
- **Người sử dụng:** Khách mua hàng.
- **Mức độ ưu tiên:** Bắt buộc.
- **Tiêu chí nghiệm thu:** Thông tin khớp với nội dung cửa hàng xác nhận; thống nhất giữa trang chủ, trang liên hệ và chân trang; khách tìm được hướng dẫn COD trước khi đặt.

### F02 — Xem danh mục và danh sách sản phẩm

- **Mô tả:** Phân loại đồ uống pha sẵn, trà khô và món tráng miệng; hiển thị ảnh, tên, giá và mô tả vị ngắn.
- **Người sử dụng:** Khách mua hàng.
- **Mức độ ưu tiên:** Bắt buộc.
- **Tiêu chí nghiệm thu:** Chọn danh mục hiển thị đúng sản phẩm; giá thống nhất với trang chi tiết; món tạm hết có thông báo rõ; trường hợp danh mục trống có thông báo phù hợp.

### F03 — Xem chi tiết sản phẩm

- **Mô tả:** Cung cấp ảnh, giá, thành phần chính, hương vị và tình trạng bán; trà khô có quy cách, cách pha, bảo quản.
- **Người sử dụng:** Khách mua hàng.
- **Mức độ ưu tiên:** Bắt buộc.
- **Tiêu chí nghiệm thu:** Hiển thị đúng sản phẩm đã chọn và nội dung được cửa hàng duyệt; phân biệt rõ trà khô với đồ uống pha sẵn; không đưa công dụng chưa được xác minh vào mô tả.

### F04 — Chọn tùy chọn món

- **Mô tả:** Chọn kích cỡ, độ ngọt, lượng đá hoặc topping theo cấu hình từng món.
- **Người sử dụng:** Khách mua hàng.
- **Mức độ ưu tiên:** Bắt buộc đối với món có tùy chọn; cần xác nhận cấu hình và phụ phí.
- **Tiêu chí nghiệm thu:** Chỉ hiện lựa chọn cửa hàng phục vụ; tùy chọn bắt buộc phải được chọn; phụ phí được tính đúng; lựa chọn được giữ trong giỏ và đơn; không nhận topping tạm hết.

### F05 — Quản lý giỏ hàng

- **Mô tả:** Thêm, xóa và thay đổi số lượng; xem món, tùy chọn, phụ phí và tiền sản phẩm.
- **Người sử dụng:** Khách mua hàng.
- **Mức độ ưu tiên:** Bắt buộc.
- **Tiêu chí nghiệm thu:** Số lượng phải là số nguyên dương; cập nhật số lượng hoặc xóa món tính lại tiền; cùng món nhưng khác tùy chọn được phân biệt; giỏ trống không thể gửi đơn.

### F06 — Kiểm tra vùng giao và phí giao

- **Mô tả:** Kiểm tra địa chỉ theo vùng phục vụ và xác định phí, khả năng giao chung các nhóm hàng.
- **Người sử dụng:** Khách mua hàng.
- **Mức độ ưu tiên:** Bắt buộc; cần xác nhận quy tắc với cửa hàng.
- **Tiêu chí nghiệm thu:** Địa chỉ trong vùng được tính đúng phí; ngoài vùng có thông báo và không tiếp nhận đơn; chưa xác định được phí thì không cho gửi đơn; đơn hỗn hợp chỉ được nhận khi đáp ứng quy tắc giao chung.

### F07 — Đặt hàng không cần đăng nhập

- **Mô tả:** Nhập họ tên, số điện thoại, địa chỉ và ghi chú; kiểm tra dữ liệu, giá và khả năng phục vụ trước khi lưu.
- **Người sử dụng:** Khách mua hàng.
- **Mức độ ưu tiên:** Bắt buộc.
- **Tiêu chí nghiệm thu:** Không bắt buộc tài khoản; dữ liệu thiếu hoặc sai được báo rõ; hệ thống kiểm tra lại giá và tình trạng bán; nếu thông tin thay đổi, khách phải kiểm tra lại trước khi xác nhận; thao tác gửi lặp cùng yêu cầu không tạo đơn trùng.

### F08 — Ghi nhận đơn COD

- **Mô tả:** Lưu phương thức thanh toán khi nhận hàng, mã đơn, số tiền cần thu và trạng thái ban đầu.
- **Người sử dụng:** Khách mua hàng.
- **Mức độ ưu tiên:** Bắt buộc.
- **Tiêu chí nghiệm thu:** Đơn hợp lệ được lưu với mã riêng, trạng thái chờ xác nhận và chưa thanh toán; tổng tiền gồm tiền món, phụ phí và phí giao; trang kết quả chỉ báo thành công sau khi lưu đơn thành công; không yêu cầu thanh toán trước.

### F09 — Đăng nhập quản trị

- **Mô tả:** Xác thực tài khoản được cấp quyền quản trị.
- **Người sử dụng:** Quản trị viên.
- **Mức độ ưu tiên:** Bắt buộc.
- **Tiêu chí nghiệm thu:** Tài khoản hợp lệ truy cập được trang quản trị; thông tin sai bị từ chối; truy cập trực tiếp chức năng quản trị khi chưa đăng nhập bị chặn; đăng xuất kết thúc phiên truy cập.

### F10 — Quản lý sản phẩm

- **Mô tả:** Cập nhật danh mục, ảnh, mô tả, giá, tùy chọn, phụ phí và trạng thái bán.
- **Người sử dụng:** Quản trị viên.
- **Mức độ ưu tiên:** Bắt buộc.
- **Tiêu chí nghiệm thu:** Dữ liệu cập nhật được lưu và hiển thị đúng; giá âm hoặc dữ liệu bắt buộc bị thiếu không được lưu; món tạm hết bị chặn khi đặt; sửa giá thực đơn không thay đổi giá đã lưu trên đơn cũ.

### F11 — Quản lý đơn COD

- **Mô tả:** Xem thông tin đơn, xác nhận, cập nhật chuẩn bị, giao hàng, hoàn tất, hủy và kết quả thu tiền.
- **Người sử dụng:** Quản trị viên.
- **Mức độ ưu tiên:** Bắt buộc.
- **Tiêu chí nghiệm thu:** Xem đúng món, tùy chọn, giá và thông tin nhận hàng; phân biệt trạng thái xử lý với thanh toán; đơn có thể được chuẩn bị khi chưa thanh toán; chỉ ghi đã thanh toán khi xác nhận thu tiền; hoàn tất sau khi xác nhận giao thành công và thu đủ tiền; hủy hoặc giao thất bại có lý do, không tự ghi đã thu tiền.

### F12 — Tra cứu trạng thái đơn trực tuyến

- **Mô tả:** Xem trạng thái đơn thuộc tài khoản sau khi đăng nhập.
- **Người sử dụng:** Khách có tài khoản.
- **Mức độ ưu tiên:** Phát triển sau; phụ thuộc F14.
- **Tiêu chí nghiệm thu dự kiến:** Khi được triển khai, khách chỉ xem đơn của mình; truy cập đơn người khác bị từ chối; trạng thái khớp dữ liệu quản trị. Không dùng yêu cầu này làm điều kiện bàn giao phiên bản đầu.

### F13 — Gợi ý món thay thế

- **Mô tả:** Hiển thị món thay thế do cửa hàng lựa chọn cho món tạm hết.
- **Người sử dụng:** Khách mua hàng.
- **Mức độ ưu tiên:** Phát triển sau.
- **Tiêu chí nghiệm thu dự kiến:** Món gợi ý còn bán, liên kết đúng; khách tự quyết định lựa chọn; không tự đổi món trong giỏ. Không thuộc nghiệm thu bắt buộc phiên bản đầu.

### F14 — Quản lý tài khoản và lịch sử mua hàng

- **Mô tả:** Đăng ký, đăng nhập, cập nhật thông tin và xem lịch sử mua hàng.
- **Người sử dụng:** Khách có tài khoản.
- **Mức độ ưu tiên:** Phát triển sau.
- **Tiêu chí nghiệm thu dự kiến:** Xác thực đăng nhập; chỉ sửa thông tin và xem đơn thuộc tài khoản; không tự gán đơn khách vãng lai vào tài khoản chỉ vì trùng số điện thoại. Luồng đặt hàng không tài khoản vẫn hoạt động.

### F15 — Chatbot hỗ trợ lựa chọn sản phẩm

- **Mô tả:** Đánh giá chatbot hiện có trong phạm vi thông tin sản phẩm và thao tác thực sự được hỗ trợ.
- **Người sử dụng:** Khách mua hàng.
- **Mức độ ưu tiên:** Hiện có, cần kiểm thử trước khi đưa vào bàn giao.
- **Tiêu chí nghiệm thu:** Có bảng kịch bản và kết quả kiểm thử; thông tin giá, sản phẩm khớp dữ liệu được duyệt; không tự khẳng định công dụng hoặc thành công của thao tác chưa thực hiện; không tiết lộ dữ liệu đơn khác. Nếu có chức năng thêm giỏ thì phải kiểm tra món, tùy chọn và giá; lỗi chatbot không chặn luồng đặt hàng thông thường.

### F16 — Thanh toán trực tuyến

- **Mô tả:** Tích hợp phương thức trực tuyến và ghi nhận kết quả giao dịch khi nhóm mở rộng phạm vi.
- **Người sử dụng:** Khách mua hàng, quản trị viên.
- **Mức độ ưu tiên:** Phát triển sau.
- **Tiêu chí nghiệm thu dự kiến:** Chốt phương thức trước khi xây dựng tiêu chí chi tiết; kiểm thử thành công, thất bại, chưa xác minh và kết quả lặp; không ghi đã thanh toán nếu chưa có kết quả xác nhận. Không thuộc nghiệm thu COD phiên bản đầu.

## 5. Yêu cầu phi chức năng

| Mã | Yêu cầu | Tiêu chí kiểm tra |
| --- | --- | --- |
| NFR01 | Giao diện đáp ứng nhiều kích thước | Kiểm tra ở chiều rộng 375 px, 768 px và 1366 px; nội dung chính không bị che hoặc tràn ngang; thao tác giỏ và đặt hàng sử dụng được. |
| NFR02 | Kiểm tra dữ liệu đầu vào | Dữ liệu bắt buộc, số lượng, giá và tùy chọn được kiểm tra ở phía xử lý; sửa dữ liệu gửi từ trình duyệt không làm hệ thống chấp nhận giá hoặc tùy chọn sai. |
| NFR03 | Bảo vệ quyền truy cập | Trang và thao tác quản trị đều yêu cầu quyền phù hợp; khách không đọc hoặc sửa đơn khác bằng cách thay mã đơn. |
| NFR04 | Bảo vệ thông tin bí mật | Không đưa mật khẩu, khóa API hoặc thông tin kết nối thật vào repository, tài liệu hay mã gửi về trình duyệt; bản trình diễn dùng dữ liệu giả lập. |
| NFR05 | Nhất quán dữ liệu | Lưu giá tại thời điểm đặt; không tạo trùng khi gửi lặp; đơn, dòng sản phẩm và tổng tiền được ghi nhận thống nhất hoặc báo lưu thất bại. |
| NFR06 | Mã nguồn dễ kiểm tra | Tổ chức theo chức năng; tên gọi nhất quán; có hướng dẫn cấu hình và chạy sau khi chốt công nghệ; thay đổi được quản lý trong GitHub. |
| NFR07 | Thông báo dễ hiểu | Lỗi nhập liệu gắn với trường cần sửa; phân biệt đặt thành công, đang chờ xác nhận và đã thanh toán; không hiển thị chi tiết lỗi nội bộ cho khách. |
| NFR08 | Hạn chế lạm dụng gửi đơn | Có chống tạo trùng và giới hạn tần suất gửi theo ngưỡng nhóm thống nhất; kiểm thử ngưỡng và khả năng đặt lại hợp lệ. |
| NFR09 | Không mất thông tin khi có lỗi | Khi thao tác lưu hoặc cập nhật thất bại, không báo thành công; quản trị viên có thể kiểm tra kết quả thực tế trước khi thử lại. |

## 6. Giới hạn và giả định

### Giới hạn

- Nhóm có sáu thành viên, thực hiện theo phân công trong README và PROJECT_PLAN; ưu tiên nghiệp vụ bán hàng cốt lõi.
- Tài liệu hiện tại chưa chốt công nghệ frontend, backend, cơ sở dữ liệu và môi trường triển khai. Nhóm cập nhật sau khi thống nhất, không mặc định một nền tảng cụ thể.
- Phiên bản đầu dùng COD, chưa yêu cầu tích hợp cổng thanh toán hoặc dịch vụ giao hàng tự động.
- Chatbot đã có theo ghi nhận của nhóm nhưng chưa được coi là hoàn thành trước khi kiểm thử.
- Chưa xác định vùng giao, biểu phí, phụ phí, ngưỡng giới hạn gửi đơn và mọi quy tắc vận hành cụ thể; cần xác nhận trước nghiệm thu chức năng liên quan.

### Giả định và điều kiện cần xác minh

- Cửa hàng cung cấp hoặc duyệt tên sản phẩm, ảnh, giá, thành phần, tùy chọn, bảo quản và tình trạng bán.
- Cửa hàng xác nhận vùng giao riêng theo nhóm hàng, khả năng giao chung và cách tính phí.
- Có người phụ trách xác nhận đơn, cập nhật thực đơn và ghi nhận kết quả giao, thu tiền.
- Quy tắc thay đổi, hủy đơn và xử lý giao thất bại được cửa hàng xác nhận; hệ thống không tự suy đoán chính sách.
- COD là phương án nhóm lựa chọn; cách giao, thu hộ và đối soát cần được kiểm tra với cửa hàng trước vận hành thực tế.
- Thông tin khách hàng và dữ liệu trình diễn sử dụng dữ liệu giả lập; kết quả AI phải được thành viên phụ trách kiểm tra.
- Các chức năng ngoài phạm vi chỉ được bổ sung sau khi nhóm thống nhất và cập nhật tài liệu.

