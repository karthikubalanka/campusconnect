# CampusConnect 🎓
### Smart College Management & Student Communication Platform
> **“Connecting Students, Faculty & Campus — All in One Place.”**

Designed and engineered for **BVC Engineering College** as a modern, responsive Flutter Web mini project for the **Department of Computer Science & Engineering**.

---

## 📌 Problem Statement
Traditional higher education institutions often suffer from fragmented communication channels: notices posted on physical bulletin boards, timetables circulated via unofficial chat groups, attendance tracked on offline registers, and assignment deadlines communicated verbally. This lack of centralized infrastructure causes missed deadlines, attendance shortages, and communication delays between students and professors.

---

## 🎯 Objectives
- **Centralized Academic Hub**: Provide students with an intuitive, unified dashboard displaying timetable schedules, announcements, assignments, and examination dates.
- **Transparent Attendance Tracking**: Real-time attendance percentage breakdown per subject with automatic calculation of safe bunk limits and mandatory 75% university eligibility criteria.
- **Paperless Workflow**: Allow students to submit project reports and assignments digitally with instant state updates.
- **Direct Faculty Interaction**: Bridge the communication gap between faculty members and students through integrated instant messaging.
- **Demonstration Ready**: Engineered with realistic mock data and clean architecture, enabling local demonstration without external backend dependencies, while structured for seamless Firebase/REST API integration.

---

## 🚀 Key Features & Screen Walkthrough

| # | Screen | Description |
|---|---|---|
| 1 | **Splash Screen** | Animated logo emblem, institutional branding (*BVC Engineering College*), tagline, loading progress indicator, and auto-navigation to login. |
| 2 | **Login Page** | Responsive SaaS login with form validation, password visibility toggle, forgot password flow, and a **One-Click Demo Login** button with preset credentials. |
| 3 | **Student Dashboard** | Personalized greeting (`Good Morning, Karthik 👋`), 4 high-level stat cards (Attendance 85%, Assignments 4 Pending, Announcements 6 New, Upcoming Exams 3), Today's Timetable schedule, recent announcements feed, upcoming assignment deadlines, and attendance circular gauge + weekly trend bar chart. |
| 4 | **Announcements Page** | College notice board with categories (`Academic`, `Events`, `Placement`, `General`, `Important`), full-text search, category filter chips, and a detailed "Read More" modal dialog. |
| 5 | **Attendance Page** | Overall attendance gauge (85%), university 75% rule indicators, subject-by-subject attendance cards with visual progress bars (Green ≥85%, Orange 75–84%, Red <75%), safe bunks calculator, and a responsive Card/Table view toggle. |
| 6 | **Timetable Page** | Weekly schedule navigation (`Monday` to `Saturday`), lecture timing badges, room allocations (e.g. *Room 204*, *Computing Lab 3*), faculty details, and current active session highlights. |
| 7 | **Assignments Page** | Digital assignment tracker with filter chips (`All`, `Pending`, `Submitted`, `Overdue`), search bar, status distribution progress bar, and an interactive **Submit** workflow that turns in files and triggers instant SnackBar feedback. |
| 8 | **Exams Page** | Upcoming examination timetable (Internal Assessment - 1), countdown timer block for the nearest examination (days & hours remaining), syllabus unit specifications, and a digital **Hall Ticket download** dialog. |
| 9 | **Notifications Page** | Centralized notification center with `Unread` and `Read` filter tabs, category icons, "Mark as Read" action, "Mark All as Read" batch action, and deep links to relevant screens. |
| 10 | **Messages / Chat Page** | Interactive student-faculty communication interface featuring a faculty directory (*Dr. Ramesh*, *Prof. Anitha*, *Mr. Kumar*, *Placement Officer*), live chat bubbles, and simulated automated faculty replies after 1.2 seconds for realistic presentation. |
| 11 | **Student Profile Page** | Comprehensive student identity card displaying Karthik's academic profile (CGPA 8.72, 112 Credits, Roll No: `21BVC05A12`), contact details, and an interactive **Edit Profile** dialog that updates profile state in real-time. |
| 12 | **Settings Page** | Live **Dark Mode toggle** that dynamically switches the entire application between Slate Dark and Crisp Light themes, notification preferences (Push, Email, SMS), language selector, password change dialog, and secure logout. |

---

## 🛠️ Technology Stack

- **Language**: Dart (SDK ^3.12.2)
- **Framework**: Flutter (v3.44.6 Web)
- **Design System**: Material Design 3 (Material 3)
- **Typography**: Google Fonts (Inter)
- **Architecture**: Clean Model-View-State separation with `InheritedNotifier` (`AppState`)
- **Supported Platforms**: Chrome, Edge, Safari, Firefox (Desktop, Tablet, & Mobile browsers)

---

## 📂 Project Structure

