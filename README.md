# Deep Learning Fake News Lab: Analyzing Covid-19 Myths

## Project Overview

This project aims to explore and analyze the most discussed topics and keywords surrounding Covid-19 myths using machine learning techniques. We employed Latent Dirichlet Allocation (LDA) and text summarization methods to extract key insights from a dataset of Covid-19 related discussions. The project also includes various visualizations such as heatmaps and bar graphs to better understand the topic distribution.

## Table of Contents

1. [Introduction](#introduction)
2. [Data Description](#data-description)
3. [Methodology](#methodology)
4. [Results](#results)
5. [Visualizations](#visualizations)
6. [Conclusion](#conclusion)
7. [How to Run the Project](#how-to-run-the-project)
8. [Future Work](#future-work)
9. [Authors](#authors)

## Introduction

Since the onset of the Covid-19 pandemic in 2020, a surge in public discussions around Covid-19 myths has been observed. This project delves into these discussions, aiming to uncover the most frequently discussed topics and keywords. We hypothesized that topics related to medical care, prevention methods, and personal experiences would dominate the discussions.

To achieve our goals, we took the following steps:

1. Plotted a heatmap to explore relationships among topics, comparing true and false statements.
2. Performed Latent Dirichlet Allocation (LDA) to model the most discussed topics and keywords.
3. Used deep learning for text summarization to identify top-discussed topics.

Our findings suggest that LDA is a more effective method for identifying the most discussed topics, with individuals, government, conspiracies, spread, and lockdown being the most popular themes.

## Data Description

The dataset contains 2526 observations and 26 variables, including:

- **Topic Information**: Includes various topics such as aid, animals, conspiracies, detection, food, governments, hospitals, individuals, laws, lockdown, medical equipment, medicine, origins, other diseases, predictions, religion, risk factors, spread, symptoms, travel, and vaccines.
- **Text Data**: Contains summaries and full text of the discussions.
- **Labels**: Indicate whether the statements are true or false.

### Key Variables:

- **Text**: The main body of text related to the discussions.
- **Summary**: A brief summary of the discussion.
- **Label**: Binary indicator (1 for true statements, 0 for false statements).
- **Topics**: Various topics discussed in the text, e.g., governments, individuals, conspiracies.

## Methodology

### 1. Data Exploration
- **Heatmap**: Plotted to examine the relationships among topics, comparing true and false statements.
- **Waffle Chart**: Used to visualize the categorization of topics.

### 2. Latent Dirichlet Allocation (LDA)
- LDA was applied to identify the most frequently discussed topics and keywords. This helped in understanding the primary themes in the dataset.

### 3. Text Summarization
- A deep learning-based text summarization method was used to identify the top-discussed topics. The performance of text summarization was compared with LDA results.

## Results

### Key Findings:
- Identified 21 topics, with the top 5 being individuals, government, conspiracies, spread, and lockdown.
- Heatmap analysis revealed that true statements often relate to reality and facts, while false statements focus on individuals, government, and conspiracies.
- LDA proved to be more effective than text summarization in identifying the most discussed topics.
- Word cloud and bar graphs indicated that the most searched keywords were "coronavirus", "covid", "19", "facebook", and "äu".

### Text Summarization Insights:
- Found that text summaries were generally concise, with most having fewer than 25 words.
- Summarization accuracy decreased as the dataset size increased, indicating that text summarization might not be as reliable as LDA for this analysis.

## Visualizations

The project includes the following visualizations:

- **Histograms**: Distribution of text lengths in summaries and full texts.
- **Pairplots**: Analyzed relationships among different variables, such as the topics and their associated frequencies.
- **Word Cloud**: Visual representation of the most frequent keywords in the dataset.
- **Bar Graphs**: Displayed the frequency of top-discussed topics.

## Conclusion

Our analysis reveals that during the Covid-19 pandemic, discussions around individuals, government actions, conspiracies, and lockdowns were most prevalent. While LDA provided valuable insights into the most discussed topics, the text summarization approach highlighted the limitations of automated methods in understanding nuanced discussions.

## How to Run the Project

### Prerequisites

- Python 3.x
- Required libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `nltk`, `gensim`, `sklearn`

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Kr-Yan/fake-news-lab.git
   cd fake-news-lab
   
2. Install the required packages:
   ```bash
   pip install -r requirements.txt

### Running the Analysis

1. Data Preprocessing:
   ```bash
   python scripts/preprocess_data.py

2. LDA Analysis:
   ```bash
   python scripts/run_lda.py

3. Text Summarization:
   ```bash
   python scripts/summarize_text.py

4. Visualization:
   ```bash
   python scripts/visualize_results.py

### Output
- The results and visualizations are saved in the output/ directory.

## Future Work
To improve the analysis, future work could explore:

1. Combining classification models with text summarization to enhance topic detection.
2. Addressing the causal inference problem by analyzing the simultaneity of keyword popularity and discussion frequency.

## Authors
- Dang Pham
- Kairuo Yan


