# Nexus-AI-Internship-Tasks
Data Science and Machine Learning Work

# Data Science & Machine Learning Internship  

**Internship Organization:** Nexus AI Digital  
**Author:** Syed Huzaifa Bin Khamis  
**Role:** Data Science & Machine Learning Intern  

---

## Overview  
This repository contains the complete portfolio of projects completed during my internship at **Nexus AI Digital**.  
The work focused on solving real-world business problems for a retail company, using Data Science and Machine Learning techniques.  

The portfolio includes:  
- Exploratory Data Analysis (EDA)  
- Interactive Dashboards  
- Customer Churn Prediction (Baseline & Advanced)  
- Product Recommendation System  
- Sales Forecasting (Time Series)  

Each task demonstrates end-to-end workflow: **data preprocessing → modeling → visualization → business insights**.  

---

# Task 1: Exploratory Data Analysis (EDA)  

**Objective:**  
Before building predictive models, it is important to understand the data. This task explores the **Online Retail dataset** through cleaning, descriptive statistics, and visualization.  

**Steps Taken:**  
1. Data Loading (Pandas).  
2. Data Cleaning (removed missing `CustomerID`, dropped duplicates, converted date fields).  
3. Descriptive Stats (mean, median, spread of `Quantity`, `UnitPrice`, `TotalSales`).  
4. Visualizations:  
   - Histogram of customer sales  
   - Bar chart of sales by product  
   - Line chart of monthly sales  
   - Sales by country  
   - Customer spend distribution  

**Key Insights:**  
- A small number of products generate the majority of sales.  
- The UK contributes the highest revenue, followed by few other countries.  
- Clear **seasonal trends** (peaks in Nov–Dec).  
- Spending is skewed — few high-value customers dominate revenue.  
- Many impulse, low-value purchases.  

**How to Run:**  
```bash
pip install -r requirements.txt

🔹 Task 2: Interactive Dashboard

Objective:
Convert EDA insights into a clean, interactive dashboard for non-technical stakeholders.

Key Features:
Monthly Sales Trend (line chart)
Top 10 Products by Sales (bar chart)
Top Countries by Sales (bar chart)
Customer Spend Distribution (histogram)
Country Filter (dropdown)

How to Run:
pip install dash plotly pandas

🔹 Task 3: Customer Churn Prediction (Baseline Model)

Objective:
Predict which customers are at risk of leaving (churn) so GlobalMart can offer retention incentives.

Steps Taken:
Preprocessing: removed IDs, handled missing values, label-encoded categorical data.
Train-Test Split (80/20, stratified).
Model Training: Logistic Regression.
Evaluation: Accuracy + Confusion Matrix.

Results:
Accuracy: ~80%

Confusion Matrix:
✅ True Negatives → correctly predicted stayers
✅ True Positives → correctly predicted churners
⚠️ False Positives → predicted churn but actually stayed (extra retention cost)
❌ False Negatives → predicted stay but churned (most dangerous for business)
Key Insight: Logistic Regression is a good baseline but struggles with false negatives (missed churners).

How to Run:
pip install pandas numpy matplotlib seaborn scikit-learn

🔹 Task 4: Advanced Churn Prediction

Objective:
Improve churn prediction using advanced models.

Models Tested:
Logistic Regression (baseline)
Random Forest
XGBoost

Results (approx.):
Model	Accuracy	Precision	Recall	F1-Score
Logistic Regression	~80%	Moderate	Low	Moderate
Random Forest	~82%	Better	Improved	Better
XGBoost	~85%+	High	Best	Best

Key Insight:
XGBoost achieved the best recall (catching churners), which is critical in business.
Recommendation → Use XGBoost for deployment.

Technologies: Python, Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn

How to Run:
pip install pandas numpy matplotlib seaborn scikit-learn xgboost

🔹 Task 5: Product Recommendation System (Movies Example)

Objective:
Build a content-based recommendation system similar to e-commerce platforms.

Steps Taken:
Loaded TMDB 5000 Movies Dataset.
Converted descriptions → TF-IDF vectors.
Measured similarity (Cosine Similarity).
Built a recommender function → returns top 5 similar movies.

Example Results:
Input: The Dark Knight → Recommended: Batman Begins, The Dark Knight Rises, Iron Man…
Input: Avatar → Recommended: John Carter, Guardians of the Galaxy, Star Trek…
Input: Inception → Recommended: Shutter Island, Interstellar, The Matrix…

Key Takeaway:
Effective for new users (no history needed). Works on content similarity, but does not personalize beyond content.

🔹 Task 6: Forecasting Future Sales (Time Series Analysis)

Objective:
Forecast next 30 days of sales to optimize inventory & supply chain.

Steps Taken:
Data Preparation: converted dates, aggregated daily sales, handled missing days.
Stationarity Check: ADF test, applied differencing.
Model Training: SARIMA (1,1,1)(1,1,1,7).
Forecast: 30-day prediction with confidence intervals.

Visualization:
Historical Sales (blue)
Forecast (red)
Confidence Interval (shaded)

Results:
SARIMA captured weekly sales seasonality.
Forecast shows realistic trends with uncertainty bands.

Business Impact:
Prevent stockouts (lost revenue).
Avoid overstocking (extra costs).
Data-driven inventory management.

📈 Internship Outcomes & Learnings
Built end-to-end ML pipelines: EDA → Modeling → Evaluation → Visualization → Insights.

Strengthened skills in:
Python, Pandas, Numpy, Scikit-learn, Seaborn, Matplotlib, XGBoost
Data Cleaning & Feature Engineering
Machine Learning (Regression, Classification, Clustering, Forecasting)
Business Intelligence (Dashboards in Dash/Plotly, Power BI)
Learned how data-driven insights improve business strategy.

Nexus-AI-Internship-Tasks/
│── Code-1/         # Jupyter Notebook for Task 1
│── Task-1 Readme   # Task 1 Readme
│── Code-2/         # Jupyter Notebook for Task 2
│── Task-2 Readme   # Task 2 Readme      
│── Code-3/         # Jupyter Notebook for Task 3
│── Task-3 Readme   # Task 3 Readme      
│── Code-4/         # Jupyter Notebook for Task 4
│── Task-4 Readme   # Task 4 Readme
│── Code-5/         # Jupyter Notebook for Task 5
│── Task-5 Readme   # Task 5 Readme      
│── Code-6/         # Jupyter Notebook for Task 6
│── Task-6 Readme   # Task 6 Readme     
│── README.md       # Final Readme File

🚀 How to Use
Clone the repository:

git clone https://github.com/Syed-Huzaifa-coder/Nexus-AI-Internship-Tasks.git
cd Nexus-AI-Internship-Tasks


Install dependencies:
pip install -r requirements.txt

Run individual notebooks for each task inside notebooks/.

🙌 Acknowledgements
This project was completed as part of my Data Science & Machine Learning Internship at Nexus AI Digital.
Special thanks to my mentors for enabling real-world problem solving.
