# CS5344 - Amazon Reviews Big Data Analysis - Group 21

## Project Overview

Our project aims to empower online sellers and brands in the dynamic e-commerce landscape, particularly focusing on the Singaporean housing market. By leveraging advanced big data techniques and analytics, we provide enhanced insights into buyer sentiments, simplifying complexities and aiding sellers in navigating the market effectively.

## Table of Contents

1. [Install Dependencies](#install-dependencies)
2. [Repository Structure](#repository-structure)
3. [Code Execution](#code-execution)

## 1. Install Dependencies

Ensure you have the following dependencies installed:

- **Python 3.x**
- **Apache Spark 3.4.1** (For Mac users, install via Homebrew. Reference: [Mac Spark Installation Guide](https://spark.apache.org/docs/latest/spark-standalone.html#macos))
- **Scala 2.12.17**
- **OpenJDK 20.0.1** (Homebrew installation)
- **Spacy**: `pip install spacy`
- **Spacy's en_core_web_lg**: `python -m spacy download en_core_web_lg`
- **NLTK**: `pip install nltk`
- **NLTK's VADER**: `import nltk; nltk.download('vader_lexicon')`
- **Jupyter Notebook / Google Colab**
- **Tableau**

## 2. Repository Structure

The repository contains the following files and folders:

- **Dataset Folder**
  - `Electronics.json`: Original Amazon reviews data.
  - `meta_Electronics.json`: Metadata.
  - `Electronics_preprocessed`: Data after preprocessing and cleaning.
  - `filtered_reviews`: Reviews with a minimum of 5 upvotes.

- **Checkpoint Folder**
  - Contains checkpoints (trained models from BERT model training).

- **Bert_Data Folder**
  - Contains three subset data files (train, val, test) from `Electronics_preprocessed` for BERT model training.

- **extracted_aspects Folder**
  - Contains the final extracted aspects, with top 5 aspects for each product and associated opinions and sentiments.

- **src Folder**
  - Contains code files for different analyses:
    - `Product KPI`: Code for generating Product KPIs (e.g., Total Average Rating, last year's rating).
    - `Top 5 Products`: Code to find the top 5 similar products for each product clustered by Product Category.
    - `dataprep`: Data preprocessing code.
    - `aspect_extraction`: Code for aspect extraction.
    - `sentiment_analysis`: Code for sentiment analysis using Logistic Regression, Naive Bayes, and BERT models.

## 3. Code Execution

The code can be executed on Jupyter Notebook, Google Colab, or a local machine. Ensure to adjust the file paths according to your setup before running the code.

- **Data Preprocessing**: `spark-submit DataPreprocessing.py`
- **Aspect Extraction**: `spark-submit AspectExtraction.py`
- **Notebook Files**: Run directly cell by cell.

---

Feel free to customize this template further based on your project's specific needs and details.
