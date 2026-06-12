Netflix Recommendation System

Project Overview

This project develops a movie recommendation system using the Netflix Prize Dataset.

The objective is to predict user ratings and generate personalized movie recommendations using collaborative filtering and matrix factorization techniques.

The project investigates multiple evaluation strategies, including random, temporal, and per-user temporal splits, to better understand recommendation performance in realistic settings.


Dataset

Netflix Prize Dataset

Original Dataset:

- 100M+ ratings
- 480K+ users
- 17K+ movies

Modeling Sample

Metric | Value 

Ratings | 2,000,000 
 Users | 358,375 
 Movies | 17,324 
 Date Range | 1999 - 2005 

The sample preserves nearly the entire movie catalog while remaining computationally feasible for training and evaluation.


Project Workflow

Data Processing

1. Data Understanding
2. Exploratory Data Analysis
3. Split Diagnostics
4. Modeling Dataset Creation

Model Training

1. Item-Based Collaborative Filtering
2. Singular Value Decomposition (SVD)
3. SVD Hyperparameter Tuning
4. SVD++

Evaluation

1. RMSE Evaluation
2. Cold Start Analysis
3. Top-K Recommendation Generation
4. Ranking Metrics Evaluation

Repository Structure

Data Processing

- 01_Data_Understanding.ipynb
- 02_EDA.ipynb
- 05_Split_Diagnostics.ipynb
- 06_Modeling_Dataset_Creation.ipynb

Model Training

- 03_Random_Split_Models.ipynb
- 04_Temporal_Split_Models.ipynb
- 07_Per_User_Temporal_Split.ipynb
- 08_SVD_Hyperparameter_Tuning.ipynb
- 09_SVDpp_Model.ipynb

Evaluation

- 10_Cold_Start_Study.ipynb
- 11_TopK_Recommendations.ipynb
- 12_Ranking_Evaluation.ipynb

Final Results

- 13_Final_Results.ipynb



Models Evaluated

Model | RMSE 

Item-CF Random | 1.088 
SVD Random | 0.985 
 Item-CF Temporal | 1.125 
 SVD Temporal | 1.034 
 Item-CF Per User Temporal | 1.154 
 SVD Per User Temporal | 0.973 
 Tuned SVD | 0.970 
 SVD++ | 0.979 



Recommendation Quality

Original Evaluation

 Metric | Score 

 Precision@10 | 0.594 
 Recall@10 | 0.999 
 MAP@10 | 0.644 

Stricter Evaluation

Users with at least 10 test interactions.

Metric | Score 

 Precision@10 | 0.437 
 Recall@10 | 0.898 
 MAP@10 | 0.597 



Cold Start Analysis

Segment | Ratings | RMSE 

 Cold | 116,863 | 1.697 
 Light | 124,001 | 1.737 
 Medium | 26,493 | 1.910 
 Heavy | 446 | 3.211 

Observation

Cold-start users remain a significant challenge for recommendation systems. Performance varies considerably across user activity levels.

---

Key Findings

- Matrix factorization methods consistently outperformed Item-Based Collaborative Filtering.
- Tuned SVD achieved the best predictive performance with an RMSE of 0.970.
- Temporal evaluation provided a more realistic estimate of recommendation quality than random evaluation.
- Cold-start users remain difficult to model accurately.
- Recommendation quality remained strong under stricter ranking evaluation.

---

Reproducing Results

Install Dependencies

```bash
pip install -r requirements.txt
```

Run Notebooks in the Following Order

1. 01_Data_Understanding.ipynb
2. 02_EDA.ipynb
3. 03_Random_Split_Models.ipynb
4. 04_Temporal_Split_Models.ipynb
5. 05_Split_Diagnostics.ipynb
6. 06_Modeling_Dataset_Creation.ipynb
7. 07_Per_User_Temporal_Split.ipynb
8. 08_SVD_Hyperparameter_Tuning.ipynb
9. 09_SVDpp_Model.ipynb
10. 10_Cold_Start_Study.ipynb
11. 11_TopK_Recommendations.ipynb
12. 12_Ranking_Evaluation.ipynb
13. 13_Final_Results.ipynb



 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-Learn
- Scikit-Surprise
- Jupyter Notebook



Author

Shreya Kale , Sneha Shukla

B.Tech, Civil Engineering

Indian Institute of Technology Roorkee
