---
description: 🧠 Brain Gym — Ôn luyện tri thức hàng ngày 15-30'. Gọi /brain-gym
---

# /brain-gym — Daily Knowledge Review Workflow

> **Triết lý:** Tri thức chỉ thành trực giác khi được DÙNG, không phải khi được LƯU.
> **Vai trò AI:** Huấn luyện viên Socratic — gợi nhớ, thách thức, kết nối.
> **Thời lượng:** 15-30 phút / session

Khi nhận lệnh `/brain-gym`:

// turbo-all

---

## Phase 0: Scanner — Chọn notes cần review

1. **Scan vault** — tìm 2-3 notes cần review nhất:
   - Ưu tiên: notes QUÁ HẠN `next_review`
   - Tiếp: notes có `reuse_count: 0` (chưa dùng lại)
   - Cuối: notes có `maturity: seed` (còn non)

2. **Đọc TOÀN BỘ nội dung** mỗi note (dùng để so sánh Active Recall)

3. **Trình bày session overview:**

   ```
   ## 🧠 Brain Gym — [ngày hôm nay]

   Hôm nay review **3 notes**:

   | # | Note | Domain | Lý do ưu tiên |
   |---|---|---|---|
   | 1 | `[[note-name]]` | cognition | ⏰ Quá hạn review 5 ngày |
   | 2 | `[[note-name]]` | marketing | 🔇 Chưa dùng lại lần nào |
   | 3 | `[[note-name]]` | economics | 🌱 Còn non, cần nuôi dưỡng |

   Bắt đầu nhé! 💪
   ```

---

## Phase 1: Active Recall — Nhớ trước, xem sau 🧠

> **⛔ BẮT BUỘC DỪNG CHỜ TRẢ LỜI SAU MỖI NOTE.**

4. Với mỗi note, chỉ hiện **tên concept + domain + 1 câu gợi ý**. KHÔNG hiện nội dung.

5. **Hỏi Active Recall:**

   | Loại | Câu hỏi | Khi nào dùng |
   |---|---|---|
   | **Core Recall** | "Bạn nhớ gì về [concept]?" | Luôn dùng |
   | **Mechanism** | "Cơ chế hoạt động của [concept] là gì?" | Concepts có mechanism |
   | **Example** | "Cho 1 ví dụ thực tế về [concept]?" | Concepts cần grounding |
   | **Counter** | "Nếu [concept] SAI thì sao?" | Notes đã mature |

6. **⛔ DỪNG. CHỜ TRẢ LỜI.**

7. **Feedback Protocol:**

   | Mức | Ý nghĩa | Hành động |
   |---|---|---|
   | 🟢 Tốt (≥70%) | Nhớ rõ | Khen, bổ sung chi tiết nhỏ |
   | 🟡 Trung bình | Nhớ ý chính | Show note, highlight phần thiếu |
   | 🔴 Yếu | Mờ/sai | Show TOÀN BỘ note, giải thích lại |

   **KHÔNG phán xét — chỉ feedback trung lập.**

---

## Phase 2: Connection Challenge — Nối với thực tế ⚡

8. **Chọn 1 Challenge:**

   | Loại | Challenge | Khi nào |
   |---|---|---|
   | **Apply** | "Concept này áp dụng vào việc bạn đang làm?" | Mặc định |
   | **Transfer** | "Dùng concept này phân tích domain khác?" | Notes mature |
   | **Feynman** | "Giải thích cho người không biết, trong 3 câu?" | Notes phức tạp |
   | **Create** | "Viết 1 câu hook dùng concept này?" | Khi cần content |
   | **Debate** | "Phản biện concept này?" | Notes rất mature |

9. **⛔ DỪNG. CHỜ TRẢ LỜI.**

10. **Lặp lại Phase 1 + 2 cho mỗi note.**

---

## Phase 3: Wrap Up 📝

11. **Tổng kết session:** Bảng recall + challenges + insights mới

12. **Hỏi:**
    - "Muốn ghi insight nào thành note mới?"
    - "Muốn deep dive concept nào? → `/deep-research`"

---

## Phase 4: Update Metadata

> **CHỈ thực hiện SAU KHI duyệt.**

13. **Update frontmatter mỗi note:**
    - 🟢 Tốt: `review_interval × 2.0`
    - 🟡 Trung bình: giữ nguyên
    - 🔴 Yếu: `review_interval × 0.5`
    - Update: `next_review`, `review_interval`, `reuse_count`, `updated`
    - Thêm `evolution_log` entry

---

## Lưu ý
- **Active Recall TRƯỚC** — TUYỆT ĐỐI không show nội dung trước khi recall
- **Feedback trung lập** — "bạn thiếu phần này", KHÔNG "bạn sai rồi"
- **Connection Challenge là linh hồn** — không có challenge = đọc lại = vô nghĩa
- **15-30 phút** — quá 30' → gợi ý dừng
