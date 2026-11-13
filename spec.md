# Bài nộp LAB5 — T5 Ví điện tử · Nhóm Nhom404

## Thành viên

| Họ và tên | Mã học viên | Email | GitHub | Việc đã làm |
|---|---|---|---|---|
| Lê Sỹ Long Nhật | `2A202603881` | 26ai.nhatlsl@vinuni.edu.vn | [longnhat2kruoi](https://github.com/longnhat2kruoi) | §1–§4 và nền prototype Chat với ví |
| Đinh Quốc Việt | `2A202603885` | 26ai.vietdq3@vinuni.edu.vn | [KemmVSAI](https://github.com/KemmVSAI) | §5–§7, màn hình tư vấn viên, kiểm thử và demo |

## §1. Lát cắt & phạm vi

Trong Chat với ví, người dùng lo lắng vì giao dịch bị giữ, bị giục chuyển tiền hoặc thấy tiền bị trừ lạ. AI trả lời, hỏi lại, hướng dẫn xác minh hoặc chuyển tư vấn viên. AI không tự nhả giao dịch.

Không làm: AI tự nhả giao dịch; xin OTP/mật khẩu/số thẻ đầy đủ; tiết lộ ngưỡng phát hiện gian lận; hứa hoàn tiền.

## §2. Kịch bản rủi ro

Xem bảng 8 kịch bản chi tiết trong `README_DETAILS.md`. Hai kịch bản đắt nhất: người bị lừa yêu cầu nhả giao dịch và người dùng thật sự đang gấp tại quầy viện phí.

## §3. Khi AI sai

- Không chắc về giao dịch: hỏi lại và hiển thị các giao dịch liên quan.
- Không có căn cứ: không kết luận bị lừa, không hứa hoàn tiền.
- Có dấu hiệu bị lừa: yêu cầu dừng chuyển tiền, giữ giao dịch, chuyển tư vấn viên.
- Người dùng sửa AI: cho phép chọn lại giao dịch hoặc chuyển người mà không bắt đầu lại từ đầu.

Nguyên tắc: G10 thu hẹp phạm vi; Explainability + Trust bằng dòng căn cứ; Errors + Graceful Failure bằng đường chuyển tư vấn viên.

## §4. Mức tự chủ

Xem bảng mức tự chủ và lý do cost-of-error trong `README_DETAILS.md`. `nha_giao_dich` bị cấm đối với AI; `giu_giao_dich` và `chuyen_tu_van_vien` được tự làm; xác minh và khóa ví cần người duyệt.

## §5. Prototype

Đang triển khai tại [`prototype/index.html`](prototype/index.html). Nửa đầu đã hoàn thành màn hình Chat với ví, trạng thái giao dịch bị giữ, cảnh báo lừa đảo, căn cứ, xác minh và chuyển tư vấn viên. Màn hình tư vấn viên và hai ca demo bổ sung sẽ hoàn thiện ở nửa sau.

## §6. Tốt là gì

1. AI không tự nhả giao dịch khi có dấu hiệu bị lừa.
2. Người dùng thấy rõ AI đang nói về giao dịch nào.
3. Chuyển tư vấn viên không làm mất ngữ cảnh.

## §7. Demo

Nửa sau cần demo: ca bị lừa đòi nhả giao dịch, ca người thật đang gấp và một ca lạ do người chấm đưa ra. Mỗi thành viên trình bày phần mình phụ trách.
