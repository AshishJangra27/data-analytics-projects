# GeeksforGeeks Articles Analysis — Trends, Categories & Visuals

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1J9BRG8lhEnxRr20Tt2LmuAgI1qrxQhRN?usp=sharing)

**Overview:** An end-to-end analytical exploration of the GeeksforGeeks article repository to quantify content growth, analyze the consistency of technical pillars, and evaluate visual engagement patterns across different programming domains from 2014 to 2025.

## Workflow
1.  **Ingest** — Load the `gfg_articles_clean_data_for_dashboarding.csv` dataset directly from the source repository.
2.  **Preprocess** — Parse publication dates to extract granular temporal data including `last_updated_year`, `month`, and `day_of_week`.
3.  **Categorize** — Identify and isolate unique content tags (`clean_tags`) to understand the breadth of topics.
4.  **Temporal Analysis** — Track the year-over-year growth of unique categories to measure platform diversification.
5.  **Consistency Mapping** — Filter and aggregate the top 5 most consistent categories between 2020 and 2025 to identify core content staples.
6.  **Thematic Grouping** — Consolidate thousands of niche tags into broader thematic clusters like "Programming Languages," "Web Development," and "DSA" for high-level volume analysis.
7.  **Visual Evaluation** — Analyze the `no_of_images` field across tags to determine the visual density of different content types.

## Key Insights
* **Exponential Diversification**: The number of unique content tags skyrocketed from approximately 160 in 2022 to over 400 by 2025, marking a rapid expansion in topic breadth.
* **Dominant Pillars**: "Programming Languages" is the largest theme by volume with 44,133 articles, followed by "Web Development" and "Interview/Career" content.
* **High-Interest Clusters**: "Interview Experiences" and "Web Technologies" consistently account for nearly 15% of the primary content output each.
* **Visual Needs**: Categories such as "Installation Guides" and "Web Tech" exhibit high image density (over 90%), while code-heavy topics like "Scala" average near 0% image usage.
* **Language Leadership**: Python is identified as the most popular programming language on the platform, significantly surpassing JavaScript and Java in article volume.

## Tech Stack
* **Python**
* **pandas**, **NumPy**
* **Matplotlib**, **Seaborn**
* **Plotly** (Graph Objects)

## Next Steps
* Perform deeper correlation analysis between article update frequency and reader engagement signals.
* Implement time-series forecasting to predict the emergence of new technical categories.
* Automate the broader thematic grouping using Natural Language Processing (NLP) for more granular taxonomy.
* Evaluate the impact of image density on article "Picked" status or other quality metrics.
