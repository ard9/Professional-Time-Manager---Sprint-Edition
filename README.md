# Professional-Time-Manager---Sprint-Edition
A professional time and task management web app with sprint-based organization. Track productivity, manage tasks, and analyze work patterns. Pure HTML/CSS/JS - no dependencies, works offline.
# ⏱️ Sprint Time Tracker

A professional time and task management application with sprint-based organization. Track your productivity, manage tasks, and analyze your work patterns across different sprints.

![Sprint Time Tracker](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## 🚀 Features

### Sprint Management
- **Create Custom Sprints**: Organize your work into named sprints (e.g., "Week 1", "Project Phase A")
- **Sprint History**: View complete history of all past sprints with detailed statistics
- **Sprint Comparison**: Compare productivity across different sprints
- **Flexible Duration**: Sprints can be as short or long as you need

### Task Tracking
- **Real-time Timers**: Track time spent on each task with live counters
- **Productive vs Break Time**: Categorize tasks as productive work or breaks
- **Pause/Resume**: Pause and resume tasks without losing progress
- **Task History**: Complete history of all completed tasks

### Analytics & Statistics
- **Productivity Metrics**: Calculate productivity percentage (productive time / total time)
- **Visual Charts**: Bar charts showing productive vs break time distribution
- **Sprint Filtering**: View statistics for specific sprints or all-time data
- **Real-time Updates**: Statistics update automatically as you work

### Data Management
- **Local Storage**: All data stored locally in your browser
- **Export Data**: Download your data as JSON for backup
- **Clear History**: Option to reset all data when needed
- **Persistent State**: Tasks and sprints survive page refreshes

## 📸 Screenshots

### Active Sprint Dashboard
Track your current sprint with live task timers and quick controls.

### Sprint History
Review past sprints with comprehensive statistics and productivity metrics.

### Task Management
Add, pause, complete, or delete tasks with an intuitive interface.

## 🛠️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/sprint-time-tracker.git
   ```

2. **Open the file**
   ```bash
   cd sprint-time-tracker
   open time-task-manager-with-sprints.html
   ```

3. **Start tracking!**
   - Open the HTML file in any modern web browser
   - No server or dependencies required
   - Works completely offline

## 💻 Usage

### Starting Your First Sprint

1. Click **"Start New Sprint"** button
2. Enter a sprint name (e.g., "January Week 1")
3. Optionally add a description
4. Click **"Start Sprint"**

### Adding Tasks

1. Enter task name in the input field
2. Check "This is a break time" if it's a non-productive activity
3. Click **"Start Task"**
4. The timer starts automatically

### Managing Tasks

- **Pause**: Click pause button to temporarily stop the timer
- **Resume**: Click resume to continue tracking
- **Complete**: Mark task as done and add to history
- **Delete**: Remove task without saving to history

### Viewing Statistics

- **Current Sprint**: See stats for your active sprint
- **All Time**: View cumulative statistics across all sprints
- **Select Sprint**: Filter by specific past sprint

### Ending a Sprint

1. Complete or delete all active tasks
2. Click **"End Sprint"** in the banner
3. Sprint is saved to history
4. Ready to start a new sprint

## 🎨 Features in Detail

### Productivity Calculation

```
Productivity % = (Productive Time / Total Time) × 100
```

- **Productive Time**: Sum of all non-break tasks
- **Break Time**: Sum of all break tasks
- **Total Time**: Productive + Break time

### Data Storage

All data is stored in browser's `localStorage`:

- `tasks`: Currently active tasks
- `completedTasks`: History of finished tasks
- `sprints`: Completed sprint history
- `currentSprint`: Active sprint information

### Export Format

Exported JSON includes:
```json
{
  "activeTasks": [...],
  "completedTasks": [...],
  "sprints": [...],
  "currentSprint": {...},
  "exportDate": "2024-01-15T10:30:00.000Z"
}
```

## 🌟 Use Cases

- **Software Development**: Track coding sprints and tasks
- **Study Sessions**: Organize study time with breaks
- **Project Management**: Monitor time across project phases
- **Freelancing**: Track billable vs non-billable hours
- **Personal Productivity**: Analyze work patterns and habits

## 🔧 Technical Details

- **Pure HTML/CSS/JavaScript**: No frameworks or dependencies
- **Responsive Design**: Works on desktop, tablet, and mobile
- **Canvas API**: Used for chart rendering
- **LocalStorage API**: For data persistence
- **ES6+**: Modern JavaScript features

## 📊 Browser Compatibility

- ✅ Chrome 60+
- ✅ Firefox 55+
- ✅ Safari 11+
- ✅ Edge 79+
- ✅ Opera 47+

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Designed for productivity enthusiasts
- Built with simplicity and efficiency in mind
- Inspired by agile sprint methodology

## 📧 Contact

For questions or suggestions, please open an issue on GitHub.

## 🗺️ Roadmap

Future enhancements planned:

- [ ] Import data from JSON backup
- [ ] Calendar view of sprints
- [ ] Export to CSV/Excel
- [ ] Dark mode theme
- [ ] Custom color themes
- [ ] Sprint goals and notes
- [ ] Task categories/tags
- [ ] Weekly/monthly reports
- [ ] Pomodoro timer integration
- [ ] Cloud sync option

---

**Made with ❤️ for better productivity**
