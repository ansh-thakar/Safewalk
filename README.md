# 🛡️ SafeWalk — AI-Powered Smart Personal Safety Platform

SafeWalk is a real-time personal safety application designed to keep pedestrians secure on every journey. It integrates **Geoapify Pedestrian Routing**, **Google Gemini AI**, and **Firebase Realtime Database** to provide dynamic safe-place rerouting, situational AI companion support, and an automated emergency SOS protocol.

---

## ✨ Key Features

* **🗺️ Pedestrian-Optimized Navigation:** Calculates walking paths using Geoapify GIS APIs, prioritizing well-lit avenues and verified pedestrian walkways.
* **🤖 Gemini AI Safety Companion:** Integrated chat router (`gemini-1.5-flash`) that evaluates user distress and provides real-time de-escalation and safety advice.
* **🏥 1-Tap Safe Place Discovery:** Instantly locates nearby police stations, 24/7 hospitals, open stores, petrol pumps, and transit hubs within a 5 km radius.
* **🚨 10-Second Fail-Safe SOS:** Automatic or manual countdown timer that broadcasts live GPS coordinates directly to emergency contacts and Firebase Realtime Database.
* **⚡ Sub-Second Synchronization:** Built on FastAPI and Firebase for instant distress signal routing and audit logging.

---

## 🛠️ Tech Stack

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Frontend** | React Native / Expo | Cross-platform mobile client for Android & iOS |
| **Backend API** | Python / FastAPI | Asynchronous API service |
| **AI Layer** | Google Gemini API | Real-time chat assistant & safety evaluation |
| **GIS & Maps** | Geoapify API & Leaflet | Geocoding, safe route calculations, & places discovery |
| **Database** | Firebase Realtime DB | Real-time emergency state sync & contact notifications |

---

## 📁 Repository Structure

```text
safewalk/
├── mobile/                   # React Native (Expo) Client
│   ├── assets/               # App icons & branding resources
│   ├── src/
│   │   ├── components/       # UI elements, buttons, & map views
│   │   ├── screens/          # Home, Navigation, AI Chat, & SOS screens
│   │   └── services/         # Firebase & backend API clients
│   └── App.js                # React Native entry point
│
├── backend/                  # FastAPI Application Service
│   ├── app/
│   │   ├── routes/
│   │   │   ├── chat.py       # Gemini AI router
│   │   │   ├── routes.py     # Geoapify route calculation
│   │   │   └── places.py     # Nearby safe-place lookup
│   │   └── main.py           # FastAPI app instance
│   └── requirements.txt      # Python dependencies
│
└── README.md
