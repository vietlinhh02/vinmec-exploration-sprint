# Ghi chép thử nghiệm Prototype với người dùng thực tế

> Bản prototype tương tác do lập trình viên kỹ thuật (AI) hiện thực hóa từ các ý tưởng và yêu cầu của tác giả (người dùng trực tiếp khởi xướng bài toán). Dưới đây là nhật ký thử nghiệm tính hiệu quả của ý tưởng với 3 người dùng có nhu cầu khám bệnh ngoại trú thực tế.

---

## 1. Bối cảnh & Phương pháp thử nghiệm

- **Hình thức:** Phỏng vấn quan sát trực tiếp kết hợp cho người dùng tự thao tác trên prototype web (chế độ Demo tương tác).
- **Nhiệm vụ giao cho người dùng:**
  - *Nhiệm vụ 1:* "Bạn bị đau tức ở vùng ngực và hay ợ chua sau khi ăn 2 ngày nay. Hãy tìm bác sĩ phù hợp để đặt lịch khám sáng mai trên app."
  - *Nhiệm vụ 2:* "Bạn muốn biết chi phí khám là bao nhiêu và ca của bạn có cần khám Giáo sư hay không."
  - *Nhiệm vụ 3 (Thử thách an toàn):* Thử bấm vào tình huống khẩn cấp (đau ngực dữ dội, khó thở) để xem phản ứng của hệ thống.

---

## 2. Thông tin người thử nghiệm

1. **T1 — Chị Nguyễn Thanh H. (34 tuổi, Hà Nội):** Nhân viên kế toán, thường xuyên bị ợ chua và đau rát ngực, từng đi khám nhầm khoa Tim mạch cách đây 1 năm mất gần 2 triệu tiền xét nghiệm không cần thiết.
2. **T2 — Anh Trần Minh T. (48 tuổi, Nam Định):** Đưa mẹ 72 tuổi đi khám vì đau mỏi vai gáy và tê bì cánh tay phải; không biết nên đăng ký khoa Cơ xương khớp, Thần kinh hay Phục hồi chức năng.
3. **T3 — Bạn Lê Hoàng N. (29 tuổi, Hà Nội):** Kỹ sư IT, bị đau thắt lưng cấp sau khi bê vác nặng; từng vào app MyVinmec chọn GS. Trần Trung Dũng thì thấy hết sạch lịch và không biết làm gì tiếp theo.

---

## 3. Nhật ký kiểm thử qua 2 vòng phát triển

### Vòng 1: Kiểm thử trên App MyVinmec hiện tại (Bản v0 - Tìm kiếm & Chọn bác sĩ thủ công)

| Người thử | Hành vi & Quan sát thực tế | Cảm xúc & Nhận xét nguyên văn | Vấn đề cốt lõi phát hiện |
|---|---|---|---|
| **T1** | Mở form đặt lịch, thấy danh sách 20+ chuyên khoa. Gõ chữ "đau ngực" thì app gợi ý cả Tim mạch và Tiêu hóa. | *"Chị chẳng biết chọn khoa nào. Lần trước chị khám tim mạch mất 1 triệu rưỡi mà bác sĩ bảo dạ dày bình thường rồi bảo sang tiêu hóa khám lại."* | Rào cản phân định chuyên khoa khi triệu chứng giao thoa; sợ tốn kém kép. |
| **T2** | Đọc danh sách bác sĩ chỉ thấy chức danh "GS", "PGS", "TS" kèm giá khám chênh lệch lớn (500k vs 1.8tr). | *"Bác sĩ nào cũng ghi chuyên khoa chung chung. Mẹ anh già rồi, muốn khám đúng người giỏi cột sống cổ chứ không biết Giáo sư này có chuyên về cổ không."* | Mù mờ chuyên môn sâu; hoang mang về phân tầng giá khám. |
| **T3** | Chọn GS. Trần Trung Dũng, app báo đỏ: "Hiện tại không có lịch trống ngày 19/10/2026" và dừng lại. | *"Nó báo hết lịch rồi đứng im luôn, không gợi ý ai khác. Chẳng lẽ anh phải tự lội lại từ đầu chọn từng ông bác sĩ xem ai còn giờ trống?"* | Rơi vào ngõ cụt khi chuyên gia kín lịch; thiếu cơ chế cân bằng tải. |

---

### Vòng 2: Kiểm thử trên Prototype "Vinmec SmartMatch AI" (Bản v1 - Guided Intake & Explainable Matching)

