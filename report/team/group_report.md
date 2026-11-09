# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> **BẢN LÀM VIỆC CHỜ NHÓM XÁC NHẬN.** Nội dung về quy trình và giải pháp bên dưới là các gợi ý để nhóm tự kiểm tra, không phải kết quả phỏng vấn, thử nghiệm hay quyết định đã được xác minh. Theo RULES.md, AI chỉ hỗ trợ phản biện Problem Statement và quyết định; nhóm cần tự viết/chốt các phần này sau thảo luận.

## 1. Thông tin nhóm

- **Tên nhóm:** ngocquantruonganh (L3A)
- **Thành viên:** xem `TEAM.md` (chưa có danh sách xác nhận trong tài liệu cung cấp)
- **Candidate problem được chọn:** Thu thập, nhập và chuẩn hóa dữ liệu báo cáo tài chính (BCTC) 5 năm của doanh nghiệp cần xếp hạng và 5–10 doanh nghiệp so sánh (peer) đang tốn nhiều thời gian nhập liệu thủ công.
- **Cơ sở lựa chọn:** Anh Lê Hoàng Quân cho biết cả nhóm nhất trí với đề xuất trong báo cáo cá nhân của anh. **Nhóm cần xác nhận lại** biên bản pitch, các candidate của thành viên khác, chấm điểm và phạm vi đề tài cuối cùng.
- **Quyết định cuối:** *Chưa chốt — cần hoàn thành CP4–CP6.*

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Lê Hoàng Quân | Khi phân tích tín nhiệm, tôi muốn có bộ BCTC 5 năm đã chuẩn hóa của doanh nghiệp và peer để phân tích nhất quán | Chuyên viên phân tích tín nhiệm | Nhập số liệu thủ công; toàn quy trình khoảng 1–2 ngày | **[Nhóm ghi câu hỏi thực tế và người hỏi]** |
| 2 | Lê Hoàng Quân | Khi lập báo cáo, tôi muốn đối chiếu dữ liệu giữa BCTC, Excel và nội dung báo cáo để giảm sai lệch | Chuyên viên và người rà soát | Đối chiếu thủ công 1–3 giờ | **[Ghi câu hỏi thực tế]** |
| 3 | Lê Hoàng Quân | Khi đánh giá doanh nghiệp, tôi muốn tổng hợp thông tin từ các nguồn khác nhau để có căn cứ nhận định | Chuyên viên phân tích | Tổng hợp nhiều nguồn 1–2 ngày | **[Ghi câu hỏi thực tế]** |
| 4 | Nguyễn Thế Trường | Khi đến hạn nộp bài lab hàng tuần, tôi muốn đối chiếu toàn bộ checklist và cấu trúc file nộp, để không bị trừ điểm vì lỗi format ngớ ngẩn | Sinh viên thực hành lab | Rà soát thủ công từng file và mục báo cáo markdown (20–25 phút) | *"Nếu chỉ kiểm tra tên file và định dạng thì viết script regex/linter là xong, việc gì phải dùng AI?"* (Lê Hoàng Quân hỏi) |
| 5 | Nguyễn Thế Trường | Khi ôn tập thi cuối kỳ, tôi muốn gom các câu hỏi và giải đáp của GV/TA trên Discord/Zalo, để ôn tập đúng trọng tâm mà không phải lội tin nhắn | Sinh viên chuẩn bị thi | Cuộn tìm tin nhắn và ghép cặp câu hỏi - lời giải đáp (60–75 phút) | *"Tin nhắn chat sinh viên viết tắt và ngắt quãng nhiều thì làm sao gom đúng ngữ cảnh?"* (Đỗ Văn Ngọc hỏi) |
| 6 | Nguyễn Thế Trường | Khi thực hành AI mới, tôi muốn tự động sửa các lỗi xung đột giữa PyTorch, CUDA và NVIDIA driver, để chạy code mẫu không mất cả buổi | Sinh viên học AI/Deep Learning | Tìm cách fix trên StackOverflow và gỡ cài lại nhiều lần (35–45 phút) | *"Mỗi máy một cấu hình card và OS khác nhau, tra cứu rule matrix có đủ không hay cần AI?"* (Đoàn Nhật Ánh hỏi) |
| 4–12 | **[Các thành viên khác điền]** | **[Candidate đã pitch]** | | | |

### 2.2. Cluster

