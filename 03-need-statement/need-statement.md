# Need statement (theo chuẩn Stanford Biodesign)

## 1. Câu Need Statement cốt lõi

**Cách để giúp người bệnh ngoại trú có nhu cầu thăm khám nhưng chưa rõ bệnh lý chính xác, gặp khó khăn khi tự diễn đạt triệu chứng và thiếu thông tin minh bạch về chuyên môn sâu cũng như chi phí khám của từng bác sĩ, tìm được đúng bác sĩ phù hợp với tình trạng sức khỏe, khả năng tài chính và thời gian của mình, qua đó giảm nguy cơ khám sai chuyên khoa, tối ưu chi phí điều trị cho người bệnh và cân bằng tải lịch làm việc cho đội ngũ y bác sĩ.**

---

## 2. Phân rã thành phần theo cấu trúc Biodesign

| Thành phần | Nội dung chi tiết |
|---|---|
| Population (Nhóm người dùng mục tiêu) | Người bệnh ngoại trú và người thân đi khám hộ (con cái đặt cho cha mẹ già, cha mẹ đặt cho con nhỏ) có nhu cầu khám ban đầu tại bệnh viện nhưng không có kiến thức chuyên môn y khoa. |
| Problem (Vấn đề và nỗi đau cốt lõi) | 1. Rào cản diễn đạt: Người bệnh khó gọi tên căn bệnh bằng thuật ngữ y khoa, chỉ cảm nhận được cảm giác khó chịu đời thường ("nhói", "nặng tức", "râm ran"), dẫn đến bối rối khi đứng trước danh mục chuyên khoa.<br>2. Mù mờ thông tin chuyên môn và giá: Người bệnh không rõ bác sĩ nào có thế mạnh sâu về bệnh cảnh của mình; bảng giá khám chênh lệch lớn (500.000đ đến hơn 2.000.000đ) nhưng thiếu chỉ dẫn xem ca bệnh có cần thiết phải khám chuyên gia hay không.<br>3. Hệ quả: Dễ đặt nhầm khoa dẫn đến mất thêm tiền khám lần hai, hoặc dồn lịch vào các chuyên gia gây quá tải không đáng có cho các ca thông thường. |
| Outcome (Kết quả mong muốn) | Người bệnh được hỗ trợ mô tả triệu chứng một cách tự nhiên, trực quan; kết nối đúng bác sĩ có chuyên môn phù hợp trong khung giờ thuận tiện; chi phí khám minh bạch và tối ưu; bệnh viện phân bổ đồng đều công suất phòng khám. |

---

## 3. Bằng chứng thực tế dẫn tới Need Statement

| Bằng chứng thực nghiệm | Nguồn dữ liệu |
|---|---|
| **Test thực tế app MyVinmec (18/10/2026):** Luồng đặt lịch bắt người dùng tự chọn chuyên khoa hoặc chọn theo danh mục triệu chứng thô sơ; danh sách bác sĩ chỉ hiện học hàm chung chung; chọn GS. Trần Trung Dũng thì báo "hết lịch trống" và rơi vào ngõ cụt, không có gợi ý bác sĩ thay thế hay mức giá. | [`01-phong-van/myvinmec-trai-nghiem.md`](../01-phong-van/myvinmec-trai-nghiem.md) & ghi chép trải nghiệm thực tế |
| **3/3 người phỏng vấn thừa nhận "không biết mình bị bệnh gì chính xác":** Chỉ biết cảm giác khó chịu ở vùng cơ thể, sợ chọn nhầm khoa phải khám lại tốn tiền. | Phỏng vấn P1, P2, P3 (`01-phong-van/`) |
| **2/3 người từng khám nhầm chuyên khoa:** P1 đau tức ngực do trào ngược dạ dày nhưng khám khoa Tim mạch; P2 đưa mẹ đi khám đau mỏi vai gáy book khoa Cơ xương khớp nhưng nguồn gốc do thoái hóa đốt sống cổ chèn rễ thần kinh. | Phỏng vấn P1, P2 (`01-phong-van/`) |
| **3/3 người bức xúc về sự chênh lệch giá khám không rõ lý do:** Giá khám Giáo sư/Tiến sĩ cao gấp 2–3 lần Bác sĩ Đa khoa/CKI nhưng không rõ ca bệnh của mình có cần thiết phải trả mức giá đó hay không. | Phỏng vấn P1, P2, P3 (`01-phong-van/`) |
| **Thực trạng lâm sàng tại bệnh viện:** Các chuyên gia đầu ngành bị quá tải bởi những ca bệnh thông thường, trong khi các bác sĩ trẻ, giỏi chuyên môn sâu lại bị thiếu bệnh nhân. | Báo cáo vận hành lâm sàng & Best Practice quốc tế |

---

## 4. Non-goals (Những điều bài toán này TUYỆT ĐỐI KHÔNG LÀM)

- **Không chẩn đoán hay kê đơn điều trị bệnh (No Medical Diagnosis/Prescription):** Hệ thống chỉ định hướng chuyên môn (Triage & Matching) để đưa người bệnh đến đúng bác sĩ, không khẳng định kết luận bệnh lý thay bác sĩ.
- **Không thay thế việc cấp cứu khẩn cấp:** Nếu phát hiện các dấu hiệu cờ đỏ cấp cứu (đột quỵ, nhồi máu cơ tim, sốt cao co giật), hệ thống dừng luồng đặt hẹn thường và kích hoạt đường dây cấp cứu ngay lập tức.
- **Không ép buộc người bệnh chọn theo gợi ý:** Người bệnh luôn có quyền tự do lựa chọn bất kỳ bác sĩ hoặc khung giờ nào theo ý muốn cá nhân.
- **Không thương mại hóa thiên vị (No Commercial Bias):** Không ưu tiên đẩy bệnh nhân vào bác sĩ có giá khám cao nhất để tối đa hóa doanh thu bệnh viện.

---

## 5. Quá trình tinh chỉnh bài toán (Problem Framing Iteration)

1. **Bản nháp 1 (Phạm lỗi chứa giải pháp):** *"Cách để xây dựng tính năng AI hỏi đáp triệu chứng và gợi ý bác sĩ Vinmec phù hợp ngân sách."* → **Bị loại** vì có từ "AI", "tính năng", "gợi ý bác sĩ".
2. **Bản nháp 2 (Phạm lỗi quá rộng, thiếu đối tượng cụ thể):** *"Cách để người bệnh đi khám tại Vinmec không bị tốn tiền và khám nhanh hơn."* → **Bị loại** vì quá chung chung, không gắn vào khoảnh khắc chọn bác sĩ và rào cản diễn đạt nỗi đau.
3. **Bản hiện tại (Đạt chuẩn Biodesign):** Tập trung đúng vào khoảnh khắc **Tiền khám / Chọn bác sĩ**, định rõ Population (người chưa rõ bệnh lý, khó diễn đạt), Problem (rào cản ngôn ngữ triệu chứng, mù mờ chuyên môn & chi phí), Outcome (đúng bác sĩ, tối ưu chi phí, cân bằng tải).
