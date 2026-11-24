# Workshop Management System (WMS)
> **Course:** CSE326 — Internet & Web Technologies  
> **Academic Task:** CA1 Project-Based Assessment  
> **Allocated Team:** Team 19  
> **Tech Stack:** 100% Pure Semantic HTML5 & Vanilla CSS3 (Zero JavaScript, Zero Frameworks)

---

## 👥 Team 19 Member Information

| Team Role | Member Name | Registration Number | Primary Viva Modules |
| :--- | :--- | :--- | :--- |
| **Team Leader** | **Harsimran Singh** | `12601847` | Core Architecture, Semantic Layout, `:root` CSS Design Tokens, Dashboard & KPI Analytics, Accessibility |
| **Member 2** | **Yuvraj** | `12601876` | Workshop Catalog & Track Filters, Multi-Fieldset Registration Form, Form Controls & Validation States, Schedule Timeline |
| **Member 3** | **Sakalabattula Pardhu** | `12625518` | Material Logistics & Inventory Table, Attendance Tracking Roster, Certificate Generator & Print Layout, Feedback & Ratings |

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

## 🧭 System Architecture & Core Modules

The application is structured as a cohesive, accessible single-page web portal with sticky top navigation and deep-linked section anchors:

```
┌────────────────────────────────────────────────────────────────────────┐
│                        SITE HEADER & TEAM 19 BADGE                    │
├────────────────────────────────────────────────────────────────────────┤
│  STICKY NAVIGATION: Dashboard | Workshops | Register | Materials | ...  │
├────────────────────────────────────────────────────────────────────────┤
│ 1. OPERATIONS DASHBOARD     → KPI Stat Cards, Capacity Progress, Sched │
│ 2. WORKSHOP DISCOVERY       → Search, Track Filter Pills, Course Cards │
│ 3. REGISTRATION PORTAL      → 4-Step Fieldsets, Input Validation States│
│ 4. MATERIAL LOGISTICS       → Inventory Table, Hardware & Safety Accor │
│ 5. ATTENDANCE ROSTER        → Live Check-in Log, Timestamp, Eligibility│
│ 6. CERTIFICATE GENERATOR    → Clearance Criteria Checklist, Print Preview│
│ 7. PARTICIPANT FEEDBACK     → Star/NPS Sliders, Benchmarks, Testimonials│
│ 8. TEAM 19 ROSTER & ROLES   → Detailed Student Allocation & Viva Matrix │
├────────────────────────────────────────────────────────────────────────┤
│                        ACADEMIC FOOTER & COPYRIGHT                    │
└────────────────────────────────────────────────────────────────────────┘
```

### Module Breakdown

1. **Operations Dashboard (`#dashboard`):**  
   - Executive metrics grid (`.stats-grid`): Active Tracks, Total Registrations, Hardware Kits Prepared, Verified Attendance %, and Average Satisfaction Rating.
   - Overall Capacity Meter (`<progress class="capacity-progress" value="142" max="160">`).
   - Chronological workshop schedule timeline (`<ol class="timeline-list">`) with `<time>` tags, venue markers, and real-time status badges.

2. **Workshop Discovery & Catalog (`#workshops`):**  
   - Filter & Search toolbar with search input and category pills (Web Dev, Cloud & DevOps, Embedded IoT, AI & Data).
   - Detailed cards (`<article class="workshop-card">`) with instructor badges, syllabus summary, prerequisite specs, seat countdowns, and direct enrollment links.

3. **Workshop Participant Registration (`#registration`):**  
   - Multi-step semantic `<form>` organized with `<fieldset>` and `<legend>`:
     - *Step 1: Participant Identity* (Name, University Email, 8-Digit Reg No with `pattern="[0-9]{8}"`, Phone, Department).
     - *Step 2: Workshop Track & Session* (Track dropdown with `<optgroup>`, Morning/Afternoon radio options).
     - *Step 3: Material Requirements & Kit Delivery* (Hardware kit checkboxes, designated pickup counter desk).
     - *Step 4: Attendance Pledge & Terms* (Required confirmation checkbox).
   - Form actions with Submit and Clear buttons, styled with CSS `:user-invalid` and `:focus-visible` pseudo-classes.

