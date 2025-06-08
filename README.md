# California Housing Price Prediction

This project builds and evaluates machine learning models to predict housing prices in California using the California Housing dataset. It includes data preprocessing, model training with hyperparameter tuning, and visualizations to explore prediction accuracy and geographic price trends.

---

## Dataset

The dataset contains census data collected from California districts. Key features include:

- `median_income`
- `housing_median_age`
- `total_rooms`, `total_bedrooms`
- `population`, `households`
- `latitude`, `longitude`
- **Target:** `median_house_value`

---

## 🔧 Features and Engineering

The following engineered features are added:

- `AveRooms` = total rooms per household  
- `AveBedrms` = total bedrooms per household  
- `AveOccup` = population per household  

Selected features for training:
- `median_income`
- `housing_median_age`
- `AveRooms`
- `AveBedrms`
- `AveOccup`
- `latitude`, `longitude`

---

## Models Used

Two models are evaluated:

1. **Linear Regression**
2. **Random Forest Regressor** with GridSearchCV (hyperparameter tuning)

Both models are embedded in a pipeline that includes feature scaling using `StandardScaler`.

---

## Evaluation

- Cross-validation with 5 folds using Mean Absolute Error (MAE)
- The best model is selected based on the lowest CV MAE
- Final performance is evaluated on a test split

---

## Visualizations

1. **Actual vs Predicted Prices Plot**  
   - ![image](https://github.com/user-attachments/assets/1d66b40c-28db-46ed-9e89-df6bdb4b5087)


2. **Geographic Price Heatmap**  
   - ![image](https://github.com/user-attachments/assets/96dc7e54-bf22-4316-9fa3-ea74a47b0ec3)


---

## How to Run

1. Make sure `housing.csv` is in the same folder as your script.
2. Install required packages:

```bash
pip install pandas numpy matplotlib scikit-learn