| Cluster đề xuất để nhóm xem xét | Các candidate | Pattern chung |
|---|---|---|
| A — Chuẩn bị dữ liệu | Nhập, chuẩn hóa BCTC và peer | Dữ liệu phân tán, nhiều thao tác thủ công |
| B — Kiểm soát chất lượng | Đối chiếu số liệu giữa các nguồn và báo cáo | Cần phát hiện sai lệch, bảo đảm nhất quán |
| C — Tổng hợp bằng chứng | Thu thập, xác minh thông tin đa nguồn | Nhiều nguồn thông tin và công đoạn xác minh |

### 2.3. Opportunity Solution Tree rút gọn

```mermaid
flowchart TD
    O["Outcome: Rút ngắn thời gian chuẩn bị báo cáo mà vẫn giữ chất lượng"]
    O --> A["Pain: Nhập dữ liệu BCTC thủ công"]
    O --> B["Pain: Đối chiếu số liệu mất thời gian"]
    O --> C["Pain: Tổng hợp thông tin phân tán"]
```

Những ý là *solution* cần tách khỏi opportunity: “xây chatbot”, “làm AI Agent”, “dùng OCR” hoặc “viết chương trình Python”. Đây là phương án giải quyết, không phải vấn đề của người dùng.

### 2.4. Chấm điểm shortlist (1–5)

> **Nhóm tự chấm và ghi lý do; không sử dụng điểm do AI suy đoán.**

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được 4 mức | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Nhập và chuẩn hóa BCTC | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| Đối chiếu số liệu | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| Tổng hợp thông tin đa nguồn | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |

**Candidate được chọn theo thông tin anh Quân cung cấp:** Nhập và chuẩn hóa BCTC của doanh nghiệp và peer.

**Lý do đề xuất:** Công việc lặp lại; bottleneck nhập tay rõ; baseline tự báo cáo khoảng 1–2 ngày; có thể đo thời gian và sai lệch trên một bộ dữ liệu mẫu. **Cần nhóm xác nhận cách chấm và lý do loại ít nhất hai candidate còn lại.**

**Xử lý bất đồng:** [Nhóm ghi trung thực; nếu không có bất đồng, ghi rõ cách đạt đồng thuận.]

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map — danh sách giả định để kiểm chứng

| # | Giả định cần kiểm chứng | Loại | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | Nhập BCTC là công đoạn tốn thời gian nhất | Value | [ ] | [ ] | Có |
| 2 | Quy trình có thể rút ngắn mà vẫn giữ độ chính xác | Value | [ ] | [ ] | Có |
| 3 | BCTC của doanh nghiệp và 5–10 peer có thể thu thập hợp lệ, đủ 5 năm | Feasibility | [ ] | [ ] | Có |
| 4 | Một bộ ánh xạ chỉ tiêu có thể xử lý sự khác nhau giữa ngành và biểu mẫu | Feasibility | [ ] | [ ] | Có |
| 5 | Chuyên viên có thể rà soát và sửa lỗi từ hệ thống hỗ trợ | Usability | [ ] | [ ] | Có |
| 6 | Thời gian tiết kiệm lớn hơn chi phí triển khai, vận hành và kiểm soát | Viability | [ ] | [ ] | Có |

### 3.2. Kiểm chứng bằng người thật

**Tình trạng:** Chưa có phỏng vấn/survey được cung cấp. Nhóm phải tự phỏng vấn 2–3 người phù hợp hoặc làm micro-survey 5–10 người; không dùng AI giả lập người trả lời.

Các câu hỏi tham khảo theo *The Mom Test*:

1. Trong lần gần nhất xử lý dữ liệu BCTC, anh/chị đã thực hiện những bước nào?
2. Bước nào mất nhiều thời gian nhất? Có thể nhớ một ví dụ gần đây không?
3. Khi phát hiện dữ liệu không khớp, anh/chị xử lý ra sao?
4. Những công cụ hiện tại đã hỗ trợ được phần nào? Phần nào vẫn phải làm thủ công?

| Người được hỏi (vai trò, không ghi tên) | Thời điểm, phương pháp | Hành vi thực tế và thời gian | Workaround | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---|---|---|---|---|
| [Người 1] | [ ] | [ ] | [ ] | [ ] | [ ] |
| [Người 2] | [ ] | [ ] | [ ] | [ ] | [ ] |
| [Người 3, nếu có] | [ ] | [ ] | [ ] | [ ] | [ ] |

**Nhóm đã sửa problem thế nào sau kiểm chứng:** [Chỉ ghi sau khi có bằng chứng; kể cả trường hợp bằng chứng khiến nhóm phải đổi candidate hoặc bỏ AI.]

