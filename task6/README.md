# 📝 Task 6 — Notes Management System
**Nexsoft Solutions Internship · Mamoon Azam Khattak · 2026**

[![Live Demo](https://img.shields.io/badge/Live-Demo-00C7B7?style=flat&logo=netlify)](https://mamoonazamportfolio.netlify.app)
[![GitHub](https://img.shields.io/badge/GitHub-Source_Code-181717?style=flat&logo=github)](https://github.com/Mamoon12-tech/Nexsoft-solutions-projects/tree/main/task6)

---

## 📌 About This Project

A rich, Notion-inspired notes management app built with pure HTML, CSS and JavaScript. Notes are saved to `localStorage` and persist across sessions. The interface has a sidebar for navigation and a full editor on the right — just like a real notes application.

---

## ✨ Features

- ✅ Create new notes with one click
- ✅ Edit notes in a full-width rich text editor
- ✅ Delete notes with confirmation prompt
- ✅ Real-time search — filters notes by title and content instantly
- ✅ Color tagging — 5 colors to organize notes visually
- ✅ Word count tracker updates as you type
- ✅ Auto-save every 10 seconds
- ✅ Manual save with Ctrl+S keyboard shortcut
- ✅ Notes sorted by last updated (most recent first)
- ✅ Preview of note content in the sidebar
- ✅ Relative timestamps (Today's time or past dates)
- ✅ localStorage persistence — notes survive page refresh
- ✅ Responsive dashboard layout (sidebar + editor)
- ✅ Welcome screen when no note is selected

---

## 🛠️ Tech Stack

| Technology | What I used it for |
|---|---|
| HTML5 | Dashboard layout, sidebar, editor structure |
| CSS3 | Grid layout, sidebar/main split, animations |
| JavaScript | CRUD logic, search, localStorage, auto-save |
| localStorage | Saving all notes client-side |

> 📌 **Note:** The full-stack version with MongoDB + authentication is planned as a separate backend project. This version uses localStorage for persistence.

---

## 📂 File Structure

```
task6/
├── index.html    → Full notes app (HTML + CSS + JS)
└── README.md     → This file
```

---

## 🧠 How It Works

### Data Structure
Each note is stored as an object:
```javascript
{
  id: 'unique_id',       // Generated with Date.now() + random
  title: 'Note title',
  body: 'Note content',
  color: '#c24b2a',      // One of 5 color options
  updatedAt: 1234567890  // Timestamp for sorting
}
```

All notes live in a `notes` array, serialized to `localStorage` on every save.

### CRUD Operations

**Create:**
```javascript
notes.unshift({ id: genId(), title: '', body: '', color: '#c24b2a', updatedAt: Date.now() });
```

**Read:**
Notes are loaded from `localStorage` on page load and rendered in the sidebar.

**Update:**
```javascript
notes[idx].title = document.getElementById('noteTitle').value;
notes[idx].body  = document.getElementById('noteBody').value;
notes[idx].updatedAt = Date.now();
```

**Delete:**
```javascript
notes = notes.filter(n => n.id !== activeId);
```

### Search
```javascript
notes.filter(n =>
  n.title.toLowerCase().includes(query) ||
  n.body.toLowerCase().includes(query)
)
```
Filters live on every keystroke — no button needed.

### Auto-Save
```javascript
setInterval(() => { if (activeId) saveNote(); }, 10000);
```
Runs every 10 seconds silently in the background.

---

## 🎨 Design Choices

- **Style:** Editorial / Notion-inspired — warm cream tones, serif headings
- **Typography:** Fraunces (display serif for titles) + Inter (body text)
- **Layout:** CSS Grid with `260px 1fr` sidebar/main split
- **Color system:** 5 accent colors per note, shown as dots in sidebar and as an accent line at the top of the editor
- **Accent line:** 3px colored bar at the top of the editor matches the note's tag color

---

## 📱 Responsive Design

On mobile, the sidebar stacks above the editor. Both scroll independently.

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl + S` | Save current note |
| Type in search | Filters notes live |

---

## 🚀 How to Run

**Option 1 — Open directly:**
Download `index.html` and open in any browser. Notes save automatically via localStorage.

**Option 2 — Deploy on Netlify:**
1. Push to GitHub
2. Connect repo on Netlify
3. Set publish directory to `task6`
4. Deploy ✅

---

## 👨‍💻 Author

**Mamoon Azam Khattak**
- 🎓 Computer Systems Engineering — UET Peshawar
- 💼 Web Developer Intern — Nexsoft Solutions
- 🔗 [LinkedIn](https://linkedin.com/in/mamoon-azam-khattak) · [Portfolio](https://mamoonazamportfolio.netlify.app) · [GitHub](https://github.com/Mamoon12-tech)

---

*Part of a 13-task internship project series · Nexsoft Solutions 2026*
