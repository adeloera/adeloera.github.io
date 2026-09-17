# andresdeloera.com

Personal academic website of Andrés de Loera, built with [Jekyll](https://jekyllrb.com/) and Bootstrap 5 and hosted on GitHub Pages (custom domain set in `CNAME`). Pushing to `master` publishes the site.

## Where things live

| To change | Edit |
|---|---|
| Home page text: recruiting notice, bio, selected work | `_pages/home.md` |
| Research page: titles, abstracts, PDF links, status labels | `_pages/research.md` |
| Teaching page | `_pages/teaching.md` |
| Blog page | `_pages/blog.md` |
| Name, title, affiliations and contact buttons in the home-page header | `_data/pi.yml` |
| Site title, email, footer text, navigation-bar links | `_config.yml` |
| Paper PDFs | `papers/` |
| CV PDF, syllabi, teaching evaluations | `documents/` |
| CV LaTeX source (not published) | `_cv/deLoera_cv.tex` |
| Colors and fonts | `assets/main.scss` (Bootstrap variables) and `_sass/site.scss` |
| Page templates | `_layouts/`, `_includes/` |

Folders whose names start with an underscore (`_cv`, `_data`, `_includes`, ...) are never copied to the published site unless listed under `include:` in `_config.yml`.

## Updating the CV

Edit `_cv/deLoera_cv.tex`, then rebuild the PDF and copy it into `documents/`:

```
cd _cv
pdflatex deLoera_cv.tex && pdflatex deLoera_cv.tex
cp deLoera_cv.pdf ../documents/deLoera_cv.pdf
```

## Adding a paper

1. Put the PDF in `papers/`.
2. Copy one of the `<article class="paper">` blocks in `_pages/research.md` and edit the title, coauthors, status label, abstract and link.
3. Optionally add it to "Selected work" in `_pages/home.md` and to the CV.

## Previewing locally

```
bundle install
bundle exec jekyll serve
```

Then open <http://127.0.0.1:4000/>.
