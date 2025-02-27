# Machine Learning - Elastic Net Proof of Concept (POC)

This repository demonstrates how **Elastic Net Regression** balances feature selection and regularization to improve predictive models. The examples focus on two real-world scenarios:

1. **Predicting Disease Risk**: Estimating diabetes risk based on medical and lifestyle factors.
2. **Stock Price Forecasting**: Predicting stock prices based on market trends, company profits, interest rates, news, and trading volume.

## What is Elastic Net?

**Elastic Net** is a regression technique that combines two regularization methods:
- **Ridge Regression**, which reduces the influence of less important features without removing them.
- **Lasso Regression**, which can eliminate irrelevant features to simplify the model.

By combining both approaches, **Elastic Net provides a more stable and balanced prediction model**, preventing overfitting while keeping relevant variables.

### Why Use Elastic Net?
- **Prevents overfitting**: Ensures the model does not memorize noise from the data.
- **Balances feature selection and regularization**: Keeps important variables while reducing the influence of irrelevant ones.
- **Works well with high-dimensional data**: Suitable for models with many correlated variables.

## Running on Google Colab

### Step 1: Open the Notebooks in Colab
Click the links below to open the examples directly in **Google Colab**:
- [Predicting Disease Risk](https://colab.research.google.com/github/your-repo/diabetes_risk_prediction.ipynb)
- [Stock Price Forecasting](https://colab.research.google.com/github/your-repo/stock_price_forecasting.ipynb)

### Step 2: Install Dependencies (if needed)
Google Colab usually comes with required libraries pre-installed. However, if needed, run:
```python
!pip install numpy matplotlib scikit-learn
```

### Step 3: Run the Cells
Each notebook contains explanations, data, and visualizations. Execute the cells in order to train the models and visualize results.

---

## Example 1: Predicting Disease Risk

This model predicts **diabetes risk** based on medical and lifestyle factors:

- **Input Features**: 
  - Age
  - Weight
  - Blood pressure
  - Family history
  - Blood sugar levels
  - Diet and exercise habits
- **Output**: Predicted diabetes risk score
- **Comparison**: Standard Linear Regression vs. Ridge, Lasso, and Elastic Net

### Notebook Highlights:
- **Linear Regression model** is first trained, showing potential overfitting.
- **Ridge and Lasso Regression** are applied separately, demonstrating their strengths and weaknesses.
- **Elastic Net** provides a **balanced prediction**, ensuring that all relevant medical factors are considered while reducing unnecessary complexity.

---

## Example 2: Stock Price Forecasting

This model predicts **stock prices** using financial market indicators:

- **Input Features**:
  - Market trends
  - Company profits
  - Interest rates
  - Economic news sentiment
  - Trading volume
- **Output**: Predicted stock price
- **Comparison**: Standard Linear Regression vs. Ridge, Lasso, and Elastic Net

### Notebook Highlights:
- **Linear Regression model** struggles with overfitting and feature importance.
- **Ridge Regression** reduces overemphasis on minor variables but retains all features.
- **Lasso Regression** removes some features, which may lead to information loss.
- **Elastic Net** achieves the best balance, filtering out irrelevant variables while keeping the most important ones.

---

## Visualizing Results

Each notebook generates a **scatter plot** comparing **Linear Regression, Ridge, Lasso, and Elastic Net**:
- **Blue dots**: Predictions using Linear Regression.
- **Red dots**: Predictions using Ridge Regression.
- **Green dots**: Predictions using Lasso Regression.
- **Purple dots**: Predictions using Elastic Net.
- **Dashed black line**: Ideal fit (perfect prediction).
- **Lower MSE in Elastic Net**: Demonstrates improved generalization and stability.

---

## Conclusion

**Elastic Net** is a powerful regression model that combines the best of **Ridge and Lasso Regression**. It is widely used in domains such as **medical risk assessment, stock market forecasting, finance, and predictive modeling**.

By using **Elastic Net**, we ensure that:
- The model remains **generalized** and **avoids overfitting**.
- The most **important features** are **selected and retained**.
- Predictions are **more reliable** for real-world applications.

## License

This project is released under the MIT License.
