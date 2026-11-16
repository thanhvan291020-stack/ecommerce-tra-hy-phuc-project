# AI Usage Log

**Dự án:** Thiết kế và phát triển website thương mại điện tử cho thương hiệu Trà Hỷ Phúc  
**Nhóm thực hiện:** Nhóm 8

Nhật ký ghi nhận việc sử dụng AI để phân tích yêu cầu, phản biện và hoàn thiện tài liệu. Nhóm chịu trách nhiệm kiểm tra kết quả và quyết định phạm vi áp dụng. Nội dung dưới đây không phải bằng chứng các chức năng đã được lập trình hoặc kiểm thử thành công.

Các prompt được ghi là “tóm lược” thể hiện nội dung yêu cầu chính, không phải bản sao nguyên văn toàn bộ trao đổi. Nhóm lưu bản hội thoại hoặc phản hồi gốc làm minh chứng bổ sung. Nhật ký không ghi ngày hoặc mốc thời gian.

## Lần sử dụng 1 — Phân tích yêu cầu dự án

### Công cụ

ChatGPT.

### Mục đích

Phân tích mục tiêu, người dùng, chức năng, quy trình nghiệp vụ và phạm vi phù hợp với dự án website Trà Hỷ Phúc của nhóm sáu thành viên.

### Prompt chính

*Tóm lược yêu cầu phân tích đã được trình bày trong báo cáo:*

> Bạn là chuyên gia phân tích nghiệp vụ cho dự án thương mại điện tử. Dựa trên thông tin Trà Hỷ Phúc, sản phẩm, khách hàng mục tiêu, vấn đề kinh doanh, kết quả khảo sát ba website và nguồn lực nhóm, hãy đề xuất mục tiêu và phạm vi, người dùng và quyền hạn, chức năng, quy trình nghiệp vụ, yêu cầu phi chức năng, chức năng phiên bản đầu, chức năng phát triển sau, rủi ro và cách giảm thiểu. Phân biệt yêu cầu bắt buộc, yêu cầu có thể phát triển sau và đề xuất cần xác minh. Giải thích cơ sở của từng đề xuất.

Bản Word có mẫu Prompt 1 còn các trường như `[Tên dự án]`, `[Mô tả]`; nhóm cần bổ sung bản prompt thực tế đã điền thông tin để hoàn thiện minh chứng.

### Kết quả đề xuất

- Ưu tiên danh mục, trang chi tiết, giỏ hàng, đặt hàng không cần tài khoản và quản trị sản phẩm, đơn hàng.
- Mô tả hương vị, thành phần và quy cách để khách dễ lựa chọn sản phẩm.
- Kiểm tra vùng giao, phí giao và tình trạng bán trước khi tiếp nhận đơn.
- Xác minh tùy chọn món, topping, phụ phí và khả năng giao chung trà khô với đồ uống.
- Có thể sử dụng COD; thanh toán trực tuyến và các chức năng nâng cao được xem xét sau.
- Giữ giá tại thời điểm đặt, chống tạo đơn trùng và bảo vệ quyền truy cập quản trị.

### Phản biện và đánh giá

Nhóm đối chiếu đề xuất với nhu cầu cửa hàng và khả năng thực hiện. Các chức năng quản lý nguyên liệu, tích điểm, cá nhân hóa và nhiều chi nhánh làm tăng phạm vi nên chưa được lựa chọn. Chatbot đã có theo ghi nhận của nhóm, vì vậy cần kiểm tra hiện trạng thay vì mặc định phát triển mới hoặc hoãn toàn bộ.

### Quyết định của nhóm

Giữ các chức năng bán hàng cốt lõi; lựa chọn COD cho phiên bản đầu; chỉ áp dụng tùy chọn và quy tắc giao hàng đã xác nhận. Không đưa các chức năng quản lý nâng cao vào phạm vi hiện tại. Kiểm thử chatbot trước khi xác định phạm vi bàn giao.

### Người kiểm tra

Nguyễn Thị Thanh Vân phụ trách tổng hợp; các thành viên kiểm tra nội dung liên quan đến phần việc được phân công. Đây là trách nhiệm kiểm tra theo phân công, không phải xác nhận mọi đề xuất đã được nghiệm thu.

## Lần sử dụng 2 — Phản biện độc lập yêu cầu

### Công cụ

Gemini — theo ghi nhận trong tài liệu nhóm cung cấp.

### Mục đích

Đánh giá độc lập bản yêu cầu do ChatGPT đề xuất, phát hiện nội dung thiếu, chưa rõ, vượt phạm vi hoặc có rủi ro dữ liệu và quyền truy cập.

### Prompt chính

*Tóm lược từ prompt Gemini trong tài liệu đã cung cấp:*

