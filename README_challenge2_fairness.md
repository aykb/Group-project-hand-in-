This notebook addresses **Challenge 2**, focusing on data quality, fairness assessment, and fair sampling techniques. It utilizes the IBM AI Fairness 360 (AIF360) toolkit and SQL for practical implementation.

## Objectives:

1.  **Evaluate Data Quality**: Assess basic statistics and identify missing values in the Adult Census Income dataset.
2.  **Detect Bias with AIF360**: Use the AIF360 toolkit to measure fairness metrics (e.g., Statistical Parity Difference, Disparate Impact) with `sex` as a protected attribute, considering `income` as the outcome.
3.  **Create a Fairer Dataset with Reweighing**: Apply AIF360's `Reweighing` preprocessing algorithm to mitigate bias and compare fairness metrics before and after reweighing.
4.  **Implement Fair Sampling with SQL**: Demonstrate how to create a balanced training sample using SQL, specifically by selecting an equal number of rows for each value of the protected attribute (`sex`).

