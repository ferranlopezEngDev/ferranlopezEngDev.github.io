# ferranlopezEngDev.github.io

This repository contains the source files for my personal engineering portfolio website.

The site is built with MkDocs Material and is intended to be published with GitHub Pages at `https://ferranlopezengdev.github.io`.

The portfolio presents a professional engineering profile focused on mechanical engineering, computational tools, CAD/CAE workflows, simulation, automation, engineering software, and technical documentation.

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

## Build validation

Use strict mode before publishing:

```bash
mkdocs build --strict
```

## GitHub Pages deployment

Deploy the generated site to the `gh-pages` branch with:

```bash
mkdocs gh-deploy --force
```
