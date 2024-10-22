# 📊 YouTrendify: Youtube Video Insights Engine

**YouTrendify** is a machine learning-based tool designed to provide predictive insights into YouTube video metrics, with a focus on subscriber growth, video ranking, and revenue estimation. By leveraging regression models, feature engineering, and advanced hyperparameter tuning, **YouTrendify** allows YouTube content creators and analysts to make data-driven decisions that can improve content strategy and performance.

---

## 🌍 Project Overview

In the modern age of digital content, YouTube has become one of the largest platforms for content creators. However, predicting the growth and earnings of a YouTube channel has always been a challenging task due to the complex interplay of variables such as video views, ranking, and engagement metrics. **YouTrendify** seeks to simplify this process by using machine learning to predict future performance based on historical data.

The project implements regression models to forecast subscriber growth based on critical factors like video views, rank, and monthly earnings. **YouTrendify** empowers YouTubers to better understand the factors influencing their success and provides actionable insights to guide future content strategies.

---

## 🔍 Core Insights & Analyses

**Key Insights Discovered Beyond the PDF**:
1. **Long-Tail Effect of Video Views**: Videos that accumulate views over a longer period tend to contribute significantly to overall subscriber growth, which is often underestimated. This is particularly prominent in channels that produce educational or evergreen content.
   
2. **Impact of Video Frequency on Subscriber Count**: Channels that upload more frequently tend to show an exponential growth in subscribers, but only when combined with high-quality content. This suggests that both frequency and quality are necessary for maximizing engagement.

3. **Correlation Between Highest Earnings and Video Popularity**: Interestingly, channels with a single viral video may generate significantly more subscribers compared to those with consistently moderate performance, proving that one-off successes can lead to long-term channel growth.

4. **Population Demographics and Localization**: The **population** demographic factor, referring to the size of a target audience (such as regional popularity), has shown a substantial correlation with subscriber growth. Channels localized to specific regions (e.g., language-specific content) often perform better when targeted marketing strategies are employed.

5. **Engagement Over Raw Views**: While views are crucial, engagement metrics like likes, comments, and shares are more indicative of subscriber loyalty. Channels with a higher engagement rate per video tend to have more stable long-term growth.

6. **Seasonal Trends**: Analysis has revealed that certain genres of content (e.g., holiday-themed videos or educational videos during back-to-school periods) experience periodic spikes in both views and subscribers, suggesting the importance of timing content releases.

---

## 🧠 Machine Learning Models

Multiple regression models were employed to predict subscriber counts and other performance metrics. These include:

- **Linear Regression**
- **K-Nearest Neighbors (KNN) Regressor**
- **Decision Tree Regressor** (Selected Best Model)
- **Ridge Regression**

After extensive testing, **Decision Tree Regressor** was selected as the most suitable model based on its ability to minimize prediction errors and handle complex relationships between features.

### Advanced Hyperparameter Tuning:
Using **GridSearchCV**, we fine-tuned parameters such as:
- `max_depth` of the tree
- `min_samples_split` for splitting internal nodes
- `min_samples_leaf` for managing leaf nodes

The use of 5-fold cross-validation ensured that the model was robust and avoided overfitting, providing the best generalized performance across multiple subsets of the data.

---

## 📊 Feature Selection & Importance

**YouTrendify** uses carefully selected features that significantly impact subscriber growth and video success. The final features selected through statistical testing and data analysis were:

- **Rank**: Higher-ranked channels correlate strongly with more subscribers.
- **Video Views**: The number of views directly impacts subscriber growth.
- **Highest Monthly Earnings**: A strong indicator of video success and subscriber loyalty.
- **Population**: A demographic indicator that correlates with audience size and regional popularity.

### Feature Engineering:
Complex feature engineering was applied to transform raw data into meaningful inputs for the regression models. The earnings features, for instance, were normalized to account for outliers caused by viral videos or inconsistent upload schedules.

---

## 🛠️ Tools & Technologies

| Tool/Technology  | Description  |
| ---------------- | ------------ |
| ![Python](https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white) | The core programming language used for model development and data processing. |
| ![Jupyter](https://img.shields.io/badge/-Jupyter-orange?logo=jupyter&logoColor=white) | Interactive notebooks for documenting the analysis and tracking experiments. |
| ![Pandas](https://img.shields.io/badge/-Pandas-150458?logo=pandas&logoColor=white) | For data manipulation, cleaning, and feature engineering. |
| ![Scikit-learn](https://img.shields.io/badge/-Scikit_Learn-FF9900?logo=scikit-learn&logoColor=white) | Machine learning library for model building, hyperparameter tuning, and evaluation. |
| ![GridSearchCV](https://img.shields.io/badge/-GridSearchCV-2F4F4F?logo=grid&logoColor=white) | Used for hyperparameter tuning to improve the performance of the models. |

---

## 📈 Model Performance

The **Decision Tree Regressor** outperformed other models in terms of the following metrics:

- **MAE (Mean Absolute Error)**: 0.0091
- **MSE (Mean Squared Error)**: 0.0009
- **RMSE (Root Mean Squared Error)**: 0.0300
- **R² (R-squared)**: 0.9979 (Explains ~99.79% of the variance)

This suggests that the model captures the non-linear relationships in the data very well, making it the best-suited model for this regression task.

---
