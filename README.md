# Mini-Research-Agent

[![Python](https://img.shields.io/badge/python-3.11-blue)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-3.0-green)](https://fastapi.tiangolo.com/)
[![React](https://img.shields.io/badge/React-18-blue)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue)](https://www.typescriptlang.org/)

A lightweight research assistant for developers. Mini-Research-Agent combines automated code review, analysis workflows, and visual findings tracking in a modular Python + FastAPI backend with a React + Vite frontend.

## Overview

Mini-Research-Agent is built to make research workflows easier to explore and review. The backend handles data ingestion, pipeline analysis, and API delivery. The frontend focuses on displaying findings, sessions, and telemetry in a clean, interactive UI.

## Features

- Automated code review and issue discovery
- Analysis pipelines for structured evaluations
- Findings visualization in the browser
- Telemetry and session tracking for research workflows
- Modular backend / frontend separation for easier extension

## Tech stack

| Layer | Technology |
|---|---|
| Backend | Python, FastAPI |
| Frontend | React, Vite, TypeScript |
| API | REST endpoints |
| Deployment | Local dev / container-ready |

## Folder structure

```text
├── backend/             # FastAPI services: ingestion, analysis, API
├── frontend/            # React + Vite application
├── docs/                # Design notes, architecture references
├── scripts/             # Setup and helper scripts
└── README.md            # Project overview and quickstart
```

> Update these paths if your repository layout differs.

## Quickstart

1. Clone the repository:

```bash
git clone https://github.com/<username>/Mini-Research-Agent.git
cd Mini-Research-Agent
```

2. Start the backend:

```bash
cd backend
python -m venv .venv
source .venv/Scripts/activate  # Windows
pip install -r requirements.txt
uvicorn main:app --reload
```

3. Start the frontend:

```bash
cd ../frontend
npm install
npm run dev
```

4. Open the app at `http://localhost:5173`.

## API examples

### Get analysis summary

```bash
curl http://localhost:8000/api/analysis/summary
```

### Create a new session

```bash
curl -X POST http://localhost:8000/api/sessions \
  -H "Content-Type: application/json" \
  -d '{"project": "example", "notes": "Initial scan"}'
```

### List findings

```bash
curl http://localhost:8000/api/findings
```

## Architecture

The backend is responsible for:

- Ingestion: collecting and preparing input data
- Analysis: running pipeline stages and generating findings
- API: exposing results and session metadata to the UI

The frontend is responsible for:

- Rendering analysis results
- Showing session history and telemetry
- Making findings easy to scan and explore

## Future improvements

- Add user authentication and session management
- Support plugin-based analysis stages
- Add export options for findings and reports
- Improve filtering and search in the UI

## Contribution

Contributions are welcome. If you want to help:

- Open an issue for bugs or enhancements
- Create a pull request with a clear summary
- Keep changes focused and easy to review

## License

This project is available under the MIT License if a `LICENSE` file is included.
