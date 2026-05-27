# 🎓 Scholarship Portal

An intelligent, multi‑user scholarship matching platform built with **HTML, CSS, JavaScript, and Firebase**.  
Students can sign up, create their academic profile, and instantly get **personalised scholarship suggestions** with a **profile score** and **match percentages**.  
An integrated **admin panel** allows administrators to add, edit, and delete scholarships directly from the UI.

---

## 🚀 Features

### 🧑‍🎓 Student Portal
- **Authentication** – Sign up / Sign in with email & password (Firebase Auth).
- **Password Reset** – Forgot password link with spam‑folder reminder.
- **Profile Builder** – Multi‑step accordion form (personal, education, language, work, extracurricular, financial, documents, preferences).
- **Smart Matching Algorithm**
  - Hard eligibility filters (nationality, degree, GPA, language, passport).
  - Soft scoring based on academic performance, work experience, publications, awards, leadership, volunteer work, financial background, and country/field preferences.
- **Profile Score (0‑100)** – Visual progress bar with actionable interpretation.
- **Match Score & Badge** – Each scholarship shows a match % and a safety category (🟢 Safe / 🟡 Target / 🔴 Reach).
- **Detailed Suggestions** – 15+ personalised tips to improve the profile.
- **Data Privacy** – All student data is saved to Firestore under their unique user ID.

### 🛠️ Admin Panel
- **Hidden behind ⋮ menu** – Protected by login.
- **Add Scholarship** – Fill in scholarship name, university, country, degree, funding type, eligibility, minimum GPA, deadline, link, and description.
- **Edit / Delete** – View a list of all added scholarships and remove any entry.
- **Analytics Dashboard** – Total scholarships and daily searches.

### 🎨 UI / UX
- **Dark mode only** – Elegant dark theme with neon animated borders.
- **Mobile‑first responsive design** – Works perfectly on phones.
- **Bangla language** – Fully Bengali interface for students.
- **Skeleton loading** – Smooth placeholder cards while fetching results.

---

## 🔧 Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | HTML5, CSS3, JavaScript (Vanilla) |
| Backend / Hosting | GitHub Pages (static), Firebase (backend‑as‑a‑service) |
| Database | Cloud Firestore |
| Authentication | Firebase Authentication (Email/Password) |
| Hosting alternative | Firebase Hosting (optional) |

---

## 🔐 Security

- **Firestore Security Rules** ensure:
  - Scholarships are **publicly readable** but only **admins** can create/update/delete them.
  - Student data (`studentData`) is **only accessible by the owner** (the logged‑in student) and **admins**.
- Admin privileges are granted by adding their user UID to a `admins` collection in Firestore.

---

## ⚡ Quick Start

1. **Clone the repo**
   ```bash
   git clone https://github.com/syntaxbd/ScholarBD.git
   cd ScholarBD
