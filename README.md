# Sea Eyes Control Room – Web-Based Vessel Monitoring System

**Sea Eyes Control Room** is a centralized web interface designed to monitor real-time sensor data from vessels equipped with the Sea Eyes system. It supports fleet-level navigation safety by visualizing GPS locations, radar data, and proximity alerts through a cloud-based dashboard.

## 🌐 Overview

Built for port authorities, coast guard teams, and maritime supervisors, the Control Room provides an aerial view of all active boats and their sensor statuses. It connects to Firebase Realtime Database and updates in real time without refresh.

## ⚙️ Features

- **Real-Time Fleet Map**  
  Track GPS location of multiple vessels on a live map using unique IDs.

- **Radar + Sensor Monitoring**  
  Visual display of lidar radar sweeps and ultrasonic readings per boat.

- **Multi-Vessel Support**  
  Switch between boats using their device IDs to monitor specific units.

- **Danger Alerts**  
  View proximity alerts triggered by ultrasonic/sonar sensor thresholds (orange/red zones).

- **Cloud Synced**  
  Integrated with Firebase Realtime Database for instant updates from the field.

- **Scalable Design**  
  Built for future expansion — including remote control, boat status logs, and live camera feeds.

## 🖥️ Tech Stack

- **Frontend:** React.js / HTML / JavaScript
- **Backend:** Firebase Realtime Database
- **Map:** Leaflet.js / Google Maps API
- **Auth (Optional):** Firebase Auth

## 🗂️ Firebase Data Structure (Sample)

```json
{
  "boats": {
    "device123": {
      "gps": { "lat": 31.1234, "lon": 29.9876 },
      "ultrasonic": {
        "front": 40,
        "left": 35,
        "right": 50,
        "back": 45
      },
      "lidar": {
        "angle_0": 250,
        "angle_10": 240,
        ...
      }
    },
    "device456": {
      ...
    }
  }
}
📦 Setup Instructions
Clone the repository:

bash
Copy
Edit
git clone https://github.com/yourusername/sea-eyes-control-room.git
cd sea-eyes-control-room
Install dependencies:

bash
Copy
Edit
npm install
Set up Firebase config:

Add your Firebase project configuration in firebaseConfig.js

Ensure Realtime Database rules allow read access (or use Auth if needed)

Run the development server:

bash
Copy
Edit
npm start
Open http://localhost:3000 to view the dashboard.

📸 Screenshots
<!-- Add screenshots of the map view, radar, and alerts panel -->
Fleet Map	Radar Display	Sensor Table

📍 Roadmap
 Multi-vessel GPS tracking

 Live sensor data visualization

 Radar chart per vessel

 Firebase Auth integration

 Central alert system

 Boat command/control API

🧑‍💻 Author
Mohamed Fath Elbab
Behance
