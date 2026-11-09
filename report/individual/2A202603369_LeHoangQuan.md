# Báo cáo cá nhân — MSSV_HoTen

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Lê Hoàng Quân
- MSSV: 2A202603369
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: ngocquantruonganh
- Link repo nhóm: https://github.com/Dovanngoc05/K5-L3A-Day02-ngocquantruonganh-DiscoveryProblemFraming/tree/main/report

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi... tôi muốn... để... | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại | Khi phân tích tín nhiệm lần đầu cũng như định kỳ, tôi phải thu thập và chuẩn hóa BCTC từ nhiều doanh nghiệp, để bảo đảm dữ liệu đầu vào nhất quán. | Chuyên viên phân tích tín nhiệm | BCTC 5 năm gần nhất của doanh nghiệp và peer, tầm 1 - 2 ngày để nhập tay |
| 2 | Tốn thời gian | Khi lập báo cáo xếp hạng tín nhiệm, tôi muốn đối chiếu số liệu giữa BCTC, Excel và báo cáo phân tích, để hạn chế sai lệch. | Chuyên viên phân tích và người rà soát | Mất từ 1 đến 3 tiếng, tùy độ phức tạp |
| 3 | Cần đọc, tổng hợp nhiều thông tin | Khi đánh giá một doanh nghiệp, tôi muốn tổng hợp thông tin từ nhiều nguồn, để có đủ căn cứ đưa ra nhận định tín nhiệm. | Chuyên viên phân tích tín nhiệm | Từ nhiều nguồn: website doanh nghiệp, Google search, phỏng vấn doanh nghiệp, tốn từ 1 đến 2 ngày |
| 4 | Lặp lại | Khi viết báo cáo lần đầu cũng như cập nhật báo cáo định kỳ, tôi muốn cập nhật biểu đồ và nhóm doanh nghiệp so sánh, để kết quả phân tích phản ánh dữ liệu mới nhất. | Chuyên viên phân tích | Khoảng 20 biểu đồ và từ 1 đến 2 ngày làm việc |
| 5 | Pain từ người khác | Khi rà soát báo cáo tín nhiệm, tôi muốn kiểm tra tính nhất quán giữa nhận định và số liệu, để giảm số vòng chỉnh sửa. | Người kiểm soát chất lượng báo cáo | Cần 3-4 người rà soát, các lỗi về chính tả, logic, mức độ bám sát phương pháp luận, tính xác thực của thông tin |
| 6 | Cần đọc, tổng hợp nhiều thông tin | Khi giám sát rủi ro tín dụng, tôi muốn nhận diện sớm biến động chất lượng tài sản và thanh khoản, để kịp thời đánh giá rủi ro. | Chuyên viên quản trị rủi ro | 3 tháng một lần tôi phải đánh giá các thay đổi về vĩ mô, ngành và doanh nghiệp, ví dụ những biến động về lãi suất, tác động rất lớn đến ngành Bất động sản và doanh nghiệp như Vinhomes |
| 7 | Pain từ người khác | Khi người sử dụng đọc báo cáo, tôi muốn họ truy xuất được nguồn số liệu quan trọng, để thuận tiện kiểm tra và xác minh kết luận. | Người sử dụng và người rà soát báo cáo | Khách hàng có thể đọc báo cáo và phản hồi hoặc thắc mắc về dữ liệu, phương pháp luận|

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3


| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Thu thập và chuẩn hóa BCTC của doanh nghiệp và peer | Quy trình lặp lại ở mỗi kỳ phân tích; thời gian nhập thủ công khoảng 1–2 ngày; có thể đo hiệu quả cải thiện | Khả năng chuẩn hóa BCTC khác mẫu, mức độ đầy đủ và độ tin cậy của dữ liệu nguồn |
| 2 | Đối chiếu số liệu giữa BCTC, Excel và báo cáo phân tích | Tốn 1–3 giờ mỗi báo cáo; sai lệch số liệu có thể ảnh hưởng đến chất lượng phân tích tín nhiệm | Tỷ lệ sai sót thực tế, những sai lệch có thể phát hiện bằng quy tắc |
| 3 | Tổng hợp thông tin đa nguồn về doanh nghiệp | Tốn 1–2 ngày; liên quan trực tiếp đến việc thu thập bằng chứng cho nhận định tín nhiệm | Khả năng truy xuất nguồn, xác minh thông tin và xử lý dữ liệu không có cấu trúc |



### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi thực hiện phân tích tín nhiệm lần đầu hoặc định kỳ, tôi muốn thu thập và chuẩn hóa BCTC 5 năm của doanh nghiệp và các peer, để bảo đảm dữ liệu đầu vào nhất quán, đầy đủ và có thể so sánh. |
| Actor | Chuyên viên phân tích tín nhiệm |
| Thời điểm / bối cảnh | Khi bắt đầu đánh giá tín nhiệm hoặc cập nhật báo cáo định kỳ |
| Quy trình hiện tại (3–7 bước) | Xác định doanh nghiệp và peer → Thu thập BCTC → Trích xuất và nhập số liệu → Chuẩn hóa chỉ tiêu → Kiểm tra dữ liệu → Tổng hợp dữ liệu phân tích |
| Bottleneck (bước nào, mất bao nhiêu phút) | Trích xuất, nhập và chuẩn hóa số liệu BCTC thủ công; tổng thời gian quy trình khoảng 1–2 ngày làm việc. Cần đo riêng thời gian của bước nghẽn. |
| Impact (nếu không giải thì sao) | Tốn nguồn lực phân tích, làm chậm tiến độ báo cáo; tăng rủi ro sai sót khi nhập liệu |
| Success metric (baseline → target) | Baseline: 1–2 ngày làm việc. Target đề xuất thử nghiệm: tối đa 4 giờ. Đo thời gian từ khi bắt đầu thu thập đến khi bộ dữ liệu được kiểm tra và chấp thuận. |
| Phương án không dùng AI | Chuẩn hóa biểu mẫu Excel, sử dụng Power Query hoặc công cụ trích xuất dữ liệu có cấu trúc |
| Giả thuyết về AI (nếu có) | AI có thể hỗ trợ trích xuất và ánh xạ chỉ tiêu từ BCTC có cấu trúc khác nhau; chuyên viên vẫn kiểm tra số liệu |
| Cảm nhận nhanh | Workflow – cần kiểm chứng xem Rule có đủ đáp ứng hay không |

Quy trình nháp hiện tại:

```mermaid
flowchart TD
    A["Xác định doanh nghiệp và peer"] --> B["Thu thập BCTC 5 năm"]
    B --> C["Trích xuất và nhập dữ liệu"]
    C --> D["Chuẩn hóa các chỉ tiêu"]
    D --> E["Đối chiếu số liệu"]
    E --> F["Hoàn thành bộ dữ liệu"]
```

**Bottleneck dự kiến:** Trích xuất, nhập và chuẩn hóa dữ liệu thủ công.

**Thời gian:** Toàn bộ quy trình 1–2 ngày làm việc; cần bổ sung thời gian từng bước.


### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi lập báo cáo xếp hạng tín nhiệm, tôi muốn đối chiếu số liệu giữa BCTC, Excel và báo cáo phân tích, để hạn chế sai lệch và bảo đảm chất lượng báo cáo. |
| Actor | Chuyên viên phân tích tín nhiệm và người rà soát báo cáo |
| Thời điểm / bối cảnh | Trong quá trình lập, rà soát và hoàn thiện báo cáo xếp hạng tín nhiệm |
| Quy trình hiện tại (3–7 bước) | Hoàn thiện bảng tính → Lập báo cáo → Đối chiếu số liệu → Phát hiện sai lệch → Điều chỉnh → Rà soát lại |
| Bottleneck (bước nào, mất bao nhiêu phút) | Đối chiếu thủ công giữa BCTC, Excel và báo cáo; tổng thời gian khoảng 1–3 giờ tùy độ phức tạp |
| Impact (nếu không giải thì sao) | Tăng thời gian rà soát và nguy cơ sử dụng số liệu không nhất quán trong báo cáo |
| Success metric (baseline → target) | Baseline: 1–3 giờ. Target đề xuất: tối đa 30 phút. Đo thời gian hoàn tất kiểm tra một báo cáo và số sai lệch còn lại sau rà soát. |
| Phương án không dùng AI | Sử dụng Excel, công thức đối chiếu và các quy tắc kiểm tra tự động |
| Giả thuyết về AI (nếu có) | AI hỗ trợ phát hiện những điểm không nhất quán giữa số liệu và nhận định bằng văn bản |
| Cảm nhận nhanh | Rule hoặc Workflow; cần xác định những sai lệch nào vượt khả năng kiểm tra bằng quy tắc |

Quy trình nháp hiện tại:

```mermaid
flowchart TD
    A["Hoàn thiện bảng tính"] --> B["Lập báo cáo"]
    B --> C["Đối chiếu số liệu"]
    C --> D["Phát hiện sai lệch"]
    D --> E["Điều chỉnh"]
    E --> F["Rà soát lại"]
```

**Bottleneck dự kiến:** Đối chiếu và phát hiện sai lệch thủ công.

