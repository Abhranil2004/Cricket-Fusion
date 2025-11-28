# **Cricket Fusion 🏏**
![Cricket Fusion Banner](https://i.imgur.com/0qk6iCk.png)


*A modern cricket dashboard with live scores, real-time updates, and a premium UI.*

Cricket Fusion delivers live cricket data with an interface inspired by professional sports dashboards. It provides live match cards, scoreboards, upcoming fixtures, team stats, and detailed innings breakdowns — all powered by the **Cricbuzz Cricket API (RapidAPI)**.

Designed using **React + Vite + Tailwind CSS**, the website is fast, responsive, and smooth.

---

## 🚀 **Features**

### 🟢 Live Matches

* Auto-updating live scores
* Match status indicators
* Team logos & flags
* Ball-by-ball style info (where available)

### 📅 Upcoming Matches

* Date, teams, venue
* Clean fixture layout

### 📊 Match Details

* Full scoreboard (Batting + Bowling)
* Fall of wickets
* Player contributions
* Inning comparison panels
* Match summary

### 🔍 Smart Search

Find your matches instantly.

### 🎨 UI Style

* Clean modern layout
* Soft gradients
* Smooth card design
* Fully responsive
* Minimal but premium

---

## 🛠️ Tech Stack

### **Frontend**

* React
* Vite
* Tailwind CSS
* Axios

### **API**

* **RapidAPI: Cricbuzz Cricket API**
  [https://rapidapi.com/](https://rapidapi.com/)

---

## 🔌 API Integration (No ENV — Key Inside File)

You store your API key directly in:

`src/api/cricApi.js`

Example:

```js
import axios from "axios";

const API_KEY = "YOUR_RAPID_API_KEY";
const API_HOST = "cricbuzz-cricket.p.rapidapi.com";

export const getLiveMatches = async () => {
  const options = {
    method: "GET",
    url: "https://cricbuzz-cricket.p.rapidapi.com/matches/v1/live",
    headers: {
      "x-rapidapi-key": API_KEY,
      "x-rapidapi-host": API_HOST,
    },
  };

  const res = await axios.request(options);
  return res.data;
};
```

You can repeat the same structure for:

* Upcoming Matches
* Scorecards
* Match Info
* Commentary

---

## 📁 Folder Structure

```
cricket-fusion/
│── public/
│── src/
│   ├── api/
│   │   └── cricApi.js        # API key is here
│   ├── components/
│   │   ├── Navbar.jsx
│   │   ├── MatchCard.jsx
│   │   ├── MatchList.jsx
│   │   ├── Scoreboard.jsx
│   │   └── Footer.jsx
│   ├── pages/
│   │   ├── Home.jsx
│   │   ├── Live.jsx
│   │   ├── Upcoming.jsx
│   │   ├── MatchDetails.jsx
│   │   └── Search.jsx
│   ├── assets/
│   ├── App.jsx
│   ├── main.jsx
│── package.json
│── tailwind.config.js
│── README.md
```

---

## ⚙️ Installation

```bash
# Clone the project
git clone https://github.com/yourname/cricket-fusion.git

cd cricket-fusion

# Install packages
npm install

# Start development server
npm run dev
```

*No `.env` file required. API key stays inside `cricApi.js`.*

---

## 🌐 Deployment

### Deploy on Vercel

```bash
npm run build
```

Upload the project → Deploy.

Your API key is already inside the file.

### Deploy on Netlify

Drag and drop the `dist` folder after build.

---

## 📸 UI Showcase

The homepage includes:

* [Hero banner](https://i.imgur.com/EB0gkHP.jpeg)
* [Live match cards](https://i.imgur.com/EB0gkHP.jpeg)
* [Quick stats panel](https://i.imgur.com/EB0gkHP.jpeg)
* [Scrollable live feed](https://i.imgur.com/EB0gkHP.jpeg)
* [In-depth match details section](https://i.imgur.com/EB0gkHP.jpeg)
* [Elegant scoreboards](https://i.imgur.com/EB0gkHP.jpeg)
---

## 🏏 Why Cricket Fusion?

* Clean UI
* Easy to understand
* Fast load time
* Accurate live updates
* Professional design

---

## 🔮 Future Add-ons

* Team rankings
* Player profiles
* World Cup dashboard
* Push notifications
* Dark mode

---

## 👨‍💻 Author

**Abhranil Dutta**
Developer • GSA • UI Designer


