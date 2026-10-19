# Ghi chép trải nghiệm thực tế trên ứng dụng MyVinmec

- **Người dùng thử:** Tác giả (người dùng trực tiếp trải nghiệm và ghi nhận điểm đau trên app MyVinmec)
- **Thiết bị:** Xiaomi 14 (`houji`, màn hình 1200 × 2670, Android 14 / HyperOS)
- **Ứng dụng kiểm thử:** `com.vinmec.onevinmec` (MyVinmec bản chính thức)
- **Thời điểm dùng thử:** 20:30 – 21:35 ngày 18/10/2026 (~65 phút)
- **Mục tiêu dùng thử:** Trải nghiệm thực tế toàn bộ luồng tìm chuyên khoa, diễn đạt triệu chứng và lựa chọn bác sĩ khi đặt lịch khám ngoại trú trên ứng dụng MyVinmec; tìm ra các rào cản thao tác, điểm đứt gãy và ngõ cụt trải nghiệm đối với người bệnh.
- **Tài khoản:** Tài khoản đã kích hoạt trên máy cá nhân (không lưu hay chia sẻ dữ liệu nhạy cảm).

---

## 1. Hành trình các màn hình đã trải nghiệm thực tế

1. **Khởi động & Trang chủ (`01`–`03`, `08`):**
   - Mở app gặp ngay Popup quảng cáo tiêm phòng cúm mùa (nút đóng `X` ở giữa-dưới màn hình).
   - Trang chủ hiển thị: Banner Vinmec Membership (560.000đ/năm), Grid 12 dịch vụ (Lịch hẹn, Liên hệ 24/7, Dịch vụ y tế mới, Sổ tiêm, Đơn thuốc, Danh mục giá, Quyền lợi CBNV, Hỏi đáp bác sĩ...).
   - Mục "Dịch vụ mới" có 2 card: "Cổng dịch vụ khách hàng" và "Đặt lịch nhanh – Xác nhận lịch tự động".
   - Mascot AI nổi (icon robot tim) ghim cố định ở góc dưới bên phải trang chủ.
   - Bottom navigation gồm 5 mục: Trang chủ | Hồ sơ | Đặt lịch (nút tròn nổi) | Thông báo (badge đỏ) | Tài khoản.

2. **Mục "Dịch vụ mới - Đặt lịch nhanh" (`05`–`06`) & "Lịch hẹn" (`09`–`10`):**
   - Bấm vào "Đặt lịch nhanh": thực chất điều hướng trực tiếp vào form Đặt hẹn khám (`MainAct`).
   - Màn hình "Lịch hẹn" từ trang chủ: hiện trống khi chưa có lịch sắp tới; có hướng dẫn kích hoạt liên kết hồ sơ bằng SMS.

3. **Luồng "Đặt lịch hẹn" chi tiết (`11`–`45`):**
   - Chọn hình thức: Khám chuyên khoa / Khám theo triệu chứng.
   - Chọn cơ sở: Bệnh viện ĐKQT Vinmec Times City (Hà Nội).
   - Chọn chuyên khoa & bác sĩ:
     - Chọn GS. Trần Trung Dũng: App báo "Hiện tại không có lịch trống ngày 19/10/2026" (dừng lại, không gợi ý ngày còn trống tiếp theo hay bác sĩ cùng chuyên môn).
     - Đổi sang BS. Trần Văn Công: App mở danh sách khung giờ khám ngày 19/10.
   - Chọn khung giờ: App hiển thị dạng lưới các slot cố định 30 phút (`07:30`, `08:00`, `09:00`, `09:30`, `10:00`, `10:30`...).
   - Dừng lại ở bước chọn slot, không bấm "Xác nhận đặt hẹn" để tránh tạo rác hệ thống.

---

## 2. Quan sát & Bằng chứng thực tế

- **Rào cản chọn chuyên khoa & diễn đạt triệu chứng:**
  - App bắt người dùng tự chọn chuyên khoa từ danh mục y khoa thuần túy hoặc chọn từ danh mục triệu chứng thô sơ.
  - Không có giao diện trực quan (như bản đồ cơ thể Body Map hay bộ từ điển cảm giác đời thường) để người bệnh mô tả triệu chứng theo cảm nhận thực tế.
