# US Homelessness Patterns & Media Representation

## 🌟 Understanding and Addressing U.S. Homelessness Through Data Science  
*A Comprehensive Analysis of Trends (2015-2022) and Media Representation Across Political Spectrums*

---

## 📑 **Table of Contents**
1. [Problem Statement](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#1-problem-statement)
2. [Objectives](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#2-objectives)
3. [Key Concepts](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#3-key-concepts)
    - [What is Sentiment Analysis?](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#what-is-sentiment-analysis)
    - [Why Clustering Matters](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#why-clustering-matters)
    - [Understanding Association Pattern Mining](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#understanding-association-pattern-mining)
4. [Data Overview](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#4-data-overview)
5. [Methodology](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#5-methodology)
    - [Numerical Analysis](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#numerical-analysis)
    - [Media Sentiment Analysis](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#media-sentiment-analysis)
6. [Key Findings](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#6-key-findings)
7. [Visualizations](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#7-visualizations)
8. [Technical Walkthrough](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#8-technical-walkthrough)
9. [Conclusion](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#9-conclusion)
10. [Future Work](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#10-future-work)
11. [Repository Structure](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#11-repository-structure)
12. [References](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#12-references)

---

## **1. Problem Statement**

Homelessness is a complex societal issue, reflecting the socio-economic, racial, and policy frameworks of our communities. This project aims to:
- Explore **patterns and trends in U.S. homelessness** from 2015 to 2022.
- Analyze **media narratives** about homelessness across political leanings.
- Identify **data-driven policy insights** to inform advocacy and intervention strategies.

> Homelessness affects over **half a million Americans nightly**, with **72% as individuals** and **28% as families with children** (*HUD 2022 Annual Report*). However, media portrayal often shapes public perception and policy priorities in divergent ways.

---

## **2. Objectives**

### 🔎 **Key Goals**
1. **Numerical Analysis:**
   - Investigate demographic and geographical homelessness patterns.
   - Employ clustering, association mining, and predictive modeling to uncover insights.
2. **Media Sentiment Analysis:**
   - Compare sentiments and themes from left, right, and center-aligned news outlets.
   - Identify media biases in homelessness narratives.

### 🌍 **Social Impact**
- **Policy Insight:** Generate actionable recommendations for public policies aimed at reducing homelessness.
- **Advocacy Support:** Empower advocacy groups with data-backed insights.
- **Media Literacy:** Highlight media biases to foster a more informed public discourse.

---

## **3. Key Concepts**

### **What is Sentiment Analysis?**
Sentiment analysis uses **Natural Language Processing (NLP)** to evaluate the emotional tone in text data. It assigns sentiment categories (e.g., positive, neutral, negative) to phrases or entire texts.

- **Why Relevant?** Understanding media sentiment sheds light on how public perceptions of homelessness are influenced.
- **Methodology Overview:**
  1. Tokenization: Splitting text into words.
  2. Sentiment Scoring: Assigning scores using models like **BERT**.
  3. Aggregation: Summarizing sentiments for yearly trends.

**Formula** for Sentiment Scoring:
\[
\text{Sentiment Score} = \sum_{i=1}^{n} \text{Polarity(word}_i)
\]

---

### **Why Clustering Matters**
Clustering is a machine learning technique that groups data points with similar characteristics.

- **Example Application:**
   - Grouping homelessness records by **age**, **race**, and **geography**.
   - Identifying areas with similar homelessness trends.

**Algorithms Explored:**
1. **K-Means:** Efficient for large datasets but assumes spherical clusters.
2. **Hierarchical Clustering:** Builds a dendrogram but struggles with large datasets.

**Key Equation (K-Means):**
\[
J(c, \mu) = \sum_{i=1}^{n} \sum_{k=1}^{K} || x_i^{(k)} - \mu_k ||^2
\]
*where \(x_i\) represents data points and \(\mu_k\) the centroid.*

---

### **Association Pattern Mining**
This technique identifies frequent patterns in data to infer relationships.  

**Algorithm Used:** **FP-Growth**  
- **Why Chosen:** Scales better than **Apriori** for large datasets.  
- **Key Insight Example:** "Sheltered → Race - White" is a frequent association.

---

### **Understanding Gradient Boosting**
Gradient Boosting is a supervised learning algorithm that builds models sequentially. Each model corrects errors made by the previous one.

- **Why Used Here:** Effective for handling imbalanced datasets and uncovering key predictors.
- **Comparison with Random Forest:** Gradient Boosting often outperforms Random Forest in small, high-dimensional datasets but is computationally expensive.

---

## **4. Data Overview**

### **Numerical Data**
- **Source:** HUD Point-in-Time (PIT) counts (2015–2022).
- **Features:**
  - Demographics (age, gender, race).
  - Homelessness type (sheltered vs. unsheltered).

### **Media Data**
- **Source:** News headlines from:
  - *The New York Times* (Left-leaning).
  - *The Wall Street Journal* (Centrist).
  - *The Washington Examiner* (Right-leaning).
- **Total Records:** Over 10,000 headlines spanning 7 years.

---

## **5. Methodology**

### **Numerical Analysis**
1. **Data Preprocessing:**
   - Imputation for missing data.
   - Log transformation to normalize skewed distributions.
2. **Exploratory Data Analysis:**
   - Analyzed trends by demographics and geography.
   - Heatmaps for correlation analysis.
3. **Clustering Analysis:**
   - Identified natural groupings in the data (e.g., demographic clusters).
4. **Classification Models:**
   - Random Forest and Gradient Boosting used to predict high/low homelessness.

---

### **Media Sentiment Analysis**
1. **Web Scraping:**
   - Extracted news headlines using keywords like “homelessness.”
   - Random sampling to ensure balanced representation.
2. **Sentiment Analysis:**
   - BERT-based model to classify sentiments into positive, neutral, and negative.
3. **Topic Modeling:**
   - Applied **Latent Dirichlet Allocation (LDA)** to uncover recurring themes.

---

## **6. Key Findings**

### **Numerical Insights**
1. **Demographic Trends:**
   - Higher homelessness rates among males and adults.
   - Disproportionate impact on **Native Hawaiians**, **Black**, and **American Indian** populations after normalization.
2. **Geographical Trends:**
   - California and New York report the highest homelessness counts.

### **Media Insights**
1. **Sentiment Trends:**
   - Right-leaning outlets (*Washington Examiner*) align most closely with homelessness trends, displaying increased negativity during rises in homeless counts.
2. **Topic Modeling:**
   - Common themes include "shelters," "policy debates," and "crisis response."

---

## **8. Technical Walkthrough**

### Example Python Code
#### **Random Forest Classifier**
```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import classification_report

# Training the model
model = RandomForestClassifier(n_estimators=100, random_state=42)
model.fit(X_train, y_train)

# Evaluation
predictions = model.predict(X_test)
print(classification_report(y_test, predictions))
```

#### **Sentiment Analysis with BERT
```python
from transformers import pipeline

# Load sentiment analysis pipeline
classifier = pipeline("sentiment-analysis")
sentiments = classifier(["Homelessness is rising nationwide.", 
                         "New shelter policies are proving effective."])
print(sentiments)
```

---

## **9. Conclusion**
This study provides a holistic view of homelessness patterns and media portrayals. The insights inform policymakers and advocates, emphasizing the need for unbiased narratives and targeted policies.

---

## **10. Future Work**
1. Expand analysis to include social media platforms like Twitter.
2. Develop interactive dashboards to communicate findings to non-technical audiences.





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
1. HUD: Annual Homeless Assessment Reports
2. FP Growth Algorithm: Wikipedia
3. Sentiment Analysis: Hugging Face BERT
4. Gradient Boosting Explained: Towards Data Science.



