# Credit-Risk-Assessment

<img width="730" height="335" alt="image" src="https://github.com/user-attachments/assets/39723b08-1677-421a-8c73-39fd5644565f" />

The objective of this study is to develop a **Probability of Default (PD) model** for retail loan applicants based on historical credit data. The model aims to estimate the likelihood that a borrower will default on a loan, thereby supporting credit risk assessment and decision-making processes.

The analysis is based on a dataset provided by **Lending Club**, which contains detailed information on consumer loans issued between **2007 and 2015**. The dataset comprises more than **460,000 loan observations** and includes borrower characteristics, loan attributes, financial indicators, and loan performance outcomes.

### Target Variable Definition

The target variable is derived from the loan status information. A binary default indicator is constructed as follows:

* **Bad loans (default = 0):**

  * Loans with status *Charged Off*
  * Loans with status *Default*
  * Loans with payment delays of **31–120 days**

* **Good loans (default = 1):**

  * All remaining loan statuses

This formulation transforms the problem into a **binary classification task**, where the goal is to predict the probability that a loan will belong to the default class.

### Modeling Approach

The PD model is developed using a traditional credit risk modeling framework that emphasizes interpretability and regulatory compliance. The approach includes:

* **Variable binning** to capture non-linear relationships and reduce noise,
* Transformation of predictors using **Weight of Evidence (WoE)**,
* Feature selection based on **Information Value (IV)** to identify variables with strong discriminatory power.

This methodology is widely used in credit scoring applications and enables transparent interpretation of model outputs.

### Temporal Data Split

To reflect real-world credit risk modeling conditions, the dataset is divided into two time-based samples:

* a **development sample**, consisting of loan applications available at the time of model construction;
* a **validation sample**, containing applications observed after the model was developed.

This temporal split allows for the assessment of model stability over time and the evaluation of potential shifts in borrower characteristics.

### Practical Implications

The resulting PD model can be applied to:

* assess the creditworthiness of new loan applicants;
* support loan approval and pricing decisions;
* serve as an input to expected loss and broader credit risk management frameworks.
