# Project Guidelines

## Mandatory Development Checklist
- [ ] Lint: `uv run ruff check .`
- [ ] Build: `uv sync`
- [ ] Test: `uv run pytest`

## Architecture
- FastAPI + Jinja2 + HTMX app for social bingo.
- Keep HTTP routes and template wiring in `app/main.py` and `app/templates/`.
- Keep session orchestration in `app/game_service.py`.
- Keep pure board and bingo rules in `app/game_logic.py`.
- Keep data models in `app/models.py` and question data in `app/data.py`.

## Conventions
- Keep route handlers thin; move domain behavior into service/logic modules.
- Preserve immutable update patterns in game logic (avoid in-place model mutation).
- Preserve board invariants: 5x5 board, center free square pre-marked, rows/columns/diagonals all valid bingo lines.
- Add focused tests in `tests/test_api.py` and/or `tests/test_game_logic.py` for behavior changes.

## References
- Setup and overview: `README.md`
- Workshop guidance: `workshop/GUIDE.md`
- Existing style/design instructions: `.github/instructions/`
