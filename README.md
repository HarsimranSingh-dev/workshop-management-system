# Workshop Management System

A web-based platform built with pure HTML5 and CSS3 to manage technical workshop registrations, hardware/material requirements, session attendance tracking, certificate generation, and participant feedback.

This project was developed for **CSE326 (Internet Programming)** by **Team 19**.

---

# Live Links & Documentation

- **Live Website:** [https://harsimransingh-dev.github.io/workshop-management-system/](https://harsimransingh-dev.github.io/workshop-management-system/)
- **GitHub Repository:** [https://github.com/HarsimranSingh-dev/workshop-management-system](https://github.com/HarsimranSingh-dev/workshop-management-system)
- **Code Walkthrough Guide:** See [CODE_EXPLANATION.md](CODE_EXPLANATION.md) for a complete explanation of every HTML tag and CSS rule used.
- **Viva Preparation:** See [VIVA_QUESTIONS_ANSWERS.md](VIVA_QUESTIONS_ANSWERS.md) for potential examiner questions, answers, and live code modification tasks.

---

## Project Team (Team 19)

| Name | Registration Number | Role & Primary Contributions |
| :--- | :--- | :--- |
| **Harsimran Singh** | `12601847` | Team Leader — Page layout, CSS design system, operations dashboard, and metrics |
| **Yuvraj** | `12601876` | Team Member — Workshop catalog, registration form, and input validation |
| **Sakalabattula Pardhu** | `12625518` | Team Member — Material logistics, attendance tracking, certificate preview, and feedback |

---

## Problem Statement & Objective

**Assigned Title:** Workshop Management System  
**Problem Statement:**  
> Create a platform for managing workshop registrations, material requirements, attendance tracking, and certificate generation. Include features for feedback collection.

**Project Objective:**  
Develop a responsive frontend solution that organizes workshop data, simplifies the registration workflow, tracks seat capacity, and provides clear status views without relying on backend services.

---

## Key Features

The portal is implemented across seven functional sections:

1. **Operations Dashboard (`#dashboard`):**
   - Displays real-time overview metrics: 4 active tracks, 142 confirmed registrations (out of 160 total seats), 142 allocated kits, and a 94.4% overall attendance rate.
   - Includes a native `<progress>` bar tracking aggregate seat capacity.
   - Shows today's session schedule with timing, room numbers, and status indicators.

2. **Available Workshops Catalog (`#workshops`):**
   - Lists scheduled workshops across four technical tracks: Web Development, Cloud & DevOps, Embedded IoT, and Machine Learning.
   - Shows instructors, venues, remaining seats, and direct registration links.

3. **Participant Registration Form (`#registration`):**
   - Multi-section form using `<fieldset>` and `<legend>` for student details, workshop track selection, and pickup counter preferences.
   - Native HTML5 validation using `required`, `type="email"`, and `pattern="[0-9]{8}"` to ensure proper input formatting without JavaScript.

4. **Material Requirements & Logistics (`#materials`):**
   - An inventory table mapping kit codes, descriptions, and distribution desks (Counters A, B, and C) to each workshop track.
   - Tracks allocated supplies against the 142 registered attendees.

5. **Session Attendance Tracking (`#attendance`):**
   - A live check-in roster for Track W101 recording student names, registration numbers, timestamps, status badges (Present, Late, Absent), and certificate eligibility.

6. **Certificate Generation & Preview (`#certificates`):**
   - An official completion certificate preview card with student name, registration number, credential ID, and signature lines.
   - Print-ready using a dedicated `@media print` stylesheet that isolates only the certificate for A4 paper or PDF export.

7. **Participant Feedback Collection (`#feedback`):**
   - A structured evaluation form collecting 1-to-5 ratings for content quality and instructor clarity, along with suggestions for future topics.

---

## Project Structure

```text
workshop-management-system/
├── index.html                  # Main web portal (semantic HTML5)
├── styles.css                  # Core stylesheet (flat CSS3, CSS variables, print media)
├── README.md                   # Project overview and submission documentation
├── CODE_EXPLANATION.md         # Beginner-friendly guide to all HTML elements and CSS rules
└── VIVA_QUESTIONS_ANSWERS.md   # Comprehensive viva questions, answers, and live code tasks
```

---

## Tech Stack & Design Approach

- **HTML5:** Semantic elements (`<header>`, `<nav>`, `<main>`, `<section>`, `<fieldset>`, `<legend>`, `<table>`, `<progress>`) for clean document structure and accessibility.
- **CSS3:** Custom properties (`:root`) for color theming, Flexbox for navigation and toolbars, CSS Grid for responsive forms, and `@media print` for certificate printing.
- **No External Dependencies:** Zero JavaScript, zero CSS frameworks (no Bootstrap/Tailwind), and no external icons or web fonts.
- **Visual Design:** Clean, flat academic interface using high-contrast text and crisp 1px borders, avoiding heavy shadows, gradients, and unnecessary visual clutter.

---

## Running Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/HarsimranSingh-dev/workshop-management-system.git
   ```
2. Navigate to the folder:
   ```bash
   cd workshop-management-system
   ```
3. Open `index.html` in any web browser (Chrome, Firefox, Edge, Safari). No build tools, server setup, or dependencies required.

---

## Course Submission Information

- **Course Code:** CSE326 (Internet Programming)
- **Team:** Team 19
- **Project Title:** Workshop Management System
- **Repository:** `https://github.com/HarsimranSingh-dev/workshop-management-system`
- **Deployment:** `https://harsimransingh-dev.github.io/workshop-management-system/`
