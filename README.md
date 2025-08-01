## Acknowledgments
This project was made possible by the generous support of **Ningbo Yongjiang Laboratory (YLab)** in flow chemistry and intelligent synthesis group. We thank the YLab team for providing experimental data, technical resources, and invaluable guidance.

> **Notice:** The code and data used in this project comply with the confidentiality agreement of **Ningbo Yongjiang Laboratory (YLab)** and have been authorized for external release.

---

# Week 1: Batch-to-Flow ML Baseline

Welcome to Week 1 of our Batch-to-Flow ML model project! In this notebook, we will:

1. **Load & Preprocess Data**
   - Read `batch_to_flow.csv` into a DataFrame.
   - Clean missing values and inspect summary statistics.
2. **Feature Engineering**
   - Encode any categorical variables.
   - Scale continuous features (e.g., MinMax or Standard scaler).
   - Create derived features (interaction terms, polynomial features).
3. **Baseline Model Training**
   - Initialize regressors:
     - `LinearRegression`
     - `RandomForestRegressor`
     - `GradientBoostingRegressor`
   - Split data into training/validation sets (80/20 split).
4. **Evaluation Metrics**
   - Compute on validation set:
     - Root Mean Squared Error (RMSE)
     - Mean Absolute Error (MAE)
     - R² Score
5. **Results & Visualization**
   - Tabulate model performance metrics.
   - Plot predicted vs. actual flow yields.
# Week 2 to week 4: Bayesian Optimization Workflow, performance improve and deep bayesian optimization method. 

Welcome to Week 2 of our Bayesian Optimization project! In this notebook, we will:

1. **Load & Inspect Data**
   - Read in `aryltrifluoromethylation_cytosine.csv` and select key condition columns.
2. **Define Core Functions**
   - `propose_next_experiment`: Fit a Gaussian Process, compute μ (mean), σ (std), and Expected Improvement (EI).
   - `explore_exploit_score`: Calculate normalized exploration vs. exploitation metrics.
3. **Single-Step Demo**
   - Use the first 10 samples to recommend `x₁₁` (the 11th experiment) and display μ, σ, EI, and scores.
4. **performance improvement**
   - `try to limit the dataset and get better performance from the orginal model`
5. **deep bayesian optimization model**
   - `try to use the deep learning kernal to replace the original matern kernal but the performance did not improve a lot.`
# week 5: Structured Data to GraphRAG
   


