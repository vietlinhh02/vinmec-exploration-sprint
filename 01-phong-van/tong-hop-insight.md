# Tổng hợp Insight từ 3 cuộc phỏng vấn sâu & Trải nghiệm thực tế MyVinmec

> Nghiên cứu định tính dựa trên: **Trải nghiệm thực tế ứng dụng MyVinmec** + **3 cuộc phỏng vấn sâu bán cấu trúc (P1, P2, P3)** về khoảnh khắc tìm khoa, diễn đạt triệu chứng và chọn bác sĩ.

---

## 1. Bảng ma trận Bằng chứng thực nghiệm &rarr; Insight cốt lõi

| # | Insight trải nghiệm cốt lõi | Bằng chứng thực nghiệm (Trích dẫn nguyên văn & Nguồn) |
|---|---|---|
| **1** | **Rào cản ngôn ngữ triệu chứng ("Không biết gọi tên nỗi đau"):** Người bệnh không biết thuật ngữ y khoa; họ chỉ cảm nhận được cảm giác đời thường ("nhói", "nặng tức", "râm ran"). Việc app bắt tự chọn chuyên khoa đẩy họ vào bế tắc. | - P1: *"Đọc Google một hồi ra toàn nhồi máu cơ tim làm hoảng loạn mất ngủ... Người bệnh chỉ biết đau ở đâu, làm sao biết đau ngực do dạ dày mà tự chọn khoa!"*<br>- P2: *"Bà cụ chỉ bảo cầm đôi đũa gắp thức ăn mà mấy ngón tay cứ tê dại như kiến bò... làm sao biết từ ngữ y khoa."*<br>- Trải nghiệm thực tế trên app: Bắt chọn khoa từ danh sách khô khan hoặc danh mục triệu chứng thô sơ. |
| **2** | **Khám nhầm chuyên khoa dẫn đến "Tổn thất kép" (Double Cost & Time):** Do triệu chứng giao thoa, người bệnh dễ chọn nhầm khoa, dẫn đến việc phải đóng thêm phí khám lần 2, làm xét nghiệm không cần thiết và chờ đợi lại từ đầu. | - P1: Khám nhầm Tim mạch do trào ngược dạ dày, mất 2.500.000đ tiền cận lâm sàng rồi phải đóng thêm 550.000đ sang khoa Tiêu hóa.<br>- P2: Dìu mẹ 71 tuổi chân yếu chống gậy lội ngược từ tầng nọ sang tầng kia đổi từ Cơ xương khớp sang Ngoại thần kinh. |
| **3** | **Mù mờ về năng lực chuyên môn sâu của bác sĩ:** Danh sách bác sĩ chỉ hiển thị học hàm chung chung (GS, PGS, TS, ThS), không nêu rõ thế mạnh điều trị thực chiến đối với từng ca bệnh cụ thể. | - P2: *"Danh sách bác sĩ ai cũng thấy ghi Giáo sư, Tiến sĩ... nhưng tuyệt nhiên không biết ai giỏi về cổ, ai giỏi về gối."*<br>- Trải nghiệm thực tế trên app: Màn hình chọn bác sĩ của MyVinmec chỉ có ảnh, tên và chuyên khoa lớn, không có thông tin chi tiết về lĩnh vực chuyên sâu. |
| **4** | **Bất an chi phí & Hiện tượng "Bảo hiểm bằng Giáo sư":** Giá khám phân tầng lớn (500k vs 2tr). Thiếu sự minh bạch khiến người bệnh cắn răng chi tiền triệu chọn chuyên gia VIP vì tâm lý lo sợ, gây lãng phí tài chính và quá tải bác sĩ tuyến trên. | - P1: Cắn răng book Giáo sư 1.500.000đ vì sợ bệnh hiểm nghèo.<br>- P3: *"Ca của em chỉ là căng cơ thể thao thông thường, đâu cần thiết phải dồn vào Giáo sư 2 triệu cho tốn kém và quá tải bệnh viện."* |
| **5** | **Ngõ cụt trải nghiệm khi chuyên gia kín lịch (Dead-end UX):** Khi bác sĩ đầu ngành hết slot, app dừng luồng hoàn toàn, không có cơ chế điều phối cân bằng tải hay gợi ý bác sĩ cùng chuyên môn có lịch trống gần nhất. | - P3: *"App báo 'không có lịch trống' rồi đứng im luôn như ngõ cụt đóng sập trước mặt người bệnh đang đau đớn."*<br>- Trải nghiệm thực tế trên app (18/10): Chọn GS. Trần Trung Dũng báo đỏ hết lịch ngày 19/10 và dừng luồng. |
| **6** | **Khao khát tính minh bạch của AI (Explainability) & An toàn y tế:** Người bệnh sẵn sàng đón nhận gợi ý của AI nếu AI giải thích thuyết phục *lý do kết nối* và tích hợp bộ lọc cờ đỏ cấp cứu khẩn cấp. | - P1: *"Muốn app giải thích: ca này chỉ cần khám bác sĩ tiêu chuẩn 500k là đủ, không cần khám Giáo sư."*<br>- Cả 3 người thử prototype đều đánh giá cao màn hình đỏ cảnh báo cấp cứu 115 khi phát hiện triệu chứng nguy hiểm. |

