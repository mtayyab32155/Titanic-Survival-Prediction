
# 🚢 Titanic Survival Prediction - ML Project

## 📊 Project Overview
Complete machine learning pipeline predicting Titanic passenger survival with **83.29% accuracy**. Implemented 7 algorithms with hyperparameter tuning and advanced feature engineering.

## 🏆 Model Performance
| Model | Accuracy | Best Parameters |
|-------|----------|-----------------|
| Gradient Boosting | **83.29%** | learning_rate=0.01, n_estimators=300 |
| Random Forest | 83.14% | max_depth=10, n_estimators=300 |
| Support Vector Machine | 81.88% | C=100, kernel= rbf |
| Logistic Regression | 81.32% | C=1.0 |
| Decision Tree | 81.18% | max_depth=30 |
| Naive Bayes | 77.68% | var_smoothing=1e-08 |
| K-Nearest Neighbors | 77.53% | n_neighbors=7 |

## 🔍 Key Insights Discovered
### Top Survival Factors:
1. **Gender**: Women had 74% survival vs 19% for men
2. **Passenger Class**: 1st class = 63% survival, 3rd class = 24%
3. **Group Size**: Pairs/trios (2-3 people) = 71% survival (optimal)
4. **Age**: Children (<16) = 55% survival

### My Feature Engineering Success:
- **TicketGroupSize**: Created from ticket data → 8% feature importance
- **Cabin_Deck**: Extracted from cabin numbers
- **Title Extraction**: Mr/Mrs/Miss patterns from names

## 🛠️ Technical Implementation
### Data Pipeline:
```python
1. Data Cleaning → Missing value imputation
2. Feature Engineering → 5+ new features created
3. Preprocessing → ColumnTransformer with dual encoding
4. Model Training → 7 algorithms with GridSearchCV
5. Evaluation → 5-fold stratified cross-validation
