# K5-L3B-Day05-T5-Nhom404

## Thông tin nhóm

- Lớp: L3B
- Track: T5 — Ví điện tử
- Tên nhóm: Nhom404
- Sản phẩm: Trợ lý chat khi giao dịch ví bị tạm giữ
- Trạng thái: Hoàn thiện prototype và spec theo checklist LAB5

## Thành viên và phân công

| Thành viên | MSSV | Phạm vi phụ trách |
|---|---|---|
| Lê Sỹ Long Nhật | `2A202603881` | Lát cắt, kịch bản rủi ro, mức tự chủ, logic an toàn và nền prototype |
| Đinh Quốc Việt | `2A202603885` | Màn hình tư vấn viên, ca demo, ảnh prototype, hoàn thiện spec và kiểm thử |

## Nội dung đã hoàn thành

- `spec.md` có đủ §1–§7 theo template.
- Có 8 kịch bản phủ 4 lớp lỗi và 2 kịch bản rủi ro cao.
- Có mức tự chủ và cost-of-error cho toàn bộ 5 tool.
- Có prototype người dùng và tư vấn viên.
- Có ca bị lừa, ca viện phí, người thân nhắn thay, ca lạ hỏi ngưỡng và ca nhiều giao dịch nhỏ liên tiếp.
- Có xác nhận trước thao tác khóa ví/nhả giao dịch.
- AI không tự nhả giao dịch, không xin OTP/mật khẩu/số thẻ và không tiết lộ ngưỡng chống gian lận.
- Có ảnh minh họa được đánh số trong `prototype/screenshots/`.

## Mở prototype

Mở [prototype/index.html](prototype/index.html) bằng trình duyệt. Chọn các nút “Ca bị lừa”, “Ca viện phí”, “Người thân nhắn”, “Ca lạ” để kiểm tra các luồng. Chọn “Màn hình tư vấn viên” để kiểm tra chuyển ca và các thao tác có xác nhận.

Chi tiết phân tích và bàn giao: [README_DETAILS.md](README_DETAILS.md).
