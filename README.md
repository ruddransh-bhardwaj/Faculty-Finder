🎓 Faculty Finder Pro (FFCS Edition)
Eliminating the endless wait outside faculty cabins through Smart OCR Matrix Matching & Live Status Tracking.

💡 The Problem
In large universities (like VIT with the FFCS system), students often waste hours waiting outside faculty cabins because they don't know when the professor is free, or if they are currently in class. Manually cross-checking a student's timetable with a faculty's timetable to find a mutual free slot is tedious, error-prone, and frustrating.

🚀 The Solution
Faculty Finder Pro is a smart academic scheduling portal. By utilizing advanced Client-Side OCR, the system automatically reads a screenshot of the student's/faculty's FFCS timetable, maps the exact slot codes (e.g., A11, B12, L1), and instantly algorithmically determines the absolute closest mutual free time for an appointment.

✨ Key Features
🤖 Smart FFCS OCR Engine: Upload a screenshot of your timetable. The system uses a Fuzzy Logic OCR Fixer (powered by Tesseract.js) to accurately extract standard slot codes and automatically populate your busy slots in a visual matrix.

⚡ Instant Mutual Free-Time Matcher: Select a faculty member, and the algorithm compares both matrices in real-time to suggest the nearest overlapping free slot.

📍 Live Location & Status Ping: Faculty can toggle their status in real-time (e.g., 🟢 Available in Cabin A-102 vs 🔴 In Class - Room 204).

📅 One-Click Appointment Booking: Students can request meetings for mutual free slots with a specified purpose.

📊 Role-Based Dashboards: Distinct, intuitive portals for Students (to find & book) and Faculty (to manage requests and override schedules).

📥 Calendar Integration: Export confirmed appointments directly as .ics files to add to Google/Apple Calendar.

🛠️ Tech Stack
This prototype was built specifically for speed, accessibility, and zero-latency client-side processing:

Frontend: HTML5, Vanilla JavaScript, CSS3 (Custom Minimalist Glassmorphism UI).

AI / Computer Vision: Tesseract.js (for entirely client-side Optical Character Recognition).

Database: HTML5 LocalStorage (implemented as a fully functional mock-DB for instant hackathon demonstration without backend setup).

🧠 How the Smart Match Works (Architecture)
The Grid: We mapped the standard 6-day, 8-slot university schedule to an exact matrix of slot names (e.g., Tuesday Slot 1 = B11 / L7).

The Extraction: Tesseract reads the uploaded image text. Our custom regex engine cleans the text (fixing common OCR errors like "A ll" to "A11").

The Matrix Intersection: The parsed codes are checked against the Grid. If a match is found, the slot is marked BUSY.

The Match: When booking, the algorithm performs a StudentMatrix AND FacultyMatrix logic check to output an array of purely free slots, ignoring anything already marked as an approved appointment.

⚙️ Installation & Usage
Because this project utilizes a client-side architecture and LocalStorage, there are zero backend dependencies.

Clone the repository:

Bash
git clone https://github.com/YourUsername/faculty-finder-pro.git
Navigate to the directory:

Bash
cd faculty-finder-pro
Run the app:
Simply double-click the index.html file to open it in any modern web browser (Chrome, Edge, Safari, Firefox).
(Optional: You can also use VS Code's "Live Server" extension for a better experience).

🧪 How to test it during the Hackathon:
Open the app and select Faculty.

Login with ID: EMP001 and any Name (e.g., "Dr. Anjali"). You will see a pre-populated schedule.

Open a new tab, select Student, and login with a dummy ID (e.g., 24BCE10001).

Upload a sample FFCS timetable screenshot in the Student dashboard.

Go to Home, Search for "Anjali", and click Run Smart FFCS Match!

🔮 Future Scope (Post-Hackathon)
Backend Integration: Migrate LocalStorage to a scalable backend (Node.js/Express + MongoDB/PostgreSQL).

Hardware Integration: Integrate RFID/Biometric sensors at cabin doors to automatically toggle the Faculty's "Live Status" without manual clicking.

Email & SMS Alerts: Automated notifications when an appointment is approved or rescheduled.

👨‍💻 Team

Jay Modha - Team Lead - https://www.linkedin.com/in/jay-modha-5a9904376/ 
Ruddransh Bhardwaj - Full Stack Developer / UI-UX - Linkedin -https://www.linkedin.com/in/ruddransh-bhardwaj/ 
Yash Sharma -  - https://www.linkedin.com/in/yash-vashisth-8609b1341/ 
Aditya Raj - Contributor - https://www.linkedin.com/in/aditya-jha-684b32324/ 
Deep Jaiswal - Contributor - https://www.linkedin.com/in/deep-jaiswal-0996a3383/ 

Built with ❤️ at [Summer of CodeFest 2.0 / 2026]
