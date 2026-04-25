# ⏱️ Professional Time Manager — Sprint Edition

A professional time and task management web app with sprint-based organization.  
Track your productivity, manage tasks, add notes, and analyze work patterns — all in a single HTML file with **zero dependencies**.

![Version](https://img.shields.io/badge/version-2.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![No Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen.svg)

---

## 🚀 Features

### 🏃 Sprint Management
- **Create Custom Sprints** — Organize work into named sprints (e.g., "Week 1", "Project Phase A")
- **Active Sprint Banner** — Always see your current sprint name, description, and start time at the top
- **End Sprint** — Close a sprint and archive it to history
- **Delete Sprint** — Remove any completed sprint and all its associated tasks
- **Sprint History** — Full history of past sprints with statistics per sprint
- **Sprint Comparison** — Compare productivity metrics across different sprints

### ✅ Task Tracking
- **Real-time Timers** — Live counters on every active task
- **Productive vs Break** — Categorize each task as productive work or a break
- **Pause / Resume** — Pause a task without losing elapsed time
- **Complete** — Mark a task done and move it to history with accurate duration
- **Delete** — Remove a task without saving it

### 📝 Notes & Comments
- **Add Note to Any Task** — Click any active task card to open a note modal
- **View / Edit Note on Completed Tasks** — Click any row in the history table to open and edit its note
- **Note Indicator** — A small 📝 badge appears on tasks that have notes (both on cards and in history)
- **Notes Persist** — Notes are saved to localStorage and survive page refresh and export/import

### 📊 Statistics & Analytics
- **Productive Time** — Total time spent on productive tasks
- **Break Time** — Total time spent on breaks
- **Total Time** — Combined productive + break time
- **Productivity %** — Calculated as `(Productive Time / Total Time) × 100`
- **Visual Progress Bar** — Instant visual of productivity ratio
- **Bar Chart** — Canvas-rendered chart comparing productive vs break time

### 🔍 Filtering
- **Current Sprint** — View stats and history for the active sprint only
- **All Time** — Cumulative statistics across every sprint
- **Select Sprint** — Dropdown to filter by any specific past sprint

### 💾 Data Management
- **Local Storage** — All data stored in the browser, no server needed
- **Export to JSON** — Download a full backup including active tasks, completed tasks, and sprints
- **Import from JSON** — Restore a backup; active tasks resume their timers with correct elapsed time
- **Clear Specific Sprint** — Delete one sprint without touching others
- **Clear All Data** — Double-confirmation reset that only removes app data (not unrelated browser storage)

---

## 🛠️ Installation

No install required. Just open the file in a browser.

```bash
git clone https://github.com/YOUR_USERNAME/sprint-time-tracker.git
cd sprint-time-tracker
open time-tracker.html
```

Or simply download the HTML file and double-click it. Works 100% offline.

---

## 💻 Usage

### Starting Your First Sprint
1. Click **"Start New Sprint"**
2. Enter a sprint name and optional description
3. Click **"Start Sprint"**

### Adding a Task
1. Enter the task name
2. Optionally add a description/note in the text area
3. Check **"This is a break time"** if it's non-productive
4. Click **"Start Task"** — the timer starts immediately

### Managing Active Tasks
| Action | How |
|--------|-----|
| Pause timer | Click **⏸️ Pause** on the task card |
| Resume timer | Click **▶️ Resume** |
| Add / Edit note | Click anywhere on the card (not on a button) |
| Complete task | Click **✅ Complete** |
| Delete task | Click **🗑️ Delete** |

### Viewing & Editing Notes on Completed Tasks
- In the **Task History** table, click any row to open the note modal
- Edit the note and click **💾 Save Note**
- A 📝 badge appears in the table if the task has a note

### Ending a Sprint
1. Complete or delete all active tasks
2. Click **"End Sprint"** in the active sprint banner
3. The sprint is archived to Sprint History

### Deleting a Sprint
1. Scroll to **Sprint History**
2. Hover over any completed sprint
3. Click the **🗑️ Delete** button that appears
4. Confirm — the sprint and all its tasks are removed

### Export & Import
- **Export**: Click **📤 Export Data** — a JSON file is downloaded
- **Import**: Click **📥 Import Data** and select a JSON backup file
  - Active tasks resume with their saved elapsed time
  - All sprints, completed tasks, and notes are restored

---

## 🔧 Technical Details

- **Pure HTML / CSS / JavaScript** — no frameworks, no npm, no build step
- **Single file** — everything in one `.html` file, easy to share
- **Canvas API** — used for the productivity bar chart
- **localStorage API** — for all data persistence
- **ES6+** — modern JavaScript (arrow functions, spread, template literals, etc.)
- **Responsive layout** — CSS Grid, works on desktop and tablet

### localStorage Keys

| Key | Contents |
|-----|----------|
| `tasks` | Active (running) tasks array |
| `completedTasks` | History of finished tasks with notes |
| `sprints` | Completed sprint archive |
| `currentSprint` | Active sprint object |

### Export JSON Structure

```json
{
  "version": "1.0",
  "exportDate": "2025-04-25T10:30:00.000Z",
  "activeTasks": [
    {
      "id": 1714038600000,
      "name": "Fix login bug",
      "note": "Related to issue #42",
      "isBreak": false,
      "sprintId": 1713900000000,
      "startTime": "2025-04-25T08:00:00.000Z",
      "isRunning": true,
      "duration": 3600
    }
  ],
  "completedTasks": [...],
  "sprints": [...],
  "currentSprint": {...}
}
```

### Duration Calculation

```
finalDuration = totalElapsed - pausedDuration

totalElapsed   = now - startTime  (in seconds)
pausedDuration = sum of all pause intervals
```

On import, `startTime` is recalculated as `now - savedDuration` so the timer continues correctly without drift.

---

## 📊 Browser Compatibility

| Browser | Supported |
|---------|-----------|
| Chrome 60+ | ✅ |
| Firefox 55+ | ✅ |
| Safari 11+ | ✅ |
| Edge 79+ | ✅ |
| Opera 47+ | ✅ |

---

## 🗺️ Roadmap

- [x] Sprint creation and management
- [x] Pause / resume tasks
- [x] Export & import JSON backup
- [x] Per-task notes with modal editor
- [x] Notes on completed tasks (history table)
- [x] Delete individual sprints
- [x] Sprint selector in statistics filter
- [ ] Dark mode theme
- [ ] Export to CSV / Excel
- [ ] Calendar view of sprints
- [ ] Task categories / tags
- [ ] Weekly & monthly reports
- [ ] Pomodoro timer integration
- [ ] Cloud sync option

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Armin**  
[![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white)](https://github.com/YOUR_USERNAME)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR_USERNAME)

---

*Made with ❤️ for better productivity*