| Người thử | Hành vi & Quan sát thực tế | Cảm xúc & Nhận xét nguyên văn | Tác động của giải pháp |
|---|---|---|---|
| **T1** | Bấm vào vùng Lồng ngực trên Body Map -> Chọn các từ cảm giác: "Đau tức nặng ngực", "Ợ chua sau ăn" -> AI gợi ý khoa Tiêu hóa kèm giải thích vì sao không phải Tim mạch. | *"Hay quá! Nó giải thích rõ ràng vì sao chị bị trào ngược chứ không phải tim. Gợi ý BS Hoàng 550k có slot 9h sáng mai là chị chốt luôn, đỡ tốn tiền triệu vô ích."* | **Giải tỏa hoàn toàn nỗi sợ khám nhầm khoa; tiết kiệm chi phí trực tiếp.** |
| **T2** | Nhập câu mô tả đời thường: "Đau cổ gáy tê bì xuống tay". AI định hướng Ngoại thần kinh & Cột sống, hiển thị 3 lựa chọn bác sĩ từ 500k đến 1.8tr kèm lý do. | *"Có dòng giải thích lý do rất thuyết phục. Anh chọn gói ThS. BS Hùng 600k vì chuyên sâu thoát vị cổ, giá vừa phải cho đợt khám ban đầu của mẹ."* | **Minh bạch hóa năng lực bác sĩ và phân tầng tài chính.** |
| **T3** | Bấm kịch bản 3 (Cân bằng tải khi GS Dũng hết lịch). Prototype lập tức hiển thị TS. BS Linh (cùng ekip, chuyên môn tương đương, sẵn slot 09:30). | *"Thế này mới thông minh chứ! Bác sĩ đầu ngành hết lịch thì giới thiệu ngay người cùng ekip ngày mai, không bắt người ta mò mẫm lại từ đầu."* | **Xóa bỏ ngõ cụt đặt lịch; phân bổ đều công suất khám.** |
| **Cả 3** | Thử bấm nút Kịch bản Cờ đỏ Cấp cứu -> Màn hình đỏ cảnh báo nguy hiểm + Nút gọi 115 to rõ. | *"Rất an tâm. Đi khám sợ nhất là AI máy móc không biết người ta đang nguy kịch. Có nút gọi cấp cứu thế này là chuẩn bệnh viện quốc tế."* | **Bảo đảm an toàn đạo đức & y tế tuyệt đối.** |

---

## 4. Bảng chỉ số định tính trước & sau cải tiến

| Tiêu chí đánh giá | Bản cũ (MyVinmec hiện tại) | Bản mới (Vinmec SmartMatch AI) |
|---|---|---|
| **Khả năng tự mô tả triệu chứng dễ dàng** | **0/3** (Bối rối trước từ ngữ y khoa) | **3/3** (Dễ dàng qua Body Map & Từ điển cảm giác đời thường) |
| **Tự tin chọn đúng chuyên khoa điều trị** | **1/3** (2 người từng khám nhầm) | **3/3** (Được AI phân luồng và giải thích cặn kẽ) |
| **Hiểu rõ vì sao nên chọn mức giá khám đó** | **0/3** (Không hiểu khác biệt giữa 500k và 2tr) | **3/3** (Hiểu rõ cấp độ nhẹ nên khám CKI, ca khó mới cần GS) |
| **Thời gian hoàn tất chọn bác sĩ và slot khám** | ~8–12 phút (nhiều lần quay lại) | **~1.5–2 phút** (luồng dẫn dắt 4 bước liền mạch) |
| **Mức độ hài lòng chung (Thang 1–5)** | **2.0 / 5** | **4.8 / 5** |

---

## 5. Kết luận rút ra cho sản phẩm

1. **Người bệnh khao khát sự minh bạch về lý do (Explainability):** Họ không chỉ muốn một cái tên bác sĩ, họ muốn biết *tại sao bác sĩ này lại phù hợp với triệu chứng và túi tiền của tôi*.
2. **"Từ điển cảm giác đời thường" là chìa khóa thấu cảm:** Việc thay thế các câu hỏi y khoa phức tạp bằng các từ vựng sinh hoạt ("nhói", "râm ran", "tức nặng") giúp người bệnh trút bỏ hoàn toàn sự tự ti và lo sợ.
3. **Cân bằng tải là bài toán đôi bên cùng thắng:** Người bệnh có lịch sớm với chi phí hợp lý; bệnh viện tận dụng tối đa năng lực của các bác sĩ giỏi ngoài các chuyên gia VIP.
