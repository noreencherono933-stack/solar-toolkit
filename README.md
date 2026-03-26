SolarPulse Toolkit
Description
The SolarPulse Toolkit is a specialized web interface designed for real-time monitoring and visualization of photovoltaic (PV) system performance. Built as an engineering-first dashboard, it translates raw energy data (like kW output and battery state-of-charge) into intuitive visual analytics. This project demonstrates the integration of renewable energy concepts with modern full-stack development.

Key Features
Real-time Performance Metrics: Instant visualization of Current Power Output (kW), Storage Levels (%), and System Efficiency.

Dynamic Yield Analytics: An interactive Area Chart tracking the 24-hour diurnal solar cycle to identify peak generation hours.

System Status Heartbeat: A visual diagnostic indicator to confirm active connectivity between hardware logic and the UI.

Responsive UI: A mobile-first design optimized for on-site field inspections and remote monitoring.

Technologies Used
Frontend: React.js (Vite)

Styling: Tailwind CSS (Utility-first framework)

Visualization: Recharts (SVG-based charting library)

Icons: Lucide-React

Deployment: Netlify

Installation Requirements
Node.js: v18.0.0 or higher

NPM: v9.0.0 or higher

Editor: VS Code (recommended)

Installation Instructions
Clone the Repository:

Bash
git clone https://github.com/noreencherono933-stack/solar-toolkit.git
Install Dependencies:

Bash
npm install
Start Development Server:

Bash
npm run dev
Basic Usage Example
The dashboard is designed for zero-configuration. Upon launch, the Dashboard component initializes the Recharts engine to render the current day's energy profile.

JavaScript
// Example of the StatCard component used for PV metrics
<StatCard 
  title="Current Output" 
  value="5.8 kW" 
  Icon={Zap} 
/>
Configuration Options
Theme: The UI uses an "Amber/Slate" theme tailored for solar branding. Colors can be adjusted in tailwind.config.js.

Data Source: Currently utilizes a mock data array in App.jsx. This can be replaced with a fetch() call to a live IoT API.

Troubleshooting
Script Execution Error: If npm scripts fail on Windows, ensure you are using Command Prompt (cmd) instead of PowerShell, or update your system's Execution_Policy.

Styles not loading: The project uses a CDN-injected Tailwind link in index.html to ensure styling reliability in restricted environments.

Code Structure Overview
Plaintext
solar-toolkit/
├── src/
│   ├── App.jsx        # Main Dashboard logic and UI components
│   ├── index.css      # Tailwind directives and global styles
│   └── main.jsx       # React entry point
├── public/            # Static assets
├── index.html         # HTML template with Tailwind CDN
├── tailwind.config.js # Styling configuration
└── package.json       # Project dependencies and scripts

Contributing Guidelines
1.Fork the repository.
2.Create a feature branch (git checkout -b feature/NewSolarMetric).
3.Commit your changes.
4.Push to the branch and open a Pull Request.

License Information
Distributed under the MIT License. See LICENSE for more information.
