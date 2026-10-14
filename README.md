# Getting Started with IBM Bob and the Premium Package for i

A short, hands-on guide for new IBM Bob users on IBM i: developers, green-screen
programmers and administrators. Not a lab: a list of ideas to try, with a method
and example prompts for each.

- **Read it online:** https://bmarolleau.github.io/bob-ppi-prompt-guide/
- **Source:** [`src/bob-ppi-prompt-guide.md`](src/bob-ppi-prompt-guide.md)

## Layout

| Path | Purpose |
|---|---|
| `src/bob-ppi-prompt-guide.md` | The guide (edit this) |
| `src/redbook-template.html` | Pandoc template (Redbook-style look) |
| `src/build.py` | Refreshes the Markdown table of contents and generates `content/index.html` |
| `content/index.html` | Generated page, published as the site home |
| `mkdocs.yml`, `requirements.txt` | MkDocs project used to publish to GitHub Pages |

## Edit and rebuild

Requires Python 3 and [pandoc](https://pandoc.org/).

```sh
python3 src/build.py
```

## Preview and publish

MkDocs 1.6 needs Python 3.8 or newer. If your default `python3` is older, use a newer
interpreter to create the virtual environment.

```sh
python3 -m venv .venv && .venv/bin/pip install -r requirements.txt
.venv/bin/python -m mkdocs serve                  # local preview
.venv/bin/python -m mkdocs gh-deploy --strict     # publish to the gh-pages branch
```

In the repository settings, set **Pages** to deploy from the `gh-pages` branch, root (`/`).
Pushing to `main` alone does not publish.
