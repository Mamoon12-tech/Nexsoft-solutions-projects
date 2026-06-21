# 🧮 Task 4 — Calculator App
**Nexsoft Solutions Internship · Mamoon Azam Khattak · 2026**

[![Live Demo](https://img.shields.io/badge/Live-Demo-00C7B7?style=flat&logo=netlify)](https://mamoonazamportfolio.netlify.app)
[![GitHub](https://img.shields.io/badge/GitHub-Source_Code-181717?style=flat&logo=github)](https://github.com/Mamoon12-tech/Nexsoft-solutions-projects/tree/main/task4)

---

## 📌 About This Project

A fully functional calculator app built with vanilla JavaScript. It handles all basic arithmetic operations, edge cases like division by zero, and even supports keyboard input — so you never have to use a mouse.

The UI is inspired by modern dark-theme design, with a calculation history panel that lets you reuse previous results.

---

## ✨ Features

- ✅ All arithmetic operations — addition, subtraction, multiplication, division
- ✅ Division by zero error handling with clear message
- ✅ Toggle sign (+/−) to flip between positive and negative
- ✅ Percentage (%) operator
- ✅ AC (All Clear) to reset everything
- ✅ Backspace support via keyboard
- ✅ Calculation history — last 8 results, click any to reuse
- ✅ Full keyboard support (numbers, operators, Enter, Escape, Backspace)
- ✅ Expression display shows what you're calculating
- ✅ Chained operations (press operator without = to chain)
- ✅ Responsive and works on mobile

---

## 🛠️ Tech Stack

| Technology | What I used it for |
|---|---|
| HTML5 | Calculator layout and button grid |
| CSS3 | Dark theme, grid layout, button styles, animations |
| JavaScript | All calculation logic, keyboard events, history |

---

## 📂 File Structure

```
task4/
├── index.html    → Full calculator (HTML + CSS + JS)
└── README.md     → This file
```

---

## 🧠 How the Logic Works

### State Variables
```javascript
let current = '0';   // What's shown on display
let prev = '';       // First number before operator
let op = null;       // Current operator (+, -, *, /)
let justCalc = false; // Whether we just pressed =
```

### Input Handling
When a number is pressed, it appends to `current`. If `justCalc` is true (just pressed =), it starts fresh.

### Operator Handling
`setOp()` saves `current` to `prev`, stores the operator, and sets `justCalc = true` so the next number starts fresh.

### Calculation
`calculate()` reads `prev` and `current`, runs the operation in a `switch` statement, handles division by zero, and displays the result.

### Error Handling
```javascript
if (op === '/' && b === 0) {
  mainEl.textContent = 'Cannot ÷ 0';
  mainEl.classList.add('error'); // turns red
}
```

### Keyboard Support
```javascript
document.addEventListener('keydown', e => {
  if (e.key >= '0' && e.key <= '9') input(e.key);
  else if (e.key === 'Enter') calculate();
  else if (e.key === 'Escape') clearAll();
  // etc.
});
```

---

## 🎨 Design Choices

- **Theme:** Near-black `#0d0d12` background with purple accent `#6c47ff` for the equals button
- **Typography:** Space Grotesk (UI labels) + Space Mono (display numbers) — great contrast between UI and data
- **Button grid:** CSS `grid-template-columns: repeat(4, 1fr)` — clean 4-column layout
- **History panel:** Stored in a JS array, rendered below the calculator, clickable to reuse values

---

## 🚀 How to Run

**Option 1 — Open directly:**
Download `index.html` and open in any browser. Fully offline.

**Option 2 — Deploy on Netlify:**
1. Push to GitHub
2. Connect repo on Netlify
3. Set publish directory to `task4`
4. Deploy ✅

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
|---|---|
| `0–9` | Number input |
| `+ - * /` | Operators |
| `Enter` or `=` | Calculate |
| `Escape` | Clear all |
| `Backspace` | Delete last digit |
| `.` | Decimal point |

---

## 👨‍💻 Author

**Mamoon Azam Khattak**
- 🎓 Computer Systems Engineering — UET Peshawar
- 💼 Web Developer Intern — Nexsoft Solutions
- 🔗 [LinkedIn](https://linkedin.com/in/mamoon-azam-khattak) · [Portfolio](https://mamoonazamportfolio.netlify.app) · [GitHub](https://github.com/Mamoon12-tech)

---

*Part of a 13-task internship project series · Nexsoft Solutions 2026*
