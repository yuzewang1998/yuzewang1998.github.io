 
# Yuze Wang's academic homepage

Static website for <https://yuzewang1998.github.io/>. No build step or JavaScript framework is required.

## Files

- `index.html`: biography, preprints, publications grouped by year, and academic services.
- `stylesheet.css`: typography and responsive layout.
- `images/`: portrait, publication figures, CV, and other existing assets.
- `takinglangsplatw/` and `GOI-Hyperplane/`: existing project pages with their own styles and assets.
- `.github/workflows/pages.yml`: GitHub Pages deployment workflow.

## Preview locally

From the repository directory, run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open <http://127.0.0.1:8000/>. If that port is occupied, choose another port.

## Update a publication

1. Edit or copy one `<article class="publication">` block in `index.html` under the appropriate year. Use a unique `id`.
2. Check the title, full author list, author order, venue, year, and links against the publisher or the authors' public materials. For conferences, use the conference year; Scholar may show a later indexing year. For journals, use the issue year where available.
3. Bold Yuze Wang in the author list. Preserve contribution markers according to the paper.
4. Add only working resource links. Omit unavailable Code or Data links.
5. If a verified paper image is available, place it under `images/` and add an image with meaningful alt text, `loading="lazy"`, and `decoding="async"`. Otherwise use `class="publication publication--text"` and omit the image.
6. Add a year heading and year-navigation link when needed. Keep the separate Preprints section before Selected Publications.
7. Update the footer's `<time datetime="YYYY-MM-DD">` value and visible date together.

Review desktop and mobile widths, check local assets and section anchors, and run `git diff --check` before publishing.

## Publish

The existing GitHub Actions workflow deploys the static repository on pushes to `master`, and also supports manual dispatch. Local edits or previewing the site do not publish them.

## Image attribution

`images/urban-gs-2026.png` is Figure 1 rendered from the authors' [CVPR 2026 open-access paper](https://openaccess.thecvf.com/content/CVPR2026/papers/Wang_Urban-GS_A_Unified_3D_Gaussian_Splatting_Framework_for_Compact_and_CVPR_2026_paper.pdf). Existing publication figures remain associated with their original papers.

`images/gsbrief-2026.png` and `images/visual-camera-localization-2026.png` were supplied by Yuze Wang for the GSBrief and TIP papers, respectively. Both files are preserved as supplied.

The original homepage template was adapted from [Yansong Qu's website](https://quyans.github.io/).
