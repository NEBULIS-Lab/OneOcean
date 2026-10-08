# Web Documentation

`docs/` contains the public website sources served by GitHub Pages.

- `index.html`: primary project website for the paper and public release.
- `platform/index.html`: platform/data usage page with a static GitHub-Pages explorer for a lightweight current-field subset.
- `demo/`: integrated interactive demo, task demos, and six-task overview.
- `oneocean_appendix.pdf`: standalone copy of the appendix, retained for existing links.
- `oneocean_paper.pdf`: complete paper with the original and expanded appendix, linked from the project website.
- `static/`: website assets (logo, copied paper figures, demo media, CSS, JavaScript, and the exported web-data subset under `static/data/`).

Local preview:

```bash
cd docs
python -m http.server 8000
```

To rebuild the platform explorer dataset from a local `combined_environment.nc`:

```bash
python tools/export_platform_web_data.py \
  --input /path/to/combined_environment.nc
```

## Deployment

The repository is published at https://nebulis-lab.github.io/OneOcean/.
The project page, platform guide (`platform/`), and demo (`demo/`) are deployed together from `docs/` by `.github/workflows/pages.yml` on pushes to `main`.
In repository Settings → Pages, select **GitHub Actions** as the source.
The paper and appendix PDFs are published from the current author-attributed manuscript.

Published entry points:

- [Project website](https://nebulis-lab.github.io/OneOcean/)
- [Platform guide](https://nebulis-lab.github.io/OneOcean/platform/)
- [Interactive demo](https://nebulis-lab.github.io/OneOcean/demo/)
- [Task demos](https://nebulis-lab.github.io/OneOcean/demo/tasks.html)
- [Paper](https://nebulis-lab.github.io/OneOcean/oneocean_paper.pdf)
- [Supplementary appendix](https://nebulis-lab.github.io/OneOcean/oneocean_appendix.pdf)

The demo, screenshots, and task pages are maintained directly in `docs/demo/` as part of this repository.
