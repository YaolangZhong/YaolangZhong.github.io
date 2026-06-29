# yaolang-zhong.com

Personal academic website for **Yaolang Zhong** — Project Lecturer, Graduate School of
Economics, University of Tokyo (東京大学大学院経済学研究科 特任講師).

Plain static site (HTML/CSS/JS, no build step), hosted on GitHub Pages.

## Structure

Run `tree -L 2` to see the layout. Key files:

- `index.html` — the entire single-page site (About, Research, Teaching, CV, Contact).
- `assets/css/style.css` — all styling.
- `assets/js/main.js` — mobile nav toggle + footer year.
- `assets/img/profile.jpg` — profile photo (add this file; a "YZ" monogram shows until you do).
- `assets/cv.pdf` — CV download, generated from `CV/main.tex`.
- `CV/main.tex` — LaTeX source of the CV; run `make` in `CV/` to rebuild + sync the PDF.

> The custom domain `yaolang-zhong.com` is no longer served from this repo — it 301-forwards
> to `yaolangzhong.github.io` at the registrar. No `CNAME` file is needed.

## Editing content

Everything is plain HTML in `index.html` — edit the relevant `<section>`. To add a
publication, copy a `<li class="pub">…</li>` block in the Research section and fill it in.

## Local preview

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Deployment

Hosted via GitHub Pages from the repository's default branch. Pushing to the default
branch publishes the site. See the deployment notes shared during setup for DNS / custom
domain steps.
