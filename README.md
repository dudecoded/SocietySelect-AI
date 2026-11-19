# SocietySelect AI

AI-powered student society recruitment and performance management system.

SocietySelect AI helps college societies manage recruitment through student profiles, applications, assessments, interviews, probation projects, and evidence-based recommendations. Machine-learning outputs support mentors; final selection decisions remain with human mentors.

## Project scope

- Student and mentor workflows for society recruitment.
- Resume processing and technical skill extraction.
- Skill matching between student profiles and society requirements.
- Candidate recommendations using transparent weighted scoring.
- Student performance and probation-risk analytics.
- Mentor-facing insights and student feedback.

## Technology

| Area | Technologies |
|---|---|
| Frontend | React, Vite |
| Backend | Python, FastAPI |
| Database | PostgreSQL |
| Data processing | Pandas, NumPy |
| ML | Scikit-learn |
| NLP | spaCy, Sentence Transformers |
| Resume parsing | PyMuPDF |

## Repository structure

```text
SocietySelect-AI/
├── backend/
│   ├── app/routers/
│   ├── ml/
│   │   ├── resume_processing/
│   │   ├── skill_matching/
│   │   ├── recommendation/
│   │   └── data/sample/
│   ├── tests/
│   └── requirements.txt
├── frontend/
├── docs/
├── .gitignore
└── README.md
```

## Getting started

Clone the repository and move into the project:

```bash
git clone https://github.com/dudecoded/SocietySelect-AI.git
cd SocietySelect-AI
```

Create a Python environment (Windows PowerShell):

```powershell
cd backend
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

macOS/Linux:

```bash
cd backend
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

The backend and ML modules are being developed incrementally. See the module README files and `docs/` for implementation notes.

## ML workstreams

### Resume, NLP and recommendation

1. Extract text from PDF resumes.
2. Identify skills using a baseline skill vocabulary.
3. Match extracted skills against society requirements.
4. Add semantic similarity with Sentence Transformers.
5. Rank candidates using documented, configurable weighted scoring.
6. Expose the pipeline through FastAPI endpoints.

### Performance and risk modelling

Performance prediction and probation-risk modelling are separate workstreams. Their training data, feature definitions, evaluation, and limitations should be documented before integration.

## Data and responsible use

- Do not commit private resumes, personal information, credentials, API keys, or real student records.
- Use synthetic or appropriately licensed/consented sample data during development.
- Keep synthetic and real datasets clearly separated.
- Treat similarity scores and recommendations as decision-support signals, not automatic selection decisions.
- Document model limitations and validate models before using them with real applicants.

## Collaboration

Use feature branches and pull requests rather than committing experimental work directly to `main`.

Suggested branches:
- `feature/ml-nlp`
- `feature/ml-performance`
- `feature/frontend`

## Current status

Initial repository structure and development documentation. Individual modules are under active development.
