# Fusion of Custom Search Engine with LLMs for Enhanced Speed and Results

## Overview

This project, undertaken as part of the Data Structure and Algorithms course (Fall 2023-24), focuses on optimizing corpus query processing using a fusion of a custom search engine and Large Language Models (LLMs). The assignment involved implementing a search mechanism and scoring system to identify top-k paragraphs for input queries, feeding them to LLMs to improve results, and speed up queries for large documents.

## Project Components

### 1. Custom Search Engine

#### Search Results Ranking (Finding Top-k Paragraphs)
Our search mechanism involves the following steps:
1. **Elimination of Stop Words:** Removing common stop words to enhance query accuracy.
2. **Word Score Adjustment:** Modifying word scores using a tailored formula.
   - Word score calculation: \( Score(w) = \log\left( \frac{Total\:word\:in\:corpus}{Count\:of\:w\:in\:corpus} + 1 \right) \)
   - Paragraph score calculation: \( Score(para) = \sum Score(w) \times (Count\:of\:w\:in\:para) \)

### 2. Fusion with LLMs

#### Querying the LLM
To enhance speed and specific results, we fused our custom search engine with LLMs, utilizing tools and technologies such as Hashing and vectors for word processing, scoring paragraphs, and Minheap for obtaining top-k paragraphs. The OpenAI Python module facilitated query requests to ChatGPT.

## Performance Metrics

The final project demonstrates impressive results:
- Average query processing time: 1.48 seconds on a local PC for 100 books (~150 MB .txt file).
- Accuracy: 83%

## Concepts Used

In the second segment of the assignment, several methodologies were implemented to optimize the existing code and yield enhanced results when executing the same query. The key concepts used are:

1. **Elimination of Stop Words:**
   - Commonplace words in English were excluded to refine the accuracy of the query.

2. **Word Score Adjustment:**
   - A tailored method was employed to modify the score of words, aiming to derive superior scores for individual words.
   - Word score calculation: \( Score(w) = \log\left( \frac{Total\:word\:in\:corpus}{Count\:of\:w\:in\:corpus} + 1 \right) \)
   - Paragraph score calculation: \( Score(para) = \sum Score(w) \times (Count\:of\:w\:in\:para) \)


## How to Use the Tool

### Requirements
- Python 3
- openai

### Building Data Structure
Before this please make sure written your OpenAI API Key and relvent query also you can add you txt files in corpus and make the suiltable changes in `main.cpp`.
Run the following bash command:
```
make
```
After inserting all corpus data, input the number of queries from "queries.txt" in the terminal.
Run tools using ```make run```
Now you will bw able to see your Answer on terminal, also in output.txt with additional relevent paragraphes.
Note: For running this tool, you need an OpenAI API key which can be obtained by signing up at [OpenAI](https://openai.com/product)
Enjoy querying! 🙂

#### Follow Up
If you find an issue please do ping me or create a PR :)
P.S. : If you find it useful please give a star to it.