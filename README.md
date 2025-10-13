# Big Data Text Processing using PySpark

**License:** MIT  

##  Description
This project demonstrates large-scale text processing and information retrieval using **PySpark**.  
It includes two primary components:

1. **Named Entity WordCount** — Extracts and counts named entities (people, places, organizations) from a large text corpus using NLP and Spark's distributed processing.  
2. **Movie Plot Search Engine** — Implements a scalable TF-IDF–based movie plot search engine with cosine similarity ranking.

Both tasks highlight distributed computation, natural language processing, and large-scale data handling using the Spark framework.

---

##  Tech Stack
- **Language:** Python  
- **Framework:** Apache Spark (PySpark)  
- **Libraries:** NLTK, NumPy, wget  
- **Datasets:**  
  - [Project Gutenberg](https://www.gutenberg.org/) — for Named Entity WordCount  
  - [CMU Movie Summary Corpus](http://www.cs.cmu.edu/~ark/personas/data/MovieSummaries.tar.gz) — for Movie Plot Search Engine  
- **Environment:** Jupyter Notebook / Local Spark / Spark Cluster  

---

##  Features

###  Task 1 — Named Entity WordCount
- Downloads a text file from **Project Gutenberg** using `wget`.  
- Extracts **Named Entities** (people, places, organizations) with **NLTK**.  
- Performs a distributed **WordCount** on entities using Spark’s MapReduce.  
- Displays the **Top 25 most frequent named entities**.

####  Sample Output
![Task 1 Output](Task%201.png)

---

###  Task 2 — Movie Plot Search Engine (TF-IDF + Cosine Similarity)

This task builds a **mini search engine** using the CMU Movie Summary Corpus.  
It demonstrates how to compute **TF**, **IDF**, and **TF-IDF** manually using Spark RDDs for large-scale text retrieval.

####  Part A — Single-Term Query Search
- Calculates **TF-IDF scores** for every word in each movie plot.  
- Accepts a **single-term search query** (e.g., “romantic”, “funny”, “adventure”).  
- Ranks all movies by their TF-IDF value for that word.  
- Displays the **Top 10 most relevant movies** for the query.  

####  Sample Output
![Task 2A Output](Task%202_a.png)


##  Usage

###  1. Named Entity WordCount
Run:
```bash
spark-submit wordcount_entities.py

### 2.A Single Term Query Search
Run:
```bash
spark-submit tfidf_single_query.py

