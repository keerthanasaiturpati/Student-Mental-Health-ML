# Student Mental Health - Stress Level Prediction
Predicting the student stress levels(low/medium/high) based on screen time, sleep duration, physical activities, age, education level, gender, anxiety befor exams and academic performance change.

## Problem Statement
Mental health is a concern and for students who build the future it is even more concerning. So through this small project I tried to predict the Stress levels based on their lifestyle.As they say, Prevention is better than cure; if stress is identified early before it causes damage, it can be a great support for students.

## Dataset
- **Source:** Kaggle
- **Size:** 1000 rows, 10 columns
- **Target Column:** Stress level( Low/ Medium/ High)
- **Type of problem:** Multi class Classification(used 3)

## Tech Stack:
- **Language:** Python
- **Libraries:** Numpy, Pandas, Plotly Express, Scikit-Learn
- **Environment:** VS Code Notebook

## Project Pipeline:
1. EDA(Exploratory Data Analysis)
2. Preprocessing(Encoding+Scaling)
3. Train-Test Split
4. Model Training
5. Evaluation
6. Feature Importance

## EDA(Exploratory Data Analysis)
- **Visualization Tool:** Plotly Express
**Observations:**
  - **Medium stress class had the most smaples, causing class imbalance**
  - **More screen time showed higher stress levels(obvious I guess)**
  - **More sleep duration showed lower stress levels(Even more obvious)**
  - This dataset felt real-world enough to work with as 2 observations already show it.

## Preprocessing:
- Dropped the column named Name because predicting the stress levels have nothing to do with a person's name
- Label Encoding, Used for ordinal colmns like Educational level, Stress level because they have a natural order like low < medium < high
- One Hot Encoding, Used for nomial columns like Gender, Anxious Before exams, Academic Performance change because these columns donot have a natural order.
- Feature Scaling, Used StandardScaler to normalize features so that no single feature dominates.

## Model Training
Trained 3 models and compared them:
- **Logistic Regression:** simple and fast
- **Decision Tree:** splits data based on conditions
- **Random Forest:** a bunch of decision trees voting together!(ensemble learning)

Used `class_weight='balanced'` for all 3 models to handle class imbalance — 
so the model doesn't just keep predicting Medium every time!

## Evaluation Results
| Model | Accuracy |
|---|---|
| Logistic Regression | ~37% |
| Decision Tree | ~38% |
| Random Forest | ~40% |

Yeah the accuracy is low I know, but here's what I learned from this —
low accuracy isn't always a failure. Sometimes the data just doesn't have strong enough patterns and no amount of tuning will fix that. The real skill is understanding WHY model is struggling, not just chasing a higher number!

## Feature Importance
Used Random Forest to find which features mattered the most:
1. Screen Time (hrs/day)
2. Sleep Duration (hrs)
3. Physical Activity (hrs/week)
4. Age
5. Education Level

This matched exactly what I observed during EDA.

## Key Learnings
- Class imbalance can completely fool your model
- Data quality matters more than model complexity
- EDA observations and feature importance should tell the same story
- Sometimes the data just isn't good enough — and that's okay!
- A complete pipeline matters more than a perfect accuracy score

## Author

**Keerthana Sai Turpati**

CSE Student | Machine Learning Enthusiast | Learning in Public 🙌

⭐ If this helped you in any way, feel free to star the repo!


