# CSL7110 Assignment 4 - Data Science & Large Scale Systems

This repo contains my solutions for Assignment 4, covering clustering, search indexing, and PageRank.

## What's Inside?
1. **Clustering:** Python implementation of Farthest-First (k-center) and k-Means++ initialization.
2. **Search Engine:** A manual implementation of an inverted index using custom Hash Tables and Sets.
3. **PageRank:** A PySpark script that handles iterative rank updates on a graph of 1,000 nodes.

## Requirements
- `pyspark`
- `numpy`
- `random`, `time`, `os`

## Running the Code
The code is written in a `.ipynb` format meant for Google Colab. 
1. Open `CSL7110_Assignment4.ipynb`.
2. Mount your Google Drive to access the datasets.
3. Run the cells in order. The Spark section will automatically install `pyspark` and initialize the `SparkContext`.

## 📊 Results Summary

### Part 1: Clustering Performance
| Algorithm | Metric | Value |
| :--- | :--- | :--- |
| **k-center (k=10)** | Execution Time | 1.7711s |
| **k-means++ (k=10)** | Objective Score | 24,081.99 |
| **Coreset (k1=50) → k-means++** | Objective Score | 194,762.41 |

### Part 2: Search Engine Queries
- **Query "stack":** Successfully returned `stack_cprogramming`, `stack_datastructure_wiki`, and `stackoverflow`.
- **Query "delhi":** Corrected returned `No webpage contains word delhi`.
- **Position Tracking:** Accurately mapped exact word offsets within `.txt` source files.

### Part 3: PageRank Rankings (1000 Nodes)
- **Top 5 Node IDs:** `263, 537, 965, 243, 285`
- **Bottom 5 Node IDs:** `408, 424, 62, 93, 558`
