# CP4 – Interview Snapshot 1
## Nghiên cứu quy trình thu thập và chuẩn hóa BCTC

### 1. Thông tin nghiên cứu

- **Checkpoint:** CP4 – Research
- **Chủ đề:** Thu thập, trích xuất và chuẩn hóa báo cáo tài chính (BCTC) 5 năm của doanh nghiệp và các doanh nghiệp peer.
- **Đối tượng dự kiến phỏng vấn:** Chuyên viên phân tích tín nhiệm hoặc người có kinh nghiệm xử lý báo cáo tài chính.
- **Mục tiêu:** Tìm hiểu quy trình hiện tại, xác định công đoạn tốn nhiều thời gian, khó khăn khi chuẩn hóa dữ liệu và nhu cầu cải thiện.

**Trạng thái:** Chuẩn bị nghiên cứu, chưa có dữ liệu phỏng vấn thực tế được xác nhận.

### 2. Vấn đề cần tìm hiểu

Trong quá trình phân tích tín nhiệm, chuyên viên cần thu thập BCTC của doanh nghiệp và các doanh nghiệp peer trong khoảng 5 năm. Dữ liệu có thể khác nhau về định dạng, cách trình bày, tên gọi chỉ tiêu và đơn vị tính.

Việc trích xuất, nhập liệu, ánh xạ và chuẩn hóa thủ công có thể làm tăng thời gian xử lý và nguy cơ sai sót. Nhóm cần tìm hiểu xem khó khăn lớn nhất nằm ở công đoạn nào và liệu các công cụ hỗ trợ có thể cải thiện quy trình hay không.

### 3. Câu hỏi phỏng vấn dự kiến

| STT | Câu hỏi | Mục đích |
|---|---|---|
| 1 | Anh/chị thường thực hiện những bước nào để chuẩn bị dữ liệu BCTC phục vụ phân tích tín nhiệm? | Tìm hiểu quy trình hiện tại |
| 2 | Anh/chị thường thu thập BCTC từ những nguồn nào? | Xác định nguồn dữ liệu |
| 3 | Việc thu thập BCTC trong 5 năm của doanh nghiệp và các peer có khó khăn gì? | Xác định khó khăn khi thu thập |
| 4 | Công đoạn nào thường mất nhiều thời gian nhất: thu thập, trích xuất, nhập liệu hay chuẩn hóa? | Xác định bottleneck |
| 5 | Anh/chị thường gặp khó khăn gì khi các BCTC có cách trình bày hoặc tên chỉ tiêu khác nhau? | Tìm hiểu vấn đề ánh xạ |
| 6 | Những lỗi nào thường xuất hiện khi nhập và chuẩn hóa số liệu? | Xác định rủi ro |
| 7 | Anh/chị đang sử dụng Excel, Power Query hoặc công cụ nào để hỗ trợ công việc? | Tìm hiểu giải pháp hiện tại |
| 8 | Những tiêu chí nào cần được kiểm tra trước khi chấp nhận bộ dữ liệu đã chuẩn hóa? | Xác định yêu cầu kiểm tra |
| 9 | Nếu có công cụ hỗ trợ trích xuất và ánh xạ chỉ tiêu, anh/chị cần kiểm tra những thông tin gì trước khi sử dụng kết quả? | Tìm hiểu yêu cầu đối với công cụ hỗ trợ |
| 10 | Theo anh/chị, thời gian xử lý dữ liệu có thể giảm xuống mức nào mà vẫn bảo đảm độ chính xác? | Xác định metric và mục tiêu |

### 4. Những thông tin cần ghi nhận khi phỏng vấn

| Nhóm thông tin | Dữ liệu cần thu thập |
|---|---|
| Khối lượng công việc | Số doanh nghiệp, số năm BCTC và số lượng chỉ tiêu cần xử lý |
| Thời gian | Thời gian cho từng công đoạn |
| Khó khăn | Định dạng tài liệu, tên chỉ tiêu, đơn vị và kỳ báo cáo |
| Sai sót | Số lỗi nhập liệu, lỗi ánh xạ và trường hợp phải làm lại |
| Công cụ | Excel, Power Query, OCR hoặc các công cụ đang sử dụng |
| Kiểm tra | Cách đối chiếu số liệu với tài liệu gốc và tiêu chí duyệt |

### 5. Giả thuyết nghiên cứu ban đầu

- Trích xuất, nhập liệu và chuẩn hóa có thể là những công đoạn tiêu tốn nhiều thời gian.
- Sự khác biệt về định dạng và tên gọi chỉ tiêu có thể làm tăng khối lượng công việc thủ công.
- Rule có thể xử lý các trường hợp có cấu trúc rõ ràng; AI/OCR có thể hỗ trợ những trường hợp phức tạp hơn.
- Chuyên viên vẫn cần kiểm tra và phê duyệt dữ liệu trước khi sử dụng.

### 6. Kết quả dự kiến và hướng kiểm chứng

Nhóm cần đối chiếu các giả thuyết trên với thông tin từ người có kinh nghiệm thực tế và tài liệu BCTC. Đặc biệt, cần đo riêng thời gian của từng công đoạn thay vì chỉ dựa vào tổng thời gian xử lý.

Baseline 1–2 ngày và mục tiêu thử nghiệm tối đa 4 giờ hiện là các giá trị được đề xuất trong Problem Card, chưa được xác nhận bằng phép đo thực tế.

### 7. Kết luận nghiên cứu ban đầu

Nghiên cứu tập trung xác định bottleneck trong quy trình chuẩn bị dữ liệu BCTC, đánh giá khả năng áp dụng Rule và AI để hỗ trợ trích xuất, ánh xạ và chuẩn hóa. Phạm vi giải pháp không bao gồm tự động đưa ra nhận định hoặc quyết định xếp hạng tín nhiệm. Chuyên viên phân tích vẫn giữ vai trò kiểm tra và phê duyệt dữ liệu cuối cùng.