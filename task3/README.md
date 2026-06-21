# ✅ Task 3 — To-Do List Application
**Nexsoft Solutions Internship · Mamoon Azam Khattak · 2026**

[![Live Demo](https://img.shields.io/badge/Live-Demo-00C7B7?style=flat&logo=netlify)](https://mamoonazamportfolio.netlify.app)
[![GitHub](https://img.shields.io/badge/GitHub-Source_Code-181717?style=flat&logo=github)](https://github.com/Mamoon12-tech/Nexsoft-solutions-projects/tree/main/task3)

---

## 📌 About This Project

A fully functional To-Do List app built with vanilla JavaScript. Tasks are saved to `localStorage` so they survive page refreshes — your list is always there when you come back.

The UI is clean, minimal and satisfying to use. Checking off a task actually feels good.

---

## ✨ Features

- ✅ Add tasks dynamically (type + press Enter or click Add)
- ✅ Delete individual tasks with one click
- ✅ Mark tasks as completed with visual strikethrough
- ✅ 3-tab filter — All / Active / Completed
- ✅ Tasks stored in `localStorage` — persists after refresh
- ✅ Progress bar showing how many tasks are done
- ✅ Live stats — remaining tasks + completed count
- ✅ Clear all completed tasks in one click
- ✅ Live date display at the top
- ✅ Empty state messages for each filter
- ✅ Slide-in animation for new tasks
- ✅ Responsive and clean UI

---

## 🛠️ Tech Stack

| Technology | What I used it for |
|---|---|
| HTML5 | App structure and layout |
| CSS3 | Styling, animations, responsive design |
| JavaScript | DOM manipulation, logic, localStorage |
| localStorage | Saving tasks across sessions |

---

## 📂 File Structure

```
task3/
├── index.html    → Full app (HTML + CSS + JS in one file)
└── README.md     → This file
```

---

## 🧠 How It Works

### Adding a Task
User types in the input field and presses **Enter** or clicks **+ Add**. The task is pushed to the `tasks` array, saved to `localStorage`, and the list re-renders.

### Completing a Task
Clicking the circle checkbox toggles `completed: true/false` on the task object. The item gets a strikethrough and fades slightly. The progress bar updates live.

### Filtering
Three buttons update a `filter` variable (`'all'`, `'active'`, `'completed'`). The render function filters the array before building the HTML.

### Persistence
Every change calls `localStorage.setItem('nexsoft_tasks', JSON.stringify(tasks))`. On page load, tasks are read back with `JSON.parse(localStorage.getItem(...))`.

---

## 🎨 Design Choices

- **Background:** Warm off-white `#f7f5f0` — easier on the eyes than pure white
- **Accent:** Purple `#6c47ff` — clear, modern, not overused
- **Typography:** DM Sans + DM Mono — clean and readable
- **Animations:** CSS `@keyframes slideIn` for new tasks, smooth transitions on checkboxes

---

## 📱 Responsive Design

Works on all screen sizes. Input and buttons stack cleanly on mobile. Touch-friendly targets.

---

## 🚀 How to Run

**Option 1 — Open directly:**
Download `index.html` and open in any browser. No server or install needed.

**Option 2 — Deploy on Netlify:**
1. Push to GitHub
2. Connect repo on Netlify
3. Set publish directory to `task3`
4. Deploy ✅

---

## 👨‍💻 Author

**Mamoon Azam Khattak**
- 🎓 Computer Systems Engineering — UET Peshawar
- 💼 Web Developer Intern — Nexsoft Solutions
- 🔗 [LinkedIn](https://linkedin.com/in/mamoon-azam-khattak) · [Portfolio](https://mamoonazamportfolio.netlify.app) · [GitHub](https://github.com/Mamoon12-tech)

---

*Part of a 13-task internship project series · Nexsoft Solutions 2026*
