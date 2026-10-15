# AGENTS.md

## Project

Static HTML/CSS portfolio — a student's "Advanced Web Design" (高级网页设计) coursework collection. No build tooling, no package manager, no tests, no CI.

## Structure

- `index.html` — landing page with links to all works
- Numbered HTML files (`2-1.html` through `10-4.html`) — standalone CSS technique demos (flexbox, grid, transitions, animations, selectors, etc.)
- `css.css` — minimal shared styles (only used by some pages)
- `img/` — image assets referenced by the HTML files
- `_backup/` — older versions of some demos
- `_shots/` — screenshot previews

## Conventions

- All content is in Chinese (zh-CN)
- Each demo file is self-contained with inline `<style>` — no external CSS framework
- Open any `.html` file directly in a browser to preview; no dev server needed
- File naming: `{lesson-number}-{demo-number}.html` (e.g., `6-1 flex.html` = lesson 6, demo 1, flexbox topic)

## Naming Rules

- All CSS class names, ID names, and JS variables must use the `guan_` prefix (e.g., `.guan_container`, `#guan_header`, `guan_count`)

## Prompt Logging

- Before executing any user prompt, append it to `guan_prompt.md` with the following format:
  - Timestamp (date + time)
  - Model used
  - Full prompt content
- Always append — never overwrite previous entries
- Format:
  ```
  ## [YYYY-MM-DD HH:MM] Model: {model-name}

  {prompt content}

  ---
  ```
