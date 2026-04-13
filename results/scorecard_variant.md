# Scorecard: variant_hybrid_rerank
Generated: 2026-04-13 15:26

## Summary

| Metric | Average Score | Bar |
|--------|:-------------:|-----|
| Faithfulness | 3.70/5 | ████░ |
| Relevance | 3.80/5 | ████░ |
| Context Recall | 5.00/5 | █████ |
| Completeness | 3.50/5 | ████░ |

## Per-Question Results

| ID | Category | Q (short) | Faithful | Relevant | Recall | Complete | Notes |
|----|----------|-----------|:--------:|:--------:|:------:|:--------:|-------|
| q01 | SLA | SLA xử lý ticket P1 là bao lâu? | 5 | 5 | 5 | 5 | The answer accurately reflects the SLA details for ticket P1 |
| q02 | Refund | Khách hàng có thể yêu cầu hoàn tiền | 5 | 5 | 5 | 5 | The answer accurately reflects the information provided in t |
| q03 | Access Control | Ai phải phê duyệt để cấp quyền Leve | 5 | 5 | 5 | 5 | The answer accurately reflects the requirement for Level 3 a |
| q04 | Refund | Sản phẩm kỹ thuật số có được hoàn t | 4 | 5 | 5 | 3 | The answer correctly states that digital products are non-re |
| q05 | IT Helpdesk | Tài khoản bị khóa sau bao nhiêu lần | 5 | 5 | 5 | 5 | The answer is completely grounded in the context, accurately |
| q06 | SLA | Escalation trong sự cố P1 diễn ra n | 5 | 5 | 5 | 5 | Every claim in the answer is directly supported by the retri |
| q07 | Access Control | Approval Matrix để cấp quyền hệ thố | 1 | 1 | 5 | 1 | The answer 'Không đủ dữ liệu' does not provide any claims th |
| q08 | HR Policy | Nhân viên được làm remote tối đa mấ | 5 | 5 | 5 | 4 | The answer accurately reflects the information provided in t |
| q09 | Insufficient Context | ERR-403-AUTH là lỗi gì và cách xử l | 1 | 1 | None | 1 | The answer 'Không đủ dữ liệu' does not provide any claims or |
| q10 | Refund | Nếu cần hoàn tiền khẩn cấp cho khác | 1 | 1 | 5 | 1 | The answer 'Không đủ dữ liệu' does not provide any claims th |

## Full Answers

### [q01] SLA xử lý ticket P1 là bao lâu?
**Answer:** SLA xử lý ticket P1 là 4 giờ cho việc khắc phục và 15 phút cho phản hồi ban đầu [1].

**Expected:** Ticket P1 có SLA phản hồi ban đầu 15 phút và thời gian xử lý (resolution) là 4 giờ.

---

### [q02] Khách hàng có thể yêu cầu hoàn tiền trong bao nhiêu ngày?
**Answer:** Khách hàng có thể yêu cầu hoàn tiền trong vòng 7 ngày làm việc kể từ thời điểm xác nhận đơn hàng [1].

**Expected:** Khách hàng có thể yêu cầu hoàn tiền trong vòng 7 ngày làm việc kể từ thời điểm xác nhận đơn hàng.

---

### [q03] Ai phải phê duyệt để cấp quyền Level 3?
**Answer:** Để cấp quyền Level 3, cần có sự phê duyệt của Line Manager, IT Admin và IT Security [2].

**Expected:** Level 3 (Elevated Access) cần phê duyệt từ Line Manager, IT Admin, và IT Security.

---

### [q04] Sản phẩm kỹ thuật số có được hoàn tiền không?
**Answer:** Sản phẩm kỹ thuật số không được hoàn tiền, trừ khi có lỗi do nhà sản xuất và đáp ứng các điều kiện khác [1].

**Expected:** Không. Theo chính sách hoàn tiền, sản phẩm thuộc danh mục hàng kỹ thuật số (license key, subscription) là ngoại lệ không được hoàn tiền.

---

### [q05] Tài khoản bị khóa sau bao nhiêu lần đăng nhập sai?
**Answer:** Tài khoản bị khóa sau 5 lần đăng nhập sai liên tiếp [1].

**Expected:** Tài khoản bị khóa sau 5 lần đăng nhập sai liên tiếp.

---

### [q06] Escalation trong sự cố P1 diễn ra như thế nào?
**Answer:** Escalation trong sự cố P1 diễn ra như sau: Nếu không có phản hồi trong 10 phút, ticket sẽ tự động escalate lên Senior Engineer. Ngoài ra, trong trường hợp khẩn cấp, IT Admin có thể cấp quyền tạm thời (tối đa 24 giờ) sau khi được Tech Lead phê duyệt bằng lời, và mọi quyền tạm thời phải được ghi log vào hệ thống Security Audit [1][2].

**Expected:** Ticket P1 tự động escalate lên Senior Engineer nếu không có phản hồi trong 10 phút sau khi tạo ticket.

---

### [q07] Approval Matrix để cấp quyền hệ thống là tài liệu nào?
**Answer:** Không đủ dữ liệu

**Expected:** Tài liệu 'Approval Matrix for System Access' hiện tại có tên mới là 'Access Control SOP' (access-control-sop.md).

---

### [q08] Nhân viên được làm remote tối đa mấy ngày mỗi tuần?
**Answer:** Nhân viên được làm remote tối đa 2 ngày mỗi tuần [1].

**Expected:** Nhân viên sau probation period có thể làm remote tối đa 2 ngày/tuần, với điều kiện được Team Lead phê duyệt.

---

### [q09] ERR-403-AUTH là lỗi gì và cách xử lý?
**Answer:** Không đủ dữ liệu

**Expected:** Không tìm thấy thông tin về ERR-403-AUTH trong tài liệu hiện có. Đây có thể là lỗi liên quan đến xác thực (authentication), hãy liên hệ IT Helpdesk.

---

### [q10] Nếu cần hoàn tiền khẩn cấp cho khách hàng VIP, quy trình có khác không?
**Answer:** Không đủ dữ liệu

**Expected:** Tài liệu chính sách hoàn tiền không đề cập đến quy trình đặc biệt cho khách hàng VIP. Theo chính sách hiện hành, tất cả yêu cầu hoàn tiền đều theo cùng quy trình tiêu chuẩn trong 3-5 ngày làm việc.

---

