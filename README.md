# US Homelessness Patterns & Media Representation

## Understanding and Addressing U.S. Homelessness Through Data Science  
*A Comprehensive Analysis of Trends (2015-2022) and Media Representation Across Political Spectrums*

---

## 📑 **Table of Contents**
1. [Introduction](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#1-introduction)
2. [Problem Statement](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#2-problem-statement)
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

## 1. Introduction  
The true strength of a society often shows in how it treats its most vulnerable members. Homelessness is a telling challenge in this regard, reflecting not just the availability of shelter but broader issues like economic health and community support. Between 2007 and 2022, the story of homelessness in the U.S. has varied greatly, and not all these stories make it to the headlines.

This research is set against the backdrop of notable shifts in homelessness demographics. We're exploring how factors like age, gender, race, and geographical location influence patterns of homelessness. The landscape is vast: from young adults facing homelessness to elderly individuals navigating unique challenges. Notably, while some areas have successfully curtailed the rise of homelessness with innovative strategies, others find themselves battling unexpected surges. We additionally aim to spotlight regions that have excelled in their approach, serving as potential models for others.

An equally important facet of our study is the media's portrayal of homelessness. Through quantitative and qualitative analysis, we'll assess the themes present in online news articles segmented by state. By comparing these media depictions, analyzing their sentiments against actual homelessness statistics, we aim to discern any disparities, offering a deeper understanding of potential media biases or misrepresentations.

To uncover these insights, we're turning to data mining—employing techniques that delve deep into large datasets to uncover patterns and trends. While we will dive deeper into our methods later, it's worth noting that our approach is comprehensive, merging hard data with narrative analysis. This ensures a holistic understanding, shedding light on both statistics and stories.

In essence, "Bridging Realities" is not merely a research endeavor. It seeks to empower policymakers, NGOs, urban planners, and social welfare experts with a nuanced understanding of homelessness. By challenging prevailing narratives and offering a clearer picture, we hope to inspire a renewed commitment to addressing and understanding this pressing issue.

---

## 2. Problem Statement  
We aim to investigate changing patterns related to homelessness from 2015 to 2022 by conducting a thorough numerical analysis of homeless counts across diverse demographics such as age, gender, race, and state. Utilizing clustering, association pattern mining, and classification models (Random Forest, Gradient Boosting), we seek to identify underlying patterns and factors significantly influencing homelessness.

Additionally, our study involves a text analysis of news titles related to homelessness from left-wing, neutral, and right-wing media categories. Employing sentiment analysis (BERT), word frequency, and topic modeling (LDA), we aim to assess media portrayals of homelessness across political wings. Furthermore, we seek to assess the alignment between Internet news portrayals by state and the actual circumstances of homelessness.

---

## 3. Related Work  
In recent research, machine learning and artificial intelligence have been harnessed to model complex systems, particularly within the context of homelessness. One study employs these technologies to predict returns to homelessness, examining numerous possible allocations of households to homeless services and generating reentry predictions for each combination of household and service [1]. Additionally, it explores mathematical and theoretical optimization possibilities for the allocation process and investigates how predictions can enhance the understanding of homeless service efficacy, focusing on the case of St. Louis, MO, USA.

Another study contributes to addressing various critical social issues, including homelessness, through the development of data-driven algorithmic solutions. Specifically, it seeks to mitigate homelessness by devising equitable policies and data-driven strategies to connect individuals with appropriate resources, ensuring a higher likelihood of a safe and stable exit from homelessness [2].

Our study is split into two parts. We first perform numerical analysis of data that consists of counts of homeless people across different demographics like age, gender, race, state, etc. We employ various algorithms like clustering, association pattern mining, and classification models like Random Forest and Gradient Boosting to understand underlying patterns in the data and factors that significantly influence homelessness.

The latter part of our study focuses on analyzing media headline data related to "homeless," i.e., text analysis of news titles scraped from news websites belonging to three different media categories—left-wing, neutral, and right-wing. We perform sentiment analysis (BERT), word frequency analysis, and topic modeling (LDA) to assess media depiction of homelessness by each political wing. We finally compare the analyses from both parts, numerical and text, to discern the relationship between media sentiments and the actual state of homelessness.

---

## 4. Methodology  
In our endeavor to comprehensively analyze the patterns of homelessness and their portrayal in the media, we've devised a multi-faceted approach. The methodology is segmented into specific tasks and grouped under distinct data categories for clarity and precision. Below is a detailed breakdown of our methods and analytical techniques:

### 4.1 Section 1: Numerical Analysis  
- **Part 0. Data Preprocessing**  
- **Part 1. Correlation**  
  - Using a heatmap to analyze strong correlations among variables to find patterns.  
- **Part 2. Clustering**  
  - Perform clustering to understand which demographics tend to group together.  
- **Part 3. Association Pattern Mining**  
  - Use the FP Growth algorithm to uncover demographic associations.  
- **Part 4. Classification Models**  
  - Apply classification models to identify factors influencing high/low homelessness levels.  

### 4.2 Section 2: Media Analysis  
- **Part 1. Web Scraping for News Headlines (2016-2022):**  
  - Scrape 100+ news article headlines per year using the keyword "homeless."  
  - Target three outlets with distinct political leanings: The New York Times (left), The Wall Street Journal (center), and The Washington Examiner (right).  

- **Part 2. Random Selection of Headlines:**  
  - Randomly select 100 headlines per media outlet annually.  

- **Part 3. Sentiment Analysis on Selected Headlines:**  
  - Conduct sentiment analysis (BERT), topic modeling (LDA), and word frequency analysis.  

- **Part 4. Analyze and Visualize Sentiment Analysis Data:**  
  - Extract and normalize sentiment data for visualization.  

- **Part 5. Annual Total Homeless Counts (2015-2022):**  
  - Calculate and visualize annual homeless trends using datasets.  

- **Part 6. Comparative Analysis of Media Sentiment:**  
  - Create line plots to compare sentiment by media outlet.  

- **Part 7. Detailed Sentiment Analysis by Media Outlet:**  
  - Aggregate and visualize sentiment scores across political categories.  

- **Part 8. Correlation Analysis Between Homelessness Data and Sentiment:**  
  - Check statistical assumptions and quantify relationships using correlation coefficients.  

---

---
# 5. Experiment

## 5.1 Section 1: Numerical Analysis

### 5.1.1 Data Acquisition - Homeless Count Data
The dataset utilized in this research project was acquired from the U.S. Department of Housing and Urban Development (HUD). The dataset comprises Point-In-Time (PIT) counts collected by Continuums of Care (CoCs) from 2007 to 2022. 

> *"PIT counts are unduplicated one-night estimates of homeless populations, encompassing both sheltered and unsheltered individuals. These counts are conducted annually nationwide during the final week of January. CoCs represent local planning bodies responsible for coordinating a comprehensive range of homelessness services within specific geographic areas, which can encompass cities, counties, metropolitan areas, or entire states"* [3].

---

### 5.1.2 Data Visualization

#### (a) Trend
1. **Trend of Overall Count**
   - The count of homelessness has not significantly reduced over the years.
   - A dip in 2021 is observed due to data collection issues post-pandemic.
2. **Trend Categorized by Age**
   - More homeless adults than children (under 18).
3. **Trend Categorized by Gender**
   - There are more homeless males than females.
   - The count for other genders is very low compared to males and females.
4. **Trend Categorized by Race**
   - **Before Normalizing:**
     - White and Black populations are most affected.
     - The White population shows higher absolute counts due to their larger share of the total population (76%).
     - Black populations face disproportionately high counts, driven by factors such as systemic racism, unfair incarceration, and drug addiction.
   - **After Normalizing:**
     - Native Hawaiian and Other Pacific Islanders, Black, American Indian, and Alaskan Native populations are most affected.
     - The normalized data reveals that the White population is less impacted in comparison.
     - Patterns persist across all years.
5. **Trend Categorized by Type of Homelessness (Sheltered vs. Unsheltered)**
   - Sheltered counts are decreasing, while unsheltered counts are increasing, indicating a worsening issue.

#### (b) Distribution of Data for Each Year (2015-2022)
- Distribution assessed using histograms and boxplots after applying log transformation.
- Log transformation normalized the data distribution, as shown in Appendix A and B.

#### (c) Variability Across Years
- Side-by-side boxplots reveal consistent variability in homeless counts across years.
- Homelessness has not shown significant improvement since 2015.

#### (d) Visualization by State
1. **Trends by State (Across Years):**
   - California and New York consistently show worse homelessness counts compared to other states.
   - Likely causes include high cost of living, violence, and drug abuse.
2. **2022 Homeless Counts (US Map):**
   - California and New York demonstrate significantly higher homelessness counts in 2022.

---

### 5.1.3 Numerical Analysis

#### (a) Part 1: Correlation Matrix
- Strong positive correlations (≥ 0.9) observed between the following variables:
  1. Under 18 and African American
  2. Under 18 and Female
  3. Over 18 and Female
  4. Over 18 and Male
  5. Female and Sheltered
  6. Male and Sheltered
- Further analysis conducted using clustering and association pattern mining.

#### (b) Part 2: Clustering
- **Dendrogram** and **Elbow Method** used to determine optimal clusters.
- Four clusters identified:
  1. **Cluster 2:**
     - Highest mean values for Under 18, Male, White, and Black populations.
     - Label: *Under 18, White and African American*.
  2. **Cluster 1:**
     - Highest mean for Over 18, Female, and significant counts for White and Black populations.
     - Label: *Adult Females, Predominantly White and African American*.
  3. **Cluster 4:**
     - Mixed demographic without strong dominance.
     - Label: *Diverse Group*.
  4. **Cluster 3:**
     - Minimal representation across all demographics.
     - Label: *Minimal or Non-Represented Demographics*.

#### (c) Part 3: Association Pattern Mining
- **FP Growth Algorithm** identified top 10 associated rules:
  1. Sheltered → White
  2. White → Sheltered
  3. Under 18 → White
  4. White → Under 18
  5. Under 18 → Sheltered
  6. Sheltered → Under 18
  7. Over 18 → White
  8. White → Over 18
  9. Over 18 → Sheltered
  10. Sheltered → Over 18

#### (d) Part 4: Random Forest and Gradient Boosting
- **Classification Models:** Random Forest and Gradient Boosting Classifiers applied to predict high (Class 1) vs. low (Class 0) homelessness levels.
  - Target variable based on overall homeless counts relative to the median.
- **Random Forest Model:**
  - Accuracy: 0.99
  - Metrics (Precision, Recall, F1): All ≥ 0.99.
- **Gradient Boosting Model:**
  - Accuracy: 0.99
  - Metrics (Precision, Recall, F1): All ≥ 0.99.
- **Cross-Validation Results:**
  - Consistently high performance across both models.
  - Important factors influencing homelessness:
    1. Gender - Male
    2. Age - Over 18

---

### (e) Conclusion
- **Key Findings:**
  - Homelessness has not significantly decreased over the years, with disparities among racial groups after normalization.
  - Clustering identified distinct demographic patterns, emphasizing homelessness among younger and minority groups.
  - Random Forest and Gradient Boosting models highlight significant demographic predictors of high homelessness.
- **Implications:**
  - The study underscores the need for targeted interventions and policy reforms addressing homelessness’s complex demographic factors.


# Section 2. Media Analysis

## (a) Part 1-3: Preparing Dataset
- **Data Collection:**  
  - Web-scraped news headlines (2016–2022) from three media outlets with distinct political leanings:
    - *The New York Times* (Left-leaning)
    - *The Wall Street Journal* (Centrist)
    - *The Washington Examiner* (Right-leaning)
  - Randomly selected 100 headlines from each outlet per year, resulting in a dataset of 2,100 headlines.

- **Analysis Methods:**  
  - Sentiment Analysis using BERT.  
  - Topic Modeling using LDA.  
  - Word Frequency Analysis.  

- **Data Storage:**  
  - Organized all collected data into structured text files for further analysis.

---

## (b) Part 4: Analyze and Visualize Sentiment Analysis Data

### **Sentiment Analysis Interpretation**
- **General Trends:**
  - *Very Negative* sentiments dominate across all years.
  - *Neutral* sentiments remain stable, with a slight increase in 2021.
  - *Positive* and *Very Positive* sentiments fluctuate, reflecting policy shifts or public perception changes.

- **Media-Specific Insights:**
  - *The New York Times* (Left):  
    - Higher proportion of *Very Negative* sentiment.
    - Slightly higher *Very Positive* sentiment compared to other outlets, indicating a mix of optimism and criticism.  
  - *The Wall Street Journal* (Center):  
    - Predominantly *Neutral* sentiment, reflecting balanced reporting.  
  - *The Washington Examiner* (Right):  
    - Lowest *Very Positive* sentiment, with significant *Very Negative* tones, indicating a critical narrative.

---

### **Word Frequency Analysis**
- **Key Observations:**
  - Terms like *shelters*, *school*, and *crisis* indicate societal discussions on homelessness.  
  - Mentions of *California*, *Trump*, and *policy* suggest political and regional focuses.  
  - Terms related to the COVID-19 pandemic emerge in 2020, highlighting its impact on homelessness.

---

### **Topic Analysis**

#### *The New York Times* (Left)
- **2016–2022:**  
  - Shift from broad societal discussions to specific issues like crime, housing solutions, and policy impacts.
  - Persistent focus on policy and social implications of homelessness.

#### *The Wall Street Journal* (Center)
- **2016–2022:**  
  - Emphasis on political leadership, state policies, societal infrastructure, and economic impacts.
  - Balanced approach blending policy critique with social narratives.

#### *The Washington Examiner* (Right)
- **2016–2022:**  
  - Politically charged coverage, emphasizing crime, housing policies, and societal issues.
  - Strong focus on immediate concerns and governance.

### **Narrative Comparisons Across Outlets**
- *The New York Times:* Policy-oriented with broader societal implications.  
- *The Wall Street Journal:* Analytical with emphasis on economic and social balance.  
- *The Washington Examiner:* Reactive and focused on immediate societal impacts.

---

## (c) Part 5: Annual Total Homeless Counts (2015–2022)

- **2021 Data Adjustment:**  
  - Used the average of 2020 and 2022 data due to anomalies caused by COVID-19.  
  - Maintains consistency in trend analysis while recognizing limitations of this estimation.

---

## (d) Part 6: Comparative Analysis of Media Sentiment

### **Key Observations:**
- Normalized *Overall Negative* and *Overall Positive* sentiments for comparative analysis.  
- *The Washington Examiner* most responsive to homeless count changes:
  - Strong correlation between rising counts and increased negative sentiment.  
- *The New York Times* and *The Wall Street Journal*:  
  - Less pronounced shifts, maintaining a balanced tone.  

---

## (e) Part 7: Detailed Sentiment Analysis by Media Outlet

### **Heatmap Insights:**
- *The Washington Examiner:*  
  - Significant shifts in negative sentiment during homelessness increases (e.g., 2018, 2020).  
- *The Wall Street Journal:*  
  - Stable neutral sentiment with occasional negative peaks.  
- *The New York Times:*  
  - Persistent *Very Negative* sentiment, tempered by slight positive shifts in later years.

---

## (f) Part 8: Correlation Analysis Between Homelessness Data and Sentiment

### **Correlation Insights:**
- *The Washington Examiner:*  
  - Strong positive correlation between *Overall Negative* sentiment and homeless counts (+0.876).  
  - Strong negative correlation between *Overall Positive* sentiment and homeless counts (-0.639).  
- *The Wall Street Journal:*  
  - Moderate correlations across sentiment categories, maintaining balance.  
- *The New York Times:*  
  - Moderate correlation for neutral sentiments; weak trends for positive and negative sentiments.

---

## (g) Media Sentiment Analysis - Comprehensive Conclusion

### **Synthesis of Findings:**
- *The Washington Examiner:*  
  - Most responsive to homelessness changes, amplifying societal concerns.  
- *The New York Times:*  
  - Critical, yet contextualized within broader societal and policy frameworks.  
- *The Wall Street Journal:*  
  - Maintains consistency with balanced reporting.

### **Integration of Insights:**
- Reveals the interplay of sentiment, topical focus, and word choice in framing homelessness.  
- Highlights the role of political orientation in shaping media narratives.

---

# 5.3. Comparison of Results from Numerical and Media Analysis

- Media negativity mirrors numerical increases in homelessness (2018–2020).  
- Media coverage of California aligns with numerical findings of high homeless counts.  
- *The Washington Examiner* aligns most closely with homeless count changes.  

---

# 6. Conclusion of Analysis

### **Key Takeaways:**
- Numerical analysis reveals persistent demographic disparities in homelessness.
- Media narratives add contextual layers, reflecting and shaping public discourse.
- Alignment of negative sentiment and numerical trends highlights interconnected realities.

### **Policy Implications:**
- Emphasize targeted interventions informed by integrated data and narrative analysis.  
- Address demographic disparities and regional challenges, particularly in California.  

---

# 7. Bibliography
1. A. Kube, *Data-driven decision-making: Using counterfactual predictions to allocate scarce homeless services fairly and efficiently*. Ph.D. dissertation, Washington University in St. Louis, 2022. [Online]. Available: [ProQuest](https://www.proquest.com/docview/2659594394)  
2. A. Rahmattalabi, *Towards Trustworthy and Data-Driven Social Interventions*. Ph.D. dissertation, Dept. Computer Science, University of Southern California, 2022. [Online]. Available: [Harvard Projects](https://projects.iq.harvard.edu/files/teamcore/files/thesis_aidarahmattalabi.pdf)  
3. U.S. Department of Housing and Urban Development, *The 2022 Annual Homeless Assessment Report to Congress - Part 1: Point-in-Time Estimates of Homelessness*. [Online]. Available: [HUD User](https://www.huduser.gov/portal/sites/default/files/pdf/2022-ahar-part-1.pdf)  

---

# 8. Appendix
- **Appendix A:** Distribution Analysis Plots  
- **Appendix B:** Variability Analysis Plots  
- **Appendix C:** Word Frequency and Topic Analysis Plots  
- **Appendix D:** Heatmap Analysis Plots  
- **Appendix E:** Correlation Scatter Plots  


---

## **9. References**
1. HUD: Annual Homeless Assessment Reports
2. FP Growth Algorithm: Wikipedia
3. Sentiment Analysis: Hugging Face BERT
4. Gradient Boosting Explained: Towards Data Science.



