# Context

* This repo demonstrates a problem I'm having with Quarto and GitHub Pages.
* Structure of the repo includes a `code` directory -- stubbed out for this example but suffice it to say that a main use-case for me is going to be having repos with non-trivial amounts of code, along with docs documenting that code.
* I'm following https://quarto.org/docs/websites/publishing-websites.html#github-pages

# The problem
* GitHub Pages requires us to publish docs from the `docs` subdir of the repo, or the root of the repo -- no other choices
* `docs-source/_quarto.yml` lets me specify `output-dir: _site`
* If I do that then `quarto preview` and/or `quarto render` within `docs-source` both work fine. But they do not put docs where GitHub Pages wants them, i.e. in `docs`
* If I instead put `output-dir: ../docs` in my `docs-source/_quarto.yml` then `quarto preview` and `quarto render` both appear to do nothing.
* Also when I touch `.nojekyll` per the docs, regardless GitHub Pages is asking me to "choose a theme" for Jekyll.

How can I configure `_quarto.yml` to write doc artifacts into the `docs` directory which GitHub Pages requires?
