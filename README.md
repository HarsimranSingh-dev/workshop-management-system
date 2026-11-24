# Workshop Management System (WMS)
> **Course:** CSE326 — Internet & Web Technologies  
> **Academic Task:** CA1 Project-Based Assessment  
> **Allocated Team:** Team 19  
> **Tech Stack:** 100% Pure HTML5 & CSS3 (Zero JavaScript, Zero Frameworks)

---

## 1. Project Overview & Problem Statement

*Extracted directly from the official university allocation sheet `CSE326_MM_Team_Project_Allocation.xlsx` (Row 20, Team 19):*

* **Assigned Project Title:** Workshop Management System
* **Problem Statement:**  
  > *"Create a platform for managing workshop registrations, material requirements, attendance tracking, and certificate generation. Include features for feedback collection."*
* **Project Objective:**  
  > *"Develop a responsive web-based solution for workshop management system that organizes the required information, simplifies the main workflow, supports clear user actions, and provides useful status or summary views."*
* **Core Requirements Fulfilled:**
  - Responsive web interface (desktop, tablet, mobile)
  - Structured forms for adding and updating records with validation
  - Workshop catalog with dates, venues, instructors, and seat availability
  - Material requirements and inventory distribution tracking
  - Session attendance tracking roster with status badges
  - Official certificate generation and preview layout
  - Participant feedback collection form
  - Dashboard and summary metrics

---

## 2. Team 19 Roster & Academic Details

| Role | Student Name | Registration Number | Module Responsibilities |
| :--- | :--- | :--- | :--- |
| **Team Leader** | **Harsimran Singh** | `12601847` | Overall project architecture, semantic HTML structure, CSS styling, dashboard and metrics |
| **Team Member** | **Yuvraj** | `12601876` | Workshop catalog table, participant registration form, input validations |
| **Team Member** | **Sakalabattula Pardhu** | `12625518` | Material requirements table, attendance tracking roster, certificate preview, feedback form |

---

## 3. Live Project Links

