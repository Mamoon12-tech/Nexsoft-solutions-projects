# ☁️ Task 5 — Weather App using API
**Nexsoft Solutions Internship · Mamoon Azam Khattak · 2026**

[![Live Demo](https://img.shields.io/badge/Live-Demo-00C7B7?style=flat&logo=netlify)](https://mamoonazamportfolio.netlify.app)
[![GitHub](https://img.shields.io/badge/GitHub-Source_Code-181717?style=flat&logo=github)](https://github.com/Mamoon12-tech/Nexsoft-solutions-projects/tree/main/task5)

---

## 📌 About This Project

A real-time weather app that fetches live weather data from the OpenWeatherMap API. Search any city in the world and instantly see the temperature, weather condition, humidity, wind speed, visibility, and pressure.

The background color changes dynamically based on the weather — sunny days look different from rainy ones.

---

## ✨ Features

- ✅ Fetch live weather data from OpenWeatherMap public API
- ✅ Display temperature in °C
- ✅ Show weather condition (Clear, Cloudy, Rain, etc.)
- ✅ Feels-like temperature display
- ✅ Humidity, wind speed, visibility, and pressure details
- ✅ Dynamic weather emoji icons based on condition
- ✅ Dynamic background gradient changes with weather
- ✅ City search with Enter key support
- ✅ Quick-select chips for popular cities (Peshawar, Islamabad, Lahore, etc.)
- ✅ Loading spinner while fetching
- ✅ Error handling for invalid city names and bad API keys
- ✅ Responsive weather interface

---

## 🛠️ Tech Stack

| Technology | What I used it for |
|---|---|
| HTML5 | App layout and structure |
| CSS3 | Styling, dynamic backgrounds, glassmorphism UI |
| JavaScript | API calls, DOM updates, error handling |
| OpenWeatherMap API | Real-time weather data source |
| Fetch API | Making HTTP GET requests to the weather API |

---

## 📂 File Structure

```
task5/
├── index.html    → Full weather app (HTML + CSS + JS)
└── README.md     → This file
```

---

## ⚙️ Setup — API Key Required

This app uses the **OpenWeatherMap API** (free tier).

### Steps:
1. Go to [openweathermap.org](https://openweathermap.org/api)
2. Sign up for a free account
3. Go to **API Keys** in your dashboard
4. Copy your API key
5. Open `index.html` and find this line:
```javascript
const API_KEY = 'YOUR_API_KEY';
```
6. Replace `YOUR_API_KEY` with your actual key
7. Save and open in browser ✅

> **Free tier** allows 60 calls/minute and 1,000,000 calls/month — more than enough.

---

## 🧠 How It Works

### API Call
```javascript
const res = await fetch(
  `https://api.openweathermap.org/data/2.5/weather?q=${city}&appid=${API_KEY}&units=metric`
);
```

### Response Data Used
```javascript
data.name            // City name
data.sys.country     // Country code
data.main.temp       // Temperature in °C
data.main.feels_like // Feels like
data.main.humidity   // Humidity %
data.wind.speed      // Wind speed (m/s → converted to km/h)
data.visibility      // Visibility in meters
data.main.pressure   // Atmospheric pressure
data.weather[0].description // Weather condition text
data.weather[0].main        // Weather category for background
```

### Error Handling
```javascript
if (res.status === 404) → "City not found"
if (res.status === 401) → "Invalid API key"
if (API_KEY === 'YOUR_API_KEY') → Prompts to add key
```

### Dynamic Background
Weather category (`Clear`, `Rain`, `Clouds`, `Snow`, etc.) maps to a different CSS gradient, applied directly to `document.body.style.background`.

---

## 🌍 Pre-loaded Cities

Quick-tap chips for: Peshawar · Islamabad · Lahore · Karachi · London · Dubai

---

## 🎨 Design Choices

- **Style:** Glassmorphism — semi-transparent card with `backdrop-filter: blur(20px)`
- **Background:** Dynamic gradient — changes based on weather condition
- **Icons:** Unicode weather emojis mapped to condition descriptions
- **Typography:** Outfit — clean, modern, readable at all sizes

---

## 🚀 How to Run

1. Add your API key (see Setup above)
2. Open `index.html` in any browser
3. Search a city or tap a quick-chip ✅

---

## 👨‍💻 Author

**Mamoon Azam Khattak**
- 🎓 Computer Systems Engineering — UET Peshawar
- 💼 Web Developer Intern — Nexsoft Solutions
- 🔗 [LinkedIn](https://linkedin.com/in/mamoon-azam-khattak) · [Portfolio](https://mamoonazamportfolio.netlify.app) · [GitHub](https://github.com/Mamoon12-tech)

---

*Part of a 13-task internship project series · Nexsoft Solutions 2026*