```
lib/
├── main.dart                      # App entry point, authentication guards & routes
├── models/
│   ├── student.dart               # Student profile model with copyWith
│   ├── announcement.dart          # Announcement model & category enum
│   ├── attendance.dart            # Attendance model & calculation logic
│   ├── assignment.dart            # Assignment model & status enums
│   ├── exam.dart                  # Examination model & countdown helpers
│   ├── notification.dart          # Notification model & type enums
│   ├── message.dart               # Faculty and ChatMessage models
│   └── timetable.dart             # Timetable slot model
├── data/
│   ├── mock_data.dart             # Realistic sample college data for Karthik
│   └── app_state.dart             # Centralized ChangeNotifier reactive state
├── screens/
│   ├── splash_screen.dart         # 1. Animated Splash Screen
│   ├── login_screen.dart          # 2. Responsive Login & Demo Credentials
│   ├── dashboard_screen.dart      # 3. Main Student Dashboard
│   ├── announcements_screen.dart  # 4. Filterable Announcements
│   ├── attendance_screen.dart     # 5. Subject Attendance & Calculator
│   ├── timetable_screen.dart      # 6. Weekly Schedule & Day Tabs
│   ├── assignments_screen.dart    # 7. Assignment Submission & Tracker
│   ├── exams_screen.dart          # 8. Exam Schedule & Live Countdown
│   ├── notifications_screen.dart  # 9. Notification Center
│   ├── messages_screen.dart       # 10. Student-Faculty Messaging Demo
│   ├── profile_screen.dart        # 11. Student Profile & Local Editing
│   └── settings_screen.dart       # 12. Dark Mode & System Preferences
├── widgets/
│   ├── app_scaffold.dart          # Responsive shell (Desktop sidebar / Mobile drawer)
│   ├── sidebar.dart               # Nav sidebar, badges, tooltips & AppScope
│   ├── top_bar.dart               # Global search, theme toggle & user dropdown
│   ├── stat_card.dart             # Metric cards with hover animations
│   ├── announcement_card.dart     # Category badge card & Read More modal
│   ├── attendance_card.dart       # Color-coded progress card (Green/Orange/Red)
│   ├── assignment_card.dart       # Assignment submission card & detail modal
│   ├── notification_card.dart     # Unread indicator & action card
│   ├── timetable_card.dart        # Schedule period card with active highlight
│   └── chart_widgets.dart         # Circular gauge & weekly trend bar charts
├── theme/
│   └── app_theme.dart             # Modern Light and Dark theme configurations
└── utils/
    └── constants.dart             # Routes, colors, breakpoints & sample credentials
```

---

## 🔑 Demo Credentials

CampusConnect features both **Student Portal** and **Teacher / Faculty Portal** with one-click demo login buttons:

### 🎓 1. Student Portal (Karthik)
- **Select Role**: `Student` Tab
- **Student ID**: `student123`
- **Password**: `123456`
- **Portal Access**: Personal dashboard, attendance tracker (85%), timetable, assignments submission, upcoming exams countdown, notifications, and direct chat with faculty.

### 👨‍🏫 2. Teacher / Faculty Portal (Dr. Ramesh — HOD CSE)
- **Select Role**: `Teacher / Faculty` Tab
- **Faculty ID**: `faculty123`
- **Password**: `123456`
- **Portal Access**: Teaching schedule today, class attendance marker, assignment grading & feedback tool, department notice publisher (broadcasts to student notice board & triggers instant alerts), and student inquiry inbox.

*(Any non-empty ID and password also simulates a successful login for flexible demonstration)*

---

## 💻 How to Run

### Prerequisites
- [Flutter SDK](https://docs.flutter.dev/get-started/install) (v3.0.0 or higher)
- Google Chrome or any modern web browser

### 1. Install Dependencies
```bash
flutter pub get
```

### 2. Run on Chrome
```bash
flutter run -d chrome
```

### 3. Build for Production Web Deployment
```bash
flutter build web
```
The optimized production web artifacts will be generated in `build/web/`, ready to be hosted on Firebase Hosting, GitHub Pages, Vercel, or Netlify.

---

## 🔮 Future Enhancements
The codebase is intentionally decoupled to allow rapid extension for production deployment:
1. **Firebase Authentication**: Integration with Google Sign-In and institutional Microsoft 365 OAuth.
2. **Cloud Firestore**: Real-time synchronization of college notices, attendance records, and submissions.
3. **Faculty & Admin Dashboards**: Dedicated portals for professors to upload marks, post circulars, and mark attendance.
4. **WebSocket / Firebase Chat**: Real-time peer-to-peer and broadcast messaging between classes and mentors.
5. **AI Campus Assistant**: An integrated generative AI assistant for student inquiry answering, syllabus doubt clarification, and timetable reminders.
6. **College ERP Integration**: Direct synchronization with university student management databases.
