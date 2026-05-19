# zoltan9191.github.io
Online CV
https://zoltan9191.github.io/

# CV Viewer (JSON-driven)

This project is a **static CV website** powered entirely by a single JSON file (`cv.json`) and rendered dynamically in the browser.

It is designed for **GitHub Pages hosting** and allows you to update your CV without touching any HTML.

---

# 🚀 Overview

- CV data stored in `cv.json`
- `index.html` renders everything dynamically
- Empty sections are automatically hidden
- No backend required
- Works on GitHub Pages, Netlify, Vercel

---

# 📁 Project Structure
/cv-viewer

├── index.html

├── cv.json

├── profile.jpg (optional)

└── README.md


---

# ⚙️ How it works

1. Browser loads `index.html`
2. JS fetches `cv.json`
3. Data is parsed and rendered into sections:
   - Header (name, position, contacts)
   - Summary
   - Work experience
   - Education
   - Skills
   - Projects
   - Languages
   - Certifications

4. Empty data is automatically hidden

---

# 📊 CV JSON Format

## 🔹 Root object

```json
{
  "name": "Full Name",
  "position": "Job Title",
  "contactInformation": "+123456789",
  "email": "email@example.com",
  "address": "City, Country",
  "profilePicture": "image-url",
  "socialMedia": [],
  "summary": "",
  "education": [],
  "workExperience": [],
  "projects": [],
  "skills": [],
  "languages": [],
  "certifications": []
}
```
🌐 Social Media
"socialMedia": 
```json
[
  {
    "socialMedia": "LinkedIn",
    "link": "https://linkedin.com/in/username"
  },
  {
    "socialMedia": "GitHub",
    "link": "https://github.com/username"
  }
]
```
Rules:
Always use full URLs (https://)

🧠 Summary
"summary": "Short professional bio..."
Supports multiline text
Displayed in hero section
🎓 Education
```json
{
  "school": "University Name",
  "degree": "Bachelor / Master",
  "startYear": "2018-09-01",
  "endYear": "2022-06-01"
}
```
💼 Work Experience
```json
{
  "company": "Company Name",
  "position": "Job Title",
  "description": "Role description",
  "startYear": "2020-01-01",
  "endYear": "2024-01-01"
}
```
Notes:

Empty fields are automatically hidden
🛠 Skills
```json
{
  "title": "Technical Skills",
  "skills": [
    "JavaScript",
    "Node.js",
    "React"
  ]
}
```
Rules:
Empty skill groups are hidden

📂 Projects
```json
{
  "name": "Project Name",
  "description": "Project description"
}
```
🌍 Languages
Simple format
```json
"languages": ["English", "Ukrainian"]
```
Advanced format
```
"languages": [
  {
    "language": "English",
    "level": "B2"
  }
]
```
🏆 Certifications
```json
[
  "Cisco IoT 2017",
  {
    "name": "Cisco IoE",
    "year": "2018"
  }
]
```
