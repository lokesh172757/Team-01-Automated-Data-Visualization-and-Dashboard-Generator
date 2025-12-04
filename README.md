Instant dashboards from Excel/CSV — Zero manual work.

📝 Problem Statement

Organizations deal with large amounts of data in spreadsheets.
Manually converting this data into charts and dashboards using Excel or Power BI is time-consuming and requires technical skills.

This project solves that problem by providing a plug-and-play web application where users can:

Upload a dataset

Automatically detect column types

Instantly generate charts

Apply filters

Download insights

No coding or analytics knowledge needed.

🚀 Features
Core Functionalities

Upload Excel (.xlsx) / CSV files

Auto type detection (Number, Category, Date)

Auto-generated charts:

Line charts

Bar/Column charts

Pie/Donut charts

Global filters (Date, Category, Range)

Aggregations: SUM, AVG, COUNT

Export chart/report

Responsive dashboard layout

System Capabilities

Intelligent parser

Chart selection logic based on column types

Error-handling for invalid files

Fast rendering for large datasets

🛠️ Tech Stack
Frontend

React (Vite + TypeScript)

Tailwind CSS

shadcn/ui

Recharts (or Chart.js / Plotly)

Backend

(Choose the one your repo uses)

Node.js (Express)
OR

Python (Flask/FastAPI)

File Parsing

CSV → Papaparse / Pandas

Excel → XLSX / OpenPyXL

📁 Folder Structure
project-root/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── charts/
│   │   ├── utils/
│   │   └── styles/
│   ├── public/
│   └── package.json
│
├── backend/
│   ├── routes/
│   ├── controllers/
│   ├── services/
│   ├── utils/
│   └── server.js (or app.py)
│
├── sample-data/
│   └── dataset.xlsx
│
└── README.md

🧪 Setup & Installation
1️⃣ Clone the repository
git clone <repo-url>
cd <project-folder>

2️⃣ Frontend Setup
cd frontend
npm install
npm run dev

3️⃣ Backend Setup
Node.js:
cd backend
npm install
npm start

Python:
pip install -r requirements.txt
python app.py

📚 API Documentation
POST /api/upload

Upload Excel/CSV file.

Payload
multipart/form-data → file

Response

{
  "columns": {
    "Month": "date",
    "Revenue": "number",
    "Region": "category"
  },
  "data": [...]
}

POST /api/filter

Apply filters and return updated chart data.

Example Response:

{
  "filteredData": [...],
  "charts": {
    "line": [...],
    "bar": [...],
    "pie": [...]
  }
}

GET /api/summary

Returns aggregated metrics (sum, avg, count).

🖼️ Screenshots

(Add your actual images in a screenshots folder)

/screenshots
   upload.png
   dashboard.png
   filters.png


Use in README:

![Upload Screen](./screenshots/upload.png)
![Dashboard](./screenshots/dashboard.png)

🏁 Outcome

A smart, fast, and user-friendly automated dashboard generator that helps users convert raw spreadsheets into meaningful insights instantly.