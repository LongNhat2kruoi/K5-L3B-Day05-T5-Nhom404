# K5-L3B-Day05-T5-Nhom404

## Thông tin nhóm

- Lớp: L3B
- Track: T5 — Ví điện tử
- Tên nhóm: Nhom404
- Sản phẩm thiết kế: Trợ lý chat khi giao dịch ví bị tạm giữ

## Thành viên và phân công end-to-end

| Thành viên | MSSV | Email | GitHub | Phạm vi phụ trách | Trạng thái |
|---|---|---|---|---|---|
| Lê Sỹ Long Nhật | `2A202603881` | 26ai.nhatlsl@vinuni.edu.vn | [longnhat2kruoi](https://github.com/longnhat2kruoi) | Phân tích lát cắt, kịch bản rủi ro, mức tự chủ, logic an toàn và nền prototype | Đã hoàn thành nửa đầu |
| Đinh Quốc Việt | `2A202603885` | 26ai.vietdq3@vinuni.edu.vn | [KemmVSAI](https://github.com/KemmVSAI) | Màn hình tư vấn viên, ca lạ, kiểm thử, ảnh prototype, hoàn thiện spec và demo | Cần triển khai tiếp |

## Công việc đã hoàn thành

Lê Sỹ Long Nhật đã hoàn thành phần nền độc lập:

- Xác định lát cắt T5 và phạm vi không làm.
- Viết 8 kịch bản rủi ro phủ đủ 4 lớp lỗi.
- Chọn 2 kịch bản có chi phí sai cao nhất.
- Gán mức tự chủ cho toàn bộ tool.
- Xây dựng prototype màn hình Chat với ví.
- Thêm luồng an toàn cho ca người dùng bị lừa và ca thiếu thông tin.
- Đảm bảo prototype không có thao tác AI tự nhả giao dịch.

Chi tiết bàn giao nằm trong [`README_DETAILS.md`](README_DETAILS.md). Prototype hiện tại ở [`prototype/index.html`](prototype/index.html).

## Việc cần hoàn thành tiếp

Đinh Quốc Việt chỉ nên sửa các phần được bàn giao trong `README_DETAILS.md`:

- Hoàn thiện màn hình tư vấn viên.
- Thêm luồng người dùng thật sự đang gấp.
- Thêm luồng người thân nhắn thay chủ ví.
- Thêm ca demo lạ và kiểm thử các nút.
- Cập nhật §5–§7 trong `spec.md`.
- Chụp ảnh prototype và kiểm tra checklist rubric.

Không thay đổi tên tool, nguyên tắc an toàn hoặc mức tự chủ đã chốt nếu chưa cập nhật lại §4.
