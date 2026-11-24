# Workshop Management System (WMS)
> **Course:** CSE326 — Internet & Web Technologies  
> **Academic Task:** CA1 Project-Based Assessment  
> **Allocated Team:** Team 19  
> **Tech Stack:** 100% Pure Semantic HTML5 & Simple CSS3 (Zero JavaScript, Zero Frameworks)

---

## 👥 Team 19 Member Information

| Team Role | Member Name | Registration Number | Primary Viva Modules |
| :--- | :--- | :--- | :--- |
| **Team Leader** | **Harsimran Singh** | `12601847` | Core Architecture, Semantic HTML Skeleton, `:root` CSS Design Tokens, Operations Dashboard |
| **Member 2** | **Yuvraj** | `12601876` | Workshop Catalog & Cards, Registration Form, Form Validation, Schedule Timeline |
| **Member 3** | **Sakalabattula Pardhu** | `12625518` | Material Logistics Table, Attendance Tracking Roster, Certificate Preview, Feedback Collection |

---

## 📌 Assigned Problem Statement & Objectives

*Extracted directly from official course allocation `CSE326_MM_Team_Project_Allocation.xlsx` (Row 20, Team 19):*

* **Project Title:** Workshop Management System
* **Problem Statement:**  
  > *"Create a platform for managing workshop registrations, material requirements, attendance tracking, and certificate generation. Include features for feedback collection."*
* **Project Objective:**  
  > *"Develop a responsive web-based solution for workshop management system that organizes the required information, simplifies the main workflow, supports clear user actions, and provides useful status or summary views."*
* **Core Functional Requirements:**  
  - Responsive web interface
  - Structured forms for adding/updating records
  - Search, filtering, and categories where applicable
  - Status/progress tracking
  - Dashboard or summary view
  - Input validation and clear success/error messages

---

## 🚀 Live Demo & Repository Links

* **GitHub Repository:** [https://github.com/HarsimranSingh-dev/workshop-management-system](https://github.com/HarsimranSingh-dev/workshop-management-system)
* **GitHub Pages Live Deployment:** [https://harsimransingh-dev.github.io/workshop-management-system/](https://harsimransingh-dev.github.io/workshop-management-system/)

---

## 🧭 System Architecture & Sections

The project is structured into 8 clean, simple semantic sections:

1. **Operations Dashboard (`#dashboard`):** 4 key stat cards (Active Workshops, Registrations, Kits Dispatched, Attendance Rate), a seat capacity progress meter (`<progress>`), and session schedule.
2. **Workshop Catalog (`#workshops`):** Multi-track cards (Web Dev, Cloud, IoT, AI) displaying instructors, venues, timings, and seats left with a direct "Register" button.
3. **Participant Registration Form (`#registration`):** Structured form organized into two clean `<fieldset>`s (Student Information and Workshop/Kit Preference) with native HTML5 input validation (`required`, `pattern="[0-9]{8}"`).
4. **Material Requirements & Logistics (`#materials`):** Tabular overview of kit codes, material descriptions, allocation counts, and pickup desks, with a collapsible `<details>` prerequisites guide.
5. **Session Attendance Tracking (`#attendance`):** Live check-in log table showing student names, registration numbers, timestamps, status badges (`Present`, `Late`, `Absent`), and certificate clearance.
6. **Certificate Generation & Preview (`#certificates`):** Elegant completion certificate card featuring institutional header, student name, registration number, credential ID, and a print button.
7. **Participant Feedback & Evaluation (`#feedback`):** Star ratings, Net Promoter Score range slider, comment textarea, and benchmark summary scores.
8. **Academic Team 19 Information (`#team`):** Direct breakdown of team members, registration numbers, and individual responsibilities.

---

## 🎨 Clean & Vibrant Color Palette

- **Header Gradient:** Royal Blue (`linear-gradient(135deg, #1e40af, #2563eb)`) with a warm amber badge (`#fef3c7`)
- **Primary Buttons & Links:** Royal Blue (`#2563eb`) with darker hover state (`#1d4ed8`)
- **Success / Present:** Emerald Green (`#16a34a` / `#dcfce7`)
- **Warning / Waitlist:** Warm Amber (`#d97706` / `#fef3c7`)
- **Danger / Absent:** Red (`#dc2626` / `#fee2e2`)
- **Backgrounds:** Clean light slate page canvas (`#f8fafc`) with pure white card surfaces (`#ffffff`)

---

## 🎓 Quick Viva Guide for Team 19

### 1. Why pure HTML and CSS without JavaScript?
> "The CA1 assessment evaluates core web fundamentals. We used native HTML5 features (`pattern`, `required`, `<details>`, `<progress>`) and CSS3 Flexbox/Grid to deliver full functionality without external scripts or frameworks."

### 2. How did you structure the CSS?
> "All reusable colors, borders, and spacing are defined in `:root` variables at the top of `styles.css`. This makes theme adjustments instant and keeps the stylesheet clean and maintainable."

### 3. How does the responsive layout work?
> "We used CSS Grid with `repeat(auto-fit, minmax(...))` and Flexbox. On mobile screens (under 768px), grids collapse to a single column and tables scroll horizontally via `.table-wrap`, preventing horizontal page overflow."

### 4. How does the certificate print feature work?
> "We included an `@media print` rule in `styles.css` that hides the header, navigation, and other sections, isolating only the certificate card for clean printing on standard A4 paper."

---

## 📋 CA1 Mandatory Submission Form (UMS Reference)

| Field Name | Detail |
| :--- | :--- |
| **Project Name & Title** | Workshop Management System |
| **Team Name** | Team 19 |
| **Course Code** | CSE326 |
| **Registration Number(s)** | Reg. No. 1: `12601847` (Harsimran Singh)<br>Reg. No. 2: `12601876` (Yuvraj)<br>Reg. No. 3: `12625518` (Sakalabattula Pardhu) |
| **GitHub Link** | `https://github.com/HarsimranSingh-dev/workshop-management-system` |
| **Deployed Link** | `https://harsimransingh-dev.github.io/workshop-management-system/` |
| **Video Presentation Link** | *(Insert YouTube/Drive Link created by team)* |