### 3.3. Research giải pháp đã có

> Dưới đây là **hướng nghiên cứu**, không phải kết quả research đã tự kiểm nguồn.

| Công cụ / pattern cần nghiên cứu | Link cần nhóm tự mở và kiểm | Bước có thể giải | Điểm cần thử | Khoảng trống cần kiểm chứng | Kết luận nghiên cứu |
|---|---|---|---|---|---|
| Excel Power Query | [Nguồn chính thức + ngày kiểm] | Import, chuyển đổi bảng có cấu trúc | Định dạng và ánh xạ nhiều file | PDF không đồng nhất, bảng phức tạp | [ ] |
| Python (pandas, công cụ trích bảng) | [Nguồn chính thức + ngày kiểm] | Chuẩn hóa, kiểm tra quy tắc | Tỷ lệ bao phủ các mẫu BCTC | Bảo trì parser | [ ] |
| OCR / trích xuất tài liệu có cấu trúc | [Nguồn chính thức + ngày kiểm] | Đọc bảng từ PDF/scan | Độ chính xác số âm, đơn vị, dòng gộp | Rủi ro nhầm hàng/cột | [ ] |

---

## 4. Quy trình trước/sau (CP5) — GỢI Ý ĐỂ NHÓM TỰ KIỂM

### 4.1. Quy trình hiện tại (nháp)

```mermaid
flowchart TD
    A["Xác định doanh nghiệp và peer"] --> B["Thu thập BCTC 5 năm"]
    B --> C["Nhập số liệu thủ công — bottleneck"]
    C --> D["Chuẩn hóa chỉ tiêu"]
    D --> E["Đối chiếu với nguồn gốc"]
    E --> F["Bộ dữ liệu được chấp thuận"]
```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | Chuyên viên | Danh sách doanh nghiệp cần xếp hạng | Danh sách 5–10 peer | [Cần đo] | Có thể khác theo ngành |
| 2 | Chuyên viên | Danh sách doanh nghiệp | BCTC 5 năm | [Cần đo] | Kiểm tra phiên bản, kỳ, hợp nhất/riêng |
| 3 | Chuyên viên | BCTC nguồn | Bảng nhập liệu | [Cần đo] | **Bottleneck theo kinh nghiệm anh Quân** |
| 4 | Chuyên viên | Bảng nhập liệu | Bộ chỉ tiêu chuẩn hóa | [Cần đo] | Kiểm tra đơn vị, định nghĩa |
| 5 | Chuyên viên/rà soát | Bảng dữ liệu, BCTC | Danh sách sai lệch và dữ liệu được duyệt | [Cần đo] | Kiểm soát nguồn |
| 6 | Chuyên viên | Dữ liệu đã duyệt | Bộ dữ liệu sẵn sàng phân tích | [Cần đo] | Lưu dấu vết |

**Baseline đã cung cấp:** khoảng 1–2 ngày làm việc cho việc nhập/chuẩn hóa BCTC. Chưa có đo thời gian từng bước và chưa chốt cách tính thời gian chờ.

### 4.2. Quy trình tương lai — hai phương án để đánh giá

```mermaid
flowchart TD
    A["Tải BCTC và lưu nguồn"] --> B["Rule/parser đọc bảng"]
    B --> C["Ánh xạ chỉ tiêu theo template"]
    C --> D["Kiểm tra số học, kỳ, đơn vị"]
    D --> E{"Chuyên viên xác minh"}
    E -->|Đạt| F["Phê duyệt dữ liệu"]
    E -->|Không đạt| G["Nhập/sửa thủ công từ BCTC"]
    G --> D
```

**Phương án A — Rule trước:** sử dụng dữ liệu có cấu trúc, Power Query/Python, bộ ánh xạ và đối chiếu số học; người dùng duyệt.

**Phương án B — Workflow có AI, nếu thử nghiệm A chưa đủ:** bước AI chỉ hỗ trợ trích xuất/đề xuất ánh xạ đối với tài liệu khó; hiển thị trang/dòng nguồn và mức tin cậy; không tự phê duyệt.

**Boundary đề xuất:** Không tự sửa BCTC nguồn, không tự suy diễn số liệu thiếu, không tự duyệt chỉ tiêu, không tự đưa ra bậc xếp hạng. Nếu lỗi hoặc thiếu nguồn, quay về quy trình nhập và đối chiếu thủ công.

