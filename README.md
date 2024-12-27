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
Sentiment Analysis is a Natural Language Processing (NLP) technique that identifies and categorizes emotions expressed in text. At its core, it determines whether the sentiment of a given piece of text is **positive**, **negative**, or **neutral**. Advanced models like **BERT (Bidirectional Encoder Representations from Transformers)** have made sentiment analysis far more accurate by capturing the nuances of human language, such as sarcasm, context, and tone.

- **How it works:**
  1. **Preprocessing:** Text is cleaned by removing stop words, punctuation, and special characters.
  2. **Tokenization:** The text is broken into smaller units, such as words or phrases, for processing.
  3. **Sentiment Scoring:** Algorithms assign polarity scores to tokens or entire sentences, indicating their sentiment.

**Mathematical Foundation:**
Sentiment analysis often employs a polarity function \( P \):
\[
P = \frac{\text{Positive Words Count} - \text{Negative Words Count}}{\text{Total Words Count}}
\]
This yields a normalized score between -1 and 1.

- **In this Project:**
   Sentiment analysis was applied to over 10,000 headlines from politically diverse media outlets (*The New York Times*, *The Wall Street Journal*, *The Washington Examiner*). We used **BERT-based models** for their superior performance in understanding nuanced headlines. By mapping sentiment scores to homelessness trends, we revealed disparities between actual data and media portrayal.

---

### **Why Clustering Matters**
Clustering is a machine learning method that groups data points with similar characteristics. In the context of homelessness, clustering helps identify demographic patterns, revealing insights about which groups are most affected and why.

- **Key Clustering Algorithms:**
  1. **K-Means Clustering:** Partitions data into \( K \) clusters by minimizing within-cluster variance.
      \[
      J(c, \mu) = \sum_{i=1}^{n} \sum_{k=1}^{K} || x_i - \mu_k ||^2
      \]
      Here, \( x_i \) represents a data point, and \( \mu_k \) is the centroid of the \( k \)-th cluster.

  2. **Hierarchical Clustering:** Builds a tree (dendrogram) to represent nested groupings.

  3. **DBSCAN (Density-Based Spatial Clustering):** Groups points based on density, useful for identifying outliers.

- **Why it’s important:**
   For homelessness data, clustering helps us discover:
   - Groups disproportionately affected by homelessness (e.g., age-race combinations).
   - Geographical areas with similar trends (e.g., California and New York often cluster due to high homelessness rates).

- **In this Project:**
   We applied **K-Means** to demographic data, identifying four distinct clusters:
   - Young individuals disproportionately represented among White and African American groups.
   - Adults, especially females, clustering within specific racial demographics.
   - Diverse groups with mixed patterns.
   - Small or non-represented demographic clusters.

---

### **Association Pattern Mining**
Association Pattern Mining discovers relationships between variables in datasets. For example, in a retail setting, it’s used to find that "People who buy bread often buy butter." In this project, it uncovers which demographics and homelessness types frequently co-occur.

- **FP-Growth Algorithm:**
   Unlike traditional Apriori algorithms, FP-Growth is faster and avoids generating redundant candidate sets. It builds a **frequent pattern tree (FP-tree)** to store compressed data representations.

   **Steps in FP-Growth:**
   1. Construct the FP-tree from the dataset.
   2. Generate frequent patterns by traversing the FP-tree.

**Mathematical Context:**
Association rules are defined as:
\[
\text{Confidence}(X \rightarrow Y) = \frac{\text{Support}(X \cup Y)}{\text{Support}(X)}
\]
Where:
- \( X \): Antecedent
- \( Y \): Consequent
- Support: Proportion of transactions containing the itemset.

- **Why it matters:**
   In homelessness data, association rules reveal:
   - "Sheltered → Race: White" as a common pattern.
   - Strong associations between age and type of homelessness, such as "Under 18 → Sheltered."

