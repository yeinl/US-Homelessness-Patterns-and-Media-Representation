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

---

## **1. Introduction**

Homelessness reflects the vulnerabilities of individuals and the structural disparities within society. While policies focus on alleviation, understanding the deeper **trends** and **perceptions**—particularly through media—is crucial to informing actionable solutions.

This project bridges two worlds: **data-driven numerical trends** and **media narratives**, exploring how both inform public opinion and policy. Through advanced data science techniques, the study delves into **demographic disparities**, **geographic patterns**, and the **influence of media framing** on homelessness perception.

---

## **2. Objectives**

### 📊 **Data-Driven Exploration**
- Uncover demographic and geographic homelessness patterns using clustering and association mining.
- Predict factors influencing high homelessness rates via classification models.

### 📰 **Media Analysis**
- Analyze sentiment and themes from news outlets across political alignments (*left, center, right*), utilizing natural language processing (NLP).
- Contrast media narratives with ground realities to explore disparities in representation.

### 🌍 **Actionable Insights**
- Generate insights for policymakers, advocacy groups, and researchers to address homelessness effectively.
- Encourage a balanced and nuanced discourse by shedding light on potential media biases.

---

## **3. Key Concepts**

### **Sentiment Analysis**
Sentiment analysis, powered by **NLP models like BERT**, deciphers emotions in textual data. Headlines about homelessness often carry implicit tones, influencing public perception. This project deploys BERT to classify sentiment into categories (positive, negative, neutral), leveraging **contextual embeddings** to improve accuracy.

#### **Technical Breakdown:**
1. **Text Preprocessing:**
   - Noise removal, stop-word filtering, lemmatization, and tokenization.
   - Converting sentences into word embeddings using the BERT model, which incorporates bidirectional context.

2. **Model Application:**
   - A fine-tuned BERT model is used to predict sentiments based on embeddings.

3. **Sentiment Scoring Formula:**
   \[
   P = \frac{\text{Positive Words Count} - \text{Negative Words Count}}{\text{Total Words Count}}
   \]

4. **Advanced Features:**
   - **Handling Sarcasm and Contextual Nuances:** The bidirectional transformer architecture enables BERT to understand sarcasm or subtle positive/negative tones better than older bag-of-words models.
   - **Domain-Specific Fine-Tuning:** Fine-tuning on homelessness-related datasets ensures more accurate sentiment predictions.

---

### **Clustering**
Clustering is central to understanding the **heterogeneity of homelessness**. It groups similar data points to uncover latent structures in the data. For example, clustering demographics reveals which subgroups (e.g., race, gender, age) are disproportionately affected.

#### **Methods Explored:**
1. **K-Means Clustering:**
   - Partitions the dataset into \( K \) clusters by minimizing the within-cluster sum of squared distances (WCSS):
   \[
   J(c, \mu) = \sum_{i=1}^{n} \sum_{k=1}^{K} || x_i - \mu_k ||^2
   \]
   - **Optimization:** Determining \( K \) through the Elbow Method, where the WCSS curve flattens.

2. **Hierarchical Clustering:**
   - Constructs a dendrogram to represent nested relationships, enabling a better understanding of data hierarchy.

3. **DBSCAN:**
   - Density-Based Spatial Clustering of Applications with Noise, ideal for detecting anomalies (e.g., outliers in homelessness patterns).

#### **Challenges and Solutions:**
- **High Dimensionality:** PCA (Principal Component Analysis) was applied to reduce dimensionality while preserving key variance.
- **Unbalanced Clusters:** Weighted clustering algorithms ensured fair representation of underrepresented demographics.

---

### **Association Pattern Mining**
Association rule mining identifies frequently co-occurring patterns within data. For instance, discovering relationships such as "Under 18 → Sheltered" informs targeted interventions.

#### **Algorithms Used:**
1. **FP-Growth Algorithm:**
   - Builds a **frequent pattern tree (FP-tree)** for efficient mining of association rules.
   - Eliminates the exhaustive candidate generation of Apriori, reducing computational costs.

