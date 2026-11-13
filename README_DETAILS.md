# README_DETAILS — Phạm vi và kiểm tra bàn giao

## 1. Phân công

| Phần | Người phụ trách | File |
|---|---|---|
| Phân tích lát cắt, rủi ro, tự chủ | Lê Sỹ Long Nhật | `spec.md` §1–§4 |
| Chat người dùng và logic an toàn | Lê Sỹ Long Nhật | `prototype/index.html` |
| Màn hình tư vấn viên, ca lạ | Đinh Quốc Việt | `prototype/index.html` |
| Tiêu chí, demo, ảnh và kiểm thử | Đinh Quốc Việt | `spec.md` §5–§7, `prototype/screenshots/` |

## 2. Quyết định an toàn đã chốt

AI không được tự gọi `nha_giao_dich`, xin OTP/mật khẩu/số thẻ đầy đủ, nói ngưỡng hoặc cách phát hiện gian lận, hay hứa hoàn tiền cho giao dịch đã hoàn tất. `giu_giao_dich` tự làm trong thời hạn 15 phút; xác minh và khóa ví cần người duyệt; chuyển tư vấn viên được tự động; nhả giao dịch bị cấm với AI.

## 3. Prototype hiện có

`prototype/index.html` gồm:

- Màn hình người dùng và màn hình tư vấn viên.
- Giao dịch dựng 6.200.000đ lúc 23:48 đang tạm giữ, còn 15 phút.
- Ca bị lừa, ca viện phí, người thân nhắn thay chủ ví, ca lạ hỏi ngưỡng và chuỗi giao dịch nhỏ liên tiếp.
- Xem bằng chứng, xác minh an toàn và chuyển tư vấn viên giữ nguyên ngữ cảnh.
- Tư vấn viên thấy tóm tắt hội thoại, nhãn ca, giao dịch và lý do chuyển.
- Khóa ví và nhả giao dịch đều có hộp xác nhận; AI không có quyền nhả.
- Mức tự chủ và chú thích HAX/PAIR hiển thị trên giao diện.

Ảnh minh họa:

- `prototype/screenshots/01-user-flow.svg`: bằng chứng, cảnh báo và quyền điều khiển của người dùng.
- `prototype/screenshots/02-advisor-panel.svg`: tóm tắt chuyển ca và quyền thao tác của tư vấn viên.

## 4. Checklist kiểm thử cuối

- [x] Không có luồng AI tự nhả giao dịch.
- [x] Không xin OTP, mật khẩu hoặc số thẻ đầy đủ.
- [x] Không tiết lộ ngưỡng chống gian lận.
- [x] Không bỏ qua chuỗi giao dịch nhỏ và không tiết lộ quy tắc phát hiện.
- [x] Không hứa hoàn tiền cho giao dịch đã hoàn tất.
- [x] Ca mơ hồ có câu hỏi/giới hạn phù hợp.
- [x] Có đường chuyển tư vấn viên.
- [x] Chuyển người giữ lại hội thoại và giao dịch.
- [x] Có ít nhất hai mức tự chủ trên màn hình.
- [x] Khóa ví và nhả giao dịch cần xác nhận.
- [x] Có ảnh prototype được đánh số.

## 5. Cách demo

1. Chọn “Ca bị lừa”, bấm “Chuyển tư vấn viên”, chuyển sang màn hình tư vấn viên và thử thao tác giữ/xác minh/khóa/nhả.
2. Chọn “Ca viện phí”, kiểm tra xác minh nhanh và chuyển ưu tiên; AI không tự nhả.
3. Chọn “Người thân nhắn” để kiểm tra không xác nhận danh tính thay chủ ví.
4. Chọn “Ca lạ” để kiểm tra từ chối tiết lộ ngưỡng.
5. Chọn “Giao dịch nhỏ liên tiếp” để kiểm tra cảnh báo chuỗi giao dịch, giữ giao dịch đang chờ, không hứa hoàn tiền và chuyển tư vấn viên.
