COLLABORATION & RECOMMENDATIONS

1. Clarify RL Agent Logic and Document Random Seed
Current Approach: The RL agent’s glucose profile is simulated using a Gaussian process with fixed mean and standard deviation, serving as a placeholder for a true reinforcement learning (RL) controller.

Recommendation: In future versions, explicitly describe the RL agent’s policy logic and, if possible, integrate an actual RL agent (e.g., DDPG, PPO) for more realistic simulation. Ensure all random seeds (e.g., np.random.seed(42)) are documented for full reproducibility.

2. Add Rate-of-Change Features and Address Feature Scaling
Current Approach: Engineered features include rolling means, lagged values, and interaction terms.

Recommendation: Incorporate rate-of-change (first derivative) and acceleration (second derivative) features, which are known to improve prediction of glycemic events. Although tree-based models like Random Forests do not require feature scaling, document your approach to scaling for transparency and to facilitate use with other model types.

3. Explain Feature Weight Choices and Clarify Thresholding
Current Approach: The binary target is generated using a weighted sum of features plus Gaussian noise, thresholded at the median.

Recommendation: Provide justification for the choice of feature weights in the target construction function (e.g., based on clinical relevance or literature). Clearly state whether thresholding is performed globally or per-patient.

4. Report Number of Features Retained and Compare Selection Methods
Current Approach: Recursive Feature Elimination with Cross-Validation (RFECV) is used for feature selection.

Recommendation: Report the number and identity of features retained after RFECV. For transparency, compare RFECV results with simpler selection methods (e.g., univariate selection or domain-based selection) and discuss any differences in model performance.

5. Justify Random Forest Choice and Mention Alternatives
Current Approach: Random Forest is used as the primary classifier.

Recommendation: Justify the choice of Random Forest (e.g., robustness to noise, interpretability, performance on tabular data). Consider benchmarking against alternative models such as XGBoost, LightGBM, or logistic regression, and report comparative results.

6. Add Calibration Metrics and Discuss Class Balance
Current Approach: Model evaluation includes accuracy, AUC, precision, recall, and F1-score.

Recommendation: Include calibration metrics (e.g., Brier score, calibration plots) to assess the reliability of predicted probabilities, which is important for clinical applications. Discuss class balance in both the synthetic and real datasets and describe any mitigation strategies for potential imbalance (e.g., resampling, class weighting).

7. Clarify Real/Synthetic Validation and Describe Hybrid Approach
Current Approach: Validation is performed using synthetic data, with some reference to real-world benchmarks.

Recommendation: Clearly describe the validation process, specifying whether real patient data was used and how it was integrated (e.g., for external validation, transfer learning, or calibration). If a hybrid approach is used (combining synthetic and real data), provide details on the methodology and results.

We welcome collaboration and contributions that address these recommendations. For detailed implementation notes, see the supplementary documentation and code comments.