4. **Material Requirements & Logistics (`#materials`):**  
   - Comprehensive semantic `<table>` with `<caption>`, `<thead>`, `<tbody>`, and `<tfoot>`.
   - Columns: Item Code (`.mono-cell`), Material Specification, Workshop Track, Allocation Count, Pickup Desk, and Fulfillment Status.
   - Interactive native accordions (`<details>` and `<summary>`) for software prerequisites and hardware safety protocols.

5. **Session Attendance Tracking (`#attendance`):**  
   - Real-time session check-in log table showing Attendee ID, Student Name, Reg Number, Workshop, Check-in Timestamp (`<time>`), and Status (`Present`, `Late`, `Absent`).
   - Clear visual indicators of certificate eligibility.

6. **Certificate Generation & Preview (`#certificates`):**  
   - Student ID verification clearance tool with a 3-point requirement checklist.
   - Official Certificate of Completion frame (`<article class="certificate-preview-frame">`) featuring institutional crest, recipient name, workshop title, unique Credential ID (`CERT-WMS-2026-1901`), faculty signature line, and issuance date.
   - Print-ready with dedicated `@media print` rules for clean single-page printing.

7. **Participant Feedback & Evaluation (`#feedback`):**  
   - Structured rating scales (1 to 5) for content quality, instructor guidance, and lab utility.
   - Net Promoter Score (NPS) range slider (`<input type="range" min="1" max="10">`).
   - Key takeaway and suggestions textareas.
   - Aggregate evaluation benchmark progress bars and authentic participant testimonials.

8. **Team 19 Roster (`#team`):**  
   - Cards presenting Harsimran Singh, Yuvraj, and Sakalabattula Pardhu with registration numbers and exact viva module ownership.

---

## 🎨 UI & Color Design System

The visual design adheres strictly to a clean, editorial, human-first aesthetic with high legibility and WCAG AAA compliance:

| Design Token | CSS Variable | Hex Value | Purpose |
| :--- | :--- | :--- | :--- |
| **Canvas Background** | `--color-bg-canvas` | `#f8fafc` | Soft stone/slate neutral page surface |
| **Surface Card** | `--color-bg-surface` | `#ffffff` | Pure white for cards, forms, and data tables |
| **Muted Surface** | `--color-bg-subtle` | `#f1f5f9` | Light slate for table headers and toolbars |
| **Primary Ink** | `--color-text-main` | `#0f172a` | Deep ink slate for headings and primary copy |
| **Muted Text** | `--color-text-muted` | `#334155` | Secondary text, descriptions, and labels |
| **Subtle Text** | `--color-text-subtle` | `#64748b` | Timestamps, table footers, and hints |
| **Primary Brand** | `--color-primary` | `#1e3a8a` | Classic university navy blue for primary actions |
| **Accent Sky** | `--color-accent` | `#0284c7` | Understated blue for focus rings and highlights |
| **Success Status** | `--color-success` | `#15803d` | Deep forest green for "Present", "In Stock" |
| **Warning Status** | `--color-warning` | `#b45309` | Warm amber for "Late", "Waitlist" |
| **Danger Status** | `--color-danger` | `#b91c1c` | Refined crimson for "Absent", "Required" |

*No neon gradients, artificial purple glows, or distracting animations.*

---

## 🎓 Viva & Code Walkthrough Guide for Team 19

Use this guide during your viva examination to confidently explain the code structure and design decisions:

### Q1: Why did you use pure HTML and CSS without JavaScript?
> **Answer:**  
> "The CA1 assessment tests core fundamentals of Internet & Web Technologies. By relying on pure semantic HTML5 and modern CSS3, we demonstrate complete mastery of the browser's native platform capabilities—such as native form validation (`pattern`, `required`, `:user-invalid`), interactive accordions (`<details>` and `<summary>`), semantic progress bars (`<progress>`), and layout systems (CSS Grid and Flexbox)—without introducing external dependencies or brittle scripts."

