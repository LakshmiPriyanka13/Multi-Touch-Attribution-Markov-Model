# Multi-Touch Attribution: Markov Chain Analysis

## Project Overview
In digital marketing, traditional "last-click" attribution models are fundamentally flawed—they ignore the multi-step journey users take before converting. This project moves beyond rule-based logic to build a **probabilistic Markov Chain model** from scratch to quantify the true value of every marketing touchpoint.

## Methodology
Instead of relying on black-box libraries, this model was built using custom matrix mathematics:
1.  **Journey Construction:** Transformed raw transaction logs into unique user "Paths to Purchase."
2.  **Transition Matrix:** Computed the conditional probability of a user moving from one channel (e.g., Social Media) to the next (e.g., Email).
3.  **Removal Effect Algorithm:** Iteratively "removed" each channel from the matrix to calculate the total percentage drop in conversion probability. 

## Key Insights
Our analysis of the customer journey revealed the following impacts on total conversion probability if a channel budget is cut:

| Channel | Removal Effect (Conversion Drop) |
| :--- | :--- |
| **Direct Traffic** | 30.89% |
| **Referral** | 30.89% |
| **Social Media** | 30.52% |
| **Search Ads** | 30.29% |
| **Display Ads** | 30.05% |
| **Email** | 30.74% |

**Strategic Takeaway:** The data shows a highly synergistic ecosystem. Unlike many retail models where one channel dominates, this customer journey is resilient; no single channel carries the entire conversion weight. This suggests a balanced media mix strategy is optimal for this specific audience.

## Tech Stack
* **Python**
* **Pandas & NumPy** (Matrix mathematics and sequence processing)
* **Statsmodels** (Statistical validation)

## How to Run
1. Ensure `multi_touch_attribution_data.csv` is in the same directory
2. Run `Attribution_Project.ipynb` to generate the transition probabilities and removal effect coefficients
