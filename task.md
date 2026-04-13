## Phân task — Cả 2 cùng build, cùng eval

---

### 👤 Quốc Nam 
| Sprint | Việc cần làm |
|--------|-------------|
| Sprint 1 | Implement `get_embedding()` + `build_index()` |
| Sprint 2 | Implement `retrieve_dense()` + `call_llm()` |
| Sprint 3 | Implement variant đã chọn |
| Sprint 4 | Chấm **5 câu đầu** (Q1–Q5) trong `test_questions.json`, điền `scorecard_baseline.md` phần mình |
| Docs | Viết `docs/tuning-log.md` |

**Deliverables:** `index.py`, `rag_answer.py`, `docs/tuning-log.md`, `reports/individual/[tenA].md`

---

### 👤 Quang Hưng
| Sprint | Việc cần làm |
|--------|-------------|
| Sprint 1 | Implement `list_chunks()` + kiểm tra metadata (source, section, effective_date) |
| Sprint 2 | Implement `rag_answer()` wrapper + test 3+ câu mẫu |
| Sprint 3 | Chạy `compare_retrieval_strategies()`, ghi nhận kết quả |
| Sprint 4 | Chấm **5 câu sau** (Q6–Q10), điền `scorecard_baseline.md` phần mình, chạy `compare_ab()` |
| Docs | Viết `docs/architecture.md` |

**Deliverables:** `eval.py`, `results/scorecard_*.md`, `docs/architecture.md`, `reports/individual/[tenB].md`

---

### 🔗 Sync points

| Thời điểm | Việc sync |
|-----------|-----------|
| Cuối Sprint 1 | Ghép code A + B → chạy `python index.py` thành công |
| Cuối Sprint 2 | Ghép `rag_answer.py` → cả 2 cùng test 3 câu mẫu |
| Cuối Sprint 3 | Cả 2 xem kết quả `compare_retrieval_strategies()`, thống nhất chọn variant |
| Cuối Sprint 4 | Gộp scorecard → cả 2 cùng chạy `compare_ab()` và review kết quả |