### Q2: What semantic HTML elements did you use and why?
> **Answer:**  
> - `<header>` and `<footer>` define the landmark introductory and closing academic metadata.
> - `<nav aria-label="Main Navigation">` provides keyboard-accessible jump links across the page.
> - `<main>` acts as the single primary document landmark.
> - `<section>` groups individual workflows (`#dashboard`, `#workshops`, `#registration`, etc.) with `aria-labelledby` headers.
> - `<article>` encapsulates self-contained content units like workshop cards, testimonial blocks, and the certificate frame.
> - `<fieldset>` and `<legend>` group related form controls in the 4-step registration workflow, essential for screen-reader accessibility.
> - `<table>`, `<caption>`, `<thead>`, `<tbody>`, `<tfoot>`, `<th scope="col">` ensure data rosters are tabular, accessible, and structured.
> - `<details>` and `<summary>` create native, zero-JS disclosure accordions.
> - `<time>` with the `datetime` attribute provides machine-readable timestamps for session schedules.
> - `<progress>` visually and programmatically communicates capacity utilization.

### Q3: How is responsiveness handled without frameworks like Bootstrap or Tailwind?
> **Answer:**  
> "We used native CSS Grid and Flexbox with fluid `minmax()` and `auto-fit` column sizing:
> - The stats cards use `grid-template-columns: repeat(auto-fit, minmax(200px, 1fr))`, automatically reflowing from 5 columns on desktop down to 1 column on mobile.
> - Workshop cards use `repeat(auto-fill, minmax(320px, 1fr))`.
> - Data tables are wrapped in a `.table-responsive-wrapper` with `overflow-x: auto` to prevent horizontal viewport clipping on mobile screens.
> - Media queries at `992px` and `768px` adjust layouts, collapse multi-column form grids into single columns, and stack certificate previews gracefully."

### Q4: How does the certificate print feature work without JavaScript?
> **Answer:**  
> "The certificate preview card uses a dedicated `@media print` stylesheet in `styles.css`. When the user triggers print (via browser Ctrl+P or the print button), navigation, headers, toolbars, and forms are hidden with `display: none !important;`, leaving only the certificate frame formatted with clean borders and page-break isolation for A4 paper output."

### Q5: How do CSS Custom Properties (`:root`) benefit the project?
> **Answer:**  
> "All design tokens (colors, font sizes, radii, shadows, and spacing) are defined once in `:root`. If the examiner asks us to change the primary brand color or increase text contrast during the viva, we only need to modify `--color-primary` in one place and the entire portal updates instantly."

---

## 📋 CA1 Mandatory Submission Form (UMS Reference)

*Fill out the official submission Excel file as required by the CA1 instructions:*

| Field Name | Detail |
| :--- | :--- |
| **Project Name & Title** | Workshop Management System |
| **Team Name** | Team 19 |
| **Course Code** | CSE326 |
| **Registration Number(s)** | Reg. No. 1: `12601847` (Harsimran Singh)<br>Reg. No. 2: `12601876` (Yuvraj)<br>Reg. No. 3: `12625518` (Sakalabattula Pardhu) |
| **GitHub Link** | `https://github.com/HarsimranSingh-dev/workshop-management-system` |
| **Deployed Link** | `https://harsimransingh-dev.github.io/workshop-management-system/` |
| **Video Presentation Link** | *(Insert YouTube/Drive Link created by team)* |

---

## 🛠️ Local Development & Preview

To run and preview the project locally:
1. Clone the repository:
   ```bash
   git clone https://github.com/HarsimranSingh-dev/workshop-management-system.git
   ```
2. Open `index.html` directly in any web browser (Google Chrome, Mozilla Firefox, Microsoft Edge, or Safari).
3. Alternatively, launch with VS Code's **Live Server** extension on `http://127.0.0.1:5500`.