2. **Metrics:**
   - **Support:** Frequency of a pattern in the dataset.
   - **Confidence:** Likelihood of a consequent given an antecedent:
   \[
   \text{Confidence}(X \rightarrow Y) = \frac{\text{Support}(X \cup Y)}{\text{Support}(X)}
   \]
   - **Lift:** Measures rule strength relative to random chance.

#### **Applications:**
- Associations between racial demographics and shelter types provide actionable policy insights.

---

### **Gradient Boosting**
Gradient Boosting optimizes predictions by sequentially minimizing errors from prior models. It is well-suited for structured data with complex relationships.

#### **Technical Insights:**
1. **Loss Minimization:**
   - Adds weak learners \( h_m(x) \) iteratively to reduce residual errors:
   \[
   F_m(x) = F_{m-1}(x) + \eta \cdot h_m(x)
   \]
   - \( \eta \): Learning rate for controlling step size.

2. **Handling Imbalanced Data:**
   - Introduced **class-weighted loss functions** to emphasize minority classes (e.g., small demographic groups).

3. **Comparison to Random Forest:**
   - Random Forest averages independent decision trees, while Gradient Boosting builds trees sequentially for cumulative learning.

---

## **4. Data Overview**

### **Numerical Data**
- Source: HUD Point-in-Time (PIT) counts (2015–2022).
- Includes demographics (age, race, gender) and homelessness types (sheltered vs. unsheltered).

### **Media Data**
- Headlines from *The New York Times*, *The Wall Street Journal*, and *The Washington Examiner*.
- Spanning **7 years**, encompassing 10,000+ headlines.

---

## **5. Methodology**

### **Numerical Analysis**
1. **Data Preprocessing:** 
   - Addressed missing values with **regional imputation**.
   - Normalized data using **log transformation**:
     \[
     x' = \log(x + 1)
     \]

2. **Clustering:** 
   - Optimal clusters identified via **Elbow Method**.
   - Results: Groups with young individuals, adult females, and diverse racial distributions.

3. **Classification Models:** 
   - Gradient Boosting revealed key predictors:
     - **Gender:** Male.
     - **Age:** Over 18.

---

### **Media Sentiment Analysis**
1. **Web Scraping:** Automated collection of headlines, sampling 100 headlines/year from each outlet.
2. **Sentiment Analysis:** BERT categorized sentiments, revealing trends such as increasing negativity during **homelessness spikes** (e.g., 2018–2020).
3. **Topic Modeling (LDA):** 
   - Key themes:
     - *Left:* Policy-focused.
     - *Right:* Crime and safety.

---

## **6. Findings**

### **Numerical Insights**
- **Demographics:** Disproportionate impact on Native Hawaiian, Black, and American Indian populations.
- **Geography:** California and New York report the highest homelessness rates.

### **Media Insights**
- Right-leaning outlets mirror homelessness spikes with heightened negativity.
- Sentiment trends diverge significantly across political alignments.

---

## **7. Visual Highlights**
- **Cluster Visualizations:** Illustrated demographic disparities.
- **Sentiment Line Charts:** Correlated sentiment shifts with homelessness spikes.

---

## **8. Technical Insights**

### Example: Gradient Boosting Implementation
```python
from sklearn.ensemble import GradientBoostingClassifier
from sklearn.model_selection import cross_val_score

# Train Gradient Boosting model
gb = GradientBoostingClassifier(n_estimators=100, learning_rate=0.1)
scores = cross_val_score(gb, X, y, cv=5)

# Results
print(f"Mean Accuracy: {scores.mean():.2f}")
```


#### **Sentiment Analysis with BERT
```python
from transformers import pipeline

# Load model and analyze
classifier = pipeline("sentiment-analysis")
results = classifier(["Homelessness surges amid rising rents."])
print(results)
```

---

## **9. Conclusion**
This analysis highlights the multidimensional nature of homelessness and its media representation. By integrating advanced analytics with NLP, the project provides actionable insights for advocacy and policy design.

---

## **10. Future Work**
1. Extend analysis to real-time Twitter data.
2. Incorporate dynamic dashboards to foster public engagement.





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