### 4.3. Before / after — mục tiêu cần pilot

| Chỉ số | Trước | Sau (giả thuyết, chưa đo) | Cách kiểm |
|---|---|---|---|
| Tổng thời gian | 1–2 ngày | Mục tiêu thử nghiệm ≤4 giờ | Đo cùng phạm vi dữ liệu trước/sau |
| Tỷ lệ chỉ tiêu đúng | [Chưa đo] | Không thấp hơn baseline | Đối chiếu từng chỉ tiêu với BCTC gốc |
| Số bước thủ công | [Cần đếm] | [Cần pilot] | Nhật ký thao tác |
| Bottleneck | Nhập dữ liệu | Có thể chuyển sang kiểm tra ngoại lệ | Quan sát pilot |
| Rủi ro mới | Sai sót nhập tay | Sai ánh xạ/OCR, tự tin quá mức | Tỷ lệ ngoại lệ, dấu vết nguồn |

---

## 5. Problem Statement v0 (CP5)

> **PHẦN NHÓM PHẢI TỰ VIẾT VÀ CHỐT.** Gợi ý kiểm tra đủ sáu trường; không dùng đoạn gợi ý của AI làm sản phẩm nộp nguyên trạng.

| Trường | Câu hỏi nhóm cần trả lời từ dữ liệu đã kiểm chứng |
|---|---|
| **Actor** | Ai trực tiếp nhập và kiểm tra BCTC? Ai duyệt dữ liệu cuối? |
| **Quy trình** | Phạm vi 5 năm và 5–10 peer có áp dụng cho một báo cáo cụ thể không? |
| **Bottleneck** | Bao nhiêu phút thực sự nằm ở khâu nhập tay, bao nhiêu ở tìm kiếm và chuẩn hóa? |
| **Impact** | Việc chậm/nhập sai đã tác động đến thời hạn và chất lượng ra sao? |
| **Success Metric** | Baseline được đo thế nào, target nào nhóm chấp nhận, có chỉ tiêu chất lượng đi kèm không? |
| **Boundary** | Dữ liệu nào không được tự suy đoán; ai chịu trách nhiệm kiểm tra và phê duyệt? |

**Problem Statement v0 do nhóm tự viết:**

> [Nhóm điền sau khi có CP4 và sơ đồ CP5 được xác nhận.]

**Phản biện đã nhận và cách sửa:** [Nhóm ghi thật.]

---

## 6. Mức can thiệp AI (CP6) — KHUNG PHẢN BIỆN

### 6.1. Ma trận độ mơ hồ × độ phức tạp

**Nhóm tự xác định ô:** [ ]

**Lập luận cần kiểm tra:** Bảng và chỉ tiêu đã chuẩn hóa có độ mơ hồ thấp hơn PDF scan hoặc biểu mẫu không đồng nhất; không nên gộp mọi nguồn thành một nhóm.

### 6.2. So sánh bốn mức

| Mức | Phương án cần đánh giá | Đủ khi nào | Rủi ro chính | Nhóm chọn? |
|---|---|---|---|---|
| No AI | Checklist, phân công và biểu mẫu chuẩn | Phần lớn trễ do tổ chức công việc | Vẫn nhập tay | [ ] |
| Rule | Power Query/Python, kiểm tra số học và ánh xạ cố định | BCTC có cấu trúc đủ ổn định | Rule dễ vỡ khi biểu mẫu đổi | [ ] |
| Workflow | Rule kết hợp AI cho trường hợp khó, người duyệt | Tài liệu đa dạng vượt khả năng parser | Trích sai chỉ tiêu | [ ] |
| Agent | AI tự chọn nhiều bước và công cụ | Chỉ khi quy trình thực sự biến động, không thể định trước | Khó kiểm soát, chi phí, audit trail | [ ] |

**Mức nhóm chọn:** [Tự chốt sau CP4–CP5]

**Vì sao mức đơn giản hơn không đủ:** [Nêu bằng chứng pilot; nếu Rule đủ, không cần AI Canvas/PAIR.]

### 6.3. AI Canvas rút gọn (chỉ điền nếu chọn Workflow/Agent)

| Thành phần | Câu hỏi cần nhóm trả lời |
|---|---|
| Prediction | AI tạo bảng/ánh xạ chỉ tiêu nào? |
| Judgment | Chuyên viên kiểm tra số liệu nào và theo quy tắc nào? |
| Action | Ai duyệt bộ dữ liệu cuối? |
| Outcome | Thời gian, tỷ lệ chính xác và độ đầy đủ đo thế nào? |
| Input | File BCTC và template có đủ, hợp lệ và được phép xử lý không? |
| Feedback | Những lỗi ánh xạ nào được ghi lại để sửa quy trình? |

