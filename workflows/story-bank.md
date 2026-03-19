---
name: story-bank
description: 📖 Story Bank — Nhập raw story → chuẩn hóa thành atomic notes. Gọi /story-bank
---

# /story-bank — Story Collection & Knowledge Atomization

> Chuyển câu chuyện thô thành structured atoms → lưu vào đúng thư mục vault.
> 1 raw story có thể tạo NHIỀU atoms (story + concept + insight + quote).

// turbo-all

---

## ⛔ Safety Rules

1. **KHÔNG XÓA file** trong vault mà không hỏi
2. **KHÔNG SỬA file sẵn có** — chỉ TẠO MỚI
3. **LUÔN dùng template chuẩn** từ `_Templates/`
4. **Trước khi ghi file** → report → chờ confirm

---

## Naming Convention (BẮT BUỘC)

- Stories: `{topic}-story-{slug}.md`
- Concepts: `{topic}-concept-{slug}.md`
- Insights: `{topic}-insight-{slug}.md`
- Frameworks: `{topic}-framework-{slug}.md`
- Quotes: `{topic}-quote-{slug}.md`

**Topics hợp lệ**: career, content, productivity, mindset, relationship, decision, learning, business, marketing, writing, life, philosophy, money, health, technology

---

## Workflow 6 bước

### Bước 1: Nhận raw input
Người dùng gửi: text trực tiếp, file path, hoặc link.

### Bước 2: Phân tích & phân loại

| Loại | Dấu hiệu | Thư mục đích |
|------|-----------|--------------|
| **Story** | Có nhân vật, bối cảnh, bước ngoặt, kết quả | `01-Atomic/Stories/` |
| **Concept** | Định nghĩa, khái niệm | `01-Atomic/Concepts/` |
| **Insight** | Nhận thức sâu, bài học từ quan sát | `01-Atomic/Insights/` |
| **Framework** | Mô hình, quy trình có bước rõ ràng | `01-Atomic/Frameworks/` |
| **Quote** | Câu nói đáng nhớ | `01-Atomic/Quotes/` |

### Bước 3: Cấu trúc hóa theo template chuẩn
Dùng templates trong _Templates/ tương ứng.

### Bước 4: Report (TRƯỚC KHI GHI FILE)
```
📋 Phân tích xong! Sẽ tạo:
1. 📖 Story: `career-story-xxx.md` → 01-Atomic/Stories/
2. 💡 Insight: `career-insight-yyy.md` → 01-Atomic/Insights/
Confirm để ghi file nhé?
```

### Bước 5: Ghi file (SAU KHI CONFIRM)

### Bước 6: Xác nhận
```
✅ Đã tạo:
- 01-Atomic/Stories/career-story-xxx.md (1.2KB)
- 01-Atomic/Insights/career-insight-yyy.md (0.8KB)
```

---

## POKA-YOKE Checks

- ⛔ Story KHÔNG CÓ protagonist → REJECT
- ⛔ Story KHÔNG CÓ bước ngoặt → YÊU CẦU bổ sung
- ✅ Mỗi story PHẢI có ít nhất 3/5 sections
- ✅ Naming convention PHẢI khớp convention hiện tại
- ✅ Topic PHẢI nằm trong danh sách hợp lệ

---

## Tips
1. **Kể chi tiết cảm xúc** — càng raw càng tốt
2. **Nhắc số liệu** — "3 tháng", "tăng 40%"
3. **Nhắc bước ngoặt** — điều gì khiến bạn thay đổi?
4. **Không cần văn vẻ** — AI sẽ cấu trúc lại
