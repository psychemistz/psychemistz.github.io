# psychemistz.github.io

Source for [psychemistz.github.io](https://psychemistz.github.io), the personal
academic site of Seongyong Park (Cancer Data Science Laboratory, NCI/CCR, NIH).

## Layout

| Path | Contents |
|------|----------|
| `_pages/` | Home, Research, Publications, 404 |
| `_data/navigation.yml` | Top navigation |
| `_config.yml` | Site and author settings |
| `CV/` | Awesome-CV LaTeX sources (excluded from the built site) |
| `files/cv.pdf` | Published CV, built from `CV/` |
| `images/` | Figures used by the Research page |

## Building the site

```sh
bundle install
bundle exec jekyll serve
```

## Building the CV

Requires XeLaTeX. From `CV/`:

```sh
xelatex cv.tex && xelatex cv.tex   # twice, for the page references
cp cv.pdf ../files/cv.pdf
```

`cv.tex` pulls its sections from `CV/resume/`. The fonts in `CV/fonts/` are
vendored so the build does not depend on system font installation.

## Credits

Built on the [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes)
Jekyll theme by Michael Rose (MIT). The CV uses
[Awesome-CV](https://github.com/posquit0/Awesome-CV) by Claud D. Park
(CC BY-SA 4.0), with local modifications noted in `awesome-cv.cls`.
