# Workshop Management System (WMS)
> **Course:** CSE326 — Internet Programming  
> **Allocated Team:** Team 19  
> **Tech Stack:** 100% Pure HTML5 & CSS3 (Zero JavaScript, Zero Frameworks)

---

## 1. Project Overview & Problem Statement

*Extracted directly from the official course allocation sheet `CSE326_MM_Team_Project_Allocation.xlsx` (Row 20, Team 19):*

* **Assigned Project Title:** Workshop Management System
* **Problem Statement:**  
  > *"Create a platform for managing workshop registrations, material requirements, attendance tracking, and certificate generation. Include features for feedback collection."*
* **Project Objective:**  
  > *"Develop a responsive web-based solution for workshop management system that organizes the required information, simplifies the main workflow, supports clear user actions, and provides useful status or summary views."*
* **Core Requirements Fulfilled:**
  - Responsive web interface (desktop, tablet, mobile) without horizontal overflow
  - Structured forms with HTML5 constraint validation
  - Workshop catalog with dates, venues, instructors, and seat availability
  - Material requirements and inventory distribution tracking
  - Session attendance tracking roster with status badges
  - Official certificate generation and preview layout with print capability
  - Participant feedback collection form
  - Dashboard and summary metrics

---

## 2. Team 19 Academic Details

| Role | Student Name | Registration Number | Module Responsibilities |
| :--- | :--- | :--- | :--- |
| **Team Leader** | **Harsimran Singh** | `12601847` | Overall architecture, semantic HTML structure, CSS styling, dashboard and metrics |
| **Team Member** | **Yuvraj** | `12601876` | Workshop catalog table, participant registration form, input validations |
| **Team Member** | **Sakalabattula Pardhu** | `12625518` | Material requirements table, attendance tracking roster, certificate preview, feedback form |

---

## 3. Live Project Links

