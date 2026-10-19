# Journey map — Khoảnh khắc "Tìm khoa & Chọn bác sĩ" khi đặt lịch khám

> Bản vẽ trực quan: [journey-map.html](journey-map.html) (mở bằng trình duyệt) — dùng để chụp vào slides.
> Phân tích hành trình người bệnh từ lúc xuất hiện triệu chứng, đối mặt với rào cản tự diễn đạt nỗi đau trên app MyVinmec, cho tới khi được khám đúng chuyên khoa.

---

## 1. Sáu giai đoạn trong hành trình người bệnh

| # | Giai đoạn | Người bệnh làm gì | Điểm chạm | Cảm xúc (1–5) |
|---|---|---|---|---|
| 1 | Khởi phát triệu chứng & Lo âu | Cơ thể khó chịu ("đau tức ngực", "mỏi vai gáy", "bụng râm ran"), tìm kiếm Google gây hoang mang | Cơ thể, Internet | 2.5 — lo âu |
| 2 | Mở app MyVinmec đặt lịch | Đăng nhập app, vào form Đặt hẹn khám, chuẩn bị chọn chuyên khoa & bác sĩ | App MyVinmec | 2.0 — bỡ ngỡ |
| 3 | **Bế tắc diễn đạt & Đắn đo chi phí (ĐÁY CẢM XÚC)** | Không biết gọi tên triệu chứng bằng từ y khoa; hoa mắt trước danh sách khoa; phân vân giá khám (500k vs 2 triệu); chọn GS đầu ngành thì kín lịch | Form Đặt hẹn MyVinmec | **1.0 — bế tắc, sợ tốn tiền & chọn sai** |
| 4 | Đặt liều hoặc gọi tổng đài | Bấm chọn đại theo linh tính hoặc phải thoát app gọi tổng đài chờ giải thích | App / Tổng đài Vinmec | 2.0 — thụ động, bất an |
| 5 | Đến viện & Đối mặt nguy cơ khám nhầm | Đến viện, gặp bác sĩ; rủi ro chọn nhầm chuyên khoa (phải chuyển viện/chuyển khoa, đóng tiền khám lần 2) | Quầy tiếp đón, Phòng khám | 1.8 — căng thẳng chi phí |
| 6 | Hoàn tất khám & Điều trị | Được chẩn đoán đúng, kê đơn thuốc hoặc can thiệp, ra về | Bác sĩ, Nhà thuốc | 4.0 — nhẹ nhõm nhưng mệt mỏi |

---

## 2. Các điểm đau cốt lõi (Pain Points)

| Mã | Điểm đau | Giai đoạn | Mức độ | Bằng chứng thực nghiệm |
|---|---|---|---|---|
| **D1** | **Rào cản diễn đạt nỗi đau:** Người bệnh không thể mô tả triệu chứng bằng thuật ngữ y khoa, chỉ có cảm giác đời thường ("nhói", "nặng tức", "râm ran") nhưng app chỉ có ô tìm kiếm khô khan. | GĐ 2–3 | **Cao** | 3/3 người phỏng vấn thừa nhận không biết mình bị bệnh gì chính xác, sợ diễn đạt sai. |
| **D2** | **Mù mờ thông tin chuyên môn sâu của bác sĩ:** Danh sách bác sĩ chỉ hiện học hàm/học vị chung chung (GS, PGS, TS), không nêu rõ bác sĩ có thế mạnh điều trị ca bệnh nào. | GĐ 3 | **Cao** | Test thực tế app MyVinmec (18/10): Danh sách bác sĩ không có mô tả lĩnh vực chuyên sâu. |
| **D3** | **Bất an về chi phí & Thiếu tối ưu tài chính:** Giá khám phân tầng lớn (từ 500k đến hơn 2.000k), người bệnh không biết ca nhẹ của mình có cần khám Giáo sư hay không, sợ phát sinh chi phí lớn. | GĐ 3 | **Cao nhất** | P1, P3 chia sẻ lo ngại về chi phí khám vượt khả năng chi trả nếu chọn nhầm chuyên gia. |
| **D4** | **Ngõ cụt khi bác sĩ VIP kín lịch:** Chọn Giáo sư đầu ngành thì app báo "không có lịch trống" và dừng lại, không gợi ý bác sĩ khác cùng chuyên môn. | GĐ 3–4 | **Cao** | Test thực tế app MyVinmec: Chọn GS. Trần Trung Dũng ngày 19/10 bị dừng luồng hoàn toàn. |
| **D5** | **Nguy cơ khám nhầm chuyên khoa (Tốn kém kép):** Bệnh nhân đau ngực do trào ngược dạ dày nhưng đặt khám Tim mạch -> Phải đóng tiền khám lần 2 sang khoa Tiêu hóa. | GĐ 5 | **Cao nhất** | P1 (từng khám nhầm Tim mạch do trào ngược), P2 (đưa mẹ khám nhầm Cơ xương khớp do thoái hóa đốt sống cổ). |

---

## 3. Cơ hội thiết kế: "Vinmec SmartMatch AI"

Đặt một **lớp trợ lý AI dẫn dắt và điều phối tiền khám thông minh** ngay tại **Giai đoạn 2 và 3**, giải quyết trọn vẹn điểm đứt gãy:

1. **Khơi gợi & Dẫn dắt mô tả nỗi đau (Guided Intake):** Bản đồ cơ thể tương tác (Body Map) + Từ điển cảm giác đời thường + Hội thoại giọng nói tự nhiên, giúp người bệnh dễ dàng bộc lộ triệu chứng mà không cần biết thuật ngữ y khoa.
2. **Minh bạch hóa & Tối ưu chi phí:** Đề xuất rõ ràng các cấp độ bác sĩ (Khám chuyên khoa 550k vs Khám Chuyên gia 1.200k) kèm tính năng tích hợp bảo hiểm y tế / bảo hiểm tư nhân.
3. **Cân bằng tải & Tránh ngõ cụt:** Kết nối đa chiều giữa triệu chứng bệnh nhân, thế mạnh sâu của bác sĩ và các slot giờ trống, giảm tải cho các chuyên gia VIP và không để bệnh nhân rơi vào màn hình "hết chỗ".
4. **Bộ lọc cờ đỏ cấp cứu (Red Flags Filter):** Phát hiện tức thời dấu hiệu nguy kịch (đột quỵ, nhồi máu cơ tim) để kích hoạt đường dây nóng cấp cứu 115 thay vì đặt lịch khám thường.
