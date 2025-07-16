## Acknowledgments
This project was made possible by the generous support of **Ningbo Yongjiang Laboratory (YLab)** in flow chemistry and intelligent synthesis group. We thank the YLab team for providing experimental data, technical resources, and invaluable guidance.

> **Notice:** The code and data used in this project comply with the confidentiality agreement of **Ningbo Yongjiang Laboratory (YLab)** and have been authorized for external release.

---

## Week1 record
- **Data Scarcity and Quality:** Limited experimental flow chemistry data may lead to overfitting or unreliable predictions.  
  - **Solution:** Use data augmentation techniques, cross-validation, and robust feature selection to improve model generalization.
- **Model Hyperparameter Tuning:** Identifying optimal model parameters for batch-to-flow predictions can be time-consuming.  
  - **Solution:** Employ automated hyperparameter search (e.g., Grid Search or Bayesian Optimization) with sensible parameter bounds to accelerate tuning.
- **Integration of Domain Knowledge:** Ensuring the machine learning workflow aligns with chemical synthesis constraints.  
  - **Solution:** Collaborate closely with YLab chemists to encode reaction heuristics and validate model outputs against expert insights.
- **Computational Resources:** Running multiple ML experiments may strain local computing capability.  
  - **Solution:** Leverage cloud or high-performance computing resources when available, and use lightweight models or early-stopping criteria.
 
## Week 2: Bayesian Optimization Workflow

Welcome to Week 2 of our Bayesian Optimization project! In this notebook, we will:

1. **Load & Inspect Data**
   - Read in `aryltrifluoromethylation_cytosine.csv` and select key condition columns.
2. **Define Core Functions**
   - `propose_next_experiment`: Fit a Gaussian Process, compute μ (mean), σ (std), and Expected Improvement (EI).
   - `explore_exploit_score`: Calculate normalized exploration vs. exploitation metrics.
3. **Single-Step Demo**
   - Use the first 10 samples to recommend `x₁₁` (the 11th experiment) and display μ, σ, EI, and scores.
4. **Iterative BO Loop**
   - Loop from iteration 11 to 35:
     - Fit GP on current training set.
     - Propose next sample, compute acquisition and scores.
     - Append true yield, update training data, and record history.
5. **Results & Visualization**
   - Compile a history DataFrame of iteration, sample index, μ, σ, EI, and explore–exploit score.
   - Plot acquisition dynamics to evaluate performance.