- **In this Project:**
   FP-Growth identified **10 key demographic patterns**, such as the correlation between youth homelessness and race. These insights inform targeted interventions, such as increasing shelter access for specific racial groups.

---

### **Understanding Gradient Boosting**
Gradient Boosting is a supervised machine learning technique that builds models sequentially. Each new model corrects the errors of the previous one. It’s highly effective for structured data and excels at capturing complex relationships.

- **How it works:**
   Gradient Boosting minimizes a loss function by iteratively adding weak learners (e.g., decision trees):
   \[
   F_m(x) = F_{m-1}(x) + \eta \cdot h_m(x)
   \]
   Here:
   - \( F_m(x) \): Current model.
   - \( F_{m-1}(x) \): Previous model.
   - \( h_m(x) \): New learner.
   - \( \eta \): Learning rate.

- **Advantages:**
   - High accuracy.
   - Handles imbalanced datasets well (common in homelessness studies).

- **Comparison with Random Forest:**
   - **Random Forest:** Builds many independent trees and averages their results.
   - **Gradient Boosting:** Builds trees sequentially, optimizing each based on the previous ones.

- **In this Project:**
   Gradient Boosting was used to predict high homelessness counts. Key predictors included:
   1. **Gender (Male)**.
   2. **Age (Over 18)**.
   The model achieved **99% accuracy**, though cross-validation was employed to check for overfitting.

---

### How These Concepts Work Together
These techniques—sentiment analysis, clustering, association mining, and predictive modeling—form an interconnected framework:
1. **Sentiment Analysis** reveals the media’s portrayal of homelessness.
2. **Clustering** identifies demographic patterns to contextualize numerical insights.
3. **Association Pattern Mining** bridges gaps by uncovering frequently co-occurring factors.
4. **Gradient Boosting** confirms the importance of key features, enabling policy recommendations.

This multi-layered approach ensures robust analysis, combining data-driven insights with narrative understanding to inform actionable policies for homelessness intervention.


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

Numerical analysis forms the backbone of this project, enabling us to extract meaningful patterns from homelessness data spanning multiple years and demographics.

#### 1. **Data Preprocessing**
Data preprocessing ensures the dataset is clean, consistent, and ready for analysis. In this project, we implemented the following:
- **Imputation of Missing Data:**
  - Missing demographic and count values were imputed using mean or median strategies depending on the variable distribution.
  - Example: For demographic categories, missing data was filled proportionally based on similar states or regions.
- **Log Transformation:**
  - Skewed distributions were normalized using the log transformation:
    \[
    x' = \log(x + 1)
    \]
    This transformation helped stabilize variance and made relationships between variables clearer.

#### 2. **Exploratory Data Analysis (EDA)**
EDA allowed us to identify patterns, trends, and anomalies in the data:
- **Trend Analysis:**
  - Visualizations showed the rise in unsheltered homelessness and its disproportionate impact on adults and males.
- **Heatmaps:**
  - Correlation analysis revealed strong relationships (e.g., sheltered homelessness correlates with younger demographics).
  - High correlations like \( \text{Age: Under 18} \leftrightarrow \text{Race: White} \) guided further clustering and modeling efforts.

#### 3. **Clustering Analysis**
Clustering was crucial in identifying natural groupings among demographics. We used **K-Means Clustering** for its simplicity and interpretability:
- **Optimal Number of Clusters:**
  - Determined using the Elbow Method, where the inertia curve's inflection point suggested 4 clusters.
- **Insights:**
  - Cluster 1: Predominantly young individuals under 18, highly represented among White and African American groups.
  - Cluster 2: Adults over 18, including a significant proportion of males and females.
  - Cluster 3: Diverse groups with mixed racial representation.
  - Cluster 4: Minimal demographic representation, indicating under-sampled or less-affected populations.

