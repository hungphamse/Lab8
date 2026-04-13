# Scorecard: baseline_dense
Generated: 2026-04-13 18:24

## Summary

| Metric | Average Score | Bar |
|--------|:-------------:|-----|
| Faithfulness | 4.80/5 | █████ |
| Relevance | 4.30/5 | ████░ |
| Context Recall | 5.00/5 | █████ |
| Completeness | 4.40/5 | ████░ |

## Per-Question Results

| ID | Category | Q (short) | Faithful | Relevant | Recall | Complete | Notes |
|----|----------|-----------|:--------:|:--------:|:------:|:--------:|-------|
| q01 | SLA | SLA xử lý ticket P1 là bao lâu? | 5 | 5 | 5 | 5 | The answer accurately reflects the SLA details for ticket P1 |
| q02 | Refund | Khách hàng có thể yêu cầu hoàn tiền | 5 | 5 | 5 | 5 | The answer accurately reflects the conditions for requesting |
| q03 | Access Control | Ai phải phê duyệt để cấp quyền Leve | 5 | 5 | 5 | 5 | The answer accurately reflects the requirement for Level 3 a |
| q04 | Refund | Sản phẩm kỹ thuật số có được hoàn t | 5 | 5 | 5 | 5 | The answer accurately reflects the information from the retr |
| q05 | IT Helpdesk | Tài khoản bị khóa sau bao nhiêu lần | 5 | 5 | 5 | 5 | The answer accurately reflects the information provided in t |
| q06 | SLA | Escalation trong sự cố P1 diễn ra n | 5 | 5 | 5 | 5 | Every claim in the answer is supported by the retrieved cont |
| q07 | Access Control | Approval Matrix để cấp quyền hệ thố | 4 | 3 | 5 | 1 | The answer accurately reflects the process for granting acce |
| q08 | HR Policy | Nhân viên được làm remote tối đa mấ | 5 | 5 | 5 | 5 | The answer accurately reflects the conditions for remote wor |
| q09 | Insufficient Context | ERR-403-AUTH là lỗi gì và cách xử l | 5 | 2 | None | 4 | The answer accurately states that there is no information ab |
| q10 | Refund | Nếu cần hoàn tiền khẩn cấp cho khác | 4 | 3 | 5 | 4 | The answer accurately summarizes the refund process steps bu |

## Full Answers

### [q01] SLA xử lý ticket P1 là bao lâu?
**Answer:** SLA xử lý ticket P1 là 15 phút cho phản hồi ban đầu và 4 giờ cho xử lý và khắc phục. Nếu không có phản hồi trong 10 phút, ticket sẽ tự động được escalate lên Senior Engineer [1].

**Expected:** Ticket P1 có SLA phản hồi ban đầu 15 phút và thời gian xử lý (resolution) là 4 giờ.

---

### [q02] Khách hàng có thể yêu cầu hoàn tiền trong bao nhiêu ngày?
**Answer:** Khách hàng có thể yêu cầu hoàn tiền trong vòng 7 ngày làm việc kể từ thời điểm xác nhận đơn hàng, với điều kiện sản phẩm bị lỗi do nhà sản xuất và chưa được sử dụng hoặc mở seal [1][2]. Nếu cần thêm thông tin, vui lòng liên hệ với bộ phận IT Helpdesk.

**Expected:** Khách hàng có thể yêu cầu hoàn tiền trong vòng 7 ngày làm việc kể từ thời điểm xác nhận đơn hàng.

---

### [q03] Ai phải phê duyệt để cấp quyền Level 3?
**Answer:** Để cấp quyền Level 3, cần có sự phê duyệt của Line Manager, IT Admin và IT Security [1].

**Expected:** Level 3 (Elevated Access) cần phê duyệt từ Line Manager, IT Admin, và IT Security.

---

### [q04] Sản phẩm kỹ thuật số có được hoàn tiền không?
**Answer:** Sản phẩm kỹ thuật số không được hoàn tiền, bao gồm các mặt hàng như license key và subscription, theo điều khoản ngoại lệ trong chính sách hoàn tiền [1]. Nếu bạn cần thêm thông tin, vui lòng liên hệ với bộ phận hỗ trợ IT Helpdesk.

**Expected:** Không. Theo chính sách hoàn tiền, sản phẩm thuộc danh mục hàng kỹ thuật số (license key, subscription) là ngoại lệ không được hoàn tiền.

