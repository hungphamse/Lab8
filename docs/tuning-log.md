# Tuning Log — RAG Pipeline (Day 08 Lab)

> Template: Ghi lại mỗi thay đổi và kết quả quan sát được.
> A/B Rule: Chỉ đổi MỘT biến mỗi lần.

---

## Baseline (Sprint 2)

**Ngày:** 13/04/2026 
**Config:**
```
retrieval_mode = "dense"
chunk_size = 400 tokens
overlap = 80 tokens
top_k_search = 10
top_k_select = 3
use_rerank = False
llm_model = gpt-4o-mini
```

**Scorecard Baseline:**
| Metric | Average Score |
|--------|--------------|
| Faithfulness | 4.80 /5 |
| Answer Relevance | 4.30 /5 |
| Context Recall | 5.00 /5 |
| Completeness | 4.40 /5 |

**Câu hỏi yếu nhất (điểm thấp):**
> q09 (ERR-403-AUTH) - context recall = 1/5 vì dense bỏ lỡ alias.

**Giả thuyết nguyên nhân (Error Tree):**
- [ ] Indexing: Chunking cắt giữa điều khoản
- [ ] Indexing: Metadata thiếu effective_date
- [ ] Retrieval: Dense bỏ lỡ exact keyword / alias
- [ ] Retrieval: Top-k quá ít → thiếu evidence
- [ ] Generation: Prompt không đủ grounding
- [ ] Generation: Context quá dài → lost in the middle

---

## Variant 1 (Sprint 3)

**Ngày:** 13/04/2026 
**Biến thay đổi:** retrieval_mode, use_rerank
**Lý do chọn biến này:**
> Chọn hybrid vì q07 (alias query) và q09 (mã lỗi ERR-403) đều thất bại với dense.
> Corpus có cả ngôn ngữ tự nhiên (policy) lẫn tên riêng/mã lỗi (ticket code, SLA label)."

**Config thay đổi:**
```
retrieval_mode: "hybrid"
use_rerank: False
# Các tham số còn lại giữ nguyên như baseline
```

**Scorecard Variant 1:**
| Metric | Baseline | Variant 1 | Delta |
|--------|----------|-----------|-------|
| Faithfulness | 4.8/5 | 4.9/5 | +0.1 |
| Answer Relevance | 4.3/5 | 4.0/5 | -0.3 |
| Context Recall | 5/5 | 5/5 | +0.0 |
| Completeness | 4.4/5 | 4.2/5 | -0.2 |

**Nhận xét:**
> Sau khi chạy, dựa theo kết quả, variant cải thiện không đáng kể các metric, thậm chí có một số metric mà baseline nhỉnh hơn
> Lí do: Có thể do cách agent "giám khảo" chấm điểm ở những câu hỏi đấy

**Kết luận:**
> Chưa đủ bằng chứng để đánh giá chính xác là variant 1 hay baseline tốt hơn
> Thậm chí baseline nhỉnh hơn ở các câu q02, q06, q10

---

## Tóm tắt học được

> TODO (Sprint 4): Điền sau khi hoàn thành evaluation.

1. **Lỗi phổ biến nhất trong pipeline này là gì?**
   > 

2. **Biến nào có tác động lớn nhất tới chất lượng?**
   > Không đánh giá được. Tuy nhiên, khi thay đổi ground promp thì điểm số từ agent giám khảo thay đổi rõ rệt ở tất cả các metric và giữa các variant

3. **Nếu có thêm 1 giờ, nhóm sẽ thử gì tiếp theo?**
   > Xây dựng thêm các câu hỏi khác mà không thể tìm thấy trong tài liệu. Đồng thời thử nghiệm thêm các promt
