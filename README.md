# Home Price Prediction

A machine learning project that uses linear regression to predict house prices based on property area.

## Project Overview

This project demonstrates a simple linear regression model built with scikit-learn to establish the relationship between property area (in square feet) and price (in US dollars). The model is trained on historical home price data and can predict prices for new properties based on their area.

## Files in This Project

### Data Files

- **`homeprices.csv`** - Training dataset containing historical home prices
  - Columns: `area` (square feet), `price` (US dollars)
  - Contains 5 sample properties with areas ranging from 2,600 to 4,000 sq ft

- **`area.csv`** - Input file with property areas to predict prices for
  - Column: `area` (square feet)
  - Contains 13 properties with areas ranging from 1,000 to 9,000 sq ft

- **`prediction.csv`** - Output file with predicted prices
  - Generated after running the prediction model
  - Columns: `area` (input areas), `prices` (predicted prices)

### Code Files

- **`ML1.ipynb`** - Jupyter Notebook containing the complete machine learning pipeline

## How It Works

### 1. **Data Loading**
   - Loads training data from `homeprices.csv`
   - Displays the dataset for inspection

### 2. **Data Visualization**
   - Creates scatter plots to visualize the relationship between area and price
   - Shows both the training data and the fitted regression line

### 3. **Model Training**
   - Uses `LinearRegression` from scikit-learn
   - Fits the model with area as the independent variable (X) and price as the dependent variable (y)
   - Extracts model coefficients and intercept

### 4. **Price Prediction**
   - Uses the trained model to predict prices for new properties in `area.csv`
   - Mathematical formula: **Price = 135.79 × Area + 180,616.44**
   - Saves predictions to `prediction.csv`

## Model Parameters

- **Slope (Coefficient):** 135.78767123 (price per square foot)
- **Intercept:** 180,616.43835616432 (base price)
- **Linear Equation:** y = 135.79x + 180,616.44

### Example Prediction
For a property with 3,300 sq ft:
```
Price = 135.79 × 3,300 + 180,616.44 = $629,286.57
```

## Dependencies

```
pandas         - Data manipulation and CSV handling
numpy          - Numerical computations
matplotlib     - Data visualization
scikit-learn   - Machine learning (Linear Regression)
```

## Running the Project

1. Open `ML1.ipynb` in Jupyter Notebook
2. Execute the cells sequentially to:
   - Load and explore the training data
   - Visualize the relationship between area and price
   - Train the linear regression model
   - Make predictions on new data
   - Save predictions to `prediction.csv`

## Project Workflow

```
homeprices.csv (training data)
        ↓
    Load & Visualize
        ↓
    Train Model
        ↓
area.csv (new areas)
        ↓
    Make Predictions
        ↓
prediction.csv (output)
```

## Key Insights

- **Positive Correlation:** Property price increases linearly with area
- **Price per Sq Ft:** Approximately $135.79 per square foot
- **Base Price:** Approximately $180,616 (intercept value)
- **Model Type:** Simple linear regression with single feature (area)

## Future Enhancements

- Add more features (bedrooms, bathrooms, location, etc.)
- Improve model accuracy with polynomial regression or other algorithms
- Add train-test split validation
- Calculate R² score and model performance metrics
- Cross-validation for model robustness

## Author & Notes

This is a beginner-level machine learning project demonstrating the fundamentals of:
- Data loading and exploration
- Model training and fitting
- Prediction making
- Data visualization
- CSV file handling
