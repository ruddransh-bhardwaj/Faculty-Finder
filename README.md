# 🎓 Faculty Finder Pro (FFCS Edition)

> **Eliminating the endless wait outside faculty cabins through Smart OCR Matrix Matching & Live Status Tracking.**

<img width="1200" height="700" alt="Screenshot 2026-07-31 at 4 30 17 AM" src="https://github.com/user-attachments/assets/2052195a-06df-40f3-92d3-8f0f3f3fe315" />
<!-- Replace this link with an actual screenshot of your project -->

## 💡 The Problem
In large universities (like VIT with the FFCS system), students often waste hours waiting outside faculty cabins because they don't know when the professor is free, or if they are currently in class. Manually cross-checking a student's timetable with a faculty's timetable to find a mutual free slot is tedious, error-prone, and frustrating.

## 🚀 The Solution
**Faculty Finder Pro** is a smart academic scheduling portal. By utilizing advanced Client-Side OCR, the system automatically reads a screenshot of the student's/faculty's FFCS timetable, maps the exact slot codes (e.g., `A11`, `B12`, `L1`), and instantly algorithmically determines the absolute closest mutual free time for an appointment.

## ✨ Key Features
*   🤖 **Smart FFCS OCR Engine:** Upload a screenshot of your timetable. The system uses a Fuzzy Logic OCR Fixer (powered by Tesseract.js) to accurately extract standard slot codes and automatically populate your busy slots in a visual matrix.
*   ⚡ **Instant Mutual Free-Time Matcher:** Select a faculty member, and the algorithm compares both matrices in real-time to suggest the nearest overlapping free slot.
*   📍 **Live Location & Status Ping:** Faculty can toggle their status in real-time (e.g., `🟢 Available in Cabin A-102` vs `🔴 In Class - Room 204`).
*   📅 **One-Click Appointment Booking:** Students can request meetings for mutual free slots with a specified purpose.
*   📊 **Role-Based Dashboards:** Distinct, intuitive portals for Students (to find & book) and Faculty (to manage requests and override schedules).
*   📥 **Calendar Integration:** Export confirmed appointments directly as `.ics` files to add to Google/Apple Calendar.

## 🛠️ Tech Stack
This prototype was built specifically for speed, accessibility, and zero-latency client-side processing:
*   **Frontend:** HTML5, Vanilla JavaScript, CSS3 (Custom Minimalist Glassmorphism UI).
*   **AI / Computer Vision:** `Tesseract.js` (for entirely client-side Optical Character Recognition).
*   **Database:** HTML5 `LocalStorage` (implemented as a fully functional mock-DB for instant hackathon demonstration without backend setup).

## 🧠 How the Smart Match Works (Architecture)
1. **The Grid:** We mapped the standard 6-day, 8-slot university schedule to an exact matrix of slot names (e.g., `Tuesday Slot 1 = B11 / L7`).
2. **The Extraction:** Tesseract reads the uploaded image text. Our custom regex engine cleans the text (fixing common OCR errors like `"A ll"` to `"A11"`).
3. **The Matrix Intersection:** The parsed codes are checked against the Grid. If a match is found, the slot is marked `BUSY`. 
4. **The Match:** When booking, the algorithm performs a `StudentMatrix AND FacultyMatrix` logic check to output an array of purely free slots, ignoring anything already marked as an approved appointment.

## ⚙️ Installation & Usage
Because this project utilizes a client-side architecture and LocalStorage, **there are zero backend dependencies.** 

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/ruddransh-bhardwaj/THE-FLATMATES---Jay-Modha-Jitendra.git](https://github.com/ruddransh-bhardwaj/THE-FLATMATES---Jay-Modha-Jitendra.git)