> Bạn là người phản biện độc lập cho dự án website thương mại điện tử của nhóm sinh viên. Dựa trên thông tin dự án, kết quả khảo sát ba website và danh sách yêu cầu do AI trước đề xuất, hãy đánh giá: yêu cầu có giải quyết vấn đề kinh doanh không; có trùng lặp, không cần thiết hoặc vượt phạm vi không; có thiếu chức năng hay quy trình không; có rủi ro dữ liệu, bảo mật và quyền riêng tư không; có nội dung chưa đủ rõ để lập trình, kiểm thử không. Với mỗi vấn đề, nêu lý do và đề xuất điều chỉnh. Không mặc định AI trước đúng và không tự ý thay đổi toàn bộ đề tài.

### Kết quả được ghi nhận trong bảng tổng hợp

Bảng phản biện trong tài liệu trước của nhóm ghi nhận các ý kiến: bổ sung mô tả vị trên danh sách; xem xét phân loại theo công dụng; dùng một vai trò quản trị; cấu hình vùng giao; gợi ý trà khô cho khách ngoài vùng giao đồ uống; bổ sung tra cứu đơn, món thay thế và biện pháp hạn chế đơn rác; lưu đơn giá tại thời điểm đặt; kiểm tra giao diện điện thoại.

**Tình trạng minh chứng:** Đã có prompt và bảng tóm tắt phản biện trong tài liệu, nhưng chưa có phản hồi Gemini nguyên văn trong các tệp đã được đối chiếu. Các ý kiến trên cần được nhóm kiểm tra với phản hồi gốc trước khi xác nhận là bản tổng hợp cuối cùng. Không xem phần diễn giải của ChatGPT là phản hồi mới của Gemini.

### Phản biện và đánh giá của nhóm

- Mô tả vị ngắn trên danh sách có thể giúp khách lựa chọn nhanh hơn.
- Phân loại theo công dụng như “Dễ ngủ”, “Đẹp da” chưa có đủ căn cứ cho từng sản phẩm.
- Một vai trò quản trị phù hợp với phạm vi phiên bản đầu.
- Tra cứu đơn, gợi ý thay thế và các chức năng mở rộng cần cân nhắc nguồn lực.
- COD cần xác nhận đơn trước khi chuẩn bị; chống tạo trùng không thay thế toàn bộ biện pháp hạn chế đơn rác.

### Quyết định được ghi trong bản thảo nhóm

Giữ mô tả vị, cấu hình vùng giao, lưu giá và kiểm thử giao diện; không lựa chọn bộ lọc công dụng; chưa triển khai tra cứu đơn và gợi ý thay thế. Giữ kiểm tra thông tin, chống gửi trùng và xem xét giới hạn tần suất phù hợp. Các quyết định được đối chiếu lại với phản hồi gốc và yêu cầu cửa hàng trước khi chốt.

### Người kiểm tra

Nguyễn Thị Thanh Vân phụ trách đối chiếu prompt, phản hồi gốc và bảng quyết định; Nguyễn Phi Long hỗ trợ rà soát nội dung kiểm thử. Việc đối chiếu phản hồi nguyên văn còn cần hoàn thiện.

## Lần sử dụng 3 — Rà soát bài và tách góc nhìn AI với nhóm sinh viên

### Công cụ

ChatGPT.

### Mục đích

Đối chiếu nội dung bài với yêu cầu giảng viên, chỉnh cách trình bày và phân biệt ý kiến AI với quyết định của nhóm.

### Prompt chính

*Tóm lược yêu cầu của nhóm trong hội thoại:*

> Đọc kỹ nội dung bài và yêu cầu giảng viên; kiểm tra mức độ đáp ứng, viết lại theo đúng chủ thể từng nhiệm vụ, tách biệt góc nhìn của AI với góc nhìn nhóm sinh viên.

### Kết quả đề xuất

- Nhiệm vụ 1–2 trình bày dưới góc nhìn nhóm thực hiện dự án.
- Nhiệm vụ 3 tách phần ChatGPT đề xuất và phần nhóm đánh giá.
- Nhiệm vụ 4 tách ý kiến phản biện của Gemini và quyết định của nhóm.
- Nhiệm vụ 5–7 thống nhất vai trò, chức năng, quy trình và cách phối hợp.
- Bổ sung tên bảng, tiêu chí kiểm tra và giải thích lý do giữ, điều chỉnh hoặc không lựa chọn chức năng.

### Phản biện và đánh giá

Nhóm yêu cầu diễn đạt dưới góc nhìn của chủ thể thực hiện, tránh đưa lời hướng dẫn của AI vào bài như kết luận của nhóm. Các khẳng định khảo sát website và kết quả kiểm thử phải có căn cứ; chỉnh văn phong không đồng nghĩa đã xác minh thực tế.

