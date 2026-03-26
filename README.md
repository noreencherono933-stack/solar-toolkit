<div align="center">

```
███████╗ ██████╗ ██╗      █████╗ ██████╗ ██████╗ ██╗   ██╗██╗     ███████╗███████╗
██╔════╝██╔═══██╗██║     ██╔══██╗██╔══██╗██╔══██╗██║   ██║██║     ██╔════╝██╔════╝
███████╗██║   ██║██║     ███████║██████╔╝██████╔╝██║   ██║██║     ███████╗█████╗  
╚════██║██║   ██║██║     ██╔══██║██╔══██╗██╔═══╝ ██║   ██║██║     ╚════██║██╔══╝  
███████║╚██████╔╝███████╗██║  ██║██║  ██║██║     ╚██████╔╝███████╗███████║███████╗
╚══════╝ ╚═════╝ ╚══════╝╚═╝  ╚═╝╚═╝  ╚═╝╚═╝      ╚═════╝ ╚══════╝╚══════╝╚══════╝
```

### ☀️ Real-Time Photovoltaic Monitoring Dashboard

[![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactjs.org/)
[![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Recharts](https://img.shields.io/badge/Recharts-FF6B6B?style=for-the-badge&logo=chart.js&logoColor=white)](https://recharts.org/)
[![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=for-the-badge&logo=netlify&logoColor=white)](https://netlify.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-F59E0B?style=for-the-badge)](./LICENSE)

*Translating raw PV energy data into intuitive visual analytics — built for engineers, designed for clarity.*

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
- [Usage](#-usage)
- [Configuration](#-configuration)
- [Project Structure](#-project-structure)
- [Troubleshooting](#-troubleshooting)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🔍 Overview

**SolarPulse Toolkit** is an engineering-first web dashboard for real-time monitoring and visualization of photovoltaic (PV) system performance. It converts raw solar energy data — power output in kW, battery state-of-charge, system efficiency — into clear, actionable visual analytics.

> Built to demonstrate the integration of renewable energy domain knowledge with modern full-stack web development.

---

## ✨ Key Features

| Feature | Description |
|---|---|
| ⚡ **Real-Time Metrics** | Live visualization of Power Output (kW), Storage Levels (%), and System Efficiency |
| 📈 **Yield Analytics** | Interactive area chart tracking the 24-hour diurnal solar cycle to identify peak generation windows |
| 💓 **System Heartbeat** | Visual diagnostic indicator confirming active hardware-to-UI connectivity |
| 📱 **Responsive UI** | Mobile-first design optimized for on-site field inspections and remote monitoring |

---

## 🛠 Tech Stack

```
Frontend    →  React.js (Vite)
Styling     →  Tailwind CSS  
Charts      →  Recharts (SVG-based)
Icons       →  Lucide React
Deployment  →  Netlify
```

---

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** `v18.0.0` or higher
- **NPM** `v9.0.0` or higher
- **VS Code** *(recommended)*

### Installation

**1. Clone the repository**
```bash
git clone https://github.com/noreencherono933-stack/solar-toolkit.git
cd solar-toolkit
```

**2. Install dependencies**
```bash
npm install
```

**3. Start the development server**
```bash
npm run dev
```

The dashboard will be live at `http://localhost:5173` 🎉

---

## 💡 Usage

The dashboard is designed for **zero configuration**. On launch, the `Dashboard` component automatically initializes the Recharts engine and renders the current day's energy profile.

```jsx
// Reusable StatCard component for PV metrics
<StatCard 
  title="Current Output" 
  value="5.8 kW" 
  Icon={Zap} 
/>
```

---

## ⚙️ Configuration

**Theme**  
The UI uses an **Amber/Slate** color scheme tailored for solar branding. Colors are easily adjustable in `tailwind.config.js`.

**Data Source**  
The project currently uses a mock data array in `App.jsx`. To connect live data, replace it with a `fetch()` call to your IoT API endpoint:

```js
// Replace mock data with a live API call
const data = await fetch("https://your-iot-api.com/metrics").then(r => r.json());
```

---

## 📁 Project Structure

```
solar-toolkit/
├── src/
│   ├── App.jsx          # Main dashboard logic & UI components
│   ├── index.css        # Tailwind directives & global styles
│   └── main.jsx         # React entry point
├── public/              # Static assets
├── index.html           # HTML template with Tailwind CDN
├── tailwind.config.js   # Styling configuration
└── package.json         # Dependencies & scripts
```

---

## 🔧 Troubleshooting

**`npm` script execution error on Windows**  
> PowerShell may block script execution due to system policy restrictions.  
> ✅ **Fix:** Use **Command Prompt (`cmd`)** instead, or adjust your `Execution_Policy` setting.

**Tailwind styles not loading**  
> This can occur in restricted environments where PostCSS isn't processing correctly.  
> ✅ **Fix:** A CDN-injected Tailwind link is included in `index.html` as a reliable fallback.

---

## 🤝 Contributing

Contributions are welcome! To get started:

1. **Fork** the repository
2. **Create** a feature branch
   ```bash
   git checkout -b feature/NewSolarMetric
   ```
3. **Commit** your changes
   ```bash
   git commit -m "feat: add NewSolarMetric component"
   ```
4. **Push** to your branch and open a **Pull Request**

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](./LICENSE) for full details.

---

<div align="center">

Made with ☀️ and React &nbsp;·&nbsp; <a href="https://github.com/noreencherono933-stack/solar-toolkit">github.com/noreencherono933-stack/solar-toolkit</a>

</div>
