# Repository Guidelines

## Project Structure & Module Organization

This repository is a Jekyll site based on the al-folio academic theme. Site-wide settings live in `_config.yml`. Editable page content belongs in `_pages/`, project entries in `_projects/`, publication records in `_bibliography/papers.bib`, and structured profile data in `_data/`. Reusable Liquid components and page templates are under `_includes/` and `_layouts/`; custom Ruby extensions live in `_plugins/`. Styles are organized in `_sass/`, while images, JavaScript, PDFs, notebooks, and other static files belong in `assets/`. Jekyll generates `_site/`; do not commit generated output.

## Build, Test, and Development Commands

- `bundle install` installs Ruby and Jekyll dependencies from `Gemfile.lock`.
- `npm install` installs Prettier and its Liquid plugin.
- `bundle exec jekyll serve` builds the site and starts a local development server with live reload.
- `bundle exec jekyll build` performs the production-style build used by CI.
- `docker compose up` serves the site in the provided container at `http://localhost:8080`.
- `npx prettier . --check` verifies formatting; use `npx prettier . --write` to apply fixes.

## Coding Style & Naming Conventions

Use two-space indentation in YAML, Markdown front matter, HTML/Liquid, CSS/SCSS, and JavaScript. Follow existing Jekyll front-matter patterns and keep keys lowercase with underscores where applicable. Name content files descriptively in lowercase, using hyphens for pages and the existing numbered pattern for projects (for example, `_projects/10_new-project.md`). Prettier is configured in `.prettierrc` with a 150-character line width, ES5 trailing commas, and Liquid support. Avoid editing vendored or minified files unless intentionally updating the upstream asset.

## Testing Guidelines

There is no unit-test suite. Treat a clean Jekyll build as the primary validation step. Before submitting changes, run `bundle exec jekyll build` and `npx prettier . --check`, then inspect affected pages locally. Verify new links, images, bibliography keys, and responsive layout. CI also runs deployment builds, accessibility checks, and offline broken-link checks.

## Commit & Pull Request Guidelines

Recent history uses short, imperative summaries such as `Add paper` and `Update CV and bib`. Keep commits focused and state the affected content clearly. Pull requests should explain the change, identify modified pages or data files, and link a relevant issue for bugs or features. Include before/after screenshots for visual changes and note the validation commands run. Do not include `_site/`, caches, or unrelated formatting changes.