### Quyết định của nhóm

Sử dụng cấu trúc tách riêng đề xuất AI và đánh giá của nhóm; giữ quyết định cuối cùng ở phần nhóm sinh viên. Những nội dung thiếu minh chứng hoặc cần xác nhận với cửa hàng được ghi rõ điều kiện.

### Người kiểm tra

Nguyễn Thị Thanh Vân tổng hợp nội dung; các thành viên rà soát phần liên quan đến trách nhiệm của mình.

## Lần sử dụng 4 — Sửa lại phương án thanh toán COD

### Công cụ

ChatGPT.

### Mục đích

Khắc phục cách diễn giải sai về thời điểm thanh toán và thống nhất các phần của bài theo phương án nhóm lựa chọn.

### Prompt chính

*Tóm lược trao đổi xác nhận của nhóm:*

> Nhóm đang làm theo hướng cho khách đặt hàng rồi thanh toán khi nhận hàng (COD), thanh toán trực tuyến có thể làm sau. Viết lại bảng đánh giá của nhóm đối với đề xuất ChatGPT cho đúng hướng này.

### Kết quả đề xuất

ChatGPT trước đó đã diễn giải nhóm chọn thanh toán trước khi chuẩn bị và giao hàng. Sau khi nhóm đính chính, nội dung được sửa thành COD: cửa hàng xác nhận đơn, chuẩn bị và giao hàng; khách trả tiền khi nhận hàng.

### Phản biện và đánh giá

Nhóm xác nhận phương án thanh toán trước không đúng yêu cầu. Nhóm giữ đề xuất COD ban đầu, không chọn điều chỉnh sang thanh toán trước. Việc đã xác nhận đơn không có nghĩa đã nhận tiền.

### Quyết định của nhóm

- Dùng COD trong phiên bản đầu.
- Ghi đơn mới là chờ xác nhận và chưa thanh toán.
- Cho phép chuẩn bị, giao đơn đã được cửa hàng xác nhận dù chưa thu tiền.
- Chỉ ghi đã thanh toán khi xác nhận thu tiền; hoàn tất khi giao thành công và thu đủ tiền.
- Thanh toán trực tuyến thuộc phạm vi phát triển sau.

### Người kiểm tra

Nguyễn Thị Thanh Vân tổng hợp quyết định; Phạm Ngọc Minh Thư kiểm tra nghiệp vụ COD; Trần Hoàng Tân và Tăng Khánh Tường kiểm tra tính thống nhất khi triển khai.

## Lần sử dụng 5 — Làm rõ cách phối hợp thành viên

### Công cụ

ChatGPT.

### Mục đích

Viết mục phối hợp phù hợp với bảng phân công sáu thành viên trong bản Word.

### Prompt chính

*Tóm lược yêu cầu:*

> Dựa trên nội dung công việc của các thành viên trong file Word, kiểm tra và điều chỉnh mục 7.3 Cách phối hợp.

### Kết quả đề xuất

Làm rõ việc bàn giao từ UI/UX sang Frontend, phối hợp Frontend với Backend, tích hợp COD, kiểm thử và xử lý lỗi. Bổ sung vai trò trưởng nhóm trong quản lý yêu cầu và cập nhật tài liệu.

### Phản biện và đánh giá

AI sử dụng tên và vai trò có trong bảng phân công, không tự thay đổi trách nhiệm đã ghi. Các phần phối hợp được trình bày dưới dạng cách làm của nhóm, không phải xác nhận những công việc đó đã hoàn thành.

### Quyết định và phạm vi áp dụng

Giữ sáu vai trò đã phân công; sử dụng bản diễn đạt để nhóm rà soát và hoàn thiện mục 7.3. Mỗi công việc có người chịu trách nhiệm chính và thành viên phối hợp kiểm tra.

### Người kiểm tra

Nguyễn Thị Thanh Vân và toàn bộ thành viên đối chiếu nội dung phối hợp với công việc thực tế.

## Lần sử dụng 6 — Tạo tài liệu khởi tạo repository

### Công cụ

ChatGPT.

### Mục đích

Tạo các tài liệu Markdown theo mẫu giảng viên, dựa trên báo cáo và các quyết định nhóm đã xác nhận.

### Prompt chính

*Tóm lược các yêu cầu liên tiếp của nhóm:*

> Tạo README.md, REQUIREMENTS.md, PROJECT_PLAN.md và AGENTS.md theo mẫu, dựa trên file Word. Giữ đúng thành viên và phạm vi COD. Không ghi mục thời gian hoặc mốc ngày trong REQUIREMENTS.md và PROJECT_PLAN.md.

