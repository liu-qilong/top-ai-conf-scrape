# Top AI conferences scraping

This repository contains Jupyter notebooks to scrape **ALL PAPERS**' BibTeX from selected top conferences:

- [CVPR 2025](https://cvpr.thecvf.com/Conferences/2025)
- [ICLR 2025](https://iclr.cc/Conferences/2025)
- [NeurIPS 2024](https://neurips.cc/Conferences/2024)

You can find them in the `output/` folder:

- `<conf><year>.bib`: BibTeX files for each conference and year. For example, `iccv2023.bib` contains all papers from ICCV 2023.
- `<conf><year>.md`: accompanying the BibTeX files, Markdown files are also generated for easier reading, e.g. with Obsidian.

> **Paper abstracts** are included in the Markdown files, making it farily easy to skim through the papers. However, abstract are omitted from the BibTeX files, in case any special symbols causing issues with LaTeX compilation.

## About the notebooks

Since every conferences has its own website, one notebook is provided for each conference. Among them:

- NeurIPS, ICML, ICLR can be easily scraped via [OpenReview](https://openreview.net/)'s API. Therefore, these notebooks are very similar. Please noted that to run these notebooks, you need to add a `.env` file under the repo folder with:

```
username='<your OpenReview username>'
password='<your OpenReview password>'
```

- CVPR, ICCV, ECCV has to be scraped with from each conference's website. Publication type (oral/highlight/poster) info has to be scraped from specific pages. Therefore , these notebooks are more complex.

It should be relatively easy to adapt these notebooks to scrape other conferences, as long as they have a similar structure.