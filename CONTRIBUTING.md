# Contributing to Neudata projects

Thank you for contributing! These guidelines apply to every repository in the [neu-data](https://github.com/neu-data) organisation unless a repository provides its own `CONTRIBUTING.md`.

## Principles

Our work rests on **scientific rigour, reproducibility, clarity, collaboration and capacity strengthening**. Every contribution should leave the project easier to review, rerun and understand.

## Workflow

1. **Open or pick an issue** using one of our templates, so work is discussed before it starts.
2. **Create a branch** from `main` using a descriptive prefix:
   - `feat/…` new analysis, feature or output
   - `fix/…` bug fix
   - `data/…` data cleaning or quality-control changes
   - `docs/…` documentation
   - `chore/…` tooling, CI, dependencies
3. **Commit small, focused changes** with clear messages in the imperative mood, e.g. `Add Kaplan–Meier plot for secondary outcome`.
4. **Open a pull request** and complete the checklist in the template.
5. **Request review** from at least one other team member. Statistical analyses that feed client deliverables should be independently checked (code review or double-programming).
6. **Squash and merge** once approved and checks pass.

## Coding standards

### R

- Follow the [tidyverse style guide](https://style.tidyverse.org/); format with `styler` and lint with `lintr`.
- Manage dependencies with `renv` and commit `renv.lock`.
- Write functions in `R/`, test with `testthat`, document with `roxygen2`.

### Python

- Follow PEP 8; format and lint with `ruff`.
- Pin dependencies in `requirements.txt` or `pyproject.toml`.
- Test with `pytest`.

### General

- Use relative paths (`here::here()` in R, `pathlib` in Python) — never absolute paths to personal machines.
- Set random seeds for anything stochastic.
- Generate figures and tables from code; do not edit outputs by hand.
- Use the Neudata colour palette for figures (see [BRAND.md](BRAND.md)).

## Data handling

- **Never commit raw, personal, patient-level or confidential data.** Keep it in approved secure storage and reference it via configuration.
- Never commit credentials. Use environment variables or `.Renviron` / `.env` files that are git-ignored.
- If sensitive data is committed by mistake, **do not just delete it in a new commit** — contact the repository maintainers immediately so history can be cleaned and the incident handled under our data-protection obligations.

## Questions

Email [contact@neu-data.com](mailto:contact@neu-data.com) or open a discussion in the relevant repository.
