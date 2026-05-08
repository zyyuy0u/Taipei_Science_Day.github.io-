# 台北科學日 — 下一梯次活動時間 看板

A pure-HTML, single-page **brutalist** countdown / schedule board for **Taipei Science Day**.
為台北科學日打造的純前端網頁，用一塊大大的時間牌告訴觀眾「下一梯次活動」幾點開始。

---

## ✨ Highlights

- **70% screen real estate** for the next session time — readable from across the room.
- **Brutalist creative-agency aesthetic** — bold yellow / black / hot-pink, harsh shadows, slightly rotated cards, mono + Archivo Black typography, animated marquee, glitch jitter, pulsing live dot.
- **Right-side info column** showing「每一梯次隔 15 分鐘」, a live clock, and a full session grid that highlights the upcoming slot.
- **Auto status switching**:
  - `活動即將開始` — before 09:15
  - `活動進行中` — between 09:15 and 16:00
  - `今日活動已結束` — after 16:00
- **Zero build / zero dependencies.** Just open `index.html` or host on GitHub Pages.

## 🗓️ Schedule logic

Sessions run **every 15 minutes from 09:15 to 16:00**:
`09:15 / 09:30 / 09:45 / … / 15:45 / 16:00`

The page polls the local clock once per second and updates the big time, the status pill, and the schedule grid automatically.

## 🚀 Deploy on GitHub Pages

```bash
git init -b main
git add index.html README.md
git commit -m "Taipei Science Day next-session board"
git remote add origin https://github.com/zyyuy0u/Taipei_Science_Day.github.io-.git
git push -u origin main
```

Then in the repo:

1. **Settings → Pages**
2. **Source:** `Deploy from a branch`
3. **Branch:** `main` / `/ (root)` → **Save**

Live URL will be:
`https://zyyuy0u.github.io/Taipei_Science_Day.github.io-/`

## 🧱 Tech

- Pure HTML + CSS + vanilla JS — no framework, no build step.
- Google Fonts: `Archivo Black`, `Noto Sans TC`, `Space Mono`.
- Designed full-screen 16:9 first, with a mobile fallback under 900px width.

## 🎨 Palette

| Token | Hex | Use |
|------|-----|-----|
| `--bg` | `#FFE500` | Brutalist yellow background |
| `--ink` | `#0A0A0A` | Borders, ink, type |
| `--paper` | `#FAF8F2` | Side panel paper tone |
| `--hot` | `#FF2D55` | Live dot, status, accents |
| `--acid` | `#00E08A` | Live clock readout |
| `--blue` | `#2D4BFF` | Idle / pre-event accent |

## 📁 Files

- `index.html` — the entire app (markup + styles + script)
- `README.md` — this file

## 📝 License

MIT — use it, remix it, run it on a projector.
