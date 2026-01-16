This notebook explores the implications of using biased human-related datasets in data analytics pipelines, focusing on bias detection and mitigation using IBM's AI Fairness 360 toolkit (aif360).

## Background

Bias in datasets can arise if they are not representative of the true population for specific *protected or sensitive attributes* like race, gender, and age. This can lead to unreliable or unfair decision-making in systems. Bias can be inherent in data collection or introduced during data preparation.

## Learning Outcomes

Upon completing this activity, students will:

*   Understand metrics for bias detection in machine learning tasks.
*   Learn how bias can be mitigated *before* applying a machine learning task, particularly in classification.
*   Recognize how data transformation operations can introduce or amplify representation bias, independent of subsequent analytical steps.

## Steps Involved

The activity is structured into three main parts:

### PART 1: Preliminaries

*   **Step 1.1:** Install and import necessary packages (e.g., aif360).
*   **Step 1.2:** Load the German Credit Risk dataset and set bias detection options, defining 'age' as the protected attribute with 'age >= 25' as the privileged group.

### PART 2: Fairness and Mitigation through Machine Learning Preprocessing

*   **Step 2.1:** Split the dataset into training and testing sets.
*   **Step 2.2:** Compute fairness metrics (Mean Difference and Disparate Impact) on the original training dataset to quantify bias.
*   **Step 2.3:** Mitigate bias by transforming the original dataset using a pre-processing technique like the Reweighing algorithm from aif360.
*   **Step 2.4:** Re-compute fairness metrics on the transformed training dataset to evaluate the effectiveness of the mitigation.

### PART 3: Representation Bias

*   **Step 3.1:** Explore fairness constraints for representation bias, calculated as the difference in ratios of unprivileged to privileged instances between original and transformed datasets (Fairness Index).
*   **Step 3.2:** Investigate how to find data transformations that reduce the fairness index while maintaining similarity to original queries (Rewriting for Fairness).
*   **Step 3.3:** Examine coverage constraints, ensuring a minimum number of instances for a sensitive group.
*   **Step 3.4:** Learn to find data transformations that satisfy coverage constraints while being similar to the original query (Rewriting for Coverage).
