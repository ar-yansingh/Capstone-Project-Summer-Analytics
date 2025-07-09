# CAPSTONE PROJECT

## Overview

This project focuses on **dynamic parking price optimization** using real-world data. It explores the effectiveness of predictive pricing models to analyze and improve the cost efficiency of parking spaces across multiple lots in a city. The workflow includes extensive data exploration, model development, and visualization of predicted pricing trends over time.

---

## Tech Stack

- **Python (Google Colab)** – Core development environment  
- **Pandas, NumPy** – Data preprocessing and manipulation  
- **Matplotlib, Plotly, Seaborn** – Data visualization  
- **Scikit-learn** – Model building and evaluation  
- **XGBoost** – Advanced gradient boosting for model accuracy  
- **Pathlib / OS** – File management  
- **Google Drive Integration** – For file storage and dataset retrieval  

---

## Architecture Diagram

```mermaid
graph TD
    A[Raw Dataset (.csv)] --> B[Google Drive / Colab Mount]
    B --> C[Data Preprocessing & Cleaning]
    C --> D[Exploratory Data Analysis (EDA)]
    D --> E1[Model 1: Predictive Pricing]
    D --> E2[Model 2: Time Series Forecast]
    E1 --> F1[Visualize Predictions]
    E2 --> F2[Visualize Predictions]
    F1 & F2 --> G[Comparison & Analysis]
```

---

## Project Architecture & Workflow

1. **Google Colab Setup**
   - Connected to Google Drive using `from google.colab import drive`
   - Managed file paths using `pathlib.Path` to ensure OS-agnostic and clean directory handling

2. **Data Loading and Preprocessing**
   - Parsed timestamps, handled missing values, formatted categorical variables
   - Combined datasets where necessary to ensure consistency

3. **Exploratory Data Analysis**
   - Visualized parking price fluctuations across lots
   - Identified temporal and seasonal trends

   ![Price Comparison](notebooks/visuals/price_comparison.png)

4. **Model Development**
   - **Model 1:** Linear Regression-based model with adjusted price prediction  
   - **Model 2:** XGBoost Time-Series optimized model with high responsiveness to changing trends

   **Model 1 Output:**  
   ![Model 1 Prediction](notebooks/visuals/model1_prediction.png)

   **Model 2 Output:**  
   ![Model 2 Prediction](notebooks/visuals/model2_prediction.png)

5. **Pathway Usage**
   - File and model organization was managed via `pathlib.Path`
   - Outputs and visualizations stored in structured folders (e.g., `/notebooks/visuals`)
   - Ensured reproducibility across sessions and team environments

6. **Evaluation & Insights**
   - Compared prediction curves for both models
   - Highlighted periods of pricing inefficiency and suggested optimal pricing strategies

---

## How to Run

1. Open the `.ipynb` notebook in **Google Colab**
2. Connect to Google Drive
3. Follow the notebook cells from top to bottom
4. All visuals will be saved under the `/notebooks/visuals/` folder

---

## Conclusion

This project demonstrates how predictive analytics can enhance real-world decisions in urban infrastructure. By modeling and analyzing pricing behavior over time, we enable data-driven adjustments that can optimize revenue and improve user satisfaction.
