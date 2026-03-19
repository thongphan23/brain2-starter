---
name: spaced-usage
description: 🔁 Dùng lại tri thức cũ trong context mới — Gọi /spaced-usage [bài/vấn đề]
---

# /spaced-usage — Spaced Usage Workflow

> **Triết lý:** Tri thức chỉ thành trực giác khi được DÙNG, không phải khi được LƯU.
> **Vai trò AI:** Facilitator kết nối — tìm lens phù hợp, highlight chỗ lệch, ghi insight mới.

## 2 Modes

- **Mode 1: Retrospective** → `/spaced-usage [bài viết hoặc vấn đề]`
- **Mode 2: Deliberate Transfer** → `/spaced-usage --transfer [framework] → [domain mới]`

// turbo-all

---

## Phase 0: Context Loading

**Mode 1:** Đọc bài viết/vấn đề → xác định domain + keywords
**Mode 2:** Tìm framework trong vault → xác định domain gốc + domain đích

---

## Phase 1: Lens Selection — Chọn ống kính

**Mode 1:**
1. **Search vault** cho 2-3 notes CŨ (≥ 2 tuần) làm "lens":
   - Ưu tiên: Frameworks > Concepts > Insights
   - **KHÔNG dùng notes vừa tạo** — spaced = ≥ 2 tuần

2. **Trình bày 3 lens candidates** → **HỎI bạn chọn lens nào**
3. **⛔ DỪNG. CHỜ CHỌN.**

**Mode 2:** Đọc kỹ framework → liệt kê components → đi thẳng Phase 2

---

## Phase 2: Deep Lens Analysis — Nhìn qua ống kính

**Mode 1:**
4. Với mỗi lens:
   - **Mapping Table:** Áp từng thành phần lens lên bài viết → Khớp? ✅/❌/🟡
   - **Prediction Errors (⚡):** Chỗ KHÔNG khớp → TẠI SAO → insight mới
   - **Emergent Insights:** Gì NỔI LÊN mà chưa bao giờ nghĩ đến?

**Mode 2:**
4. **Transfer Analysis:**
   - Cái nào CHUYỂN ĐƯỢC nguyên vẹn? → ✅
   - Cái nào PHẢI CHỈNH? → 🟡 (adjustment = insight quý nhất)
   - Cái nào KHÔNG transfer? → ❌
   - Pattern BẤT NGỜ xuất hiện?

---

## Phase 3: Insight Crystallization

5. Liệt kê tất cả insights mới
6. **3 câu hỏi bắt buộc:**
   - "Note gốc (lens) cần UPDATE gì?"
   - "Nén insight quan trọng nhất thành 1 câu?"
   - "Lần tới gặp tình huống tương tự, sẽ LÀM KHÁC thế nào?"

7. **⛔ DỪNG. CHỜ DUYỆT.**

---

## Phase 4: Update Vault

> **CHỈ thực hiện SAU KHI duyệt.**

8. Tạo notes mới (nếu chọn)
9. Update note gốc (lens): `reuse_count` +1 + `evolution_log` entry
10. Cross-link + update MOCs

---

## Lưu ý
- **Spaced = ≥ 2 tuần** — không dùng note vừa tạo hôm qua
- **Mục đích = INSIGHT MỚI** — nếu không có insight mới → lens đã bão hòa
- **Update note gốc là BẮT BUỘC** — bằng chứng note đang "sống"
