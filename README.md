# Ronaldo's Printing Shop — Prototype

Prototype FastAPI backend created from `Dasigan_RG_PRD.txt`.

Assumptions
- The PRD specifies a FastAPI backend and "without the need for a persistent database"; this prototype uses an in-memory store with an optional JSON export controlled by the env var `PRINTING_API_PERSIST`.
- Basic features: accept orders, compute totals, list and retrieve orders.

Quick run

1. Create a virtualenv and install deps:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

2. Run the dev server:

```bash
uvicorn printing_api.main:app --reload
```

3. Open interactive docs: http://127.0.0.1:8000/docs

Run tests

```bash
pytest -q
```

Next steps
- Add optional persistence via SQLite or a small admin UI for order management.
- Add authentication for staff endpoints.
- Improve validation and pricing rules (discounts, tax, shipping).
