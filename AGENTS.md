# Repository instructions

## Project overview
- This is a Quarto manuscript for a DATA 510 data science capstone about identifying U.S. ZIP codes that may benefit from DER-powered microgrids.
- The manuscript entry point is `capstone.qmd`; it includes the numbered section files from `_01_abstract.qmd` through `_07_references.qmd`.
- Project configuration is in `_quarto.yml`. HTML output is written to `_output/`, with embedded resources enabled in the manuscript.

## Editing guidance
- Make manuscript changes in the relevant `.qmd` source file, not the generated `index.html` or files under `_output/`, unless explicitly asked to modify generated output.
- Preserve Quarto structure, including YAML front matter, `{{< include ... >}}` directives, fenced code chunks, chunk options, figure labels/captions, and citation keys.
- Code examples currently use both R and Python. Keep each chunk's language and dependencies intact unless the requested change requires otherwise.
- The analysis chunks read CSVs from a sibling `project-workbook-hayden_logan_m/shared_data/` directory. That data project is not part of this repository; do not assume its files or alter their paths without checking with the user or confirming the intended layout.
- Preserve the project's existing academic tone and distinguish observed results from limitations and future-work proposals.

## Build and validation
- Render the manuscript with Quarto CLI using `quarto render` from the repository root.
- A successful render depends on Quarto and the R/Python packages used by the chunks being available, and on the referenced sibling data files existing.
- After editing, check Quarto diagnostics/render output where available. Avoid committing incidental cache or generated-output changes unless they are part of the request.

## Repository hygiene
- `.gitignore` excludes Quarto output, the `.quarto` directory, Python virtual environments, `.env`, and `.Rhistory`; retain these exclusions.
- Do not add data, API tokens, credentials, or environment-specific paths to the repository.