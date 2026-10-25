# StudyPilot AI — Professional Student Study Planner

## Features
- Polished dark dashboard
- Subject and exam-date management
- Explainable priority scoring (50% urgency, 20% difficulty, 30% pending syllabus)
- AI Plan Bot: date-wise study blocks, revision blocks, CSV export
- Save plan to schedule and mark sessions complete
- Progress analytics with charts
- Topic-specific YouTube search helper
- SQLite local persistence

## Run on Windows
Python 3.13 recommended. Open PowerShell in this folder and run:
```powershell
py -3.13 -m venv .venv
.\.venv\Scripts\python.exe -m pip install --upgrade pip
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m streamlit run app.py
```
Open the local URL printed by Streamlit, normally http://localhost:8501.

## AI Plan Bot input
One subject per line:
`Subject Name | YYYY-MM-DD | difficulty 1-5 | total topics | completed topics`

Example:
`DBMS | 2026-10-20 | 5 | 10 | 2`

This is an explainable rule-based scheduling algorithm, not a trained ML model or cloud LLM. The Video Tutor creates YouTube search links; it does not verify individual videos.
