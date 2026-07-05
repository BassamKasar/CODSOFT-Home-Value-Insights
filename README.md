# Home Value Insights Prediction

## Objective
The goal of this project was to analyze real estate data and develop a machine learning model capable of accurately estimating house prices based on various property attributes.

---

## Dataset Overview
The dataset consists of **1,000 properties** mapped against clean parameters, including:

| Feature | Description |
|---------|-------------|
| `Square_Footage` | Total area of the property |
| `Num_Bedrooms` | Number of bedrooms |
| `Num_Bathrooms` | Number of bathrooms |
| `Year_Built` | Year the property was constructed |
| `Lot_Size` | Size of the land parcel |
| `Garage_Size` | Size of the garage |
| `Neighborhood_Quality` | Quality rating (scale 1–10) |
| `House_Price` | **Target Variable** |

---

## 🧠 Methodology

### Data Preprocessing & Feature Engineering
- Calculated **House_Age** from the `Year_Built` feature to provide a continuous variable for model training.

### Feature Scaling
- Applied **StandardScaler** to normalize data distributions, ensuring that features with larger numerical ranges (like `Square_Footage`) did not heavily skew the model.

### Model Selection
- Trained a **Random Forest Regressor** to capture both **linear and non-linear relationships** in the dataset (e.g., the compounding value of high square footage in high-quality neighborhoods).

### Evaluation
- Assessed model performance using standard regression metrics:
  - **Mean Absolute Error (MAE)**
  - **Root Mean Squared Error (RMSE)**
  - **R² Score**

---

## Key Insights
- **Neighborhood Quality** acts as a massive multiplier for house value, heavily dictating the price-per-square-foot.
- The **Random Forest** model effectively captured non-linear interactions between features, providing highly accurate price estimations.

---

## Technologies Used

| Category | Tools |
|----------|-------|
| **Language** | Python |
| **Data Manipulation** | Pandas, NumPy |
| **Machine Learning** | Scikit-Learn (StandardScaler, RandomForestRegressor, metrics) |
| **Environment** | Jupyter Notebook / Python IDE |
