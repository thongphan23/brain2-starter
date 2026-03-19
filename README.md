# 🧠 Brain2 Starter Kit — Bộ não thứ 2 của bạn

> **Brain2** = Hệ thống quản lý tri thức cá nhân, biến mọi kiến thức bạn học, đọc, trải nghiệm thành **"vũ khí" có thể tái sử dụng** — powered by **Antigravity AI + Obsidian**.

## ⚡ TL;DR — Dùng thế nào?

1. Clone repo → mở vault trong Obsidian
2. Cài **Obsidian MCP** cho Antigravity
3. Tất cả ghi chú, tìm kiếm, nghiên cứu → **nói chuyện với Antigravity**
4. Obsidian chỉ là vault viewer — bạn KHÔNG CẦN mở nó để ghi chú

---

## 🎯 Brain2 giải quyết gì?

| ❌ Không có Brain2 | ✅ Có Brain2 |
|---|---|
| Đọc sách xong → quên 90% sau 1 tuần | Mỗi insight → atomic note → nhớ mãi |
| Viết content → AI generic, không chiều sâu | Content inject stories + insights CÁ NHÂN |
| Kiến thức rải rác Notion/Google Docs/Notes | 1 vault, cross-linked, searchable |
| "Biết rồi mà không nhớ" | `/brain-gym` → ôn luyện, `/spaced-usage` → dùng lại |

---

## 🏗️ Kiến trúc: Antigravity + MCP + Obsidian

```
┌────────────────────────────────────────────┐
│            BẠN (Chat Interface)            │
│                                            │
│  "Ghi lại insight này..."                  │
│  "/deep-research về chủ đề X"              │
│  "Viết bài dùng stories trong vault"       │
└──────────────┬─────────────────────────────┘
               │
      ┌────────▼────────┐
      │  ANTIGRAVITY AI  │  ← AI Agent chính
      │  (Gemini Code    │     Hiểu Brain2 rules
      │   Assist)        │     Chạy workflows
      └────────┬─────────┘
               │ MCP Protocol
      ┌────────▼────────┐
      │  OBSIDIAN MCP    │  ← Đọc/Ghi/Tìm vault
      │  (MCP Server)    │     Không cần mở app
      └────────┬─────────┘
               │
      ┌────────▼────────┐
      │  OBSIDIAN VAULT  │  ← Tri thức gốc
      │  (brain2/vault/) │     .md files
      └─────────────────┘
```

> 💡 **Key insight:** Bạn KHÔNG tương tác trực tiếp với Obsidian. Bạn nói chuyện với Antigravity, và Antigravity ghi/đọc vault qua MCP.

---

## 🗂️ Cấu trúc Vault

```
vault/
├── 00-Inbox/              ← Ném ý thô vào đây
├── 01-Atomic/             ← Tri thức đã chuẩn hóa
│   ├── Stories/           ← 📖 Câu chuyện thật (sức mạnh nhất)
│   ├── Concepts/          ← 💡 Khái niệm
│   ├── Insights/          ← 🔍 Nhận thức sâu
│   ├── Frameworks/        ← 🧩 Mô hình tư duy
│   ├── Quotes/            ← 💬 Trích dẫn đáng nhớ
│   ├── Reflections/       ← 🪞 Suy ngẫm cá nhân
│   ├── People/            ← 👤 CRM cá nhân
│   └── Resources/         ← 📚 Sách, khóa học
├── 02-Sources/            ← Nguồn thô chưa xử lý
├── 03-MOCs/               ← 🗺️ Maps of Content
├── _Templates/            ← Templates chuẩn
└── scripts/
```

---

## 🛠️ 6 Workflows có sẵn

Gọi trực tiếp trong Antigravity:

| Lệnh | Mô tả | Khi nào dùng |
|---|---|---|
| `/reflect [suy ngẫm]` | Bắt insight → atomic note | Bất kỳ lúc nào có ý hay |
| `/deep-research [topic]` | Nghiên cứu sâu + vault scan + atomize | Muốn hiểu sâu 1 chủ đề |
| `/brain-gym` | Ôn luyện 15-30' với Active Recall | Mỗi ngày/tuần |
| `/story-bank [story]` | Nhập story thô → structured atom | Có câu chuyện muốn lưu |
| `/keystone-scan` | Gap analysis vault → concept mới | "Nên học gì tiếp?" |
| `/spaced-usage [bài]` | Dùng tri thức cũ → context mới | Viết content, phân tích |

---

## ✍️ Viết Content với Brain2 (AI Content Factory)

Brain2 tương thích với **AI Content Factory pipeline**. Cách dùng:

```
"Viết bài về [topic], dùng stories và insights trong vault"
```

Antigravity sẽ:
1. **Scan vault** → tìm Stories, Insights, Concepts, Quotes liên quan
2. **Inject theo DIKW layers** → nội dung có chiều sâu trí tuệ
3. **Output:** Bài viết kết hợp trải nghiệm thật + kiến thức chuyên sâu

> 📖 Chi tiết: xem [Content Factory Bridge](content-factory-bridge/README.md)

---

## 📊 Tự nâng cấp vault — Nhờ AI phân tích

Bạn có thể nhờ Antigravity quét và phân tích toàn bộ vault:

```
"Quét toàn bộ vault Brain2, phân tích:
 - Domain nào mạnh, domain nào yếu?
 - Notes nào 'cô đơn' (ít cross-links)?
 - Đề xuất 3-5 concepts nên học tiếp"
```

Hoặc dùng `/keystone-scan` cho gap analysis chuyên sâu.

---

## 🚀 Quick Start

```bash
# 1. Clone
git clone https://github.com/thongphan23/brain2-starter.git ~/brain2

# 2. Copy workflows + AI config
cp ~/brain2/workflows/*.md ~/.agent/workflows/
cp ~/brain2/ai-config/GEMINI.md ~/.gemini/GEMINI.md

# 3. Cài Obsidian MCP cho Antigravity (xem SETUP.md)

# 4. Test!
# Mở Antigravity, gõ: /reflect [insight đầu tiên của bạn]
```

📖 **Hướng dẫn chi tiết:** [SETUP.md](SETUP.md)
🚀 **7-day Onboarding:** [ONBOARDING.md](ONBOARDING.md)

---

## 📁 Repo Structure

```
brain2-starter/
├── README.md               ← Bạn đang đọc đây
├── SETUP.md                ← Hướng dẫn cài đặt chi tiết
├── ONBOARDING.md           ← 7-day onboarding program
├── vault/                  ← Obsidian vault (mở bằng Obsidian)
│   ├── 00-Inbox/
│   ├── 01-Atomic/          ← Sample notes có sẵn
│   ├── 02-Sources/
│   ├── 03-MOCs/            ← Sample MOC
│   ├── _Templates/         ← 8 templates chuẩn
│   └── scripts/
├── workflows/              ← 6 AI workflows
├── ai-config/              ← Cấu hình cho AI agents
│   ├── GEMINI.md           ← Antigravity config
│   └── system-prompt.md    ← Claude/ChatGPT config
└── content-factory-bridge/ ← Kết nối với Content Factory
```

---

## 🤝 Credits

Built by [Thông Phan](https://thongphan.com) — Creator of Brain2 & AI Content Factory.

## 📄 License

MIT — Tự do fork, customize, dùng thương mại.
