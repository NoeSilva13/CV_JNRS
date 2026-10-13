# CV — Javier Noé Ramos Silva

LaTeX CV. Each push to `main` compiles the PDF and publishes it at a link that does not change.

## Links

- Page: https://noesilva13.github.io/CV_JNRS/
- PDF: https://noesilva13.github.io/CV_JNRS/CV_JNRS.pdf

The page redirects to the PDF. The link-preview title and description (LinkedIn, Slack, messages) come from `index.html`. The direct PDF link opens the file only.

## Update the CV

1. Edit `CV_JNRS.tex`. Publications live in `citations.bib`.
2. Push to `main`.

The action in `.github/workflows/build.yml` compiles the LaTeX and publishes `CV_JNRS.pdf` and `index.html` on the `build` branch. A few minutes later, the same links serve the new version.

The local `build/` folder is LaTeX Workshop output on your machine. Git ignores it. GitHub generates the public PDF, not that local file.

## Publishing

One-time repository setup:

1. **Settings → Actions → General → Workflow permissions:** Read and write permissions. The action needs to write the `build` branch.
2. **Settings → Pages:** Deploy from a branch, branch `build`, folder `/ (root)`. The branch appears after the first successful workflow run.

The repository must be public for GitHub Pages to serve the site.

## Origin

The layout comes from [autoCV](https://github.com/jitinnair1/autoCV) by Jitin Nair.
