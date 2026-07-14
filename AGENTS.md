# AGENTS.md

## Repository Purpose

Reference repository for migrating 58 classic Jupyter Notebook extensions (v4.x–5.x) to JupyterLab 4.x / Notebook 7.6.x. Contains a compatibility table and backup source code — no active development, build system, or tests.

## Structure

- `README.md` — compatibility table (58 extensions × NB7 + JupyterLab)
- `backup_extensions/` — original source code of all 58 extensions (JavaScript, CSS, YAML configs)

## Key Facts

- **No build/test/lint** — this is a documentation + backup repository
- **No Python package** — no setup.py, pyproject.toml, or package structure
- **Source language** — original extensions are vanilla JavaScript (RequireJS AMD modules), not TypeScript
- **Target for rework** — JupyterLab extensions use TypeScript + React, prebuilt via `copier` template

## If Reworking Extensions

```bash
# Create new JupyterLab extension from template
pip install "copier~=9.2" jinja2-time
copier copy --trust https://github.com/jupyterlab/extension-template .

# Build and install for development
pip install -e .
jupyter labextension develop --overwrite .
jlpm build
```

## Installed Extensions (WSL environment)

```bash
jupyter labextension list  # check what's installed
```

Working: jupyterlab-execute-time, jupyterlab-limit-output, jupyterlab-skip-traceback, jupyterlab-notifications, jupyterlab-spellchecker, jupyterlab-vim, jupyterlab-freeze, jupyterlab-rise, jupyterlab-code-formatter, jupyterlab-gridwidth, lckr-jupyterlab-variableinspector, python-lsp-server

Not compatible with JL 4.x: jupyterlab-autorun-cells (requires JL 3.x)

## Workflow

- Меняй README если надо исправить ошибки в описании
- ВСЕГДА пушь ВСЕ имеющиеся изменения сразу после внесения
