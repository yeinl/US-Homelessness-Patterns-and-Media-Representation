
<div style="display: flex; flex-direction: column; align-items: center;">



# US Homelessness Patterns & Media Representation

## Understanding and Addressing U.S. Homelessness Through Data Science  
*A Comprehensive Analysis of Trends (2015-2022) and Media Representation Across Political Spectrums*

---

## 📑 **Table of Contents**
1. [Introduction](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#1-introduction)
2. [Problem Statement](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#2-problem-statement)
3. [Related Work](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#3-related-work)
4. [Methodology](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#4-methodology)
    - [Numerical Analysis](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#41-numerical-analysis)
    - [Media Analysis](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#42-media-analysis)
5. [Key Concepts and Background](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#5-key-concepts-and-background)
6. [Experiment](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#6-experiment)
    - [Numerical Analysis](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#61-numerical-analysis)
    - [Media Analysis](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#62-media-analysis)
7. [Conclusion of Analysis](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#7-conclusion-of-analysis)
8. [Bibliography](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#8-bibliography)
9. [References](https://github.com/yeinl/US-Homelessness-Patterns-and-Media-Representation/blob/main/README.md#9-references)


## 1. Introduction  
The true strength of a society often shows in how it treats its most vulnerable members. Homelessness is a telling challenge in this regard, reflecting not just the availability of shelter but broader issues like economic health and community support. Between 2007 and 2022, the story of homelessness in the U.S. has varied greatly, and not all these stories make it to the headlines.
 
This research is set against the backdrop of notable shifts in homelessness demographics. We're exploring how factors like age, gender, race, and geographical location influence patterns of homelessness. The landscape is vast: from young adults facing homelessness to elderly individuals navigating unique challenges. Notably, while some areas have successfully curtailed the rise of homelessness with innovative strategies, others find themselves battling unexpected surges. We additionally aim to spotlight regions that have excelled in their approach, serving as potential models for others.
 
An equally important facet of our study is the media's portrayal of homelessness. Through quantitative and qualitative analysis, we'll assess the themes present in online news articles segmented by state. By comparing these media depictions by analyzing their sentiments, against actual homelessness statistics, we aim to discern any disparities, offering a deeper understanding of potential media biases or misrepresentations.
 
To uncover these insights, we're turning to data mining—we employ techniques that delve deep into large datasets to uncover patterns and trends. While we will dive deeper into our methods later, it's worth noting that our approach is comprehensive, merging hard data with narrative analysis. This ensures a holistic understanding, shedding light on both statistics and stories.
 
In essence, "Bridging Realities" is not merely a research endeavor. It seeks to empower policymakers, NGOs, urban planners, and social welfare experts with a nuanced understanding of homelessness. By challenging prevailing narratives and offering a clearer picture, we hope to inspire a renewed commitment to addressing and understanding this pressing issue.


---

## 2. Problem Statement  
We aim to investigate changing patterns related to homelessness from 2015 to 2022 by conducting a thorough numerical analysis of homeless counts across diverse demographics such as age, gender, race, and state. Utilizing clustering, association pattern mining, and classification models (Random Forest, Gradient Boosting), we seek to identify underlying patterns and factors significantly influencing homelessness. Additionally, our study involves a text analysis of news titles related to homelessness from left-wing, neutral, and right-wing media categories. Employing sentiment analysis (BERT), word frequency, and topic modeling (LDA), we aim to assess media portrayals of homelessness across political wings. Furthermore, we seek to assess the alignment between Internet news portrayals by state and the actual circumstances of homelessness.


---

## 3. Related Work  
In recent research, machine learning and artificial intelligence have been harnessed to model complex systems, particularly within the context of homelessness. One study employs these technologies to predict returns to homelessness, examining numerous possible allocations of households to homeless services and generating reentry predictions for each combination of household and service. Additionally, it explores mathematical and theoretical optimization possibilities for the allocation process and investigates how predictions can enhance the understanding of homeless service efficacy, focusing on the case of St. Louis, MO, USA [1]. Another study contributes to addressing various critical social issues, including homelessness, through the development of data-driven algorithmic solutions. Specifically, it seeks to mitigate homelessness by devising equitable policies and data-driven strategies to connect individuals with appropriate resources, ensuring a higher likelihood of a safe and stable exit from homelessness [2]. 

Our study has been split into two parts. We first perform numerical analysis of data that consists of counts of homeless people across different demographics like age, gender, race, state, etc. We employ various algorithms like clustering, association pattern mining and employing classification models like Random Forest and Gradient Boosting to understand underlying patterns in the data and factors that significantly influence homelessness. The latter part of our study focuses on analysis of media headline data related to ‘homeless’, i.e., text analysis of news titles scraped from news websites belonging to three different media categories - left wing, neutral, and right wing. We perform sentiment analysis (BERT), word frequency analysis, and topic modeling (LDA) to assess media depiction of homelessness by each political wing. We finally compare the analyses from both parts, numerical and text, to discern the relationship between media sentiments and the actual state of homelessness. 



---

## 4. Methodology  
In our endeavor to comprehensively analyze the patterns of homelessness and their portrayal in the media, we've devised a multi-faceted approach. The possible methodology is segmented into specific tasks and grouped under distinct data categories for clarity and precision. The following provides a detailed breakdown of considering methods and analytical techniques:

### 4.1 Section 1: Numerical Analysis  
- **Step 1: Data Preprocessing** – Prepare data for analysis.
  ![image](https://github.com/user-attachments/assets/99e2a911-19ff-44e2-84ce-299b6d779961)
  <br> 
- **Step 2: Correlation Analysis** – Identify variable relationships using heatmaps.  
- **Step 3: Clustering** – Group demographics to uncover behavioral patterns.  
- **Step 4: Association Rule Mining** – Discover demographic associations with FP Growth.  
- **Step 5: Classification Models** – Analyze factors influencing homelessness using models.

### 4.2 Section 2: Media Analysis  
- **Step 1: Web Scraping** – Collect 100+ annual headlines (2016–2022) from three politically diverse outlets.  
- **Step 2: Headline Sampling** – Randomly select 100 headlines per outlet annually.  
- **Step 3: Sentiment and Topic Analysis** – Perform sentiment analysis, topic modeling, and word frequency analysis.  
- **Step 4: Sentiment Visualization** – Normalize and chart sentiment trends.  
- **Step 5: Homelessness Trends** – Visualize annual homeless counts (2015–2022).  
- **Step 6: Media Sentiment Comparison** – Compare sentiment trends across outlets.  
- **Step 7: Sentiment by Political Leaning** – Aggregate and visualize sentiment by political category.  
- **Step 8: Correlation Analysis** – Quantify relationships between sentiment and homelessness trends.  

---

# 5. Key Concepts and Background

To provide readers with a clear understanding of the technical foundation behind our analysis, this section introduces key concepts, theories, and methodologies from statistics, data mining, and data science. These are the building blocks that drive our investigation, from discovering patterns in homelessness data to interpreting media narratives.

---

## 5.1. Correlation Analysis: Quantifying Relationships

Correlation is a statistical measure that helps us understand the strength and direction of the linear relationship between two variables. In our project, correlation analysis played a pivotal role in identifying how demographic factors like age, gender, and race relate to homelessness counts.

### The Math Behind It
The Pearson correlation coefficient \( r \) is calculated using the formula:

<div align="center">

$$
r = \frac{\sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum_{i=1}^{n} (x_i - \bar{x})^2} \sqrt{\sum_{i=1}^{n} (y_i - \bar{y})^2}}
$$

</div>

Here:
- x_i and y_i are the values of variables X and Y,
- x̄ and ȳ are their respective means,
- n is the number of observations.

A value close to 1 indicates a strong positive relationship, -1 indicates a strong negative relationship, and 0 means no correlation.


### Why It Matters
In our study, correlation helped uncover meaningful patterns, such as the strong association between certain demographic groups (e.g., under-18 females) and sheltered homelessness.


---

## 5.2. Clustering: Unveiling Hidden Groups

Clustering is a method of grouping data points so that those in the same group are more similar to each other than to those in other groups. By applying clustering to our homelessness data, we identified demographic segments with shared characteristics, helping us pinpoint areas requiring focused intervention.

### Key Techniques
1. **The Elbow Method**:
   - Helps determine the optimal number of clusters by plotting the *Within-Cluster Sum of Squares (WCSS)* and identifying the "elbow point," where adding more clusters yields diminishing returns.
<div align="center">

$$
\text{WCSS} = \sum_{k=1}^{K} \sum_{x \in C_k} ||x - \mu_k||^2
$$

</div>


2. **Hierarchical Clustering**:
   - Groups data points by successively merging the closest clusters, visualized through a dendrogram.

### Application in Our Study
Clustering revealed key demographic clusters, such as a distinct group predominantly composed of young, African American individuals. This insight highlighted systemic factors disproportionately affecting certain populations.

---

## 5.3. FP-Growth: Mining Frequent Patterns

The FP-Growth algorithm efficiently identifies frequent itemsets within large datasets, making it invaluable for discovering demographic patterns in our homelessness data.

### How It Works
1. Constructs an FP-Tree (Frequent Pattern Tree) to represent itemsets compactly.
2. Traverses the tree to extract frequent itemsets without generating candidate sets.

### What We Learned
Using FP-Growth, we identified patterns like the high co-occurrence of "Under 18" and "Sheltered" homelessness among certain racial groups. This guided further analysis into systemic issues and resource allocation.

---

## 5.4. Sentiment Analysis: Decoding Media Tone

Sentiment analysis evaluates the emotional tone of text, categorizing it as positive, negative, or neutral. In our project, we used BERT (Bidirectional Encoder Representations from Transformers) to analyze thousands of media headlines and uncover trends in sentiment over time.

### Behind the Scenes
BERT processes each word in the context of the entire sentence, capturing nuances in meaning. The sentiment score is derived using a classification head attached to the model's final layer.

### Why It’s Important
Our analysis revealed that headlines often leaned "Very Negative" during periods of increasing homelessness, reflecting critical media coverage during societal crises like the pandemic.

---

## 5.5. Random Forest and Gradient Boosting: Predictive Powerhouses

To predict high versus low levels of homelessness, we employed two powerful machine learning algorithms: Random Forest and Gradient Boosting.

### Random Forest
This algorithm builds multiple decision trees and aggregates their predictions to improve accuracy and reduce overfitting. Its formula is:
<div align="center">

$$
\hat{y} = \frac{1}{n} \sum_{i=1}^{n} f_i(x)
$$

</div>

Where f_i(x) is the prediction from the i-th tree.



### Gradient Boosting
Gradient Boosting builds models sequentially, optimizing the error at each step. It minimizes the loss function \( L \) using:

<div align="center">

$$
F_m(x) = F_{m-1}(x) + h_m(x)
$$

</div>

Where h_m(x) represents the corrective model.


### Insights Gained
These algorithms highlighted critical predictors of high homelessness levels, such as "Gender - Male" and "Age - Over 18," corroborating patterns observed in the raw data.

---

## 5.6. Topic Modeling with LDA: Uncovering Themes

Latent Dirichlet Allocation (LDA) is a natural language processing technique that discovers underlying topics in text. In our media analysis, LDA helped us identify recurring themes in homelessness coverage.

### The Mathematics
LDA models each document as a mixture of topics and each topic as a mixture of words:

<div align="center">

$$
P(w | d) = \sum_{z} P(w | z)P(z | d)
$$

</div>

Where:
- P(w | z): Probability of word w given topic z,
- P(z | d): Probability of topic z given document d.


### Why It’s Insightful
By applying LDA, we uncovered themes like "pandemic-related impacts" and "policy discussions," shedding light on how media narratives evolved during key periods.


---
# 6. Experiment

## 6.1 Section 1: Numerical Analysis

### 6.1.1 Data Acquisition - Homeless Count Data
The dataset utilized in this research project was acquired from the U.S. Department of Housing and Urban Development (HUD). The dataset comprises Point-In-Time (PIT) counts collected by Continuums of Care (CoCs) from 2007 to 2022. “PIT counts are unduplicated one-night estimates of homeless populations, encompassing both sheltered and unsheltered individuals. These counts are conducted annually nationwide during the final week of January. CoCs represent local planning bodies responsible for coordinating a comprehensive range of homelessness services within specific geographic areas, which can encompass cities, counties, metropolitan areas, or entire states”[3]. 


---

### 6.1.2 Data Visualization

#### (a) Trend
1. **Trend of Overall Count**
   <br>
   <img width="284" alt="image" src="https://github.com/user-attachments/assets/9aa1de93-3a11-4ec9-8d65-7120543ffe32" />
   - The count of homelessness has not significantly reduced over the years.
   - A dip in 2021 is observed due to data collection issues post-pandemic.
2. **Trend Categorized by Age**
   <br>
   <img width="284" alt="image" src="https://github.com/user-attachments/assets/b16f6241-e818-4d62-badd-fcab7dab6eb4" />
   - More homeless adults than children (under 18).
3. **Trend Categorized by Gender**
   <br>
   <img width="284" alt="image" src="https://github.com/user-attachments/assets/94cb6b22-29dc-4e51-a922-083f6de5f4b4" />
   - There are more homeless males than females.
   - The count for other genders is very low compared to males and females.
4. **Trend Categorized by Race**
   - **Before Normalizing:**
     <br> 
     <img width="284" alt="image" src="https://github.com/user-attachments/assets/d614e09b-1a46-4483-934c-26abca67e29a" />
   - **After Normalizing:**
     <br> 
     <img width="284" alt="image" src="https://github.com/user-attachments/assets/3ef6a678-acdf-44b1-b3e1-69132d7988e2" />
     - Native Hawaiian and Other Pacific Islanders, Black, American Indian, and Alaskan Native populations are most affected.
     - The normalized data reveals that the White population is less impacted in comparison.
     - Patterns persist across all years.
5. **Trend Categorized by Type of Homelessness (Sheltered vs. Unsheltered)**
   <br>
   <img width="284" alt="image" src="https://github.com/user-attachments/assets/532c6321-b363-496f-87db-596f57d1e9db" />
   - Sheltered counts are decreasing, while unsheltered counts are increasing, indicating a worsening issue.

#### (b) Distribution of Data for Each Year (2015-2022)
- Distribution assessed using histograms and boxplots after applying log transformation.
- Log transformation normalized the data distribution. Below are some examples:
   ![image](https://github.com/user-attachments/assets/2ddded21-fc35-4bfc-a7c3-e22dcf6168c8)
   ![image](https://github.com/user-attachments/assets/f4125c23-354a-440f-a7ac-0a1abaf899ee)
  

#### (c) Variability Across Years
<br> 
<img width="286" alt="image" src="https://github.com/user-attachments/assets/d5dc73d7-5b33-4f26-ab5d-f6f4e7e7260e" />
<br> 
- Side-by-side boxplots reveal consistent variability in homeless counts across years.
- Homelessness has not shown significant improvement since 2015.

#### (d) Visualization by State
1. **Trends by State (Across Years):**
   <br>
   <img width="335" alt="image" src="https://github.com/user-attachments/assets/f8493b34-9330-4150-a65b-b1a5937650f0" />
   -  California and New York consistently show worse homelessness counts compared to other states.
   - Likely causes include high cost of living, violence, and drug abuse.
3. **2022 Homeless Counts (US Map):**
   <br>
   <img width="365" alt="image" src="https://github.com/user-attachments/assets/14350a74-3df9-49dd-b802-c9b4e9e3e78b" />
   - California and New York demonstrate significantly higher homelessness counts in 2022.

---

### 6.1.3 Numerical Analysis

#### (a) Part 1: Correlation Matrix
<br> 
<img width="468" alt="image" src="https://github.com/user-attachments/assets/fa559c69-df7b-4414-9807-90a580bce08e" />
<br> 
- Strong positive correlations (≥ 0.9) observed between the following variables:
  1. Under 18 and African American
  2. Under 18 and Female
  3. Over 18 and Female
  4. Over 18 and Male
  5. Female and Sheltered
  6. Male and Sheltered
- Further analysis conducted using clustering and association pattern mining.

#### (b) Part 2: Clustering
<br> 
<img width="311" alt="image" src="https://github.com/user-attachments/assets/39241395-a134-451e-bb10-38b0f4e0c947" />
<br> 
<img width="311" alt="image" src="https://github.com/user-attachments/assets/39cc24c1-e3a2-41d4-8333-d7aef7066193" />
<br> 
-  **Dendrogram** and **Elbow Method** used to determine optimal clusters.
   <br> 
   <img width="364" alt="image" src="https://github.com/user-attachments/assets/7054db5f-35f4-4bfe-84d8-8cb65e3f3ed3" />
   <br> 
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
In summary, the comprehensive analysis of homelessness data reveals several critical insights. The trend analysis indicates that the overall homelessness count has not significantly decreased over the years, with a noticeable dip in 2021 attributed to data collection challenges post-pandemic. Demographic trends highlight a higher prevalence of homelessness among adults, males, and specific racial groups. However, upon normalization, it becomes apparent that Native Hawaiin and Other Pacific Islanders, Black, American Indian, and Alaskan Native populations are disproportionately affected. The clustering analysis unveils distinct demographic clusters, emphasizing the prevalence of homelessness among young individuals, particularly White and African American populations. Association pattern mining identifies strong associations, such as "Sheltered" correlating with "Race - White" and "Age - Under 18." Classification models, specifically Random Forest and Gradient Boosting, showcase exceptionally high performance metrics, prompting further investigation through cross-validation. Notably, the models identify "Gender - Male" and "Age - Over 18" as key factors influencing high levels of homelessness. Overall, this multifaceted analysis enhances our understanding of homelessness patterns, emphasizing the need for targeted interventions and policy considerations to address the complex interplay of demographic factors contributing to homelessness across the United States.



# Section 2. Media Analysis

## (a) Part 1-3: Preparing Dataset
Parts 1 and 2 involve the process of collecting media headlines. We web-scraped news headlines from 2016 to 2022 from three media outlets, each with a distinct political leaning: The New York Times (left-leaning), The Wall Street Journal (centrist), and The Washington Examiner (right-leaning). We then randomly selected 100 headlines from each outlet for each year within this range, resulting in a total of 2,100 headlines.

In Part 3, we conducted sentiment analysis using BERT, topic modeling with LDA, and word frequency analysis to examine the narratives presented.

All the collected data was then organized and stored in structured text files.


---

## (b) Part 4: Analyze and Visualize Sentiment Analysis Data

First, we’ve done sentiment analysis.



### **Sentiment Analysis Interpretation**
- **General Trends:**
  <br>
  <img width="395" alt="image" src="https://github.com/user-attachments/assets/726ca781-a1de-4c05-b9cc-8f28854fee38" />
  - *Very Negative* sentiments dominate across all years.
  - *Neutral* sentiments remain stable, with a slight increase in 2021.
  - *Positive* and *Very Positive* sentiments fluctuate, reflecting policy shifts or public perception changes.

- **Media-Specific Insights:**
  <br>
  <img width="402" alt="image" src="https://github.com/user-attachments/assets/179ad621-6d3b-4293-b9d4-8957251ed15a" />
  - *The New York Times* (Left):  
    - Higher proportion of *Very Negative* sentiment.
    - Slightly higher *Very Positive* sentiment compared to other outlets, indicating a mix of optimism and criticism.  
  - *The Wall Street Journal* (Center):  
    - Predominantly *Neutral* sentiment, reflecting balanced reporting.  
  - *The Washington Examiner* (Right):  
    - Lowest *Very Positive* sentiment, with significant *Very Negative* tones, indicating a critical narrative.

---

### **Word Frequency Analysis**
Now, we’ve done word frequency analysis.
<br> 
<img width="403" alt="image" src="https://github.com/user-attachments/assets/137cccb2-7709-43b3-a953-721c48cd9f79" />

- **Key Observations:**
  - Terms like *shelters*, *school*, and *crisis* indicate societal discussions on homelessness.  
  - Mentions of *California*, *Trump*, and *policy* suggest political and regional focuses.  
  - Terms related to the COVID-19 pandemic emerge in 2020, highlighting its impact on homelessness.

These plots will be valuable when we later analyze sentiment in conjunction with homeless count data, providing detailed and deeper insights into possible factors of certain observations.


---

### **Topic Analysis**

Now, we’ve done topic analysis. Below are some examples:
<br> 
<img width="468" alt="image" src="https://github.com/user-attachments/assets/1a035413-8c3e-4e3a-9b50-0694dacd2fef" />
<br> 
<img width="468" alt="image" src="https://github.com/user-attachments/assets/d8553230-be6e-4c79-889a-bb71e2c68e48" />
<br> 

**Key Observations are:**

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

### **Different Narratives Across Media outlets:**
The New York Times maintains a policy-centric lens, often integrating broader societal implications with specific policy discussions. In contrast, The Wall Street Journal presents a more economically and politically analytical viewpoint, merging financial implications with social policies. The Washington Examiner's coverage is notably more politically charged, frequently framing homelessness within current political debates and immediate societal impacts.

Topic analysis has uncovered dynamic discussions concerning homelessness, mirroring contemporary events, political dynamics, and societal shifts. Similar to word frequency analysis, this approach will offer further insights into our forthcoming examination of homeless population data, allowing us to gain a more comprehensive and nuanced understanding of potential determinants underlying specific observations.



---

## (c) Part 5: Annual Total Homeless Counts (2015–2022)
<br> 
<img width="366" alt="image" src="https://github.com/user-attachments/assets/eed6f5cb-362f-4236-8db6-13f9c6c9efe0" />
<br> 
<img width="391" alt="image" src="https://github.com/user-attachments/assets/edc41e9c-b5e6-4ee9-ab1b-e3f3fe5d2875" />
<br> 

- **2021 Data Adjustment:**  
  - Used the average of 2020 and 2022 data due to anomalies caused by COVID-19.  
  - Maintains consistency in trend analysis while recognizing limitations of this estimation.

---

## (d) Part 6: Comparative Analysis of Media Sentiment
<br> 
<img width="375" alt="image" src="https://github.com/user-attachments/assets/2575dfa2-8da3-4b9d-80bd-ae8dc356ac6d" />
<br> 
<img width="386" alt="image" src="https://github.com/user-attachments/assets/2717e128-fe79-42a2-b0e3-ff29dd0eb043" />
<br> 
<img width="369" alt="image" src="https://github.com/user-attachments/assets/ecdd0ce9-e01d-4bd8-821e-b815fd5eac77" />
<br> 
<img width="369" alt="image" src="https://github.com/user-attachments/assets/25278353-57a3-4a16-99f2-3b19b63e0d22" />
<br> 
<img width="369" alt="image" src="https://github.com/user-attachments/assets/6377f051-9273-4577-a343-ed004deaa90f" />
<br> 

### **Key Observations:**
- This comparative analysis of media sentiment underscores distinct patterns in how media outlets respond to homelessness trends, influenced by their political leanings.
- The Washington Examiner (Right) displays the most pronounced response, with a marked increase in negative sentiment correlating strongly with rising homeless counts. This suggests a narrative intensely reactive to changes in societal issues.
- In contrast, The New York Times (Left) adopts a more measured approach, with a less pronounced but still noticeable increase in negative sentiment during periods of heightened homelessness.
- The Wall Street Journal (Center) strives for a balanced narrative, maintaining relative stability in sentiment despite fluctuations in homelessness.
- Overall, our findings reveal that while each outlet reflects changes in homelessness, the extent and nature of their response are distinctly shaped by their political orientations.
We have completed the initial stages of our analysis, encompassing all media outlets as a collective unit. In the first three steps, we engaged in scraping and examining news headlines spanning several years. Subsequent steps, four through six, involved conducting a sentiment analysis and creating visualizations to represent these findings over multiple years.

The next phase of our project will enhance our ability to visually discern how media sentiment, this time with a focus on more detailed sentiments.

---

## (e) Part 7: Detailed Sentiment Analysis by Media Outlet
For this part, we’ve assigned categories to the media outlets based on their political leanings. And, we’ve calculated sentiment scores, for visualizations using heatmaps. Below are some examples:
<br> 
<img width="284" alt="image" src="https://github.com/user-attachments/assets/f4c562cf-1f23-4eb1-ab6a-da1a975c6e12" />
<br> 
<img width="284" alt="image" src="https://github.com/user-attachments/assets/e3838ea1-7521-43e5-8cba-85f017bd5fb1" />


### **Heatmap Insights:**
- *The Washington Examiner:*  
  - Significant shifts in negative sentiment during homelessness increases (e.g., 2018, 2020).  
- *The Wall Street Journal:*  
  - Stable neutral sentiment with occasional negative peaks.  
- *The New York Times:*  
  - Persistent *Very Negative* sentiment, tempered by slight positive shifts in later years.

---

## (f) Part 8: Correlation Analysis Between Homelessness Data and Sentiment

Before proceeding with correlation analysis, it's important to check for normality, linearity, homoscedasticity, and independence. Let's check statistical assumptions.

- Homeless Count Normality: Statistics=0.880, p=0.187
- Overall Negative Sentiment Normality: Statistics=0.917, p=0.077
- Neutral Sentiment Normality: Statistics=0.937, p=0.186
- Overall Positive Sentiment Normality: Statistics=0.917, p=0.074

The output from our Shapiro-Wilk test for normality indicates that the data for homeless counts and the sentiments (Overall Negative, Neutral, and Overall Positive) do not significantly deviate from a normal distribution. Therefore, we can proceed with statistical methods that assume normal distribution now.

For the next assumption, independence. Since the data points represent different years and the data collection process was independent from year to year, then this assumption should be satisfied.

And here, we've checked the linearity and homoscedasticity using scatter plots. Below are some examples: 

<br>
<img width="284" alt="image" src="https://github.com/user-attachments/assets/1ac9b0ca-f6b9-42d9-8ee7-9276a72dbd7b" />
<br> 
<img width="284" alt="image" src="https://github.com/user-attachments/assets/352ff310-a496-4918-9d66-5412eb7012b9" />
<br> 
<img width="284" alt="image" src="https://github.com/user-attachments/assets/4ee24316-755d-4e36-87f1-383ff96bfadb" />


Visual inspection of scatter plots suggests that while perfect linearity and homoscedasticity are not evident, the data does not exhibit strong non-linearity or clear patterns of heteroscedasticity.
Given these findings, we proceeded with Pearson’s correlation analysis, recognizing that while the assumptions are not strictly satisfied, the observed deviations appear to be minor and not excessively influential on the overall trends.
However, we should note that these factors introduce a degree of uncertainty into the correlation estimates. Further studies, potentially involving larger datasets and robust statistical techniques, would be beneficial to confirm the observed relationships.

Now, let's start on calculating correlation coefficients to explore the strength and direction of the relationship between media sentiment and homeless counts.


Correlation between Homeless Counts and Sentiments:
<br> 
<img width="404" alt="image" src="https://github.com/user-attachments/assets/27043d3c-1f6e-49b5-a7de-c652d7b9bd53" />


This analysis suggests that The Washington Examiner's coverage aligns more closely with actual changes in homeless counts, particularly by increasing negative sentiment as homeless counts rise. Conversely, The Wall Street Journal and The New York Times tend to display a decrease in positive sentiment as homeless numbers increase, though the strength of this relationship varies. However, to fully grasp the narratives presented by different media outlets, it is crucial to consider these correlations within the broader context of political climates, significant events, policy changes, and public opinion. We will talk more about this in the next (last) part, 'Media Sentiment- Comprehensive Conclusion'.



---

## (g) Media Sentiment Analysis - Comprehensive Conclusion

Our extensive analysis of media sentiment toward homelessness, through the multifaceted lenses of sentiment analysis, correlation with homeless counts, word frequency, and topic modeling, reveals a complex tapestry of media narratives deeply influenced by political orientations and societal contexts.


### **Synthesis of Findings:**
- *The Washington Examiner (Right):*  
  - Most responsive to homelessness changes, amplifying societal concerns.  
- *The New York Times (Left):*  
  - Critical, yet contextualized within broader societal and policy frameworks.  
- *The Wall Street Journal (Center):*  
  - Maintains consistency with balanced reporting.



### **Correlation with Homeless Counts:**
- Each outlet's sentiment towards homelessness exhibited varying degrees of correlation with actual homeless counts. The Washington Examiner's (Right) coverage most closely mirrored changes in homelessness, with a marked increase in negative sentiment corresponding with rising homeless counts. This suggests a narrative deeply responsive to the severity of the homelessness crisis. Conversely, The Wall Street Journal (Center) and The New York Times (Left) displayed a more moderated response, with a focus on maintaining a balanced or cautiously optimistic narrative, despite the fluctuations in homelessness figures.

### **Word Frequency and Topic Modeling Insights:**
- The topical focus and language used by the different outlets revealed their unique editorial angles and perspectives on homelessness. We observed a range of themes, from policy and political discussions in The New York Times (Left) to societal and infrastructural considerations in The Wall Street Journal (Center), and a more politically charged narrative from The Washington Examiner (Right).
- The prevalence of specific terms like "shelters," "policy," and "crisis" across the outlets indicates a shared recognition of the systemic nature of homelessness, yet the emphasis varied, reflecting each outlet's editorial focus and ideological stance.

### **Integrating the Insights:**
- This multi-dimensional analysis illuminates how media outlets not only report on homelessness but also frame the issue through their distinct ideological lenses. The interplay of sentiment, topical focus, and word choice creates narratives that both reflect and shape public understanding and discourse around homelessness.
- The Washington Examiner (Right) emerges as the most responsive to the changing realities of homelessness, with a narrative that amplifies societal concerns. The New York Times (Left), while critical, incorporates a diverse range of topics, possibly aiming to contextualize homelessness within broader societal and policy frameworks. The Wall Street Journal (Center) balances these approaches, maintaining a consistent narrative tone while navigating the complexities of the issue.

### **Final Thoughts:**
- This comprehensive analysis underscores the pivotal role media outlets play in shaping societal perceptions of complex issues like homelessness. By understanding the nuances in their narratives, we can better appreciate the multifaceted nature of homelessness and the diverse viewpoints that contribute to the public discourse. This insight is invaluable not only for media consumers seeking a more rounded understanding of homelessness but also for policymakers, advocates, and researchers who navigate these narratives to influence policy and public opinion.
 

---

# 6.3. Comparison of Results from Numerical and Media Analysis
- The consistent negative sentiment in media titles aligns with the numerical analysis, reflecting a parallel increase in negativity and homeless counts from 2018 to 2020.
- Word frequency and topic modeling confirm California's severe homelessness situation, correlating with numerical findings of the highest homeless count in the state.
- During the 2018-2020 rise in homeless counts, media sentiments turned more negative, especially in NYT and WSJ, mirroring the moderation in the rate of homeless count increase from 2020 to 2022.
- Right-wing media, notably The Washington Examiner, closely aligns with changes in homeless counts, displaying increased negative sentiment with rising counts. In contrast, The Wall Street Journal and The New York Times exhibit nuanced responses, with fluctuations in positive sentiment, underscoring the importance of considering broader contextual factors.



---

# 7. Conclusion of Analysis
In conclusion, our multifaceted analysis of homelessness, integrating numerical insights and media narratives, provides a comprehensive understanding of this complex societal issue. The numerical analysis exposes persistent challenges, emphasizing demographic disparities, particularly among Native Hawaiin and Other Pacific Islanders, Black, American Indian, and Alaskan Native populations. The media analysis accentuates the influential role of media in shaping public perceptions of homelessness, adding layers of context to the numerical findings. Crucially, the alignment between negative media sentiments and numerical trends underscores the interconnected nature of public discourse and statistical realities. The spotlight on California's severe homelessness situation, mirrored in both analyses, emphasizes the urgency for targeted interventions. The nuanced responses of media outlets, particularly the right-wing's alignment with homeless count changes, highlight the necessity of contextual considerations. This synthesis of numerical and media analyses not only deepens our comprehension of homelessness patterns but also underscores the importance of a holistic approach, merging quantitative insights with media narratives, to inform effective policies and public discourse surrounding homelessness in the United States.


---

# 8. Bibliography
1. A. Kube, *Data-driven decision-making: Using counterfactual predictions to allocate scarce homeless services fairly and efficiently*. Ph.D. dissertation, Washington University in St. Louis, 2022. [Online]. Available: [ProQuest](https://www.proquest.com/docview/2659594394)  
2. A. Rahmattalabi, *Towards Trustworthy and Data-Driven Social Interventions*. Ph.D. dissertation, Dept. Computer Science, University of Southern California, 2022. [Online]. Available: [Harvard Projects](https://projects.iq.harvard.edu/files/teamcore/files/thesis_aidarahmattalabi.pdf)  
3. U.S. Department of Housing and Urban Development, *The 2022 Annual Homeless Assessment Report to Congress - Part 1: Point-in-Time Estimates of Homelessness*. [Online]. Available: [HUD User](https://www.huduser.gov/portal/sites/default/files/pdf/2022-ahar-part-1.pdf)  


---

# 9. References**
1. HUD: Annual Homeless Assessment Reports
2. FP Growth Algorithm: Wikipedia
3. Sentiment Analysis: Hugging Face BERT
4. Gradient Boosting Explained: Towards Data Science.

</div>
