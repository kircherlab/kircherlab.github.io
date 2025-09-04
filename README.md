# kircherlab.github.io

Kircher Lab Website: Computational Genome Biology at BIH and Regulatory Genomics group at UKSH

## Creating HTML files from "templates"

- Pretty much all pages were using the same header, banner and footer and it was difficult to keep them consistant
- Therefore, the actual page content was separated from these files in the templates folder
- Please edit files in templates
- A GuitHub action will automatically create the HTML files from the templates, after pushed to the master branch, and commit them to the repository
- The Github action is defined in `.github/workflows/update-html.yml`
- Right now the following tmp files will be generated into HTML files:
  - `templates/404.tmp` → `404.html`
  - `templates/index.tmp` → `index.html`
  - `templates/impressum.tmp` → `impressum.html`
  - `templates/contact.tmp` → `contact.html`
  - `templates/people.tmp` → `people.html`
  - `templates/research.tmp` → `research.html`
  - `templates/projects.tmp` → `projects.html`
  - `templates/publications.tmp` → `publications.html`
  - `templates/IGVF_workshop_2024.tmp` → `IGVF_workshop_2024.html`
  - `templates/people/*.tmp` → `people/*.html`
  - `templates/projects/*.tmp` → `projects/*.html`
