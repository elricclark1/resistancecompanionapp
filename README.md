# 🚀 Quick Start & Local Execution

**Live Demo:** [https://resistancecompanion.serpilas.com](https://resistancecompanion.serpilas.com)

To run this application locally immediately:

```bash
# 1. Clone or navigate to the directory
cd resistancecompanionapp

# 2. Install dependencies
pip install -r requirements.txt

# 3. Start development server
python app.py
```

# Resistance Companion App

A real-time, local-network web application for the board game "The Resistance". This app allows players to use their smartphones as controllers, automating role distribution, voting, and mission tracking while eliminating the need for physical cards.

## 🎮 How to Play

1. **Lobby:** Players join by entering their names. Once at least 5 players are ready, the game starts and roles are secretly assigned.
2. **Role Reveal:** Use the "Press and Hold" button on your screen to see if you are **Resistance** or a **Spy**.
3. **Team Building:** The designated Leader selects a team for the current mission based on the required size shown on the screen.
4. **Voting:** All players vote "Approve" or "Reject" on the proposed team.
5. **Missions:** If a team is approved, members secretly vote "Success" or "Fail".
6. **Winning:** The Resistance wins by succeeding in 3 missions. The Spies win if 3 missions fail or if 5 teams are rejected in a single round.

## ✨ Tech Stack

- **Backend:** Python (Flask), Flask-SocketIO for real-time state synchronization.
- **Frontend:** Vanilla JavaScript and CSS (Single Page Application).
- **Network:** Binds to `0.0.0.0:5000` to allow LAN access.

## ⚡ Application Features

- **Local Network Play:** Optimized for LAN environments, accessible via QR code.
- **Real-time Sync:** Uses WebSockets for instant updates across all devices.
- **Secure Role Reveal:** "Press and hold" mechanic to prevent screen peeking.
- **Automated Rules:** Handles role distribution and mission sizes for 5-10 players.
- **Mission History:** Tracks results, team composition, and vote counts for every round.
- **Special Rule Support:** Automatically enforces the "2 fails required" rule for Mission 4 in large games.
- **Session Persistence:** Allows players to reconnect with the same name if their browser refreshes.

## 🐳 Deployment & Containerization

This application is fully containerized. To build and run with Docker Compose:

```bash
# Build and run containers
docker compose up -d --build
```
The application will be exposed on host port `3013`.

## 🛡️ Serpilas Brand Mission

This application adheres to the core Serpilas mission pillars:
1. **Ad-Free Experience:** UI is entirely clean, clutter-free, and optimized purely for utility.
2. **Open Source:** Public, collaborative repository.
3. **Account-Free:** No signup or login required to play.
4. **Zero Data Monetization:** Local network privacy with zero tracking cookies or profiling.

---
*Created/vibe coded by Elric at Serpilas. Learn more about our mission at serpilas.com/.*

For questions or feedback, contact: elric.projects@gmail.com
