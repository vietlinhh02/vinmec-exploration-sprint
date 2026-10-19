# Bài tập 1 tuần: Thiết kế lại khoảnh khắc "Tìm khoa và Chọn bác sĩ" trên ứng dụng MyVinmec

**Ứng viên:** Nguyễn Viết Linh, Khóa K2  
**Hạn nộp:** 23h59 thứ Hai 19/10/2026  
**Email nhận bài:** anh.ntm2@vinuni.edu.vn  
**Tiêu đề:** `[Exploration Sprint] Bài tập 1 tuần – Nguyễn Viết Linh – Khóa K2`

---

## 1. Tóm tắt giải pháp

- **Khoảnh khắc lựa chọn:** Tìm chuyên khoa, diễn đạt triệu chứng và chọn bác sĩ khi đặt lịch khám ngoại trú trên MyVinmec. Thực tế cho thấy người bệnh thường không biết gọi tên triệu chứng bằng thuật ngữ y khoa, hoang mang trước bảng giá khám chênh lệch lớn (từ 500.000đ đến hơn 2.000.000đ) và lo sợ khám nhầm khoa gây tốn kém tiền bạc lẫn thời gian.
- **Giải pháp đề xuất (Vinmec SmartMatch AI):** Trợ lý tiền khám ảo giúp người bệnh mô tả triệu chứng qua bản đồ cơ thể tương tác (Body Map) và từ điển cảm giác đời thường ("nhói", "râm ran", "tức nặng"). Hệ thống gợi ý 2-3 bác sĩ phù hợp nhất theo chuyên môn sâu và ngân sách mong muốn (Best Match, Budget Match, Expert Match), cân bằng tải lịch khám tránh tình trạng ngõ cụt, đồng thời giữ chốt chặn an toàn với bộ lọc cờ đỏ cấp cứu (chuyển hướng 115 khi có dấu hiệu nguy kịch).

---

## 2. Cấu trúc bài nộp

| Thư mục | Nội dung chi tiết | Trạng thái |
|---|---|---|
| [`01-phong-van/`](01-phong-van/) | Báo cáo trải nghiệm thực tế ứng dụng MyVinmec; Interview Guide bán cấu trúc; 3 biên bản phỏng vấn sâu P1, P2, P3; Bảng tổng hợp insight | Đầy đủ dữ liệu thực nghiệm |
| [`02-journey-map/`](02-journey-map/) | Bản đồ hành trình 6 giai đoạn, biểu đồ cảm xúc thang điểm 1-5 (đáy tại bước 3) và trang trực quan [`journey-map.html`](02-journey-map/journey-map.html) | Hoàn chỉnh |
| [`03-need-statement/`](03-need-statement/) | Need Statement chuẩn Stanford Biodesign (Population, Problem, Outcome), đối chiếu bằng chứng thực tế và ranh giới Non-goals | Chuẩn Biodesign, không chứa giải pháp |
| [`04-best-practice/`](04-best-practice/) | 3 case study quốc tế có nguồn kiểm chứng: Ada Health (giao diện triệu chứng tự nhiên), Zocdoc (khớp chuyên môn và minh bạch giá), Mayo Clinic / NHS 111 (phân luồng an toàn) | Đầy đủ tài liệu đối sánh |
| [`05-prototype/`](05-prototype/) | Prototype tương tác mô phỏng điện thoại ([`index.html`](05-prototype/index.html)), kèm bộ điều khiển kịch bản giả lập, prompt an toàn lâm sàng ([`prompts.md`](05-prototype/prompts.md)) và nhật ký thử nghiệm 3 người dùng ([`test-log.md`](05-prototype/test-log.md)) | Sẵn sàng chạy thử nghiệm |
| [`06-rui-ro-dao-duc/`](06-rui-ro-dao-duc/) | Ma trận 6 rủi ro an toàn và đạo đức (sót cấp cứu, thiên vị thương mại, bảo mật dữ liệu theo Nghị định 13/2023/NĐ-CP) cùng quy trình can thiệp của nhân viên y tế | Hoàn chỉnh |
| [`07-coach-plan/`](07-coach-plan/) | Kế hoạch 1 trang coach nhóm sinh viên K4: Lịch trình 7 ngày, cẩm nang gỡ rối tình huống và bảng kiểm nghiệm thu | Hoàn chỉnh |
| [`slides.pdf`](slides.pdf) | Bài thuyết trình 10 trang định dạng PDF, biên dịch từ [`slides.html`](slides.html) | Đúng giới hạn 10 trang |

---

## 3. Cách chạy thử Prototype tương tác

1. Mở file [`05-prototype/index.html`](05-prototype/index.html) bằng trình duyệt web thông thường (Chrome, Edge hoặc Safari).
2. Trải nghiệm luồng 4 bước trong khung điện thoại mô phỏng:
   - **Bước 1:** Chạm vào vị trí đau trên bản đồ cơ thể hoặc gõ mô tả bằng lời văn tự nhiên.
   - **Bước 2:** Chọn từ ngữ miêu tả cảm giác từ danh sách gợi ý ("đau tức", "ợ chua sau ăn", "tê bì ngón tay").
   - **Bước 3:** Chọn mức ngân sách mong muốn (Tiêu chuẩn 550k, Nâng cao 800k, Chuyên gia 1.500k) và khung giờ khám.
   - **Bước 4:** Nhận kết quả phân tích phân luồng và 3 phương án bác sĩ kèm lời giải thích minh bạch lý do đề xuất.
