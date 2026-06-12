# WPI CHIPS Design Studio -- Lab Website

Source code for the [WPI CHIPS Design Studio](https://wpi-chips-design-studio.github.io/wpi-chips-lab/) website.

## Live Site

**https://wpi-chips-design-studio.github.io/wpi-chips-lab/**

## About

The CHIPS Design Studio, led by [Dr. Suat Ay](https://www.wpi.edu/people/faculty/suatay), conducts research on custom integrated circuits for biomedical and sensing applications at Worcester Polytechnic Institute. The lab also supports undergraduate capstone (MQP) projects involving chip design, tapeout, and characterization.

## Built With

- [Jekyll](https://jekyllrb.com/) static site generator
- [al-folio](https://github.com/alshedivat/al-folio) theme
- Hosted on [GitHub Pages](https://pages.github.com/)

## Editing the Site

| What to change | Where |
|---|---|
| Lab description / homepage | _pages/about.md |
| Publications | _bibliography/papers.bib |
| Team members | _pages/profiles.md |
| Projects | _projects/ |
| News | _news/ |
| Site settings (title, URL, etc.) | _config.yml |

## Local Development

`ash
bundle install
bundle exec jekyll serve
`

Then open http://localhost:4000/wpi-chips-lab/
