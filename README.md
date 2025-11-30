# ProjexCw
🌟 MindForge — Online Learning Platform (Frontend)
🧠 Overview

MindForge is an interactive online learning platform offering a wide range of lessons — from academic subjects to creative workshops and pop-culture themed modules.
Users can browse courses, view details, add them to their cart, manage quantities, and place orders through a clean, responsive UI.

This repository contains the frontend application only, built with Vue.js and deployed on GitHub Pages.

🔗 Live Site

👉 live url at: [**https://mikacode-stack.github.io/ProjexCw/**](https://mikacode-stack.github.io/ProjexCw/)

(Main public learning portal)

🔗 Backend API (Hosted Separately)

The backend REST API is hosted in another repository and deployed on Render:
👉 [**https://mikacode-stackMindForge-Backend](https://github.com/MikaCode-stack/MindForge-Backend)

👉 Render backend URL: [https://mindforge-api.onrender.com](https://project-cw-backend-apirest.onrender.com)

🕰️ Historical Rationale

MindForge was created to provide users the ability to learn anytime, anywhere, at their own pace.
The system offers:

academic subjects

creativity-boosting courses

fun, themed courses (e.g., Harry Potter Studies)

Users simply browse through the available courses and enroll in the ones they like.

🚀 Frontend Features
📌 1. Course Catalog

Displays all available lessons

Structured with subject, description, image, price, rating, category, and spaces

Dynamically fetched from backend API

Courses properly validated with remaining spaces

📌 2. Course Details Page

Clicking a course opens an expanded view

Shows complete details

Allows adding the course to the cart

📌 3. Shopping Cart

Add/remove courses

Modify quantity

Stock validation communicating with backend

Cart persists using sessionStorage

Real-time UI updates

“Spaces left” logic applied everywhere

📌 4. Edit Cart Modal

Users can refine the order before checkout

Increase or decrease item qty

Prevents exceeding the available spaces

Modal updates totals and internal stock display reactively

All validations happen both visually (UI) and logically (functions)

📌 5. Order Submission

When an order is saved, the frontend sends a POST request to the backend server

On success:

UI displays confirmation

Cart is cleared

Course spaces are updated visually

If quantities exceed available stock (race condition), backend rejects the order and the frontend shows an error message

🔄 Navigation Flow
Home → Course Grid

Select a course → View details → Add to Cart

Home → Cart

Open cart → Review selections → Edit via modal
→ Save → Send POST request to backend

After saving order:

Cart resets

Page shows success message

Navigation returns to catalog or stays on summary depending on settings

🛠️ Technologies Used

Vue.js

Vue reactivity & computed values

GitHub Pages for hosting

Fetch API for requests

Modular components

CSS styling for responsive layout