* **GitHub Repository:** [https://github.com/HarsimranSingh-dev/workshop-management-system](https://github.com/HarsimranSingh-dev/workshop-management-system)
* **Live Deployment (GitHub Pages):** [https://harsimransingh-dev.github.io/workshop-management-system/](https://harsimransingh-dev.github.io/workshop-management-system/)

---

## 4. How Every Feature Works

The portal is organized into 8 functional sections:

### 1. Operations Dashboard (`#dashboard`)
- **Summary Metrics:** 4 summary boxes displaying active workshop tracks (4), registrations confirmed (142 / 160), kits dispatched (128), and attendance rate (94.2%).
- **Seat Capacity Meter:** A native `<progress>` element tracking total seat reservations across campus labs.
- **Schedule Table:** A clean schedule table displaying workshop timings, titles, faculty mentors, room numbers, and live session status.

### 2. Available Workshops Catalog (`#workshops`)
- A structured table listing all 4 active technical workshops:
  - *W101: Semantic Web & Modern CSS* (Dr. Arvind Sharma • Lab 34-401)
  - *W102: Cloud Microservices & Containers* (Prof. Priya Nair • Block 3 Audi)
  - *W103: Embedded IoT Sensor Networks* (Er. Rajesh Verma • Lab 14-202)
  - *W104: Practical Machine Learning* (Dr. Meenakshi Sundaram • Lab 28-105)
- Each row displays syllabus highlights, available seats, and an anchor button that links directly to the registration form.

### 3. Participant Registration Form (`#registration`)
- Built using semantic `<form>`, `<fieldset>`, and `<legend>` elements:
  - **Student Information Fieldset:** Full name, university email, 8-digit registration number, and department dropdown.
  - **Workshop & Material Fieldset:** Workshop track selection, pickup desk selection, kit request checkbox, and mandatory 80% attendance pledge.
- **Native HTML5 Validation:**
  - `required` attribute ensures critical fields cannot be submitted empty.
  - `pattern="[0-9]{8}"` enforces the exact 8-digit format for university student IDs.

### 4. Material Requirements & Logistics (`#materials`)
- A detailed inventory table showing:
  - Kit codes (`KIT-ESP32`, `ACC-CLOUD`, `DOC-SEM-CSS`, `ACC-GPU`)
  - Item descriptions (hardware components, cloud vouchers, printed handbooks)
  - Allocated vs total stock quantities
  - Assigned distribution counter desks (Desk A, B, C)
  - Fulfillment status badges (`In Stock`, `Dispatched`, `Active`)

### 5. Session Attendance Tracking (`#attendance`)
- A live session attendance roster table containing:
  - Attendee ID (`ATT-01` to `ATT-06`)
  - Student names (including Harsimran Singh, Yuvraj, and Sakalabattula Pardhu)
  - University registration numbers
  - Check-in timestamps
  - Color-coded status badges: Green for `Present`, Amber for `Late`, Red for `Absent`
  - Certificate eligibility status

### 6. Certificate Generation & Preview (`#certificates`)
- An official academic completion credential card formatted with:
  - University and department heading
  - Recipient student name (**Harsimran Singh**) and registration number (`12601847`)
  - Workshop title and completion statement
  - Unique Credential ID (`CERT-WMS-2026-1901`) and issue date
  - Signatures of the workshop mentor and course coordinator
- **Print Feature:** Includes a print button triggering `window.print()`. The stylesheet contains an `@media print` rule that hides all other page sections, printing only the certificate neatly on standard A4 paper.

### 7. Participant Feedback Form (`#feedback`)
- Simple feedback collection form with:
  - 1 to 5 radio button rating for content quality
  - 1 to 5 radio button rating for instructor clarity
  - Textarea for student comments and suggestions
  - Submit button

### 8. Team 19 Information (`#team`)
- Clean 3-column overview displaying each team member's name, role, registration number, and specific module contributions.

---

## 5. Design Principles (Avoiding AI Slop)

This project avoids artificial "AI design tropes" in favor of an authentic, functional academic portal:

1. **Flat, Controlled Color Palette:**
   - 1 Page Background: `#f3f4f6` (Clean light gray)
   - 1 Surface Color: `#ffffff` (Solid white)
   - 1 Solid Accent Color: `#1e3a8a` (Academic Navy Blue)
   - No linear or radial gradients, glowing blobs, neon drop shadows, or glassmorphism.
2. **Clean Whitespace & 1px Borders:**
   - Elements use crisp 1px solid borders (`#d1d5db`) instead of rounded floating cards with heavy blurred shadows.
   - Removed decorative left-border accent stripes and artificial card-in-card nesting.
3. **No AI Clichés:**
   - No emojis used as bullet points or icons.
   - No tiny all-caps "eyebrow" tags (`FEATURES`, `HOW IT WORKS`).
   - No fake buzzword copy or fabricated student testimonials. Real course labels, real dates, real lab numbers, and real team details carry the page.

---

## 6. Viva Walkthrough Guide (For Team 19 Members)

Use these concise questions and answers to prepare for the viva:

### Q1: Why did you use HTML and CSS without JavaScript?
> **Answer:**  
> "The objective of CA1 is to demonstrate strong fundamentals in HTML5 and CSS3. We fulfilled all functional requirements using the browser's native platform: semantic forms with `required` and `pattern` attributes for validation, standard `<table>` elements for rosters, `<progress>` for capacity tracking, and `@media print` for certificate printing."

### Q2: What semantic HTML elements did you use?
> **Answer:**  
> - `<header>` and `<footer>` for institutional metadata.
> - `<nav>` with anchor links for in-page section navigation.
> - `<main>` and `<section>` for distinct modular workflows.
> - `<form>`, `<fieldset>`, `<legend>`, `<label>`, and `<input>` for accessible, structured forms.
> - `<table>`, `<thead>`, `<tbody>`, `<tr>`, `<th>`, and `<td>` for tabular data.
> - `<progress>` for visual representation of seat capacity.

### Q3: How is the CSS structured?
> **Answer:**  
> "At the top of `styles.css`, we defined CSS variables in `:root` for our background color, surface color, text colors, and the solid navy accent (`--accent-color`). All layout rules use standard Flexbox and CSS Grid (`grid-template-columns: repeat(auto-fit, minmax(...))`) to adapt seamlessly across mobile and desktop screens."

### Q4: How does the certificate print feature work?
> **Answer:**  
> "In `styles.css`, we wrote an `@media print` rule. When a user presses the print button or Ctrl+P, all other page elements (`.site-header`, `.navbar`, `#dashboard`, `#registration`, etc.) are hidden using `display: none !important;`, allowing the certificate box to print cleanly on an A4 sheet."

---

## 7. Mandatory CA1 Submission Details (UMS Format)

| Field Name | Submission Detail |
| :--- | :--- |
| **Project Name & Title** | Workshop Management System |
| **Team Name** | Team 19 |
| **Course Code** | CSE326 |
| **Registration Number(s)** | Reg. No. 1: `12601847` (Harsimran Singh)<br>Reg. No. 2: `12601876` (Yuvraj)<br>Reg. No. 3: `12625518` (Sakalabattula Pardhu) |
| **GitHub Link** | `https://github.com/HarsimranSingh-dev/workshop-management-system` |
| **Deployed Link** | `https://harsimransingh-dev.github.io/workshop-management-system/` |
| **Video Presentation Link** | *(Attach your recorded presentation link)* |
