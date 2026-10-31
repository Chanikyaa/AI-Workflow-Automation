# AI Workflow Automation

An AI-assisted workflow automation system for processing support events, managing workflow states, handling retries, and routing sensitive cases for human review.

## Overview

This project demonstrates how AI-assisted automation can be combined with reliable backend workflow engineering.

The system processes incoming support events using deterministic rules and a mock response provider, while maintaining persistence and recovery capabilities.

## Key Features

- Automated support event processing.
- Workflow state management.
- SQLite persistence.
- Idempotent event processing.
- Retry and recovery handling.
- Human review for sensitive cases.
- Mock response provider.
- CLI-based workflow execution.
- Automated testing.

## Architecture

```text
        Incoming Support Event
                  |
                  v
          Event Processing
                  |
                  v
          Workflow Engine
                  |
          +-------+-------+
          |               |
          v               v
     Rule Evaluation   Idempotency
          |               |
          +-------+-------+
                  |
                  v
          Automation Logic
                  |
          +-------+-------+
          |               |
          v               v
      Auto Process    Human Review
          |               |
          +-------+-------+
                  |
                  v
           SQLite Storage
                  |
                  v
          Workflow Result
```

## Technology Stack

- Python
- SQLite
- Rule-based automation
- Mock AI response provider
- Pytest
- CLI workflows

## Project Structure

```text
support-workflow-automation/
│
├── src/
├── tests/
├── data/
├── requirements.txt
├── README.md
└── .gitignore
```

*Check the actual project files for the complete structure.*

## Installation

```bash
git clone https://github.com/Chanikyaa/support-workflow-automation.git
cd support-workflow-automation

python -m venv .venv
```

Activate the environment:

**Windows**
```bash
.venv\Scripts\activate
```

**Linux/macOS**
```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## Running the Project

Use the CLI entry point provided by the repository to process the included sample events.

Refer to the source code for the exact command and available arguments.

## Core Engineering Concepts

- Workflow orchestration
- Event-driven processing
- Idempotency
- Retry and recovery mechanisms
- SQLite persistence
- Human-in-the-loop review
- Deterministic automation
- Error handling

## Current Validation

- Automated tests: **10 passed**.
- CLI smoke test successfully processed **3 sample events**.
- SQLite persistence, idempotency, retry/recovery, and human-review paths are covered by the project tests.

## Limitations

- The current response provider is a mock implementation.
- Workflow decisions use deterministic heuristics.
- No real external support-system actions have been verified.
- Docker and hosted CI have not been verified.

## Future Improvements

- Integrate real LLM providers.
- Connect email and ticketing platforms.
- Add workflow scheduling.
- Implement a monitoring dashboard.
- Add role-based access control.
- Deploy as a cloud-based automation service.

## Author

**Palli Chanikya Paidi Balaji**

B.Tech – VIT Chennai (2025)  
M.Tech CSE – AI & Data Science, Mahindra University (2026–2028)

GitHub: [@Chanikyaa](https://github.com/Chanikyaa)

---

*Part of an AI/ML Engineering Portfolio.*
