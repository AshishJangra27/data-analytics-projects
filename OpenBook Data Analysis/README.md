# OpenBook Data Analysis — Shelves, Authors & Trends

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1hyxuOfKfjBD1uIJTB1BfLD81_ycCEPCr?usp=sharing)


**Overview:** End-to-end analysis of the OpenBook corpus to quantify catalog size, normalize metadata, and surface reading-engagement signals (Want-to-Read, Currently-Reading, Have-Read) across authors, categories, and years.

## Workflow
1. **Ingest** — Clone `datasets/OpenBook`, read all CSVs, concatenate to a single DataFrame.
2. **Clean** — Drop heavy text/URL fields; remove nulls/dupes using normalized `title_id`.
3. **Standardize** — Parse `publish_year` → int (1201–2023), extract `author_id` from paths.
4. **Engineer** — Parse `book_stats` → numeric `pages` (cap `<2000`), split `reading_stats` into three counts.
5. **Descriptives** — Report unique titles; Top-25 **categories** and **authors** (by book count); **yearly** publication trend; most common **titles**; authors by total **pages**.
6. **Engagement View** — Aggregate shelves by author; interactive **100% stacked horizontal** chart with a **Share↔Counts** toggle, color-blind-safe palette, labeled totals.

## Key Insights
- Distributions are **long-tailed**: a few authors dominate volume and intent.
- **Want-to-Read** generally exceeds **Have-Read**, signaling high prospective interest vs. completions.
- Notable outliers (e.g., very high “want” concentration) skew grouped-bar views—resolved via %-share faceting.

## Tech Stack
- Python, **pandas**, **NumPy**
- **Plotly** (Express & Graph Objects), `tqdm`

## Next Steps
- Canonicalize author variants; normalize category taxonomy.
- Add per-author rates (reads per title), cohort trends by decade/genre.
- Build simple recommenders from shelf signals; include class-wise metrics and confusion matrices for any downstream models.
