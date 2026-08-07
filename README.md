# GitHub AI Repositories Analysis

## Project Overview

This project explores the open-source Artificial Intelligence ecosystem by analyzing popular AI-related repositories hosted on GitHub.

The project follows a complete data science workflow, including data collection, data cleaning, exploratory data analysis (EDA), statistical analysis, and data visualization. The primary objective is to identify technology trends, repository characteristics, and relationships between different repository metrics within the AI open-source community.

---

## Dataset

The dataset was collected using the GitHub REST Search API.

Repositories were retrieved by querying 20 AI-related topics, including Artificial Intelligence, Machine Learning, Deep Learning, Large Language Models (LLMs), Generative AI, Computer Vision, Natural Language Processing (NLP), Retrieval-Augmented Generation (RAG), PyTorch, TensorFlow, and Agentic AI.

Up to 1,000 repositories were collected for each topic. Since many repositories appeared under multiple topics, duplicate entries were removed using the unique GitHub repository ID, resulting in a cleaned dataset containing **13,844 unique repositories**.

The dataset was further prepared for analysis by:

* removing duplicate repositories,
* handling missing values,
* correcting inconsistencies introduced during data collection,
* removing features with no analytical value,
* creating additional features used during the analysis.

---

## Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Plotly
* GitHub REST API
* Jupyter Notebook

---

## Repository Structure

```text
.
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
├── scraper/
├── figures/
├── README.md
├── METHODOLOGY.md
├── SCRAPER.md
├── requirements.txt
└── LICENSE
```

---

## Research Questions

1. Which programming languages dominate the AI ecosystem, and how have their trends changed over time?

2. How are the key repository popularity metrics related to one another?

3. Do stars and forks measure the same aspect of repository popularity?

4. Do organization-owned repositories attract greater community engagement than user-owned repositories?

5. Do organizations and individual users prefer different programming languages?

6. Do repositories with GitHub Discussions enabled attract greater community engagement?

7. Does repository popularity vary across different software licenses?

8. Which software licenses are most commonly used across different programming languages?

9. Do repositories written in different programming languages exhibit different AI topic distributions?

---

## Limitations

### How Have AI Topics Changed Over Time?

This analysis was intentionally omitted because the GitHub REST Search API provides only the current repository topics and does not preserve the history of topic assignments. Therefore, the available data cannot be used to reliably analyze how AI topics have evolved over time.

---

## License

This project was created for educational and portfolio purposes.
