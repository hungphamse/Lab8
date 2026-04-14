# Báo Cáo Tổng Kết Nhóm — Lab Day 08: RAG Pipeline

**Nhóm:** Nam - Hưng  
**Thành viên:**
1. Nguyễn Quốc Nam — Tech Lead
2. Phạm Quang Hưng — Eval Owner, Documentation Owner

---

## 1. Mục tiêu bài lab

Xây dựng hệ thống IT Helpdesk tự động trả lời câu hỏi nội bộ dựa trên các tài liệu chính sách (SLA, SOP, Policy) bằng kỹ thuật RAG — đảm bảo AI trả lời đúng, có nguồn trích dẫn và không tự bịa thông tin.

---

## 2. Cách nhóm thực hiện

- **Indexing (Quốc Nam):** Chunk tài liệu theo section heading, embed bằng `text-embedding-3-small`, lưu vào ChromaDB với metadata đầy đủ.
- **Retrieval (Quốc Nam):** Kết hợp BM25 + Dense search qua Reciprocal Rank Fusion, rerank bằng cross-encoder `ms-marco-MiniLM-L-6-v2`.
- **Generation (Quang Hưng):** Tinh chỉnh prompt theo ngữ cảnh IT Helpdesk, hướng dẫn AI chỉ trả lời từ tài liệu, từ chối khi không có thông tin.
- **Eval (Quang Hưng):** Wrap `rag_answer()`, chạy `compare_retrieval_strategies()`, A/B testing dùng LLM làm giám khảo, sinh scorecard.

---

## 3. Kết quả đánh giá

| Metric | Baseline (Dense) | Variant (Hybrid + Rerank) |
| :--- | :---: | :---: |
| Faithfulness | 4.0/5 | 5.0/5 |
| Relevance | 4.0/5 | 4.5/5 |
| Completeness | 3.5/5 | 4.2/5 |

Hệ thống từ chối đúng các câu hỏi ngoài phạm vi tài liệu. Variant cải thiện rõ nhất ở Completeness nhờ rerank đưa chunk chứa điều kiện ngoại lệ lên cao hơn.

---

## 4. Phân tích câu hỏi tiêu biểu

**Q03 — "Ai phải phê duyệt để cấp quyền Level 3?"**  
Baseline retrieve đúng chunk nhưng bỏ sót điều kiện: cần thêm phê duyệt của CISO nếu thuộc hệ thống production → Completeness 3/5. Lỗi ở generation, không phải retrieval. Hybrid + Rerank đẩy chunk ngoại lệ lên top-2, Completeness tăng lên 4/5.

**Câu hỏi về Approval Matrix**  
Model trả lời "không tìm thấy" dù tài liệu có ghi tên cũ đã đổi thành Access Control SOP. Lỗi ở khâu chunking làm mất thông tin — đổi retrieval strategy không giải quyết được.

---

## 5. Điều nhóm học được

- **RRF (Quốc Nam):** Không thể cộng trực tiếp điểm BM25 và cosine similarity vì khác đơn vị. RRF dùng thứ hạng thay vì điểm thô (`1/(60 + rank)`) giúp kết quả nhất quán hơn, đặc biệt với keyword chính xác như "Level 3", "P1".
- **Prompt & Hallucination (Quang Hưng):** Chỉ thay đổi hành văn prompt đã có thể khiến AI chệch hoàn toàn khỏi yêu cầu. Ngay cả LLM giám khảo đôi khi không phát hiện được hallucination.

---

## 6. Nếu có thêm thời gian

- **Query Expansion:** Dùng LLM mở rộng query thành các alias trước khi retrieve (ví dụ: "ERR-403-AUTH" → "lỗi xác thực, authentication error, 403") để tăng recall cho Q04 hiện đang bị abstain.
- **Cải thiện chunking:** Xử lý tốt hơn các metadata về tên cũ/mới của tài liệu; bổ sung thêm câu hỏi test để phát hiện lỗi ẩn.

---

## 7. Kết quả Grading Questions

Cả 10 câu đều có câu trả lời, không lỗi khi chạy. Kết quả lưu tại `logs/grading_run.json`. Hệ thống xử lý tốt các câu hỏi phức tạp về thủ tục phê duyệt và SLA xử lý sự cố.

---

*Ngày hoàn thành: 13/04/2026*
