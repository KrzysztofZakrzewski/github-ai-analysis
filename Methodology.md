# Methodology

## Project Workflow

The project follows a standard data science workflow consisting of three main stages:

1. **Data Collection** – collecting repository metadata from the GitHub REST Search API.
2. **Pre-analysis** – validating, cleaning, and preprocessing the raw dataset.
3. **Exploratory Data Analysis (EDA)** – statistical analysis, visualization, and interpretation of the cleaned data.

---

## Data Collection

Repository metadata was collected using the GitHub REST Search API.

Twenty AI-related topics were queried, including Artificial Intelligence, Machine Learning, Deep Learning, Large Language Models (LLMs), Computer Vision, Natural Language Processing (NLP), Generative AI, PyTorch, TensorFlow, Retrieval-Augmented Generation (RAG), and Agentic AI.

For each topic, up to 1,000 repositories were retrieved using the GitHub Search API pagination mechanism.

Since many repositories belonged to multiple topics, duplicate repositories were expected and later removed using the unique GitHub repository ID.

---

## Data Validation

During data collection, an inconsistency was identified in the GitHub API responses.

Some repositories contained additional nested metadata related to software licenses, while others did not. As a result, different batches produced DataFrames with different numbers of columns (109 and 110). Writing these batches directly to a CSV file caused column misalignment and inconsistent dataset architecture.

The issue was resolved by constructing a unified DataFrame before exporting the dataset. Missing fields were automatically filled with missing values, ensuring a consistent schema for every collected repository.

---

## Data Cleaning

The preprocessing stage included:

* removing duplicate repositories,
* validating repository identifiers,
* handling missing values,
* standardizing categorical values,
* removing features with no analytical value,
* converting date columns into appropriate formats,
* engineering additional features such as `created_year`,
* resetting the DataFrame index after cleaning.

The resulting dataset contained **13,844 unique repositories** ready for analysis.

---

## Exploratory Data Analysis

The cleaned dataset was used to investigate programming language trends, repository popularity, software licenses, ownership patterns, AI topics, and relationships between key repository metrics.

The analysis combines descriptive statistics, data visualization, and comparative analysis to answer the predefined research questions.