### Kết quả đề xuất

| Tài liệu | Nội dung được hỗ trợ |
| --- | --- |
| README.md | Giới thiệu, khách hàng, chức năng, thành viên, công nghệ dự kiến, các giai đoạn và liên kết tài liệu. |
| REQUIREMENTS.md | Mục tiêu, phạm vi, người dùng, yêu cầu chức năng F01–F16, tiêu chí nghiệm thu, yêu cầu phi chức năng và giả định. |
| PROJECT_PLAN.md | Sáu thành viên, các giai đoạn, công việc, người phụ trách, kết quả, trạng thái và rủi ro; không có cột thời hạn hay mốc ngày. |
| AGENTS.md | Nguyên tắc hỗ trợ đúng phạm vi, giữ chất lượng mã, chờ nhóm xác nhận trước khi sửa mã, kiểm thử, bảo mật và báo cáo. |

### Phản biện và đánh giá

- Tài liệu Word chưa xác định công nghệ đã thống nhất; AI ghi cần bổ sung thay vì tự chọn nền tảng.
- Công việc chưa có minh chứng hoàn thành được ghi chưa xác nhận tiến độ.
- Các tiêu chí nghiệm thu chi tiết do AI bổ sung là đề xuất để nhóm kiểm tra, không phải kết quả kiểm thử thực tế.
- Các liên kết tương đối chỉ hoạt động khi nhóm đặt đủ tệp trong đúng cấu trúc repository.
- Việc tạo tài liệu không đồng nghĩa đã tạo repository hoặc tải mã nguồn lên GitHub.

### Quyết định của nhóm và nội dung chờ rà soát

Giữ COD, tên và vai trò sáu thành viên; bỏ mục thời gian trong REQUIREMENTS.md và PROJECT_PLAN.md theo yêu cầu. Nhóm rà soát công nghệ, các ngưỡng kiểm tra và tiêu chí nghiệm thu trước khi dùng tài liệu làm căn cứ lập trình.

README được tạo trước yêu cầu bỏ thời gian và vẫn có khoảng ngày dự kiến ở mục kế hoạch. Nếu nhóm áp dụng yêu cầu bỏ thời gian cho toàn bộ tài liệu, README cần được cập nhật riêng; nhật ký này không khẳng định README đã được sửa.

### Người kiểm tra

Nguyễn Thị Thanh Vân tổng hợp; Hoàng Tân và Khánh Tường kiểm tra yêu cầu kỹ thuật; Minh Thư kiểm tra COD; Phi Long kiểm tra tiêu chí nghiệm thu; Minh Đăng kiểm tra nội dung và giao diện.

## Lần sử dụng 7 — Tổng hợp nhật ký sử dụng AI

### Công cụ

ChatGPT.

### Mục đích

Tạo AI_USAGE_LOG.md từ nội dung trao đổi và các tài liệu đã cung cấp, phân biệt đề xuất AI, phản biện và quyết định của nhóm.

### Prompt chính

> # AI_USAGE_LOG.md
> chạy giúp tôi nd mục này

### Kết quả đề xuất

Tổng hợp các lần sử dụng theo mục đích, prompt chính, kết quả, phản biện, quyết định và người kiểm tra; ghi rõ giới hạn minh chứng Gemini và các nội dung chưa được xác nhận.

### Phản biện và quyết định

Đây là bản nhật ký do AI hỗ trợ biên soạn để nhóm rà soát. Không dùng bản tóm tắt để thay thế phản hồi gốc hoặc tạo bằng chứng cho hoạt động chưa thực hiện. Nhóm bổ sung minh chứng và xác nhận nội dung trước khi nộp.

### Người kiểm tra

Nguyễn Thị Thanh Vân phụ trách tổng hợp cùng các thành viên.

## Nguyên tắc cập nhật nhật ký

- Ghi đúng công cụ và mục đích của từng lần sử dụng; không tự ghi phiên bản mô hình nếu không có thông tin xác nhận.
- Lưu prompt và phản hồi gốc khi có; phân biệt bản nguyên văn với phần tóm tắt hoặc tái lập.
- Tách đề xuất của AI, đánh giá của thành viên và quyết định nhóm đã thống nhất.
- Nêu rõ nội dung giữ lại, điều chỉnh, chưa áp dụng và lý do.
- Không ghi hoàn thành, kiểm thử đạt hoặc đã được cửa hàng xác nhận khi chưa có căn cứ.
- Không đưa mật khẩu, API key, token hay dữ liệu cá nhân khách hàng thật vào nhật ký.
- Bổ sung lần sử dụng mới khi AI hỗ trợ lập trình hoặc kiểm thử; ghi file thay đổi, kết quả kiểm tra và giới hạn thực tế.

