Instant Dashboards from Excel/CSV — No Coding Required

📝 Problem Statement

Businesses and individuals often rely on raw Excel/CSV files that are hard to interpret. Creating dashboards in tools like Excel, Power BI, or Tableau requires skill and time.
There is a need for a plug-and-play system where a user can:

Upload structured data

Automatically detect column types (Numeric, Categorical, Date)

Generate meaningful charts instantly

Interact with filters

Download reports

This project solves that by offering a full-stack automated dashboard generator.

🛠️ Tech Stack
Frontend

React (Vite + TypeScript)

Tailwind CSS

shadcn/ui components

Recharts (or Plotly/Chart.js depending on your implementation)

Backend

Node.js (Express) or Python Flask (choose based on your repo)

Libraries for parsing:

CSV → Papaparse / Pandas

Excel → XLSX / OpenPyXL

Data Processing

Type inference (Numeric, Categorical, Temporal)

Auto-chart selection logic

🚀 Features

Upload Excel/CSV

Auto-detect column types

Auto-generate:

Line Charts

Bar Charts

Pie Charts

Global dynamic filtering

Summaries (SUM, AVG, COUNT)

Responsive dashboard

Error handling for corrupted/missing values

Export charts

📁 Folder Structure
project-root/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── charts/
│   │   ├── utils/
│   │   └── hooks/
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

🧪 Running the Project (Setup Steps)
1️⃣ Clone the Repository
git clone <repo-url>
cd <project-folder>

2️⃣ Setup Frontend
cd frontend
npm install
npm run dev

3️⃣ Setup Backend
Node.js version:
cd backend
npm install
npm start

Python version:
cd backend
pip install -r requirements.txt
python app.py

📚 API Documentation
POST /api/upload

Uploads an Excel/CSV file.

Request
multipart/form-data
Field: file

Response

{
  "columns": {
    "Month": "date",
    "Revenue": "number",
    "Region": "category"
  },
  "data": [ ... ]
}

GET /api/summary

Returns aggregated metrics (sum, avg, count).

POST /api/filter

Filters dataset based on:

Date range

Category

Numeric ranges

Example Response

{
  "filteredData": [...],
  "charts": {
    "lineChart": [...],
    "barChart": [...],
    "pieChart": [...]
  }
}

🖼️ Screenshots (Add your real screenshots)
1. Home Page

2. Auto-Generated Dashboard

3. Filters Panel

🏁 Outcome

A tool that democratizes data analysis by allowing any user to simply upload a spreadsheet and instantly view an interactive dashboard — no data skills required.