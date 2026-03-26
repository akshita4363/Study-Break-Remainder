# 🌿 Break Reminder

A lightweight productivity tool that reminds you to take regular breaks while working or studying. After a set work interval, it automatically opens a fullscreen break screen in your browser with a countdown timer, stretch suggestions, and a chime alert.

---

## ✨ Features

- **Auto Break Alerts** — Opens a fullscreen break screen after every work interval
- **Terminal Progress Bar** — Visual countdown in CMD while you work
- **Snooze Support** — Snooze the break reminder (configurable max snoozes)
- **Stretch & Eye Exercise Tips** — 12 rotating suggestions during every break
- **Sound Chime** — Pleasant C-E-G tone plays when break ends (Web Audio API)
- **Adjustable Duration** — Change break length from the browser without restarting
- **Config File** — Edit all settings in `config.json` — no code changes needed

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Script | Python 3 (stdlib only) |
| Break Screen | HTML, CSS, Vanilla JS |
| Audio | Web Audio API (no files needed) |
| Config | JSON |

> No external Python libraries required — runs out of the box!

---

## 📁 Project Structure

```
break-reminder/
│
├── break_reminder.py     # Main script — tracks work time, triggers breaks
├── break_screen.html     # Fullscreen break page with timer, tips & chime
└── config.json           # Settings file (work time, break time, snooze)
```

---

## ⚙️ Setup & Installation

### 1. Make sure Python is installed

```cmd
python --version
```

If not installed, download from [python.org](https://python.org) and check **"Add Python to PATH"** during setup.

### 2. Clone or download the repository

```cmd
git clone https://github.com/your-username/break-reminder.git
cd break-reminder
```

### 3. No dependencies to install!

This project uses only Python's built-in modules (`time`, `webbrowser`, `os`, `json`). Nothing else needed.

---

## 🚀 Running the Project

Open CMD in the project folder and run:

```cmd
python break_reminder.py
```

You'll see a live progress bar in the terminal:

```
╔══════════════════════════════════════╗
║       🌿  Break Reminder v2.0        ║
╚══════════════════════════════════════╝
  Work  : 45 min
  Break : 5 min
  Snooze: 5 min  (max 3x)

🟢  Session #1 — working for 45 minutes…
  Session #1  [████████░░░░░░░░░░░░░░░░░░░░░░]  38:21 remaining
```

After the work interval, your browser opens the break screen automatically.

**To stop anytime:** `Ctrl + C`

---

## 🔧 Configuration

Edit `config.json` to change any setting:

```json
{
  "work_minutes": 45,
  "break_minutes": 5,
  "snooze_minutes": 5,
  "max_snoozes": 3
}
```

| Key | Description | Default |
|---|---|---|
| `work_minutes` | How long to work before a break | `45` |
| `break_minutes` | Length of the break | `5` |
| `snooze_minutes` | How long each snooze delays the break | `5` |
| `max_snoozes` | Maximum number of snoozes per break | `3` |

---

## 🖥️ Break Screen Controls

When the break screen opens in your browser:

| Action | How |
|---|---|
| Start the break timer | Click **▶ Start Break** |
| Cycle through exercise tips | Click **Next tip →** |
| Toggle sound chime | Click **🔔 / 🔕** |
| Change break duration | Enter minutes and click **Apply** |
| Break auto-closes | Timer reaches 00:00, chime plays, fullscreen exits |

---

## 💡 Break Exercises Included

The break screen rotates through 12 suggestions:

- 👁️ 20-20-20 eye rule
- 🙆 Shoulder rolls
- 🤸 Neck circles
- 💧 Hydration reminder
- 🖐️ Wrist stretches
- 🧘 Deep breathing
- 🚶 Short walk
- 🌿 Nature viewing
- And more...

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