---

### [q05] Tài khoản bị khóa sau bao nhiêu lần đăng nhập sai?
**Answer:** Tài khoản bị khóa sau 5 lần đăng nhập sai liên tiếp. Để mở khóa, bạn có thể liên hệ IT Helpdesk hoặc tự reset qua portal SSO [1].

**Expected:** Tài khoản bị khóa sau 5 lần đăng nhập sai liên tiếp.

---

### [q06] Escalation trong sự cố P1 diễn ra như thế nào?
**Answer:** Escalation trong sự cố P1 diễn ra như sau:

1. On-call engineer nhận alert hoặc ticket và xác nhận severity trong 5 phút.
2. Nếu không có phản hồi trong 10 phút, ticket sẽ tự động escalate lên Senior Engineer.
3. Lead Engineer phân công engineer xử lý trong 10 phút.
4. Engineer cập nhật tiến độ lên ticket mỗi 30 phút và nếu cần hỗ trợ thêm, có thể escalate ngay.

Ngoài ra, trong trường hợp cần cấp quyền tạm thời để fix incident, quy trình escalation khẩn cấp yêu cầu On-call IT Admin cấp quyền tạm thời (max 24 giờ) sau khi được Tech Lead phê duyệt bằng lời, và mọi quyền tạm thời phải được ghi log vào hệ thống Security Audit [1][2][3]. 

Nếu bạn cần thêm thông tin chi tiết, vui lòng liên hệ với IT Helpdesk.

**Expected:** Ticket P1 tự động escalate lên Senior Engineer nếu không có phản hồi trong 10 phút sau khi tạo ticket.

---

### [q07] Approval Matrix để cấp quyền hệ thống là tài liệu nào?
**Answer:** Tôi không tìm thấy thông tin cụ thể về "Approval Matrix" để cấp quyền hệ thống trong tài liệu. Tuy nhiên, tài liệu quy định quy trình cấp phép truy cập vào các hệ thống nội bộ của công ty và phân cấp quyền truy cập cho các cấp độ khác nhau [1][3]. 

Xin vui lòng liên hệ với bộ phận IT Helpdesk để được hỗ trợ thêm.

**Expected:** Tài liệu 'Approval Matrix for System Access' hiện tại có tên mới là 'Access Control SOP' (access-control-sop.md).

---

### [q08] Nhân viên được làm remote tối đa mấy ngày mỗi tuần?
**Answer:** Nhân viên được làm remote tối đa 2 ngày mỗi tuần sau khi hoàn thành probation period, và lịch remote phải được phê duyệt bởi Team Lead qua HR Portal [1].

**Expected:** Nhân viên sau probation period có thể làm remote tối đa 2 ngày/tuần, với điều kiện được Team Lead phê duyệt.

---

### [q09] ERR-403-AUTH là lỗi gì và cách xử lý?
**Answer:** Tôi không tìm thấy thông tin về lỗi ERR-403-AUTH trong tài liệu. Thông tin hiện có liên quan đến quy trình cấp quyền và quản lý tài khoản. Để được hỗ trợ về lỗi này, vui lòng liên hệ với IT Helpdesk. [1]

**Expected:** Không tìm thấy thông tin về ERR-403-AUTH trong tài liệu hiện có. Đây có thể là lỗi liên quan đến xác thực (authentication), hãy liên hệ IT Helpdesk.

---

### [q10] Nếu cần hoàn tiền khẩn cấp cho khách hàng VIP, quy trình có khác không?
**Answer:** Tôi không tìm thấy thông tin cụ thể về quy trình hoàn tiền khẩn cấp cho khách hàng VIP trong tài liệu. Dưới đây là thông tin liên quan mà tôi đã tìm thấy:

- Quy trình xử lý yêu cầu hoàn tiền bao gồm các bước từ việc khách hàng gửi yêu cầu đến khi Finance Team xử lý trong 3-5 ngày làm việc [2].

Xin vui lòng liên hệ với bộ phận IT Helpdesk để được hỗ trợ thêm.

**Expected:** Tài liệu chính sách hoàn tiền không đề cập đến quy trình đặc biệt cho khách hàng VIP. Theo chính sách hiện hành, tất cả yêu cầu hoàn tiền đều theo cùng quy trình tiêu chuẩn trong 3-5 ngày làm việc.

---

