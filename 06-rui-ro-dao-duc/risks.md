# Rủi ro an toàn, đạo đức và phương án kiểm soát

> Ứng dụng công nghệ hỗ trợ tiền khám đòi hỏi các chốt chặn an toàn rõ ràng về tính mạng, bảo mật dữ liệu và chuẩn mực y khoa. Dưới đây là ma trận phân tích 6 rủi ro chính và quy trình can thiệp của nhân viên y tế.

---

## 1. Ma trận rủi ro và giải pháp kiểm soát

| # | Tình huống rủi ro | Phân loại | Mức độ | Cơ chế kiểm soát cụ thể |
|---|---|---|---|---|
| R1 | **Bỏ sót dấu hiệu nguy kịch (Under-triage):** Người bệnh có dấu hiệu nhồi máu cơ tim hoặc đột quỵ nhưng hệ thống lại xếp vào lịch hẹn thông thường ngày hôm sau. | An toàn sinh mạng | Cực cao | **Bộ lọc cờ đỏ cấp cứu bằng quy tắc cứng (Rule-based):** Không dựa vào khả năng suy diễn của mô hình ngôn ngữ lớn. Khi phát hiện các dấu hiệu đe dọa tính mạng (đau thắt ngực lan cánh tay, méo miệng, yếu liệt nửa người, khó thở cấp), hệ thống lập tức khóa luồng đặt hẹn, bật cảnh báo toàn màn hình và hiện nút gọi khẩn cấp tới Tổng đài Cấp cứu Vinmec 115. |
| R2 | **Suy đoán chẩn đoán vượt thẩm quyền:** Hệ thống tự ý kết luận tên bệnh ("Bạn bị viêm loét dạ dày" hay "Bạn bị thoái hóa đốt sống"), khiến người bệnh hoang mang hoặc tự mua thuốc. | Chuyên môn y tế | Cao | **Nguyên tắc "Triage, Not Diagnosis":** Giới hạn chặt chẽ trong cấu trúc prompt: hệ thống chỉ định hướng chuyên khoa phù hợp và gợi ý bác sĩ khám, tuyệt đối không khẳng định bệnh lý. Luôn có dòng lưu ý: *"Kết quả gợi ý mang tính định hướng tiền khám, kết luận bệnh do bác sĩ tại phòng khám xác định"*. |
| R3 | **Thiên vị thương mại:** Thuật toán bị định hướng ưu tiên giới thiệu các bác sĩ có học hàm cao và giá khám đắt nhất (1.500.000đ – 2.000.000đ) nhằm tăng doanh thu. | Đạo đức nghề nghiệp | Cao | **Minh bạch hóa 3 phương án lựa chọn:** Luôn hiển thị đồng thời phương án phù hợp nhất, phương án tiết kiệm chi phí (Bác sĩ Đa khoa/CKI 550.000đ) và phương án Chuyên gia đầu ngành. Hệ thống giải thích lý do khách quan: *"Với triệu chứng mới xuất hiện ở mức độ nhẹ, thăm khám Bác sĩ CKI giúp tiết kiệm chi phí ban đầu"*. |
| R4 | **Rò rỉ dữ liệu sức khỏe cá nhân:** Thông tin vị trí đau, mô tả cảm giác và danh tính người bệnh bị truy cập trái phép hoặc chia sẻ cho bên ngoài. | Pháp lý và bảo mật | Cực cao | **Tuân thủ Nghị định 13/2023/NĐ-CP:** Dữ liệu mô tả triệu chứng được tách rời danh tính cá nhân trước khi xử lý; mã hóa lưu trữ; phiên bản prototype chạy dữ liệu cục bộ; cam kết không dùng dữ liệu mô tả của người bệnh để huấn luyện các mô hình AI mở của bên thứ ba. |
| R5 | **Mất cân đối lịch khám giữa các bác sĩ:** Bệnh nhân chỉ dồn vào một vài bác sĩ nổi tiếng, trong khi các bác sĩ trẻ có năng lực chuyên môn tốt lại trống lịch. | Vận hành bệnh viện | Trung bình | **Điều phối cân bằng tải hai chiều:** Thuật toán tính trọng số dựa trên thế mạnh điều trị chuyên sâu và lịch trống thực tế. Khi bác sĩ đầu ngành kín chỗ, hệ thống đề xuất các bác sĩ cùng nhóm chuyên môn có lịch trống sớm nhất. |
| R6 | **Khó khăn thao tác với người cao tuổi:** Người lớn tuổi hoặc người ít dùng điện thoại thông minh không quen gõ phím mô tả triệu chứng. | Tiếp cận dịch vụ | Trung bình | **Hỗ trợ đa kênh:** Tích hợp tính năng nhập liệu bằng giọng nói, chế độ đặt lịch hộ cho người thân trong gia đình, đồng thời trang bị màn hình hỗ trợ cho điều dưỡng tại quầy tiếp đón trực tiếp ở sảnh bệnh viện. |

---

## 2. Quy trình can thiệp của nhân viên y tế

Hệ thống được thiết kế theo mô hình con người giám sát (Human-in-the-loop):

1. **Chuyển hướng cấp cứu tức thời:**
   - Khi phát hiện dấu hiệu cờ đỏ, hệ thống chuyển sang giao diện gọi 115 và gửi thông báo tới đội ngũ điều phối cấp cứu của bệnh viện gần nhất.
2. **Quyền điều chỉnh của điều dưỡng tiếp đón:**
   - Tại quầy tiếp đón, điều dưỡng trưởng có thể xem lại thông tin phân luồng ban đầu. Nếu nhận thấy tình trạng thực tế của bệnh nhân khác với những gì đã nhập trên ứng dụng, điều dưỡng có thể đổi chuyên khoa ngay tại chỗ mà không phát sinh thêm chi phí khám lần hai.
3. **Quyền chủ động của người bệnh:**
   - Người bệnh không bị ràng buộc vào các gợi ý từ hệ thống. Ứng dụng luôn duy trì tùy chọn xem toàn bộ danh sách bác sĩ thông thường để người bệnh tự quyết định theo nhu cầu cá nhân.

---

## 3. Nguyên tắc vận hành

- **Lấy người bệnh làm trung tâm:** Mục tiêu là giúp người bệnh đỡ bối rối khi tìm kiếm thông tin, tránh khám sai khoa và giảm gánh nặng chi phí, không phục vụ mục đích thương mại hóa dịch vụ khám chữa bệnh.
- **Minh bạch lý do đề xuất:** Mọi gợi ý bác sĩ đều có lý giải rõ ràng bằng ngôn ngữ dễ hiểu, dựa trên thế mạnh chuyên môn, mức giá công khai và thời gian trống.
- **Tôn trọng vai trò bác sĩ:** Công nghệ chỉ đóng vai trò phân luồng và sắp xếp lịch ban đầu. Quyết định chẩn đoán và phác đồ điều trị hoàn toàn thuộc về chuyên môn của bác sĩ.