**Thời gian:** 1–3 giờ cho toàn bộ việc đối chiếu; cần đo thời gian riêng của từng bước.


### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi đánh giá tín nhiệm một doanh nghiệp, tôi muốn tổng hợp và xác minh thông tin từ nhiều nguồn, để có đủ căn cứ đưa ra nhận định tín nhiệm. |
| Actor | Chuyên viên phân tích tín nhiệm |
| Thời điểm / bối cảnh | Khi phân tích hồ sơ doanh nghiệp và lập báo cáo tín nhiệm |
| Quy trình hiện tại (3–7 bước) | Xác định nhu cầu thông tin → Thu thập thông tin từ website và nguồn công khai → Phỏng vấn doanh nghiệp → Đối chiếu và xác minh → Tổng hợp → Phân tích |
| Bottleneck (bước nào, mất bao nhiêu phút) | Thu thập, đối chiếu và tổng hợp thông tin từ các nguồn khác nhau; tổng thời gian khoảng 1–2 ngày |
| Impact (nếu không giải thì sao) | Kéo dài thời gian phân tích và có nguy cơ bỏ sót thông tin quan trọng |
| Success metric (baseline → target) | Baseline: 1–2 ngày. Target đề xuất: tối đa 4 giờ cho phần tổng hợp thông tin đã có sẵn; không tính thời gian chờ phỏng vấn. Đo thời gian thực hiện và tỷ lệ thông tin quan trọng có nguồn xác minh. |
| Phương án không dùng AI | Xây dựng checklist thông tin, biểu mẫu phỏng vấn và cơ sở dữ liệu nguồn |
| Giả thuyết về AI (nếu có) | AI hỗ trợ tìm kiếm, phân loại và tóm tắt tài liệu có dẫn nguồn; chuyên viên xác minh và tự đưa ra nhận định |
| Cảm nhận nhanh | Workflow; chưa có căn cứ để lựa chọn Agent |

Quy trình nháp hiện tại:

```mermaid
flowchart TD
    A["Xác định nhu cầu thông tin"] --> B["Thu thập thông tin công khai"]
    B --> C["Phỏng vấn doanh nghiệp"]
    C --> D["Đối chiếu và xác minh"]
    D --> E["Tổng hợp thông tin"]
    E --> F["Thực hiện phân tích"]
```

**Bottleneck dự kiến:** Thu thập và tổng hợp thông tin từ nhiều nguồn.

**Thời gian:** 1–2 ngày cho quy trình; cần tách thời gian làm việc thực tế khỏi thời gian chờ thông tin.

### Card muốn pitch nhất

- Card số: 1
- Vì sao: Đây là vấn đề lặp lại trong hoạt động phân tích tín nhiệm, có thời gian xử lý thực tế khoảng 1–2 ngày, ảnh hưởng trực tiếp đến tiến độ và chất lượng dữ liệu đầu vào. Bài toán có thể kiểm chứng bằng cách đo thời gian xử lý và đối chiếu độ chính xác của bộ dữ liệu sau chuẩn hóa.
- Câu hỏi muốn nhóm phản biện: Với các BCTC có biểu mẫu và cách trình bày khác nhau, liệu các công cụ dựa trên quy tắc như Excel hoặc Power Query đã đủ giải quyết vấn đề, hay cần kết hợp AI để trích xuất và chuẩn hóa dữ liệu?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|Chưa phân tách thời gian từng bước|Đồng ý|	Ghi rõ thời gian cho mỗi bước của cả 3 quy trình|
|Chưa rõ mức cần thiết của AI | Đồng ý| Kiểm tra Excel, Power Query và Rule trước|
|Phạm vi peer có thể quá rộng | Đồng ý| Xác định số peer fix là 10 doanh nghiệp|
---


## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card |Nhập BCTC 5 năm của doanh nghiệp cùng 5–10 peer mất 1–2 ngày.| Nhóm đồng ý |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: Một số bạn đưa ra vấn đề quá chung chung, bạn cần đi vào chi tiết 1 công việc cụ thể | Nhóm nhất trí với tôi|
| Nhận phản biện | Anh chưa ghi rõ khoảng thời gian cần thiết cho mỗi bước | Tôi đã bổ sung thông tin này |
| Chọn candidate problem | Ưu tiên các vấn đề cụ thể, trong công viêc thực tế hàng ngày| Nhóm đã nhất trí chọn vấn đề: Khi thực hiện phân tích tín nhiệm lần đầu hoặc định kỳ, tôi muốn thu thập và chuẩn hóa BCTC 5 năm của doanh nghiệp và các peer, để bảo đảm dữ liệu đầu vào nhất quán, đầy đủ và có thể so sánh |
| Kiểm chứng / research | Tôi kể cho các thành viên trải nghiệm thực tế trong công việc của mình | Tôi cho các thành viên trong nhóm xem 1 ví dụ về báo cáo xếp hạng tín nhiệm |
| Quy trình nhóm | Tôi đã đốc thúc các thành viên nhanh chóng thực hiện bài tập theo hướng dẫn và đúng tiến độ thầy giáo đề ra | Các thành viên đã nhất trí và cố gắng hoàn thiện nhanh hơn phần của mình |
| Problem Statement | Tôi đề xuất trưởng nhóm, sau đó đề xuất chọn Problem | Nhóm đã nhất trí với tôi. |
| Mức can thiệp AI | Tôi đánh giá phương án dùng Agent là tốt nhất | Nhóm đồng ý với tôi |
| Quyết định | Các tiêu Value, Usability, Feasibility và Viability đều ở mức chấp nhận được | Go |


---


## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Sử dụng ChatGPT để gợi ý và hệ thống hóa các vấn đề thực tế trong hoạt động phân tích và xếp hạng tín nhiệm doanh nghiệp. | AI giúp mở rộng các góc nhìn về công việc lặp lại, tốn thời gian, tổng hợp thông tin và khó khăn của người sử dụng báo cáo. | Các gợi ý ban đầu mang tính khái quát, chưa phản ánh đầy đủ đặc thù nghiệp vụ và thiếu bằng chứng định lượng. | Tôi lựa chọn 7 vấn đề phù hợp với công việc thực tế, bổ sung thời gian và tần suất xử lý: nhập BCTC 1–2 ngày, đối chiếu số liệu 1–3 giờ, tổng hợp thông tin 1–2 ngày và cập nhật khoảng 20 biểu đồ trong 1–2 ngày. |
| CP2 Problem Card | Nhờ ChatGPT phân tích, phản biện và gợi ý cấu trúc cho 3 Problem Cards ưu tiên; hỗ trợ mô tả quy trình bằng Mermaid. | AI giúp làm rõ actor, Job Story, bottleneck, impact, success metric và các phương án giải quyết không cần AI. | AI ban đầu chưa xác định chính xác phạm vi dữ liệu, đề xuất thời gian từng bước và target cải thiện khi chưa có số liệu kiểm chứng. | Tôi bổ sung phạm vi BCTC 5 năm của doanh nghiệp và nhóm peer, xác định nhập liệu thủ công là bottleneck chính. Tôi phân biệt thời gian thực tế với giả định và yêu cầu so sánh Excel, Power Query, Python trước khi chọn AI. |
| CP4 Research | Sử dụng ChatGPT để lập danh sách các giả định cần kiểm chứng và gợi ý hướng nghiên cứu Power Query, Python, OCR và công cụ trích xuất BCTC. | AI giúp xác định những câu hỏi cần kiểm chứng, các phương án thay thế và những rủi ro cần nghiên cứu. | AI chưa có bằng chứng phỏng vấn thực tế hoặc kết quả thử nghiệm trên BCTC của doanh nghiệp và peer. Các công cụ mới chỉ là gợi ý nghiên cứu. | Tôi chưa xem các gợi ý là kết luận. Nhóm cần tự phỏng vấn người dùng, kiểm tra tài liệu nguồn và đánh giá công cụ trên bộ dữ liệu thực tế trước khi quyết định. |
| CP5 Quy trình | Nhờ ChatGPT gợi ý sơ đồ quy trình hiện tại và các phương án cải tiến, bao gồm bước kiểm tra của con người và phương án quay về xử lý thủ công. | AI giúp trực quan hóa quy trình, làm rõ điểm nghẽn nhập dữ liệu và xác định các bước có thể áp dụng quy tắc tự động hóa. | AI chưa có số liệu thời gian riêng của từng công đoạn và chưa chứng minh hiệu quả của quy trình tương lai. | Tôi giữ thời gian 1–2 ngày là baseline hiện có, không coi các thời gian phân bổ chưa được đo là dữ liệu thực tế. Quy trình tương lai chỉ được xem là phương án đề xuất để nhóm đánh giá. |
| CP5–6 Problem Statement | Sử dụng ChatGPT để rà soát các thành phần cần có của Problem Statement v0 và v1, gồm actor, workflow, bottleneck, impact, metric và boundary. | AI giúp chỉ ra các thông tin còn thiếu, đặc biệt là cách đo success metric, giới hạn quyền tự động hóa và trách nhiệm kiểm tra dữ liệu. | Các mục tiêu giảm thời gian và tính khả thi của giải pháp mới là giả thuyết. AI không có đủ bằng chứng để tự kết luận mức cải thiện hay viết Problem Statement cuối cùng thay nhóm. | Tôi xác định cần đo thời gian thực tế, kiểm soát độ chính xác và giữ quyền phê duyệt dữ liệu cho chuyên viên. Problem Statement chính thức sẽ do nhóm tự hoàn thiện sau khi kiểm chứng. |
| CP6 Mức can thiệp / quyết định | Nhờ ChatGPT gợi ý khung so sánh No AI, Rule, Workflow và Agent; xác định các nhóm rủi ro Value, Usability, Feasibility và Viability cần đánh giá. | AI giúp phân biệt tự động hóa bằng quy tắc với Workflow có AI, đồng thời gợi ý các giới hạn kiểm soát và tiêu chí đánh giá kết quả. | AI chưa có kết quả thử nghiệm để chứng minh Workflow tốt hơn Rule. Việc lựa chọn Agent hoặc đưa ra quyết định Go khi chưa có bằng chứng có thể dẫn đến giải pháp quá phức tạp. | Tôi ưu tiên đánh giá các giải pháp đơn giản như Excel, Power Query và Python trước. Chỉ xem xét AI cho các tài liệu khó trích xuất hoặc ánh xạ; quyết định Go / Not Yet / No-Go phải dựa trên bằng chứng và do nhóm thống nhất. |


