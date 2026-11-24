# CSE326 Viva Questions & Answers Guide
> **Course:** CSE326 — Internet Programming  
> **Project Title:** Workshop Management System (Team 19)  
> **Team Members:** Harsimran Singh (12601847), Yuvraj (12601876), Sakalabattula Pardhu (12625518)  
> **Purpose:** Master every technical question, design decision, and live code modification an examiner could ask during your viva.

---

## Table of Contents
1. [General Project & Domain Questions](#1-general-project--domain-questions)
2. [HTML5 Semantic Structure & Core Concepts](#2-html5-semantic-structure--core-concepts)
3. [Forms, Inputs & Client-Side Validation](#3-forms-inputs--client-side-validation)
4. [Tables & Data Representation](#4-tables--data-representation)
5. [CSS3 Styling, Box Model, Flexbox & Grid](#5-css3-styling-box-model-flexbox--grid)
6. [Responsive Layout & Print Media](#6-responsive-layout--print-media)
7. [Live Code Modification Tasks (Step-by-Step Viva Cheat Sheet)](#7-live-code-modification-tasks-step-by-step-viva-cheat-sheet)

---

## 1. General Project & Domain Questions

### Q1: What is the problem statement and objective of your project?
> **Answer:**  
> "Our assigned project is the **Workshop Management System** (Team 19). The objective is to provide a single, unified web portal for managing campus technical workshops: tracking seat capacity and registrations, managing physical hardware kits and digital vouchers across distribution desks, logging session attendance, previewing and printing completion certificates, and collecting participant feedback."

### Q2: What is your technology stack? Why is there no JavaScript or backend?
> **Answer:**  
> "Our project is built using **100% pure HTML5 and CSS3** with zero JavaScript and zero backend frameworks. This strictly adheres to the course learning outcomes of CSE326 (Internet Programming), demonstrating complete mastery of the browser's native platform capabilities—such as semantic markup, native HTML5 form constraint validation, Flexbox and CSS Grid layouts, and print stylesheets—without relying on heavy third-party libraries."

### Q3: What was your individual contribution to the project?
> **Answer for Harsimran Singh (Team Leader - 12601847):**  
> *"I designed the overall architecture, the semantic HTML5 layout skeleton, the CSS variable design token system (`:root`), and built the Operations Dashboard with real-time summary metrics and the native capacity progress meter."*  
>
> **Answer for Yuvraj (Member - 12601876):**  
> *"I built the Available Workshops catalog table and the multi-fieldset Participant Registration Form, implementing HTML5 input validation rules (`required`, `type='email'`, and the 8-digit registration regex pattern)."*  
>
> **Answer for Sakalabattula Pardhu (Member - 12625518):**  
> *"I developed the Material Requirements & Logistics inventory table, the Session Attendance Tracking roster with color-coded status badges, the printable Certificate Preview card with `@media print` styling, and the Participant Feedback collection form."*

---

## 2. HTML5 Semantic Structure & Core Concepts

### Q4: What is semantic HTML and why is it important?
> **Answer:**  
> "Semantic HTML means using HTML tags that describe the **meaning** of the content rather than just how it looks visually. For example, instead of using a generic `<div>` for everything, we use `<header>`, `<nav>`, `<main>`, `<section>`, `<fieldset>`, and `<footer>`.  
> Semantic HTML is important for two major reasons:  
> 1. **Accessibility (a11y):** Screen readers for visually impaired students can navigate directly between sections, landmarks, and form fieldsets.  
> 2. **SEO & Maintainability:** Search engines and other developers can instantly understand the structure of the document."

### Q5: What is the difference between `<div>` and `<section>`?
> **Answer:**  
> "`<section>` is a semantic element representing a standalone thematic group of content (such as our `#dashboard`, `#workshops`, or `#registration` modules), typically with its own heading (`<h2>`).  
> In contrast, `<div>` has zero semantic meaning; it is purely a generic container used as a styling hook for CSS (like wrapping our metric boxes in `.summary-bar`)."

### Q6: What is the difference between an inline element and a block-level element?
> **Answer:**  
> - **Block-level elements** (like `<p>`, `<div>`, `<h2>`, `<section>`, `<fieldset>`) always start on a new line and stretch horizontally to take up the full available width of their parent container.  
> - **Inline elements** (like `<span>`, `<a>`, `<strong>`, `<code>`, `<small>`) do not start on a new line; they only take up as much width as their content needs and flow naturally inside text."

### Q7: What is the difference between an `id` and a `class` in HTML?
> **Answer:**  
> - An **`id`** must be completely unique within a webpage (e.g. `id="registration"` or `id="name"`). It is used for in-page anchor jump links (`href="#registration"`) and connecting `<label for="name">` to `<input id="name">`.  
> - A **`class`** can be reused multiple times across different elements (e.g. `class="panel"` or `class="btn"`). It is primarily used to apply the same CSS styling to multiple elements."

### Q8: What does the `<meta name="viewport">` tag do?
> **Answer:**  
> "It instructs mobile browsers how to control the page's dimensions and scaling:  
> `content="width=device-width, initial-scale=1.0"` sets the viewport width to match the physical screen width of the phone, and prevents mobile browsers from automatically zooming out into desktop overview mode."

---

## 3. Forms, Inputs & Client-Side Validation

### Q9: How does form validation work in your project without JavaScript?
> **Answer:**  
> "We use native HTML5 form constraint validation attributes:  
> 1. `required`: Prevents form submission if the user leaves the input empty.  
> 2. `type="email"`: Enforces that the text contains a valid email structure (like `user@domain.com`).  
> 3. `pattern="[0-9]{8}"`: Uses a regular expression to enforce that the student ID consists of exact numbers from 0 to 9, and is exactly 8 digits long.  
> If an input fails any of these rules, the browser automatically blocks submission and displays a native localized error message."

### Q10: Why did you use `<fieldset>` and `<legend>` in your form?
> **Answer:**  
> "`<fieldset>` visually and semantically groups logically related form controls together (e.g. 'Student Information' in one box, and 'Workshop & Material Requirements' in another).  
> `<legend>` acts as the title or caption for that fieldset, sitting directly on top of the border. This allows screen readers to announce the group context to the user."

### Q11: What is the purpose of the `<label for="...">` attribute?
> **Answer:**  
> "The `for` attribute on a `<label>` must match the `id` of an `<input>`. This associates the label with the input. When a user clicks on the label text, the browser automatically shifts focus into the input box or toggles the checkbox, which significantly improves usability and accessibility."

### Q12: What is the difference between `method="get"` and `method="post"` in forms?
> **Answer:**  
> - In `method="get"`, form data is appended directly to the URL as visible query parameters (e.g. `?studentName=Harsimran&regNo=12601847...#registration`). It is ideal for search forms and static client-side demonstrations.  
> - In `method="post"`, form data is sent hidden inside the HTTP request body. It is used when transmitting sensitive data (like passwords) or making database changes."

### Q13: What does the `autocomplete` attribute do?
> **Answer:**  
> "`autocomplete='name'` and `autocomplete='email'` tell the browser what type of data the field expects, allowing the browser to offer pre-saved autofill suggestions for faster user entry."

---

## 4. Tables & Data Representation

### Q14: Explain the structure of an HTML table.
> **Answer:**  
> "An accessible HTML table consists of:  
> - `<table>`: The wrapper container.  
> - `<thead>`: Contains header rows (`<tr>`) with `<th>` (table header cells) defining column titles in bold.  
> - `<tbody>`: Contains data rows (`<tr>`) with `<td>` (table data cells) displaying records.  
> - `<tfoot>`: Contains summary or total calculation rows at the bottom of the table."

### Q15: What does `border-collapse: collapse;` do in CSS?
> **Answer:**  
> "By default in HTML, table cells have separate borders with tiny gaps between them. `border-collapse: collapse;` merges adjacent cell borders into a single, clean 1px grid line."

### Q16: How did you make your tables responsive on mobile devices?
> **Answer:**  
> "We wrapped our `<table>` inside a `<div class="table-responsive">` container and applied `overflow-x: auto;` in CSS. When viewed on a narrow phone screen where the table is wider than the display, the browser adds a smooth horizontal scrollbar inside the table box, preventing the table from stretching or breaking the entire page layout."

### Q17: What does `colspan="3"` mean?
> **Answer:**  
> "`colspan='3'` tells a `<td>` cell in our table footer to stretch horizontally across 3 columns, allowing us to display summary labels without misaligning other data columns."

---

## 5. CSS3 Styling, Box Model, Flexbox & Grid

### Q18: What is the CSS Box Model?
> **Answer:**  
> "Every element on a webpage is treated as a rectangular box. The Box Model consists of 4 layers from inside to outside:  
> 1. **Content:** The actual text or image.  
> 2. **Padding:** Transparent spacing inside the border around the content.  
> 3. **Border:** The line surrounding the padding and content.  
> 4. **Margin:** The transparent space outside the border separating the element from neighbors."

### Q19: Why do you have `* { box-sizing: border-box; }` at the top of your CSS?
> **Answer:**  
> "In the default browser box model (`content-box`), adding padding or borders increases an element's total width, which often causes layout boxes to overflow their container.  
> `box-sizing: border-box;` forces the browser to calculate width *including* padding and borders, ensuring elements always stay exactly the width we set."

### Q20: What are CSS Variables (`:root`) and why did you use them?
> **Answer:**  
> "CSS Variables (custom properties) allow us to store reusable values globally in `:root`:  
> ```css
> :root {
>   --accent-color: #1e3a8a;
>   --bg-color: #f3f4f6;
> }
> ```  
> We use them because they eliminate repetitive hardcoded color codes and allow us to modify the entire website's theme live during the viva by changing just one line of code."

### Q21: What is the difference between CSS Flexbox and CSS Grid?
> **Answer:**  
> - **Flexbox (`display: flex`)** is primarily **one-dimensional**; it organizes items along a single row or column (used for our navigation bar and summary metrics).  
> - **CSS Grid (`display: grid`)** is **two-dimensional**; it organizes items simultaneously across rows AND columns (used for our responsive form inputs grid)."

### Q22: Explain this line: `grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));`
> **Answer:**  
> "This line creates a responsive multi-column grid without media queries:  
> - `auto-fit`: Calculates how many columns can fit based on screen width.  
> - `minmax(220px, 1fr)`: Each column must be at least 220px wide, but can expand to fill 1 fraction (`1fr`) of remaining space.  
> On desktop, it displays 4 columns. On tablets, it drops to 2. On mobile phones, it stacks to 1 column."

### Q23: What does `position: sticky; top: 0;` do?
> **Answer:**  
> "`position: sticky; top: 0;` allows our navbar to scroll naturally with the page until it touches the top edge of the viewport (`top: 0`), at which point it locks into place and remains visible while the rest of the page scrolls underneath."

### Q24: What is `scroll-margin-top: 50px;` and why is it necessary?
> **Answer:**  
> "Because our navigation bar is sticky and fixed at the top of the screen (50px tall), clicking a jump link like `<a href='#registration'>` would cause the browser to scroll the section heading directly behind the navbar. `scroll-margin-top: 50px;` adds a 50px offset, keeping section titles clearly visible."

### Q25: What does `tbody tr:nth-child(even)` do?
> **Answer:**  
> "It is a CSS pseudo-class that targets every even row (2, 4, 6...) in our table body and applies a subtle light-gray background color (`#f9fafb`), creating alternating 'zebra stripes' that make wide tables easier to read."

---

## 6. Responsive Layout & Print Media

### Q26: How does the certificate print feature work without backend code?
> **Answer:**  
> "In HTML, we attached `onclick='window.print()'` to our button, which opens the browser's native print / Save as PDF dialog.  
> In `styles.css`, we created an `@media print` rule:  
> ```css
> @media print {
>   .site-header, .navbar, footer, .btn,
>   #dashboard, #workshops, #registration, #materials, #attendance, #feedback {
>     display: none !important;
>   }
>   .cert-box {
>     border: 2px solid #000000 !important;
>   }
> }
> ```  
> When the print dialog opens, CSS hides all website navigation, headers, forms, and tables, leaving **only the certificate card** formatted cleanly for A4 paper."

### Q27: How did you ensure your website works on mobile screens without horizontal scroll?
> **Answer:**  
> "Through 4 key techniques:  
> 1. Setting `<meta name="viewport" content="width=device-width, initial-scale=1.0">`.  
> 2. Using relative widths (`width: 94%; max-width: 1040px;`).  
> 3. Wrapping wide tables inside `.table-responsive` with `overflow-x: auto;`.  
> 4. Using fluid CSS Grid (`minmax(220px, 1fr)`) and `flex-wrap: wrap;` so multi-column layouts stack into a single column on small screens."

---

## 7. Live Code Modification Tasks (Step-by-Step Viva Cheat Sheet)

During a viva, examiners frequently ask students to modify code live on the spot to prove they wrote and understand it. Here is how to perform every common modification:

---

### Task 1: "Change the primary color of the website from Navy Blue to Forest Green or Crimson Red."
**How to do it in 5 seconds:**  
1. Open [styles.css](file:///c:/Users/preet/OneDrive/Documents/html%20css%20project/styles.css).
2. Go to lines 13–15 inside `:root`.
3. Change `--accent-color`:
   - For **Forest Green**: Change `#1e3a8a` to `#15803d`
   - For **Crimson Red**: Change `#1e3a8a` to `#b91c1c`
4. Save and refresh the browser. The header, buttons, certificate borders, and active links will change instantly!

---

### Task 2: "Add a new workshop to the Available Workshops table (e.g. W105: Cyber Security)."
**How to do it:**  
1. Open [index.html](file:///c:/Users/preet/OneDrive/Documents/html%20css%20project/index.html).
2. Find the `<tbody>` inside `<section id="workshops">` (around line 170).
3. Paste this new `<tr>` row before `</tbody>`:
```html
<tr>
  <td>W105</td>
  <td><strong>Cyber Security & Ethical Hacking</strong><br><small>Network security, packet analysis, vulnerability tools</small></td>
  <td>Dr. K. Raman</td>
  <td>Nov 29 • Lab 12-101</td>
  <td>30 / 40 (10 left)</td>
  <td><a href="#registration" class="btn">Register</a></td>
</tr>
```
4. Save and refresh.

---

### Task 3: "Add a Phone Number field to the Registration Form."
**How to do it:**  
1. Open [index.html](file:///c:/Users/preet/OneDrive/Documents/html%20css%20project/index.html).
2. Find `<fieldset>` under `<section id="registration">` (around line 190).
3. Inside `<div class="form-grid">`, add this field:
```html
<div class="form-field">
  <label for="phone">Phone Number *</label>
  <input type="tel" id="phone" name="studentPhone" placeholder="+91 98765-43210" required>
</div>
```
4. Save and refresh. The CSS Grid automatically arranges it into the form!

---

### Task 4: "Change the certificate recipient name and student registration number."
**How to do it:**  
1. Open [index.html](file:///c:/Users/preet/OneDrive/Documents/html%20css%20project/index.html).
2. Find `<section id="certificates">` (around line 380).
3. Find `<div class="cert-student">Harsimran Singh</div>` and change it to `Yuvraj` or `Sakalabattula Pardhu`.
4. Change the registration number in `<p>Registration Number: 12601847</p>` to `12601876` or `12625518`.
5. Save and refresh.

---

### Task 5: "Make the navigation bar static instead of sticky."
**How to do it:**  
1. Open [styles.css](file:///c:/Users/preet/OneDrive/Documents/html%20css%20project/styles.css).
2. Find `.navbar` (around line 68).
3. Comment out or delete:
```css
/* position: sticky; */
/* top: 0; */
```
4. Save and refresh. The navbar will now remain at the top of the page without following the scroll.
