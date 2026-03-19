# Brain2 — Cấu hình AI Agent (Antigravity / Gemini Code Assist)

> Copy file này vào `~/.gemini/GEMINI.md` để Antigravity hiểu cách hoạt động với Brain2.

## Brain2 (Bộ não thứ 2)

Brain2 = hệ thống quản lý tri thức cá nhân trong Obsidian vault, bao gồm:
1. **Obsidian vault** — tri thức gốc, atomic notes
2. **Obsidian MCP** — AI đọc/ghi vault qua MCP protocol

### Nguyên tắc Brain2-first (BẮT BUỘC)

Khi người dùng hỏi bất kỳ điều gì liên quan đến kiến thức, trải nghiệm, hoặc tri thức:

1. **Bước 1 — Search vault TRƯỚC**: dùng Obsidian MCP (`search-vault`, `search-by-tags`, `search-by-title`) để tìm notes liên quan
2. **Bước 2 — Đọc chi tiết**: dùng `read-note` để đọc full nội dung notes tìm được
3. **Bước 3 — Tổng hợp**: kết hợp kiến thức vault + kiến thức AI → trả lời

- Knowledge đã có trong vault → **dùng nó**. Chưa có → nghiên cứu + tạo mới
- **KHÔNG ĐƯỢC** bỏ qua vault search. Vault chứa tri thức cá nhân quý giá mà AI không thể biết.

### Proactive Reflection Capture

- Trong BẤT KỲ cuộc hội thoại nào, nếu người dùng nói gì mang tính **insight / suy ngẫm / bài học**, chủ động hỏi: *"Cái này hay — lưu vào Brain2 không?"*
- Đồng ý → chạy workflow `/reflect` ngay. "Khoan" → bỏ qua.

## Workflows có sẵn

| Lệnh | Mô tả |
|---|---|
| `/reflect [suy ngẫm]` | Bắt insight nhanh → atomic note |
| `/deep-research [chủ đề]` | Nghiên cứu sâu + atomize vào vault |
| `/brain-gym` | Ôn luyện tri thức hàng ngày |
| `/story-bank [story]` | Nhập câu chuyện → structured atom |
| `/keystone-scan` | Gap analysis → gợi ý concept mới |
| `/spaced-usage [bài/vấn đề]` | Dùng tri thức cũ trong context mới |

## Vault Structure

```
vault/
├── 00-Inbox/              ← Raw thoughts chưa xử lý
├── 01-Atomic/             ← Knowledge atoms đã chuẩn hóa
│   ├── Stories/           ← Câu chuyện thật (Wisdom layer)
│   ├── Concepts/          ← Khái niệm (Information layer)
│   ├── Insights/          ← Nhận thức sâu (Knowledge layer)
│   ├── Frameworks/        ← Mô hình tư duy (Knowledge layer)
│   ├── Quotes/            ← Trích dẫn (Data layer)
│   ├── Reflections/       ← Suy ngẫm cá nhân
│   ├── People/            ← CRM
│   ├── Resources/         ← Sách, khóa học
│   └── Research/          ← Nghiên cứu sâu
├── 02-Sources/            ← Raw sources
├── 03-MOCs/               ← Maps of Content
└── _Templates/            ← Templates chuẩn
```

## Naming Convention

`{topic}-{type}-{slug}.md`

- Topics: career, content, productivity, mindset, relationship, decision, learning, business, marketing, writing, life, philosophy, money, health, technology
- Types: concept, insight, framework, story, quote, reflection

## Note Creation Rules

1. Luôn tạo notes theo template trong `_Templates/`
2. Luôn cross-link với ≥ 2 notes hiện có
3. Frontmatter YAML đầy đủ theo template
4. Trình bày nội dung note TRONG CHAT — người dùng không cần mở Obsidian để đọc

## Viết Content từ Brain2 (AI Content Factory)

Khi người dùng muốn viết content:
1. **Scan vault** tìm Stories, Insights, Concepts liên quan
2. **Inject theo DIKW layers:**
   - WISDOM (Stories) → dùng trực tiếp, rewrite theo giọng người dùng
   - KNOWLEDGE (Insights, Frameworks) → backbone cho deep dive
   - INFORMATION (Concepts) → giải thích thuật ngữ
   - DATA (Quotes) → gia vị, evidence
3. **KHÔNG BỊA stories** — nếu vault không có → bỏ qua hoặc dùng famous stories
4. Content có vault knowledge = content có chiều sâu trí tuệ, không phải AI generic
