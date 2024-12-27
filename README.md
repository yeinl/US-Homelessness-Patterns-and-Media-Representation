# US Homelessness Patterns & Media Representation

## 🌟 **Understanding and Addressing U.S. Homelessness Through Data Science**  
*A Comprehensive Analysis of Trends (2015-2022) and Media Representation Across Political Spectrums*

---

## 📑 **Table of Contents**
1. [Problem Statement](#problem-statement)
2. [Objectives](#objectives)
3. [Key Concepts](#key-concepts)
    - [What is Sentiment Analysis?](#what-is-sentiment-analysis)
    - [Why Clustering Matters](#why-clustering-matters)
    - [Understanding Association Pattern Mining](#understanding-association-pattern-mining)
4. [Data Overview](#data-overview)
5. [Methodology](#methodology)
    - [Numerical Analysis](#numerical-analysis)
    - [Media Sentiment Analysis](#media-sentiment-analysis)
6. [Results and Findings](#results-and-findings)
7. [Visualizations](#visualizations)
8. [Conclusion](#conclusion)
9. [Future Work](#future-work)
10. [Technical Walkthrough](#technical-walkthrough)
11. [Repository Structure](#repository-structure)
12. [References](#references)

---

## **1. Problem Statement**

Homelessness in the U.S. is a persistent and multifaceted challenge that demands innovative approaches. This project investigates:
- **Trends and patterns** in homelessness across demographic groups from 2015 to 2022.
- How media narratives align with or distort these trends based on political leanings.

**Significance**: By marrying statistical insights with media analyses, this research aims to drive **data-informed policymaking**, **enhance advocacy efforts**, and improve **public understanding**.

---

## **2. Objectives**

### **Goals**
- **Numerical Analysis**:
  - Identify key factors influencing homelessness trends through advanced statistical modeling.
  - Discover correlations and patterns using clustering and association mining.
- **Media Sentiment Analysis**:
  - Investigate how media sentiment differs by political spectrum.
  - Identify recurring themes using topic modeling (e.g., LDA).

### **Expected Impact**
- Foster actionable recommendations for **public policy** and **advocacy organizations**.
- Address media biases to provide a clearer picture of the homelessness crisis.

---

## **3. Key Concepts**

### What is Sentiment Analysis?
Sentiment Analysis uses **Natural Language Processing (NLP)** to extract and classify the emotional tone (positive, negative, neutral) of textual data, such as news headlines.  
**Why it’s relevant**: It helps quantify how media represents homelessness narratives.  
🔗 *Learn more about [Sentiment Analysis](https://en.wikipedia.org/wiki/Sentiment_analysis)*  

### Why Clustering Matters
Clustering groups data points with similar characteristics, enabling identification of patterns.  
**Example**: Grouping homeless individuals by demographics (age, gender, race).  
🔗 *Learn more about [Clustering in Machine Learning](https://towardsdatascience.com/clustering)*

### Understanding Association Pattern Mining
Association Rule Mining identifies relationships between variables in large datasets.  
**Algorithm Used**: **FP Growth**  
**Example**: "Type - Sheltered → Race - White" appears in frequent patterns.  
🔗 *Learn more about [FP Growth Algorithm](https://en.wikipedia.org/wiki/Association_rule_learning)*  

---

## **4. Data Overview**

### **Homelessness Data**
- **Source**: U.S. Department of Housing and Urban Development (HUD).
- **Features**:
  - Demographics (age, gender, race).
  - Annual counts (sheltered vs. unsheltered).
  - Geographical trends.

### **Media Data**
- **Sources**: Headlines from:
  - *The New York Times* (Left).
  - *The Wall Street Journal* (Center).
  - *The Washington Examiner* (Right).
- **Content**:
  - Over 10,000 articles (2015–2022).
  - Sentiment analysis and topic modeling outputs.

---

## **5. Methodology**

### **Numerical Analysis**
1. **Preprocessing**:
   - Normalization, handling missing data, log transformations.
2. **Trend Analysis**:
   - Visualizations by year and demographics.
3. **Clustering**:
   - **Algorithm**: K-Means.
   - **Why Chosen**: Handles large datasets efficiently and identifies natural groupings.
4. **Association Mining**:
   - **Algorithm**: FP Growth.
   - **Why Chosen**: Faster than Apriori for large datasets.
5. **Classification**:
   - **Algorithms**: Random Forest, Gradient Boosting.
   - **Why Chosen**: High accuracy and feature interpretability.

### **Media Sentiment Analysis**
1. **Sentiment Scoring**:
   - **Tool**: BERT-based sentiment analysis.
   - **Output**: Emotional tone (positive/negative/neutral).
2. **Topic Modeling**:
   - **Algorithm**: Latent Dirichlet Allocation (LDA).
   - **Purpose**: Extract recurring themes in media headlines.

---

## **6. Results and Findings**

### **Numerical Insights**
- **Demographic Trends**:
  - Rising unsheltered homelessness among adults, males, and minorities.
- **Key Clusters**:
  - Grouped by age, race, and type of homelessness (e.g., sheltered vs. unsheltered).

### **Media Insights**
- Right-leaning media showed the strongest correlation with rising homelessness counts.
- Left-leaning media balanced negative and positive sentiments.

---

## **7. Visualizations**

### Sample Visualization: Clustering Output
![Clustering](https://example.com/cluster_visualization.png)  
**Description**: Clusters identified by age and homelessness type.

---

## **8. Conclusion**

This project highlights the interconnectedness of data-driven homelessness insights and media narratives. Policymakers must consider both to develop effective strategies.

---

## **9. Future Work**
1. **Include Social Media Analysis** (e.g., Twitter sentiment).
2. **Interactive Dashboards** for public engagement.

---

## **10. Technical Walkthrough**

### Example Python Code
```python
# Random Forest Classifier for Homelessness Prediction
from sklearn.ensemble import RandomForestClassifier
model = RandomForestClassifier(n_estimators=100, random_state=42)
model.fit(X_train, y_train)

# Frequent Pattern Growth for Association Rule Mining
from mlxtend.frequent_patterns import fpgrowth
frequent_patterns = fpgrowth(data, min_support=0.01)
```

---

## **11. Repository Structure**
📂 data/
  ├── homelessness_data.csv
  ├── media_data.csv
📂 scripts/
  ├── preprocessing.py
  ├── sentiment_analysis.py
📂 results/
  ├── visualizations/
README.md

---

## **12. References**
HUD: Annual Homeless Assessment Reports
FP Growth Algorithm: Wikipedia
Sentiment Analysis: Hugging Face BERT