### 6.4. Hai câu hỏi Google PAIR (nếu dùng AI)

- **Augment hay automate:** [Nhóm tự đánh giá người dùng muốn AI hỗ trợ hay tự làm; không tự suy đoán.]
- **Báo nhầm hay bỏ sót nguy hiểm hơn:** [Xác định bằng ví dụ nghiệp vụ thật và cơ chế kiểm tra.]

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

> **Nhóm tự xây dựng v1 sau khi đối chiếu bằng chứng; AI chỉ dùng để chỉ ra điểm yếu.**

**Problem Statement v1:** [Nhóm điền đủ Actor, Quy trình, Bottleneck, Impact, Success Metric, Boundary, AI intervention point, Mức chọn, Rủi ro & người kiểm tra.]

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| [Nhóm chọn trường có thay đổi] | [ ] | [ ] | [Bằng chứng CP4–CP6] |

**Gợi ý thiết kế 3–5 tiêu chí eval để nhóm tự chốt:**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | Chính xác trị số | [Ngưỡng nhóm đo và xác nhận] | [Ngưỡng lỗi] |
| 2 | Đúng kỳ, loại báo cáo và đơn vị | [Kiểm tra được từ nguồn] | [Sai kỳ/đơn vị] |
| 3 | Truy xuất nguồn | [Có file, trang và vị trí số liệu] | [Không truy vết được] |
| 4 | Xử lý ngoại lệ | [Đưa người kiểm tra khi thiếu/không chắc] | [Tự suy đoán hoặc duyệt sai] |
| 5 | Thời gian xử lý | [Ngưỡng nhóm kiểm chứng] | [Vượt ngưỡng] |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ Thấp / Trung bình / Cao | Lý do / bằng chứng |
|---|---|---|---|
| Value | Chuyên viên có thật sự cần cải thiện không? | [Nhóm chấm] | [Phỏng vấn/đo thời gian] |
| Usability | Người dùng có kiểm được và sửa được dữ liệu không? | [Nhóm chấm] | [Thử nghiệm với chuyên viên] |
| Feasibility | Có đủ dữ liệu và công cụ để xử lý đúng không? | [Nhóm chấm] | [Kết quả thử BCTC đại diện] |
| Viability | Phù hợp chi phí, bảo mật và vận hành không? | [Nhóm chấm] | [Ước tính chi phí, quyền dữ liệu] |

### 8.2. Kết luận

**Quyết định Go / Not Yet / No-Go:** [NHÓM TỰ CHỐT]

**Lý do dựa trên bằng chứng:** [ ]

**Nếu Go — pilot nhỏ nhất:** [Phạm vi, người phụ trách, dữ liệu, thời hạn]

**Nếu Not Yet — cần kiểm chứng:** [ ]

**Nếu No-Go — giải pháp thay AI:** [ ]

**Ngưỡng dừng có thể đo:** [Nếu sau X tuần, chỉ tiêu Y không đạt ngưỡng Z, quay về quy trình nào?]

---

## 9. Hạn chế và hướng tiếp theo

1. Thời gian 1–2 ngày hiện là dữ liệu từ kinh nghiệm cá nhân của anh Quân; cần xác minh bằng các hồ sơ và người dùng khác.
2. Chưa có kết quả phỏng vấn/survey và tín hiệu phản bác.
3. Chưa đo thời gian từng bước và chất lượng dữ liệu baseline.
4. Chưa so sánh công cụ hiện có bằng thử nghiệm thực tế; chưa đủ căn cứ chọn Rule/Workflow/Agent hoặc quyết định Go.
5. Nhóm cần hoàn thiện `TEAM.md` và lưu bằng chứng hợp lệ trong `report/assets/`.

## 10. Tài liệu tham khảo

- Báo cáo cá nhân `report/individual/2A202603369_LeHoangQuan.md` — kinh nghiệm và số liệu tự khai về quy trình phân tích tín nhiệm.
- `README.md`, `RULES.md`, `CHECKPOINTS.md`, `RUBRIC.md`, `docs/01-worksheet.md` của repository đề bài VinUni.
- [Nhóm bổ sung 2–3 đường dẫn research đã trực tiếp mở và kiểm nội dung, kèm ngày truy cập.]
