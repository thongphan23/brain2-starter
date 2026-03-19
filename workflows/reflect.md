---
description: 💭 Lưu suy ngẫm/reflection nhanh vào vault với friction tối thiểu
---

# /reflect — Quick Reflection Capture

## Mục đích
Bắt insight/suy ngẫm nhanh nhất có thể. Bạn chỉ cần "ném" ý thô, AI xử lý toàn bộ phần còn lại.

## Input
Gửi `/reflect [nội dung suy ngẫm]` — có thể ngắn 1 câu hoặc dài vài đoạn.

## Workflow

### Bước 1: Nhận & Phân tích
// turbo-all
- Đọc nội dung reflection
- Xác định: theme chính, concepts liên quan, có kết nối gì với notes đã có trong vault không
- Nếu nội dung quá mơ hồ → hỏi TỐI ĐA 1-2 câu ngắn để làm rõ. Nếu đủ rõ → KHÔNG hỏi, làm luôn

### Bước 2: Tìm cross-links trong vault
- Search vault với keywords từ reflection
- Tìm 3-5 notes liên quan nhất để cross-link

### Bước 3: Tạo note
- **Vị trí:** `[VAULT_PATH]/01-Atomic/Reflections/`
- **Tên file:** `reflection-[chủ-đề-chính-dạng-slug].md`
- **Format:** Chuẩn vault frontmatter:
  ```yaml
  ---
  title: "[Tiêu đề tiếng Việt ngắn gọn, súc tích]"
  created: [ngày hôm nay]
  updated: [ngày hôm nay]
  type: reflection
  status: atomic
  source: "Suy ngẫm cá nhân — [ngày]"
  confidence: high
  related:
    - "[[note-liên-quan-1]]"
    - "[[note-liên-quan-2]]"
  used_count: 0
  used_in: []
  tags: [tag1, tag2, tag3]
  maturity: seedling
  review_interval: 30
  next_review: [+30 ngày]
  reuse_count: 0
  evolution_log:
    - date: [ngày hôm nay]
      change: "Khởi tạo từ /reflect"
  ---
  ```
- **Nội dung:** Cấu trúc rõ ràng nhưng KHÔNG phình ra quá xa so với ý gốc. Giữ đúng tinh thần, giọng, góc nhìn của người dùng.

### Bước 4: Confirm
- Thông báo: tên note, vị trí, cross-links đã tạo
- Trình bày NỘI DUNG note trong chat

## Nguyên tắc quan trọng
1. **Tốc độ > Hoàn hảo** — Mục tiêu là BẮT insight trước khi nó trôi, hoàn thiện sau
2. **Giọng người dùng > Giọng AI** — Giữ nguyên cách diễn đạt, góc nhìn
3. **Không phình** — Nói 3 câu thì note KHÔNG NÊN dài 3 trang. Atomic = nhỏ gọn
4. **Cross-link là giá trị ẩn** — Kết nối với notes sẵn có tạo compound effect
