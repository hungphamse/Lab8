# Scorecard: variant_hybrid_rerank
Generated: 2026-04-13 18:26

## Summary

| Metric | Average Score | Bar |
|--------|:-------------:|-----|
| Faithfulness | 4.90/5 | █████ |
| Relevance | 4.00/5 | ████░ |
| Context Recall | 5.00/5 | █████ |
| Completeness | 4.20/5 | ████░ |

## Per-Question Results

| ID | Category | Q (short) | Faithful | Relevant | Recall | Complete | Notes |
|----|----------|-----------|:--------:|:--------:|:------:|:--------:|-------|
| q01 | SLA | SLA xử lý ticket P1 là bao lâu? | 5 | 5 | 5 | 5 | The answer accurately reflects the SLA details for ticket P1 |
| q02 | Refund | Khách hàng có thể yêu cầu hoàn tiền | 4 | 5 | 5 | 5 | The answer accurately states the 7-day timeframe for refund  |
| q03 | Access Control | Ai phải phê duyệt để cấp quyền Leve | 5 | 5 | 5 | 5 | The answer accurately reflects the requirement for Level 3 a |
| q04 | Refund | Sản phẩm kỹ thuật số có được hoàn t | 5 | 5 | 5 | 5 | The answer accurately reflects the conditions for non-refund |
| q05 | IT Helpdesk | Tài khoản bị khóa sau bao nhiêu lần | 5 | 5 | 5 | 5 | The answer accurately reflects the information provided in t |
| q06 | SLA | Escalation trong sự cố P1 diễn ra n | 5 | 5 | 5 | 4 | The answer accurately reflects the escalation process and re |
| q07 | Access Control | Approval Matrix để cấp quyền hệ thố | 5 | 2 | 5 | 1 | The answer accurately reflects the information provided in t |
| q08 | HR Policy | Nhân viên được làm remote tối đa mấ | 5 | 5 | 5 | 5 | Every claim in the answer is directly supported by the retri |
| q09 | Insufficient Context | ERR-403-AUTH là lỗi gì và cách xử l | 5 | 1 | None | 5 | The answer accurately reflects the absence of information re |
| q10 | Refund | Nếu cần hoàn tiền khẩn cấp cho khác | 5 | 2 | 5 | 2 | The answer accurately reflects the conditions for requesting |

## Full Answers

### [q01] SLA xử lý ticket P1 là bao lâu?
**Answer:** SLA xử lý ticket P1 bao gồm:
- Phản hồi ban đầu: 15 phút kể từ khi ticket được tạo.
- Xử lý và khắc phục: 4 giờ.
- Escalation: Tự động escalate lên Senior Engineer nếu không có phản hồi trong 10 phút [1]. 

Nếu cần thêm thông tin, vui lòng liên hệ với IT Helpdesk.

**Expected:** Ticket P1 có SLA phản hồi ban đầu 15 phút và thời gian xử lý (resolution) là 4 giờ.

---

### [q02] Khách hàng có thể yêu cầu hoàn tiền trong bao nhiêu ngày?
**Answer:** Khách hàng có thể yêu cầu hoàn tiền trong vòng 7 ngày làm việc kể từ thời điểm xác nhận đơn hàng [1]. Nếu cần thêm thông tin, vui lòng liên hệ với bộ phận IT Helpdesk.

**Expected:** Khách hàng có thể yêu cầu hoàn tiền trong vòng 7 ngày làm việc kể từ thời điểm xác nhận đơn hàng.

---

### [q03] Ai phải phê duyệt để cấp quyền Level 3?
**Answer:** Để cấp quyền Level 3, cần có sự phê duyệt của Line Manager, IT Admin và IT Security [2].

**Expected:** Level 3 (Elevated Access) cần phê duyệt từ Line Manager, IT Admin, và IT Security.

---

### [q04] Sản phẩm kỹ thuật số có được hoàn tiền không?
**Answer:** Sản phẩm kỹ thuật số không được hoàn tiền. Cụ thể, các sản phẩm thuộc danh mục hàng kỹ thuật số như license key và subscription không đủ điều kiện hoàn tiền theo chính sách. Ngoài ra, đơn hàng đã áp dụng mã giảm giá đặc biệt hoặc sản phẩm đã được kích hoạt cũng không được hoàn tiền [1]. 

Nếu bạn cần thêm thông tin, vui lòng liên hệ với bộ phận IT Helpdesk.

