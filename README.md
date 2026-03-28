<div align="center">

# 🎱 Soc Ops

### Social Bingo for Real-World Mixers

*Break the ice. Find your people. Get five in a row.*

[![Python](https://img.shields.io/badge/Python-3.13-3776AB?logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.115-009688?logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![HTMX](https://img.shields.io/badge/HTMX-powered-3d72d7)](https://htmx.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

</div>

---

## What is Soc Ops?

**Soc Ops** is a live social bingo game designed for in-person events, workshops, and mixers. Each player gets a unique randomized 5×5 bingo card filled with prompts like *"has lived in another country"* or *"can juggle"*. Mingle with the room, find people who match, and mark your squares — first to get five in a row wins!

This repo doubles as a **hands-on GitHub Copilot lab** — the app is intentionally simple so you can focus on practicing AI-assisted development workflows.

---

## ✨ Features

- 🎲 **Randomized boards** — every player gets a unique card, no two alike
- 🆓 **Free space** — center square pre-marked, just like classic bingo
- ⚡ **Instant updates** — HTMX-powered UI with no page reloads
- 🏆 **Bingo detection** — rows, columns, and both diagonals all count
- 📱 **Mobile-friendly** — works great on phones at in-person events
- 🔄 **Easy reset** — start a fresh game anytime without losing your session

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | [FastAPI](https://fastapi.tiangolo.com) + [Uvicorn](https://www.uvicorn.org) |
| Templating | [Jinja2](https://jinja.palletsprojects.com) |
| Interactivity | [HTMX](https://htmx.org) |
| Data validation | [Pydantic](https://docs.pydantic.dev) |
| Linting | [Ruff](https://docs.astral.sh/ruff/) |
| Testing | [Pytest](https://pytest.org) |
| Package manager | [uv](https://docs.astral.sh/uv/) |

---

## 🚀 Quick Start

```bash
# Install dependencies
uv sync

# Run the app
uv run soc-ops
```

Then open **http://localhost:8000** in your browser. Share the URL with your group — each visitor gets their own independent bingo card!

If you want guided setup and workshop context, start at **[Part 00: Overview](https://copilot-dev-days.github.io/agent-lab-python/step.html?step=00-overview)**.

---

## 🧪 Development

```bash
# Lint
uv run ruff check .

# Test
uv run pytest
```

### Architecture at a glance

- [app/main.py](app/main.py): FastAPI routes and template wiring
- [app/game_service.py](app/game_service.py): Session orchestration
- [app/game_logic.py](app/game_logic.py): Pure board and bingo rules
- [app/models.py](app/models.py): Data models
- [app/templates/](app/templates/): Jinja2 templates
- [app/static/css/app.css](app/static/css/app.css): App styling

---

## 📚 Lab Guide

| Part | Title |
|------|-------|
| [**00**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview) | Overview & Checklist |
| [**01**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=01-setup) | Setup & Context Engineering |
| [**02**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=02-design) | Design-First Frontend |
| [**03**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=03-quiz-master) | Custom Quiz Master |
| [**04**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=04-multi-agent) | Multi-Agent Development |

> 📝 Lab guides are also available in the [`workshop/`](workshop/) folder for offline reading.

---

## 🤝 Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) and [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) before submitting a pull request.