---

## 2. Hệ quả thiết kế cho giải pháp "Vinmec SmartMatch AI"

Từ 6 insight trên, giải pháp cần đáp ứng 4 trụ cột thiết kế:
1. **Interactive Body Map + Từ điển cảm giác đời thường (Giải quyết Insight 1 & 2):** Cho phép người bệnh chạm vào vùng cơ thể và chọn từ ngữ miêu tả cảm giác sinh hoạt ("nhói", "ợ chua", "tê dại"), từ đó AI bóc tách thực thể y tế để phân luồng đúng chuyên khoa ngay từ đầu.
2. **Minh bạch hóa & Tối ưu chi phí (Giải quyết Insight 3 & 4):** Phân tầng rõ ràng 3 gói khám: *Tiêu chuẩn (500k–600k)*, *Nâng cao (700k–1.000k)*, *Chuyên gia VIP (1.500k–2.000k)*; đưa ra lời khuyên tài chính tối ưu cho các ca nhẹ.
3. **Cơ chế Cân bằng tải & Chống ngõ cụt (Giải quyết Insight 5):** Khi bác sĩ VIP kín lịch, tự động hiển thị bác sĩ cùng chuyên môn sâu có slot trống sớm nhất để phân bổ đều nguồn lực phòng khám.
4. **Bộ lọc Cờ đỏ Cấp cứu & Ranh giới "Triage, Not Diagnosis" (Giải quyết Insight 6):** Tuyệt đối không chẩn đoán bệnh thay bác sĩ; dừng luồng đặt hẹn thường và hướng dẫn gọi cấp cứu 115 ngay khi phát hiện dấu hiệu đe dọa tính mạng.

---

## 3. Giới hạn nghiên cứu & Hướng mở rộng

- Mẫu nghiên cứu định tính gồm 3 cuộc phỏng vấn sâu đại diện cho 3 nhóm điển hình (người đi khám lần đầu có triệu chứng giao thoa; con cái đặt lịch hộ cha mẹ già; người trẻ vận động bị chấn thương cơ học).
- Dữ liệu đối chiếu từ phiên trải nghiệm trực tiếp ứng dụng MyVinmec bản chính thức trên điện thoại.
- Nếu có thêm thời gian triển khai, nhóm nghiên cứu đề xuất phỏng vấn thêm 2 bác sĩ lâm sàng và 1 điều dưỡng trưởng quầy tiếp nhận để đánh giá mức độ giảm tải phòng khám thực tế.
