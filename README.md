<div align="center">

<br/>

```
 █████╗ ███╗   ██╗ █████╗ ████████╗ ██████╗      █████╗ ██╗
██╔══██╗████╗  ██║██╔══██╗╚══██╔══╝██╔═══██╗    ██╔══██╗██║
███████║██╔██╗ ██║███████║   ██║   ██║   ██║    ███████║██║
██╔══██║██║╚██╗██║██╔══██║   ██║   ██║   ██║    ██╔══██║██║
██║  ██║██║ ╚████║██║  ██║   ██║   ╚██████╔╝    ██║  ██║██║
╚═╝  ╚═╝╚═╝  ╚═══╝╚═╝  ╚═╝  ╚═╝    ╚═════╝     ╚═╝  ╚═╝╚═╝
```

### **3D Interactive Human Body · AI-Powered Pain Diagnosis · Smart Medical Triage**

<br/>

[![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev)
[![Three.js](https://img.shields.io/badge/Three.js-r158-000000?style=for-the-badge&logo=three.js&logoColor=white)](https://threejs.org)
[![Claude AI](https://img.shields.io/badge/Claude-API-D97706?style=for-the-badge&logo=anthropic&logoColor=white)](https://anthropic.com)
[![Node.js](https://img.shields.io/badge/Node.js-18+-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org)
[![Tailwind](https://img.shields.io/badge/Tailwind-CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)](https://tailwindcss.com)
[![License](https://img.shields.io/badge/License-MIT-8B5CF6?style=for-the-badge)](LICENSE)

<br/>

> *Hover over a body part. Describe your pain. Get AI-powered medical guidance instantly.*

<br/>

---

</div>

## 🫀 What is AnatoAI?

**AnatoAI** is a full-stack web application that combines an interactive **3D human body model** with an **AI-powered medical symptom analysis engine**. Users can click on any region of a realistic 3D body, describe their pain type and severity, and receive structured medical guidance — including home remedies, medication suggestions, and intelligent triage recommendations.

Built for patients, caregivers, and the medically curious — AnatoAI bridges the gap between "I wonder what this pain means" and "I need to see a doctor *right now*."

> ⚠️ **Medical Disclaimer:** AnatoAI is an educational tool only. It does not replace professional medical advice. Always consult a qualified healthcare provider for serious or persistent symptoms.

<br/>

---

## ✨ Features

| Feature | Description |
|---|---|
| 🫁 **Interactive 3D Body** | Full human model with hover highlighting across 24+ body regions |
| 🖱️ **Click-to-Diagnose** | Click any body part to open the anatomy analysis panel |
| 🔬 **Anatomy Details** | View muscles, bones, and nerves for each region |
| 🩺 **Pain Profiling** | Select pain type, duration, and severity (1–10 scale) |
| 🤖 **AI Analysis** | Claude API analyzes symptoms and returns structured medical guidance |
| 🟢🟡🔴 **Smart Triage** | LOW / MODERATE / HIGH / EMERGENCY urgency classification |
| 🚨 **Emergency Alerts** | Full-screen overlay for life-threatening symptoms — calls emergency services |
| 📋 **Symptom History** | Session log of all checked symptoms to share with your doctor |
| 🌗 **Dark / Light Mode** | Clinical dark mode default, toggle to light |
| 📱 **Fully Responsive** | Works on desktop, tablet, and mobile |

<br/>

---

## 🎬 Demo

```
Coming soon — screenshots and live demo link
```

> **Live Demo:** `https://anatai.vercel.app` *(deploy yours and update this link)*

<br/>

---

## 🛠️ Tech Stack

```
Frontend          Backend           AI & 3D
─────────         ──────────        ──────────────────
React 18          Node.js 18+       Anthropic Claude API
Vite              Express.js        Three.js r158
Tailwind CSS      REST API          React Three Fiber
Framer Motion     dotenv            @react-three/drei
Axios             CORS              GLTF/GLB Model
Lucide React                        Raycasting (hover)
```

<br/>

---

## 📁 Project Structure

```
anatai/
│
├── client/                          ← React Frontend
│   ├── public/
│   │   └── models/
│   │       └── human_body.glb       ← 3D model (you provide)
│   │
│   └── src/
│       ├── components/
│       │   ├── Scene3D.jsx           ← Three.js canvas, lights, camera
│       │   ├── HumanModel.jsx        ← GLB loader + hover/click detection
│       │   ├── AnatomyPopup.jsx      ← Slide-in analysis panel
│       │   ├── PainSelector.jsx      ← Pain type, duration, severity inputs
│       │   ├── AIResult.jsx          ← AI response display + triage UI
│       │   ├── EmergencyOverlay.jsx  ← Full-screen emergency alert
│       │   ├── Navbar.jsx            ← Top navigation bar
│       │   └── SymptomHistory.jsx    ← Session symptom log drawer
│       │
│       ├── hooks/
│       │   ├── useBodyHover.js       ← Raycasting hover logic
│       │   └── useAIAnalysis.js      ← API call + response state
│       │
│       ├── data/
│       │   └── bodyParts.js          ← Body part metadata & anatomy info
│       │
│       ├── App.jsx
│       ├── main.jsx
│       └── index.css
│
├── server/                          ← Node.js Backend
│   ├── routes/
│   │   └── analyze.js               ← POST /api/analyze endpoint
│   ├── index.js                     ← Express entry point
│   ├── .env                         ← ANTHROPIC_API_KEY (never commit)
│   └── package.json
│
├── .gitignore
├── README.md
└── LICENSE
```

<br/>

---

## 🚀 Getting Started

### Prerequisites

- Node.js `v18+`
- npm `v9+`
- An [Anthropic API key](https://console.anthropic.com)
- A GLB human body 3D model (see [Getting the 3D Model](#-getting-the-3d-model))

---

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/anatai.git
cd anatai
```

---

### 2. Set Up the Backend

```bash
cd server
npm install
```

Create your environment file:

```bash
cp .env.example .env
```

Edit `.env`:

```env
ANTHROPIC_API_KEY=your_api_key_here
PORT=3001
```

Start the server:

```bash
node index.js
# Server running at http://localhost:3001
```

---

### 3. Set Up the Frontend

```bash
cd client
npm install
```

Create your environment file:

```bash
cp .env.example .env
```

Edit `.env`:

```env
VITE_API_URL=http://localhost:3001
```

Start the dev server:

```bash
npm run dev
# App running at http://localhost:5173
```

---

### 4. Run Both Simultaneously

From the project root, install `concurrently` and run:

```bash
npm install -g concurrently
concurrently "cd server && node index.js" "cd client && npm run dev"
```

<br/>

---

## 🧍 Getting the 3D Model

AnatoAI requires a **GLTF/GLB human body model** where each body part is a **separately named mesh**. The hover and click detection works by identifying which named mesh the mouse ray intersects.

### Required Mesh Names

| Region | Mesh Name | Region | Mesh Name |
|---|---|---|---|
| Head | `head` | Upper Back | `upper_back` |
| Neck | `neck` | Lower Back | `lower_back` |
| Left Shoulder | `left_shoulder` | Chest | `chest` |
| Right Shoulder | `right_shoulder` | Abdomen (Upper) | `abdomen_upper` |
| Left Upper Arm | `left_upper_arm` | Abdomen (Lower) | `abdomen_lower` |
| Right Upper Arm | `right_upper_arm` | Left Hip | `left_hip` |
| Left Forearm | `left_forearm` | Right Hip | `right_hip` |
| Right Forearm | `right_forearm` | Left Thigh | `left_thigh` |
| Left Hand | `left_hand` | Right Thigh | `right_thigh` |
| Right Hand | `right_hand` | Left Knee | `left_knee` |
| Left Lower Leg | `left_lower_leg` | Right Knee | `right_knee` |
| Left Foot | `left_foot` | Right Lower Leg | `right_lower_leg` |
| Pelvis | `pelvis` | Right Foot | `right_foot` |

### Where to Find Models

| Source | Cost | Notes |
|---|---|---|
| [Sketchfab](https://sketchfab.com) | Free / Paid | Search "human body anatomy low poly GLB" |
| [BodyParts3D](https://lifesciencedb.jp/bp3d/) | Free | OBJ format — convert to GLB via Blender |
| [TurboSquid](https://turbosquid.com) | Paid | Premium quality, pre-labeled |
| [CGTrader](https://cgtrader.com) | Paid | Wide selection |

> 💡 **Tip:** After downloading, use **Blender** to rename each mesh to match the table above, then export as `.glb`. Place the final file at `client/public/models/human_body.glb`.

<br/>

---

## 🤖 AI Analysis System

### How It Works

1. User clicks a body region on the 3D model
2. A popup panel opens with anatomy details
3. User selects: **pain type**, **duration**, **severity (1–10)**, and optional notes
4. Frontend sends a POST request to `/api/analyze`
5. Backend constructs a structured prompt and calls the **Claude API**
6. Claude returns a JSON response with medical guidance
7. Frontend renders the response with color-coded urgency levels

### Response Schema

```json
{
  "urgency": "LOW | MODERATE | HIGH | EMERGENCY",
  "urgencyReason": "string",
  "possibleCauses": [
    { "name": "string", "description": "string", "likelihood": "string" }
  ],
  "homeRemedies": [
    { "title": "string", "instruction": "string", "icon": "string" }
  ],
  "medications": [
    { "name": "string", "type": "string", "dosage": "string", "warning": "string" }
  ],
  "whenToSeeDoctor": "string",
  "timeframeToImprove": "string",
  "redFlags": ["string"],
  "emergencySymptoms": ["string"],
  "disclaimer": "string"
}
```

### Urgency Levels

| Level | Color | Meaning |
|---|---|---|
| 🟢 LOW | Green | Home remedies likely sufficient |
| 🟡 MODERATE | Amber | Monitor closely; see doctor if no improvement |
| 🔴 HIGH | Red | See a doctor soon |
| 🚨 EMERGENCY | Pulsing Red | Call emergency services immediately |

> **Emergency Trigger Logic:** Automatically activates when `severity >= 8` OR when red-flag symptoms are detected (e.g., chest pain + left arm, sudden vision loss, difficulty breathing).

<br/>

---

## 🩺 Supported Pain Types

| Pain Type | Common Associations |
|---|---|
| Sharp / Stabbing | Fracture, appendicitis, cardiac event |
| Dull / Aching | Muscle strain, arthritis, chronic injury |
| Burning | Neuropathy, GERD, shingles |
| Throbbing | Infection, abscess, migraine, DVT |
| Cramping | GI distress, muscle fatigue, ectopic pregnancy |
| Tingling / Numbness | Carpal tunnel, herniated disc, stroke |

<br/>

---

## ☁️ Deployment

### Frontend → Vercel

```bash
# Push to GitHub, then:
# 1. Go to vercel.com → Import Repository
# 2. Set root directory: client/
# 3. Add environment variable: VITE_API_URL=<your-backend-url>
# 4. Deploy
```

### Backend → Railway

```bash
# 1. Go to railway.app → New Project → GitHub Repo
# 2. Set root directory: server/
# 3. Add environment variable: ANTHROPIC_API_KEY=<your-key>
# 4. Railway auto-detects Node.js and deploys
# 5. Copy the generated URL → paste into Vercel as VITE_API_URL
```

<br/>

---

## 🗺️ Roadmap

- [x] Core 3D scene with hover detection
- [x] Anatomy popup with pain selector
- [x] Claude AI integration
- [x] Urgency triage + emergency overlay
- [x] Symptom history per session
- [ ] Front and back body view toggle
- [ ] Skeletal / muscular layer switching
- [ ] Voice symptom input
- [ ] Symptom report PDF export
- [ ] Multi-language support (Hindi, Bengali, Spanish, Arabic)
- [ ] Nearby doctor finder integration
- [ ] User accounts + symptom history
- [ ] Pediatric mode (child-specific model)
- [ ] Wearable data import (Apple Health / Google Fit)

<br/>

---

## 🤝 Contributing

Contributions are welcome! Here's how to get started:

```bash
# 1. Fork the repository
# 2. Create your feature branch
git checkout -b feature/your-feature-name

# 3. Commit your changes
git commit -m "feat: add your feature"

# 4. Push to the branch
git push origin feature/your-feature-name

# 5. Open a Pull Request
```

Please follow the existing code style and include descriptive PR descriptions.

<br/>

---

## ⚠️ Security & Legal

- **Never commit your `.env` file.** It is in `.gitignore` for a reason. Rotate your Anthropic key if accidentally exposed.
- **3D Model Licensing.** Ensure any model you use permits commercial or public web use. Check for Creative Commons or MIT licenses.
- **User Data Privacy.** Do not store symptom data without a Privacy Policy and explicit user consent. Symptoms are protected health information.
- **Not a Medical Device.** AnatoAI has not been reviewed or approved by any medical regulatory body (FDA, CDSCO, etc.). It must not be used for clinical decision-making.

<br/>

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for more information.

<br/>

---

<div align="center">

**Built with** React · Three.js · Claude AI · Node.js · Tailwind CSS

<br/>

*AnatoAI — Know your body. Understand your pain.*

</div>