* **GitHub Repository:** [https://github.com/HarsimranSingh-dev/workshop-management-system](https://github.com/HarsimranSingh-dev/workshop-management-system)
* **Live Deployment (GitHub Pages):** [https://harsimransingh-dev.github.io/workshop-management-system/](https://harsimransingh-dev.github.io/workshop-management-system/)

---

## 4. Beginner's Guide: How Everything Works in Plain English

This project uses only **HTML** (the skeleton/structure of the page) and **CSS** (the styling and appearance). There are zero JavaScript files and zero complex external frameworks.

### The HTML Structure (`index.html`)
1. **`<header>` (Site Header):** Sits at the top of the webpage and introduces the title ("Workshop Management System") and subtitle.
2. **`<nav>` (Navigation Bar):** A list of links (`<ul class="nav-menu">`) that use anchor tags (`<a href="#section-id">`). When clicked, the browser smoothly jumps down to that exact section on the page.
3. **`<main>` (Main Content Container):** Contains the primary functional modules:
   - **`#dashboard` (Operations Dashboard):** Shows 4 summary boxes (Active Tracks, Total Registrations, Kits Allocated, Attendance Rate) plus a native HTML5 `<progress>` bar to visualize seat capacity. A small schedule table displays today's live sessions.
   - **`#workshops` (Workshop Catalog):** A clean `<table>` showing workshop codes, titles, instructors, venues, remaining seats, and a "Register" button.
   - **`#registration` (Registration Form):** Built with `<form>`, `<fieldset>`, and `<legend>`. Each input has a matching `<label for="id">`. HTML5 attributes like `required`, `type="email"`, and `pattern="[0-9]{8}"` ensure the browser validates user input before submission.
   - **`#materials` (Material Requirements & Logistics):** A table displaying kit codes, descriptions, target workshops, allocated quantities (matching the exact 142 registered attendees), and distribution desks.
   - **`#attendance` (Attendance Tracking):** A live check-in table for Session 1 with student names, registration numbers, timestamps, status badges (`Present`, `Late`, `Absent`), and certificate clearance.
   - **`#certificates` (Certificate Preview):** An academic certificate box featuring student name (**Harsimran Singh**), registration number (`12601847`), workshop title, credential ID, and a print button.
   - **`#feedback` (Feedback Collection):** A form with 1–5 radio ratings for content and instructor quality, plus a textarea for comments.
4. **`<footer>` (Page Footer):** A clean, simple 1-line closing copyright and portal credit.

### The CSS Styling (`styles.css`)
1. **CSS Variables (`:root`):** Just like variables in programming (e.g., in C or Python), we define our colors once at the top of the CSS file (`--accent-color: #1e3a8a;`, `--bg-color: #f3f4f6;`). If you change `--accent-color`, every button, header, and active link changes color automatically!
2. **`box-sizing: border-box`:** Tells the browser that padding and borders are counted inside the element's width, preventing boxes from accidentally overflowing or breaking mobile screens.
3. **`position: sticky` on the Navigation Bar:** Keeps the navigation bar stuck to the top of your screen as you scroll down.
4. **`overflow-x: auto` on Tables:** Wraps tables inside `.table-responsive` so if you view the site on a small smartphone, the table gets a smooth horizontal scrollbar instead of stretching the whole page.
5. **`@media print` (Print Stylesheet):** When you click the "Print Certificate" button or press Ctrl+P, CSS hides the navigation bar, headers, and all other sections (`display: none !important;`) so that **only the certificate** prints out cleanly on standard A4 paper.

---

## 5. Mathematical Data Alignment Across All Sections

All numbers across the dashboard, catalog, material logistics, and attendance sections are 100% mathematically consistent:

* **Workshop Seats:** 4 tracks × 40 seats each = **160 Total Seat Capacity**.
  - W101 (Semantic Web & Modern CSS): 38 registered (2 seats left)
  - W102 (Cloud Microservices & Containers): 36 registered (4 seats left)
  - W103 (Embedded IoT Sensor Networks): 35 registered (5 seats left)
  - W104 (Practical Machine Learning): 33 registered (7 seats left)
  - **Total Registrations:** $38 + 36 + 35 + 33 = \mathbf{142\text{ Registered}}$ (88.75% claimed, **18 Remaining Seats**).
* **Material Kits:** Total kits allocated across the 4 tracks = $38 + 36 + 35 + 33 = \mathbf{142\text{ Kits Allocated}}$ (100% demand met for all 142 registered attendees).
* **Attendance:** In Track W101 (38 registered): 36 Present (on time) + 1 Late + 1 Absent = **38 Students Accounted For** (37 attended = **97.4% Session Attendance**). Aggregate campus check-in across all morning workshops is 134 out of 142 = **94.4% Overall Attendance**.

---

## 6. Viva Walkthrough Guide (For Team 19 Members)

Use these simple explanations during your viva:

### Q1: Why did you use pure HTML and CSS without JavaScript?
> **Answer:**  
> "The assessment tests our fundamentals in Internet Programming. We used native HTML5 features—such as `<form>` validation with `required` and `pattern`, native `<progress>` bars for capacity, and `@media print` for printing certificates—to create a fully functional web portal without any external dependencies."

### Q2: What semantic HTML elements did you use and why?
> **Answer:**  
> "Instead of generic `<div>` tags everywhere, we used semantic tags: `<header>` for the top banner, `<nav>` for navigation links, `<main>` for the body container, `<section>` for each modular topic, `<fieldset>` and `<legend>` to group form fields, and standard `<table>`, `<thead>`, `<tbody>`, and `<tfoot>` tags for data rosters. This improves accessibility and search engine readability."

### Q3: How do CSS Variables (`:root`) work?
> **Answer:**  
> "In `styles.css`, we store our colors and styles in `:root` variables like `--accent-color`. If we want to change the primary brand color during the viva, we only change it in `:root` and the whole site updates instantly."

### Q4: How does the certificate print feature work?
> **Answer:**  
> "In `styles.css`, we created an `@media print` rule. When a user clicks the Print button or presses Ctrl+P, CSS automatically hides the header, navbar, forms, and tables using `display: none !important;`, leaving only the certificate neatly formatted for printing on A4 paper."

---

## 7. Mandatory Submission Details (For Excel Submission)

| Field Name | Detail |
| :--- | :--- |
| **Project Name & Title** | Workshop Management System |
| **Team Name** | Team 19 |
| **Course Code** | CSE326 |
| **Registration Number(s)** | Reg. No. 1: `12601847` (Harsimran Singh)<br>Reg. No. 2: `12601876` (Yuvraj)<br>Reg. No. 3: `12625518` (Sakalabattula Pardhu) |
| **GitHub Link** | `https://github.com/HarsimranSingh-dev/workshop-management-system` |
| **Deployed Link** | `https://harsimransingh-dev.github.io/workshop-management-system/` |
| **Video Presentation Link** | *(Attach your recorded presentation link)* |
