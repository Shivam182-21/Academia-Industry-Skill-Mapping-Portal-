# Academia–Industry Skill Mapping and Placement Portal

**Smart India Hackathon 2026 · Problem Statement SIH26044 · Group G29**

A full-stack portal that maps university curriculum skills to industry job requirements, analyses student skill gaps, and recommends learning resources.

## Features

- Extract canonical skills from course descriptions, learning outcomes, and job descriptions using NLP.
- Map academic skills to industry requirements with exact and similarity-based matching.
- Calculate weighted student skill coverage and identify missing or partially covered skills.
- Recommend learning resources based on skill gaps.
- Provide dashboards for students, faculty, placement officers, employers, and administrators.
- Evaluate extraction performance against a labelled benchmark and a keyword baseline.

## Technology stack

- **Backend:** Python, FastAPI, Pydantic, SQLAlchemy, Uvicorn, JWT authentication
- **Database:** SQLite by default; PostgreSQL-ready configuration
- **NLP:** Regex-based skill extraction, canonical skill taxonomy, TF-IDF cosine similarity
- **Frontend:** React 18, Vite, Tailwind CSS, Lucide icons
- **Testing:** Pytest and HTTPX

## Quick start

### Requirements

- Python 3.9 or newer
- Node.js 18 or newer
- npm

### Start the backend

```bash
cd backend
pip install -r requirements.txt
python run.py
```

The API is served at `http://127.0.0.1:8000`. Interactive API documentation is available at `http://127.0.0.1:8000/docs`.

### Start the frontend

Open a second terminal:

```bash
cd frontend
npm install
npm run dev
```

Open the Vite URL printed in the terminal (normally `http://localhost:5173`).

### Run tests

From the project root:

```bash
pytest backend/tests/ -v
```

## Repository structure

```text
backend/          FastAPI application, NLP modules, database models and tests
frontend/         React application, dashboards, components and API client
docs/             Software requirements and architecture diagrams
project_report/  Project report and presentation deliverables
README.md         Project overview and setup instructions
```

## Documentation

- [Software Requirements Specification](docs/SRS.md)
- [Architecture diagrams](docs/architecture_diagrams.md)
- [Project report and presentation](project_report/)

## Notes

- Install frontend dependencies with `npm install`; the `node_modules` directory is intentionally not committed.
- The local SQLite database is not included. The application creates its database and seeds demonstration data at startup.
- Do not commit real credentials, API keys, or local environment files.

