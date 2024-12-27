# Disaster Tweet Classification  

This project focuses on identifying whether a tweet is related to a disaster or not using advanced data processing and machine learning techniques.  

## Project Workflow  

### 1. Data Loading and Initial Setup  
Pranjali Ganvir:  
  - Imported required libraries.  
  - Loaded the training dataset (CSV format) containing tweets and related metadata.  

### 2. Data Preprocessing  
Natasha Kucheriya:

Data preprocessing was performed to clean and prepare the dataset for effective modeling. The following steps were taken:  

- **Duplicate Removal**:  
  - Identified and removed duplicate entries to maintain data quality and avoid redundancy.  

- **Handling Missing Values**:  
  - Addressed missing data in the "Keyword" column using a two-step approach:  
    - **POS Tagging**: Utilized Part-of-Speech tagging to infer missing keywords based on the context of the tweets.  
    - **Keyword Matching**: Checked for disaster-related terms (e.g., "earthquake") within the tweet text to populate missing keywords where possible.  

- **Text Normalization**:  
  - Performed lemmatization to reduce words to their base forms, ensuring consistency in text analysis.  

- **Column Cleanup**:  
  - Dropped unnecessary columns, such as "ID" and "Location", which were deemed irrelevant for the classification task.  

These steps ensured a cleaner, more meaningful dataset ready for exploratory analysis and modeling.  

### 3. Exploratory Data Analysis (EDA)
Atharva Kulwar:

EDA was conducted to gain a deeper understanding of the dataset and uncover patterns that could improve model performance:  
- **Data Distribution**:  
  - Analyzed the distribution of tweets labeled as disaster-related and non-disaster-related to understand class imbalance.  
- **Text Insights**:  
  - Visualized the most frequently occurring words using word clouds for both disaster and non-disaster tweets.  
  - Explored the impact of keywords and locations on the target variable.  
- **Length Analysis**:  
  - Investigated tweet lengths to identify any significant differences between the two classes.  

Insights from EDA guided subsequent steps in feature engineering and model selection.  

### 4. Feature Engineering  
Mayuresh Khatavkar:
Feature engineering transformed raw text data into meaningful numerical representations suitable for machine learning models:  
- **Word2Vec Embeddings**:  
  - Leveraged Word2Vec to generate dense vector representations of tweets, capturing semantic meanings of words and their contextual relationships.  
  - Pre-trained embeddings were fine-tuned on the dataset to enhance the quality of vectorization.  
- **Additional Features**:  
  - Extracted linguistic features such as tweet length, number of hashtags, mentions, and URLs, which were included as supplementary inputs to the model.  

### 5. Model Training
Ajinkya Bhambre and Isha Jethwa:

A machine learning pipeline was designed and implemented to classify tweets effectively:  
- **Model Selection**:  
  - Experimented with multiple algorithms, including Logistic Regression, Random Forest, and XGBoost models, to identify the best-performing model.  
- **Evaluation**:  
  - Assessed model accuracy, precision, recall, and F1-score on validation data to ensure robust performance.  

