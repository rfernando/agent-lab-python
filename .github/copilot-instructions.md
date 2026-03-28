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

## Design Guide
- Treat the UI as a product surface, not a placeholder. Favor strong visual direction over generic layouts.
- Use distinctive typography choices and avoid default-looking font stacks.
- Define and reuse CSS variables for theme tokens (color, spacing, radius, shadows, motion timing).
- Build atmosphere with layered backgrounds (gradients, patterns, shape overlays) rather than flat color fills.
- Keep motion intentional and moderate: prioritize page-entry and key state transitions over excessive micro-animations.
- Maintain responsive quality on mobile and desktop; preserve readable text and comfortable tap targets.
- Preserve existing app behavior and HTMX wiring unless explicitly requested otherwise.
- When redesigning screens that are covered by tests, keep required UI text and interaction hooks stable.
- If adding new CSS utilities or component classes, keep naming consistent and specificity low.
