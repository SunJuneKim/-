# AGENTS.md

## Cursor Cloud specific instructions

This repository is **content only**: it contains Korean-language career-preparation
documents (Markdown) targeting a job at 포티투닷 (42dot). See `README.md` for the
directory layout and intended workflow.

- **No application, services, dependencies, build system, tests, or linters exist.**
  The entire repo is Markdown (`docs/`, `projects/`, `resume/`, `questionnaire/`,
  `README.md`). There is nothing to `npm install` / `pip install`; the update script
  is intentionally a no-op.
- **Nothing to run, lint, test, or build.** Do not fabricate build/test tooling.
  Just edit the Markdown files directly.
- **Optional local preview** (not required, not committed): the docs render as plain
  GitHub-Flavored Markdown. To preview in a browser you can install a renderer
  ad-hoc (e.g. `pip install --user markdown`) and serve rendered HTML with
  `python3 -m http.server`. This tooling is not part of the repo — do not add it to
  the update script.
- Content is in Korean by design; keep new content consistent with the existing docs.
