# 🛠️ Setup Guide — Brain2 Starter Kit

## Yêu cầu

| Tool | Bắt buộc? | Mô tả |
|---|---|---|
| [Obsidian](https://obsidian.md) | ✅ | Vault viewer — nơi lưu trữ notes (miễn phí) |
| [Antigravity](https://antigravity.dev) | ✅ | AI Agent chính — giao tiếp, ghi chú, nghiên cứu qua đây |
| Git | ✅ | Clone repo |

> 💡 **Quan trọng:** Bạn sẽ tương tác với Brain2 **qua Antigravity** là chính, không cần mở Obsidian để ghi chú. Obsidian chỉ là vault viewer — nơi bạn xem lại notes khi cần. Mọi thao tác ghi, tìm, phân tích đều qua Antigravity.

---

## Bước 1: Clone repo

```bash
git clone https://github.com/thongphan23/brain2-starter.git ~/brain2
```

Hoặc download ZIP từ GitHub → giải nén vào `~/brain2`.

## Bước 2: Mở Obsidian vault

1. Mở Obsidian
2. Nhấn **"Open folder as vault"**
3. Chọn folder: `~/brain2/vault`

## Bước 3: Cài MCP Servers cho Antigravity

MCP (Model Context Protocol) là cách Antigravity kết nối với các hệ thống bên ngoài. Bạn cần cài các MCP servers sau:

### 🔴 BẮT BUỘC: Obsidian MCP

Cho phép Antigravity **đọc, ghi, tìm kiếm** notes trong Obsidian vault.

```json
// Thêm vào file cấu hình MCP của Antigravity
{
  "obsidian": {
    "command": "npx",
    "args": ["-y", "obsidian-mcp"],
    "env": {
      "OBSIDIAN_VAULT_PATH": "~/brain2/vault"
    }
  }
}
```

> Sau khi cài, Antigravity có thể: tạo note, đọc note, search vault, list notes — tất cả qua chat.

### 🟡 KHUYÊN DÙNG: Các MCP bổ sung

| MCP Server | Tác dụng | Khi nào cài |
|---|---|---|
| **Firecrawl** | Web scraping + search cho `/deep-research` | Khi muốn AI nghiên cứu online |
| **Exa** | Academic search cho research sâu | Khi cần tìm papers/nghiên cứu |
| **Context7** | Tra cứu docs thư viện/framework | Khi làm kỹ thuật |
| **Memory** | Knowledge graph bổ sung | Khi vault lớn, cần graph view |

## Bước 4: Copy AI Workflows vào Antigravity

```bash
# Copy workflows
mkdir -p ~/.agent/workflows
cp ~/brain2/workflows/*.md ~/.agent/workflows/

# Copy AI config
mkdir -p ~/.gemini
cp ~/brain2/ai-config/GEMINI.md ~/.gemini/GEMINI.md
```

> ✅ Sau bước này, bạn có thể dùng `/reflect`, `/deep-research`, `/brain-gym`... trực tiếp trong Antigravity.

## Bước 5: Cài Obsidian Plugins (tùy chọn)

Vào **Settings → Community Plugins → Turn on**

| Plugin | Tại sao cần |
|---|---|
| **Templater** | Tạo note từ template nhanh (khi dùng Obsidian trực tiếp) |
| **Dataview** | Query vault, tạo bảng tự động |

> 💡 Brain2 hoạt động tốt ngay cả KHÔNG có plugin. Plugins chỉ hữu ích khi bạn mở Obsidian trực tiếp.

## Bước 6: Test thử!

Mở Antigravity và nói:

```
/reflect Hôm nay mình nhận ra rằng việc ghi chú có cấu trúc giúp mình nhớ lâu hơn gấp 3 lần so với ghi chú tự do.
```

→ Nếu Antigravity tạo được 1 note trong `01-Atomic/Reflections/` → **Setup thành công!** 🎉

---

## Cách dùng Brain2 qua Antigravity (workflow chính)

### 📝 Ghi chú — Không cần mở Obsidian

```
/reflect [suy ngẫm bất kỳ]           → Antigravity tự tạo note qua Obsidian MCP
/story-bank [kể câu chuyện]          → Tự cấu trúc thành story atom
```

### 🔍 Tìm kiếm — Hỏi AI thay vì tự lục

```
"Mình đã ghi gì về Curiosity Gap?"    → Antigravity search vault, trả kết quả
"Tìm stories liên quan đến career"    → Search theo tags/keywords
```

### 🧠 Nghiên cứu — AI đào sâu + lưu vault

```
/deep-research [chủ đề]              → Nghiên cứu online + vault → tạo atomic notes
/brain-gym                           → Ôn luyện 3 notes, Active Recall
```

### 📊 Phân tích & Nâng cấp vault

```
"Quét toàn bộ vault, phân tích gaps"  → Antigravity scan MOCs + concepts → đề xuất
/keystone-scan                        → Gap analysis chuyên sâu
/spaced-usage [bài viết]              → Dùng tri thức cũ trong context mới
```

### ✍️ Viết content chất lượng cao (AI Content Factory)

```
"Viết bài về [topic], dùng stories    → Antigravity lấy stories từ vault
 và insights trong vault"             → Inject DIKW layers vào bài viết
                                      → Content có chiều sâu trí tuệ
```

---

## Bước tiếp theo

→ Chuyển sang [ONBOARDING.md](ONBOARDING.md) để bắt đầu 7-day onboarding! 🚀
