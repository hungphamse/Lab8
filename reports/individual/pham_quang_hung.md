# Báo Cáo Cá Nhân — Lab Day 08: RAG Pipeline

**Họ và tên:** Phạm Quang Hưng  
**Vai trò trong nhóm:** Eval Owner, Documentation Owner  
**Ngày nộp:** 13/04/2026  
**Độ dài yêu cầu:** 500–800 từ

---

## 1. Tôi đã làm gì trong lab này? (100-150 từ)

> Tôi thực hiện hầu hết các sprint, chủ nhiều nhiều nhất là sprint 4. Nếu bạn Quốc Nam hoàn thành phần lớn các sprint đầu thì tôi thực hiện tinh chỉnh prompt theo ngôn ngữ IT Help desk, cải thiện điểm số A/B

_________________

---

## 2. Điều tôi hiểu rõ hơn sau lab này (100-150 từ)

> Tôi hiểu được rằng mỗi chiến lược RAG có ưu nhược điểm khác nhau. Để phản hồi của model AI đạt kết quả tốt nhất thì cần kết hợp giữa chunking, retrieving strategy, prompt engineering và chọn model. Và tôi còn biết được rằng có thể thực hiện test với mô hình AI, cụ thể là A/B Testing dùng LLM làm "giám khảo"

_________________

---

## 3. Điều tôi ngạc nhiên hoặc gặp khó khăn (100-150 từ)

> Các model AI rất thông minh nhưng cũng có nhiều hạn chế. Chẳng hạn, phần phản hồi của model dùng từ bối cảnh "context" thay vì dùng từ "tài liệu". Bên cạnh đó, rất khó để chỉ ra phương án để giảm hallucination của model AI. Việc kết hợp các phương án không đồng nghĩa là model sẽ không còn hallucination (ngay cả model "giám khảo" cũng không nhận ra hallucination). Và prompt ảnh hưởng rất lớn đến việc model có hallucination hay không, chỉ cần thay đổi hành văn prompt sẽ khiến AI có thể "chệch" hoàn toàn ra khỏi yêu cầu từ prompt

_________________

---

## 4. Phân tích một câu hỏi trong scorecard (150-200 từ)

> Chọn 1 câu hỏi trong test_questions.json mà nhóm bạn thấy thú vị.
> Phân tích:
> - Baseline trả lời đúng hay sai? Điểm như thế nào?
> - Lỗi nằm ở đâu: indexing / retrieval / generation?
> - Variant có cải thiện không? Tại sao có/không?

**Câu hỏi:** Approval Matrix để cấp quyền hệ thống là tài liệu nào?

**Phân tích:**
- Trong tài liệu đề cập rõ việc tài liệu Approval Matrix for System Access đã được đổi tên thành Access Control SOP (access-control-sop.md). Tuy nhiên model vẫn phản hồi là "không tìm thấy thông tin"
- Lí do ban đầu: Lỗi ở quá trình tiền xử lý tài liệu dẫn đến mất thông tin, do đó dùng variant khác không giải quyết vấn đề


_________________

---

## 5. Nếu có thêm thời gian, tôi sẽ làm gì? (50-100 từ)

> Cải tiến lại khâu tiền xử lý và chunking tài liệu để model có thể nhận diện được các thông tin quan trọng. Đồng thời bổ sung thêm các câu hỏi khác để mở rộng phạm vi đánh giá và tìm ra các lỗi ẩn của RAG pipeline

_________________

---
