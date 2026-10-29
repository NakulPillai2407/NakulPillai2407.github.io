# Holdout Research

Source for https://nakulpillai2407.github.io: an independent systematic strategy research lab (personal project), built with MkDocs Material.

## Local preview

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve
```

## Adding a strategy

1. Copy `templates/strategy-template.md` to `docs/strategies/<name>.md` and give it the next reference (HR-004, ...).
2. Fill in each section and add it to `nav` in `mkdocs.yml` as `HR-NNN Name`.
3. Add a row to `docs/strategies/index.md`, `docs/index.md` and `docs/research-log.md`.
4. Push to `main`; the site deploys automatically.
