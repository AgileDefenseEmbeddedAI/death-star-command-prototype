# Prototype guide for Claude Code

Autonomous AI-powered Death Star command system with real-time threat assessment, tactical recommendations, and human command override for Galactic Empire operations.

The source PRD / Epic: https://bytecubed.atlassian.net/browse/AL-372

## How this repo works

Each ticket for this prototype is filed as a GitHub issue. When an issue is opened,
the workflow in `.github/workflows/claude.yml` runs you (Claude Code) to implement it
and open a pull request. Work one issue at a time and keep every change runnable.

## Tech stack & conventions

Python 3.11+ backend (FastAPI for sub-second latency), React 18 frontend for command interface. Use SQLite for engagement history and threat data. Mock Death Star sensors and Rebel movement feeds via simulation. Implement agent decision loops with configurable autonomy thresholds. All inter-service communication encrypted (TLS). Deploy as containerized stack (Docker) with monitoring via Prometheus + Grafana. Run locally: `docker-compose up` for full system. Use pytest for unit/integration tests, ab/wrk for latency validation.

## Working agreement

- Build the simplest thing that satisfies the issue's acceptance criteria — this is a
  prototype, not production. Favor a working end-to-end slice over breadth.
- Keep the project runnable at every step. Document any new setup/run command in the
  README under a "Running" section.
- Open one pull request per issue and reference the issue with "Closes #<number>".
- Don't introduce secrets or external services that require credentials the repo
  doesn't have.