- **Mù mờ về năng lực chuyên môn sâu của bác sĩ:**
  - Danh sách bác sĩ chỉ hiển thị ảnh đại diện, họ tên và học hàm/học vị chung chung (GS, PGS, TS, ThS, BSCK).
  - Không có thông tin mô tả lĩnh vực chuyên sâu hay thế mạnh điều trị thực tế (ví dụ: cùng khoa Cơ xương khớp nhưng ai chuyên thoái hóa cột sống cổ, ai chuyên khớp gối thể thao).
- **Phân tầng giá khám thiếu chỉ dẫn phù hợp:**
  - Giá khám phân tầng lớn (từ 500.000đ – 600.000đ cho Bác sĩ Đa khoa/CKI đến 1.500.000đ – 2.000.000đ cho Giáo sư/Chuyên gia).
  - Thiếu gợi ý định hướng xem với mức độ triệu chứng ban đầu, người bệnh có thực sự cần thiết phải đặt lịch Giáo sư hay không.
- **Ngõ cụt trải nghiệm khi chuyên gia kín lịch (Dead-end UX):**
  - Khi chọn GS. Trần Trung Dũng cho ngày 19/10, app hiển thị thông báo đỏ *"Hiện tại không có lịch trống ngày 19/10/2026"* và dừng luồng hoàn toàn.
  - Không có gợi ý bác sĩ cùng chuyên môn có lịch trống gần nhất, không có danh sách chờ (waitlist), đẩy người bệnh đang đau đớn vào thế bế tắc.
- **Thiếu chốt chặn an toàn cho các ca cấp cứu:**
  - Luồng đặt lịch không có bước sàng lọc cờ đỏ cấp cứu (nhồi máu cơ tim, đột quỵ, khó thở cấp) để kịp thời khuyến cáo người bệnh gọi 115 thay vì đặt lịch khám thường ngày hôm sau.

---

## 3. Vướng mắc & Điểm "đau" trải nghiệm cốt lõi

1. **Rào cản ngôn ngữ triệu chứng ("Không biết gọi tên nỗi đau"):**
   - Người bệnh không có chuyên môn y tế, chỉ cảm nhận được triệu chứng qua cảm giác sinh hoạt ("đau tức", "nhói", "râm ran"). Việc bắt người bệnh tự đoán chuyên khoa dẫn đến nguy cơ rất cao đặt nhầm khoa, gây tổn thất kép cả về thời gian lẫn chi phí khám lần hai.
2. **Tâm lý "Bảo hiểm bằng Giáo sư" & Bất an chi phí:**
   - Do thiếu thông tin chuyên môn minh bạch và hoang mang về bệnh tình, người bệnh thường có tâm lý cố đặt Giáo sư giá cao cho "chắc cú", dẫn đến lãng phí tiền bạc của người bệnh và gây quá tải không đáng có cho các bác sĩ đầu ngành với các ca bệnh nhẹ.
3. **Bế tắc vì ngõ cụt khi chuyên gia kín lịch:**
   - Thông báo hết lịch cộc lốc khiến người dùng thất vọng, tăng tỷ lệ bỏ rơi ứng dụng (drop-off) và buộc họ phải gọi điện lên tổng đài chờ đợi phân luồng thủ công.

---

## 4. Kết luận & Định hướng cho bài tập

- **Đánh giá hướng ý tưởng "Vinmec SmartMatch AI": HOÀN TOÀN ĐÚNG TRỌNG TÂM VÀ CÓ CƠ SỞ THỰC NGHIỆM VỮNG CHẮC.**
  - Kết quả trải nghiệm thực tế xác nhận các khoảng trống lớn trên app MyVinmec về: khơi mở triệu chứng đời thường, minh bạch hóa thế mạnh bác sĩ, tối ưu chi phí khám và cơ chế cân bằng tải tránh ngõ cụt.
  - Giải pháp đề xuất tích hợp **Trợ lý tiền khám ảo (Body Map + Từ điển cảm giác đời thường + Gợi ý 3 phân tầng bác sĩ minh bạch + Bộ lọc cờ đỏ cấp cứu 115)** giải quyết triệt để điểm đau lớn nhất trong khoảnh khắc "Tìm khoa & Chọn bác sĩ" khi đặt lịch trên MyVinmec.