3. Thử nhanh các kịch bản thực tế qua thanh công cụ giả lập ở cạnh khung máy:
   - *Kịch bản 1:* Đau ngực kèm ợ chua (tránh nhầm Tim mạch, hướng đúng khoa Tiêu hóa).
   - *Kịch bản 2:* Đau mỏi vai gáy tê bì tay (phân định Cơ xương khớp vs Ngoại thần kinh cột sống).
   - *Kịch bản 3:* Bác sĩ chuyên gia kín lịch (tự động gợi ý bác sĩ cùng ekip còn lịch trống ngày mai).
   - *Kịch bản 4:* Dấu hiệu nguy kịch (kích hoạt cảnh báo cờ đỏ cấp cứu và nút gọi 115 khẩn cấp).

---

## 4. Minh bạch về vai trò: Tác giả (Người dùng & Khởi xướng ý tưởng) và AI (Người phát triển kỹ thuật)

Theo yêu cầu minh bạch của đề bài, mối quan hệ và ranh giới trách nhiệm giữa tác giả và công cụ AI được xác lập như sau:

> **Bối cảnh vai trò:**  
> - **Tác giả (Đóng vai trò Người dùng thực tế & Chủ nhân ý tưởng):** Trực tiếp trải nghiệm ứng dụng MyVinmec với tư cách một người dùng thực tế, phát hiện các điểm nghẽn trải nghiệm và đưa ra toàn bộ ý tưởng cốt lõi: *làm tính năng chọn bác sĩ thông minh từ triệu chứng và nỗi đau đời thường, tính đến việc người bệnh khó mô tả nỗi đau của mình, tối ưu chi phí cho cả người bệnh lẫn bác sĩ, cân bằng tải lịch khám và giữ chốt chặn an toàn cấp cứu*. Tác giả trực tiếp chỉ đạo định hướng thiết kế và chịu trách nhiệm cao nhất về nội dung.  
> - **Công cụ AI (Đóng vai trò Người phát triển kỹ thuật - Developer):** Đóng vai trò là lập trình viên và người hỗ trợ kỹ thuật, nhận các bài toán, ý tưởng và yêu cầu từ tác giả để hiện thực hóa thành mã nguồn prototype tương tác (HTML/CSS/JS), hỗ trợ tra cứu tài liệu đối sánh, dựng layout slide và định dạng tài liệu theo chỉ đạo của tác giả.

| Hạng mục bài nộp | Vai trò của Tác giả (Người dùng & Định hướng ý tưởng) | Phần AI thực hiện (Người phát triển kỹ thuật từ ý tưởng) |
|---|---|---|
| `01-phong-van/*` | Trực tiếp dùng thử MyVinmec trên điện thoại với tư cách người dùng đi khám, phát hiện nỗi đau thực tế; trực tiếp phỏng vấn 3 người bệnh P1/P2/P3, ghi chép và trích dẫn dữ liệu thô | Hỗ trợ định dạng bảng ma trận insight, phân loại trích dẫn theo các cụm chủ đề |
| `02-journey-map/*` | Định hình 6 giai đoạn hành trình của người bệnh, xác định điểm đáy cảm xúc tại khâu chọn khoa và bác sĩ từ chính trải nghiệm của bản thân | Hỗ trợ cú pháp CSS và mã SVG vẽ đường biểu đồ cảm xúc |
| `03-need-statement/*` | Đề xuất bài toán cốt lõi, xác lập các thành phần Population, Problem, Outcome theo chuẩn Stanford Biodesign và ranh giới Non-goals | Rà soát câu chữ, kiểm tra lỗi vô tình lọt giải pháp vào câu Need Statement |
| `04-best-practice/*` | Đưa ra yêu cầu tìm kiếm các mô hình quốc tế giải quyết đúng bài toán diễn đạt triệu chứng bình dân (Ada Health) và minh bạch giá (Zocdoc) | Hỗ trợ tra cứu tài liệu học thuật, đối chiếu nguồn dẫn chứng từ BMJ và Lancet |
| `05-prototype/*` | Khởi xướng ý tưởng: Body Map, từ điển cảm giác đời thường ("nhói", "râm ran", "tức nặng"), 3 mức ngân sách (550k–1.5M) và kịch bản cờ đỏ cấp cứu; trực tiếp kiểm thử trên người dùng | Lập trình toàn bộ mã nguồn HTML/CSS/JavaScript cho giao diện mô phỏng điện thoại và bộ điều khiển kịch bản giả lập |
| `06-rui-ro-dao-duc/*` | Đặt ra các yêu cầu khắt khe về đạo đức y tế: chống thiên vị thương mại ép khám Giáo sư, bảo vệ dữ liệu theo Nghị định 13/2023/NĐ-CP và quyền ghi đè của điều dưỡng | Soạn thảo ma trận rủi ro chi tiết và mô hình hóa quy trình can thiệp lâm sàng theo chỉ đạo của tác giả |
| `07-coach-plan/*` | Đúc kết kinh nghiệm thực tế thành cẩm nang gỡ rối và phương pháp hướng dẫn nhóm sinh viên khóa sau (K4) | Hỗ trợ định dạng bảng biểu và bố cục 1 trang |
| `slides.pdf` | Chọn lọc luận điểm thuyết trình, quyết định nội dung từng trang, duyệt bố cục và trực tiếp bảo vệ bài | Dựng mã nguồn HTML slide và biên dịch sang file PDF đúng 10 trang |

---

*Ghi chú về bảo mật và riêng tư: Dữ liệu người tham gia phỏng vấn đã được ẩn danh hoàn toàn. Bản prototype chạy dữ liệu giả lập cục bộ trên trình duyệt, không thu thập hay lưu trữ thông tin y tế thực của người dùng.*

