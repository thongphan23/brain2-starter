# Content Factory Bridge — Kết nối Brain2 với AI Content Factory

## Tổng quan

**AI Content Factory** là pipeline tạo content chất lượng cao bằng AI, sử dụng tri thức từ Brain2 vault.

Brain2 Starter Kit dùng **cùng folder structure** với Content Factory → plug and play.

## DIKW Model — 4 tầng tri thức trong content

```
WISDOM      ← Stories (trải nghiệm thật → trực giác)      weight: 10
KNOWLEDGE   ← Insights + Frameworks (hiểu WHY)            weight: 7
INFORMATION ← Concepts (hiểu WHAT + HOW)                   weight: 3
DATA        ← Quotes + Data Points (số liệu, trích dẫn)   weight: 1
```

**Content "trí tuệ" = Knowledge + Wisdom layer.** Đa số content chỉ dừng ở Data + Information.

## Cách dùng

Khi viết content, yêu cầu AI:

```
Viết bài về [topic].
Tìm trong vault: stories, insights, concepts liên quan.
Inject theo DIKW layers.
```

AI sẽ:
1. Scan vault tìm atoms liên quan
2. Ưu tiên Stories (weight 10) > Insights (7) > Concepts (3) > Quotes (1)
3. Inject vào bài viết tự nhiên
4. Bài viết có chiều sâu trí tuệ — không phải AI generic

## Folder Mapping

| Folder Brain2 | DIKW Layer | Cách dùng trong content |
|---|---|---|
| `01-Atomic/Stories/` | Wisdom | Dùng trực tiếp, rewrite theo giọng bạn |
| `01-Atomic/Insights/` | Knowledge | Backbone cho deep dive |
| `01-Atomic/Frameworks/` | Knowledge | Cấu trúc bài viết |
| `01-Atomic/Concepts/` | Information | Giải thích thuật ngữ |
| `01-Atomic/Quotes/` | Data | Gia vị, evidence |

## Poka-Yoke Rules (Chống lỗi)

- ⛔ Vault KHÔNG có atom liên quan → BỎ QUA. **KHÔNG BỊA.**
- ⛔ KHÔNG tự tạo stories cá nhân — chỉ dùng từ vault hoặc famous stories
- ✅ Framework PHẢI có credibility (ai tạo + credential)
- ✅ Ghi rõ source trong metadata