**Expected:** Không. Theo chính sách hoàn tiền, sản phẩm thuộc danh mục hàng kỹ thuật số (license key, subscription) là ngoại lệ không được hoàn tiền.

---

### [q05] Tài khoản bị khóa sau bao nhiêu lần đăng nhập sai?
**Answer:** Tài khoản bị khóa sau 5 lần đăng nhập sai liên tiếp. Để mở khóa, bạn có thể liên hệ IT Helpdesk hoặc tự reset qua portal SSO [1].

**Expected:** Tài khoản bị khóa sau 5 lần đăng nhập sai liên tiếp.

---

### [q06] Escalation trong sự cố P1 diễn ra như thế nào?
**Answer:** Escalation trong sự cố P1 diễn ra như sau:

1. Nếu không có phản hồi trong 10 phút, ticket P1 sẽ tự động được escalate lên Senior Engineer.
2. Phản hồi ban đầu phải được thực hiện trong 15 phút và xử lý phải hoàn thành trong 4 giờ [2].

Nếu bạn cần thêm thông tin chi tiết hoặc hỗ trợ, vui lòng liên hệ với IT Helpdesk.

**Expected:** Ticket P1 tự động escalate lên Senior Engineer nếu không có phản hồi trong 10 phút sau khi tạo ticket.

---

### [q07] Approval Matrix để cấp quyền hệ thống là tài liệu nào?
**Answer:** Tôi không thể tìm thấy thông tin về tài liệu Approval Matrix để cấp quyền hệ thống trong tài liệu đã cung cấp. Dưới đây là thông tin liên quan mà tôi đã tìm thấy:

- Tài liệu quy định quy trình cấp phép truy cập vào các hệ thống nội bộ của công ty [1].
- Quy trình yêu cầu cấp quyền bao gồm việc tạo Access Request ticket và phê duyệt từ Line Manager [3].

Xin vui lòng liên hệ với bộ phận IT Helpdesk để được hỗ trợ thêm.

**Expected:** Tài liệu 'Approval Matrix for System Access' hiện tại có tên mới là 'Access Control SOP' (access-control-sop.md).

---

### [q08] Nhân viên được làm remote tối đa mấy ngày mỗi tuần?
**Answer:** Nhân viên được làm remote tối đa 2 ngày mỗi tuần sau khi đã qua probation period. Lịch remote phải được phê duyệt bởi Team Lead qua HR Portal. Ngày onsite bắt buộc là Thứ 3 và Thứ 5 theo lịch team [1].

**Expected:** Nhân viên sau probation period có thể làm remote tối đa 2 ngày/tuần, với điều kiện được Team Lead phê duyệt.

---

### [q09] ERR-403-AUTH là lỗi gì và cách xử lý?
**Answer:** Tôi không tìm thấy thông tin về lỗi ERR-403-AUTH và cách xử lý trong tài liệu. Dưới đây là thông tin mà tôi đã tìm thấy:

- Không có thông tin liên quan đến lỗi ERR-403-AUTH.

Xin vui lòng yêu cầu hỗ trợ từ IT Helpdesk để có thêm thông tin.

**Expected:** Không tìm thấy thông tin về ERR-403-AUTH trong tài liệu hiện có. Đây có thể là lỗi liên quan đến xác thực (authentication), hãy liên hệ IT Helpdesk.

---

### [q10] Nếu cần hoàn tiền khẩn cấp cho khách hàng VIP, quy trình có khác không?
**Answer:** Tôi không thể tìm thấy thông tin về quy trình hoàn tiền khẩn cấp cho khách hàng VIP trong tài liệu. Dưới đây là thông tin liên quan mà tôi đã tìm thấy:

- Khách hàng được quyền yêu cầu hoàn tiền khi đáp ứng đủ các điều kiện như sản phẩm bị lỗi do nhà sản xuất, yêu cầu gửi trong vòng 7 ngày làm việc, và đơn hàng chưa được sử dụng hoặc chưa bị mở seal [1].

Xin vui lòng liên hệ với bộ phận IT Helpdesk để được hỗ trợ thêm.

**Expected:** Tài liệu chính sách hoàn tiền không đề cập đến quy trình đặc biệt cho khách hàng VIP. Theo chính sách hiện hành, tất cả yêu cầu hoàn tiền đều theo cùng quy trình tiêu chuẩn trong 3-5 ngày làm việc.

---

