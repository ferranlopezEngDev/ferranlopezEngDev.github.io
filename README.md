# ferranlopezEngDev.github.io

This repository contains the source files for my personal engineering portfolio website.

The site is built with MkDocs Material and published with GitHub Pages at `https://ferranlopezengdev.github.io`.

The portfolio is intended to document a developing profile at the intersection of mechanical engineering, computational engineering, CAD/CAE workflows, numerical simulation, technical automation, and engineering software.

## What This Repository Contains

- MkDocs source files under `docs/`
- Site configuration in `mkdocs.yml`
- Minimal Python dependency definition in `requirements.txt`
- Portfolio content focused on projects, tools, technical notes, reports, and profile pages

The editable source stays on `main`. The generated static site is deployed to `gh-pages`.

## Local development

Create a virtual environment, install the dependencies, and run MkDocs locally:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
mkdocs serve
```

The local development server is available at `http://127.0.0.1:8000`.

## Build

Use strict mode to validate the site before publishing:

```bash
mkdocs build --strict
```

## Deploy

Deploy the generated site to the `gh-pages` branch with:

```bash
mkdocs gh-deploy --force
```

`main` should keep the source files. `gh-pages` should contain the generated HTML managed by MkDocs.

## Repository Structure

```text
.
├── README.md
├── mkdocs.yml
├── requirements.txt
└── docs/
    ├── index.md
    ├── about.md
    ├── projects/
    │   ├── index.md
    │   ├── hn3ttk.md
    │   ├── uav-cae-learning-lab.md
    │   ├── structural-automation-lab.md
    │   ├── cad-cae-workflows.md
    │   ├── geometry-rotations.md
    │   └── computational-engineering-notes.md
    ├── technical-notes/
    │   └── index.md
    ├── tools/
    │   └── index.md
    ├── reports/
    │   └── index.md
    ├── cv.md
    └── contact.md
```

## Notes

- The portfolio is intentionally conservative in tone: active development, academic work, learning exercises, and planned work are clearly distinguished.
