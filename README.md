# Soc Ops

Soc Ops is a fast, social bingo game for in-person events.
You meet people, match prompts, and race to complete a line before anyone else.

Built as a hands-on GitHub Copilot workshop app, it is intentionally simple to run and easy to redesign.

## Why This Project Is Fun

- Live, interactive gameplay powered by HTMX with no frontend build pipeline
- FastAPI + Jinja2 architecture that is easy to understand and extend
- Clean separation between HTTP routes, session orchestration, and pure bingo logic
- Great for workshops, hack sessions, onboarding, and AI-assisted coding demos

## Quick Start

1. Install [uv](https://docs.astral.sh/uv/)
2. Sync dependencies

	```bash
	uv sync
	```

3. Run the app

	```bash
	uv run uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
	```

4. Open http://localhost:8000

## Developer Checklist

Run these before committing:

```bash
uv run ruff check .
uv run pytest
```

## Architecture At A Glance

- [app/main.py](app/main.py): FastAPI routes and template wiring
- [app/game_service.py](app/game_service.py): Session-level game orchestration
- [app/game_logic.py](app/game_logic.py): Pure bingo board and win rules
- [app/models.py](app/models.py): Data models
- [app/templates/](app/templates/): Jinja2 UI templates
- [app/static/css/app.css](app/static/css/app.css): App styling

## Workshop Path

| Part | Title |
|------|-------|
| [00](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview) | Overview & Checklist |
| [01](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=01-setup) | Setup & Context Engineering |
| [02](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=02-design) | Design-First Frontend |
| [03](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=03-quiz-master) | Custom Quiz Master |
| [04](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=04-multi-agent) | Multi-Agent Development |

Offline workshop notes are available in [workshop/](workshop/).

## Build Something On Top

Try one of these extensions:

- Custom question packs by event type (hackathon, onboarding, conference)
- Team mode with shared boards
- Leaderboard and timed rounds
- Theme packs for branded events