---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**
Các vấn đề mà tất cả chúng tôi cùng gặp phải là xử lý các tác vụ lặp đi lặp lại, mặc dù đơn giản nhưng tốn nhiều thời gian và rất dễ có sai sót

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**
Có đôi lúc chúng tôi bị tình trạng như vậy. Tuy nhiên, chúng tôi nhận ra và xử lý tình trạng này bằng cách nghĩ nhiều hơn đến công việc và những vấn đề hàng ngày mình đang gặp phải

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**
Tôi có. Khi các bạn phản biện rằng vấn đề mà tôi đang gặp phải cũng khá phổ biến chứ không chỉ bó hẹp trong lĩnh vực tài chính của tôi. Sau khi tìm hiểu, tôi đã nhất trí với các bạn.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**
Tôi không thấy bất ngờ. AI giúp công việc nhanh hơn và giảm thiểu được sai sót

**6.5. Điều khó nhất khi viết Problem Statement là gì?**
Diễn giải các khái niệm trong lĩnh vực tài chính cho các thành viên không có background tài chính

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**
Tôi sẽ phản biện nhóm mạnh hơn ở điểm: so sánh các công cụ hiện có với AI để đảm bảo rằng AI có ưu thế rõ ràng, ngay cả với những nhân sự low-tech

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

Problem: Vấn đề nhóm tôi lựa chọn là việc thu thập, nhập và chuẩn hóa BCTC 5 năm của doanh nghiệp cùng 10 peer mất khoảng 1–2 ngày làm việc, trong đó nhập liệu thủ công là điểm nghẽn lớn nhất.

Quy trình: Quy trình hiện tại gồm xác định doanh nghiệp và peer, thu thập BCTC, nhập số liệu, chuẩn hóa chỉ tiêu, đối chiếu dữ liệu và hoàn thiện bộ dữ liệu phân tích.

Metric: Chúng tôi sử dụng thời gian xử lý làm chỉ tiêu chính, với baseline 1–2 ngày và mục tiêu thử nghiệm tối đa 4 giờ, đồng thời phải bảo đảm độ chính xác dữ liệu không suy giảm.

Boundary: Giải pháp không được tự tạo số liệu còn thiếu, tự sửa BCTC gốc hoặc tự phê duyệt dữ liệu; chuyên viên phân tích vẫn chịu trách nhiệm kiểm tra và xác nhận kết quả.

Mức can thiệp: Nhóm cần đánh giá Excel, Power Query và Python theo quy tắc trước; chỉ cân nhắc Workflow có AI nếu các phương án này không xử lý tốt sự khác biệt trong cấu trúc BCTC.

Rủi ro: Việc lựa chọn giải pháp phải xem xét nhu cầu thực tế, khả năng sử dụng, tính khả thi về dữ liệu và hiệu quả chi phí, đặc biệt là rủi ro trích xuất hoặc ánh xạ sai chỉ tiêu tài chính.

Quyết định: Sau khi kiểm chứng, nhóm quyết định Go, dựa trên kết quả đo lường, khả năng kiểm soát sai sót và mức độ cải thiện thực tế.

## 7. Tài liệu tham khảo

-
