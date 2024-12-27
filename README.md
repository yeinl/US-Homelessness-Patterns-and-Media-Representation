# US-Homelessness-Patterns-and-Media-Representation
Analyzing U.S. homelessness trends (2015-2022) and their media portrayals across political spectrums to inform policy and advocacy.

# US Homelessness Patterns & Media Representation

## **Problem Statement**

### **Objective**
To analyze **homelessness trends in the U.S. from 2015 to 2022**, focusing on:
- Demographic patterns
- The portrayal of homelessness in media across political spectrums

### **Approach**
This project uses advanced **data analysis and machine learning techniques** alongside **media sentiment analysis** to:
1. Identify factors influencing homelessness patterns.
2. Compare media portrayals with actual homelessness trends.

### **Social Impact**
The insights aim to:
- Guide **public policies** and advocacy efforts.
- Address misconceptions or biases in media representations.
- Enhance community strategies for intervention and prevention.

---

## **Data Sources**

### **1) Homelessness Data**
- **Sources:** U.S. Department of Housing and Urban Development, local government datasets, and non-profits.
- **Content:** 
  - Demographics (age, gender, race)
  - Geographical distribution
  - Annual homeless counts (sheltered vs. unsheltered)

### **2) Media Data**
- **Sources:** Over 10,000 articles from major news outlets (left-leaning, centrist, right-leaning).
- **Content:**
  - Sentiment analysis scores
  - Frequency of specific themes
  - Political biases tagged for comparative metrics

### **3) Combined Dataset Characteristics**
- **Homelessness Data:** 5,000+ rows of detailed demographic and homelessness information.
- **Media Data:** Analyzed for sentiment, themes, and correlation with homelessness trends.

---

## **Methodology**

### **1) Numerical Analysis**

#### **1.1 Data Preprocessing**
- Handled missing values and inconsistencies.
- Normalized datasets for clustering and classification tasks.

#### **1.2 Correlation Analysis**
- **Goal:** Discover relationships between variables.
- **Output:** Heatmaps highlighting strong correlations.

#### **1.3 Clustering**
- **Method:** K-Means and DBSCAN
- **Objective:** Group similar demographic factors contributing to homelessness.

#### **1.4 Association Pattern Mining**
- **Algorithm:** FP-Growth
- **Output:** Top 10 demographic patterns frequently occurring together:
  - E.g., "Sheltered -> Race - White"

#### **1.5 Classification Models**
- **Algorithms:** Random Forest, Gradient Boosting
- **Objective:** Identify the most critical factors influencing high levels of homelessness.
- **Key Factors Identified:**
  - Gender: Male
  - Age: Over 18

---

### **2) Media Analysis**

#### **2.1 Sentiment Analysis**
- **Method:** BERT-based sentiment scoring of headlines.
- **Findings:** Clear bias in sentiment by political leaning.

#### **2.2 Topic Modeling**
- **Method:** LDA
- **Insights:** Key themes across outlets (e.g., policy failures, crisis framing).

#### **2.3 Comparative Sentiment Trends**
- Negative sentiments peaked in 2018-2020, correlating with an increase in homeless counts.

#### **2.4 Word Frequency Analysis**
- Frequent terms like "shelters," "policy," and "crisis" reflect shared concerns but varying editorial focus.

---

## **Key Insights**

### **1) Homelessness Trends**
- Stable overall counts with demographic disparities:
  - Higher prevalence among adults, males, and racial minorities.
  - Disproportionate impact on Native Hawaiian, Black, and Alaskan Native populations.

### **2) Media Narratives**
- **Left-Leaning Media:** Balanced negative and positive sentiments; focus on policy failures and successes.
- **Centrist Media:** Neutral reporting; occasional criticism.
- **Right-Leaning Media:** Persistent negative sentiment; emphasis on societal challenges.

### **3) Correlations**
- Strong alignment between media negativity and rising homeless counts (2018-2020).

---

## **Conclusion**

This project highlights:
- Persistent demographic challenges in homelessness.
- Media's influential role in shaping public discourse.
- The need for **targeted policy interventions** informed by data and media narratives.

By integrating numerical and media analyses, this study provides a holistic view of homelessness patterns and media representation in the U.S., aiming to drive **effective policies and public awareness**.

---

## **Getting Started**

### **Prerequisites**
- Python 3.8+
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `openai`

### **Installation**
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/US-Homelessness-Patterns-Media-Representation.git