#### 4. **Classification Models**
To predict high or low homelessness levels, we implemented two machine learning models:
- **Random Forest:**
  - An ensemble learning technique that combines multiple decision trees.
  - Features were ranked by importance using Gini impurity reduction:
    \[
    G = 1 - \sum_{i=1}^{n} p_i^2
    \]
    where \( p_i \) is the proportion of samples classified into class \( i \).
- **Gradient Boosting:**
  - Built sequential models to minimize the loss function:
    \[
    F_m(x) = F_{m-1}(x) + \eta \cdot h_m(x)
    \]
    Here, \( h_m(x) \) represents the weak learner added at iteration \( m \).

- **Why These Models Were Chosen:**
  - Random Forest: Robust to overfitting, handles missing values well.
  - Gradient Boosting: Captures complex, non-linear relationships in the data.

- **Results:**
  - Both models achieved high accuracy (99%), but cross-validation ensured reliability and minimized overfitting.

---

### **Media Sentiment Analysis**

To complement the numerical analysis, media sentiment analysis revealed how homelessness is portrayed across political spectra.

#### 1. **Web Scraping**
We used automated tools to extract over 10,000 headlines related to homelessness:
- **Process:**
  - Targeted three media outlets (*The New York Times*, *The Wall Street Journal*, *The Washington Examiner*), chosen for their distinct political leanings.
  - Keywords like "homelessness," "shelters," and "crisis" guided the scraping process.
  - To avoid bias, random sampling was employed, ensuring 100 headlines per year per outlet.

#### 2. **Sentiment Analysis**
**BERT (Bidirectional Encoder Representations from Transformers)** was used to classify the sentiment of each headline:
- **How BERT Works:**
  - Encodes input text into context-aware embeddings.
  - Applies classification layers to predict sentiments as positive, neutral, or negative.

**Key Formula for Sentiment Scoring:**
\[
\text{Sentiment Score} = \frac{\text{Positive Count} - \text{Negative Count}}{\text{Total Count}}
\]
This normalized score helped quantify sentiment trends across years and outlets.

- **Insights:**
  - Right-leaning media (*The Washington Examiner*) exhibited stronger negative sentiments during homelessness spikes.
  - Left-leaning media (*The New York Times*) maintained a balance between critical and optimistic tones.

#### 3. **Topic Modeling**
To uncover recurring themes in headlines, we applied **Latent Dirichlet Allocation (LDA)**:
- **How LDA Works:**
  - Models each document as a mixture of topics.
  - Topics are distributions over words.
- **Example Topics Identified:**
  - "Policy and Funding": Frequently discussed in *The New York Times*.
  - "Crime and Safety": Prominent in *The Washington Examiner*.
  - "Economic Impacts": Central in *The Wall Street Journal*.

**Mathematical Representation of LDA:**
\[
P(w) = \sum_{z} P(w|z) P(z|d)
\]
Where:
- \( P(w) \): Probability of a word \( w \) in a document \( d \).
- \( P(z|d) \): Probability of topic \( z \) given the document \( d \).
- \( P(w|z) \): Probability of word \( w \) given the topic \( z \).

- **Insights:**
  - Thematic focus varied significantly by political leaning:
    - Left: Policy and funding solutions.
    - Center: Economic analyses.
    - Right: Crime and safety concerns.

#### 4. **Comparative Sentiment Trends**
By normalizing sentiment scores and correlating them with homelessness data, we identified:
- Strong alignment between rising homelessness and increased negative sentiment in right-leaning outlets.
- Moderated responses in center and left-leaning outlets, reflecting editorial stances.

---

### How These Methods Work Together
This methodology integrates diverse techniques, ensuring comprehensive insights:
1. **Numerical Analysis:** Reveals the "what" and "why" of homelessness trends.
2. **Media Analysis:** Explores the "how" behind public perception and narratives.
3. **Correlation Studies:** Links statistical data with societal narratives, highlighting media's role in shaping discourse.

Together, these approaches bridge numerical realities with media portrayals, providing a holistic view of homelessness patterns in the U.S.


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



