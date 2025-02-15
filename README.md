# InsurPrime: Can You Guess the Insurance Premium?

This repository is dedicated to the **InsurPrime** challenge, part of the **Data
Challenge 2025** organized by the **École Normale Supérieure (ENS)** and
**Université PSL**, in partnership with **Crédit Agricole Assurances**.

## Challenge Overview

The **InsurPrime** challenge aims to develop predictive models to accurately
estimate the **pure fire premium** for agricultural multi-risk insurance
contracts. Participants are tasked with creating models that predict:

-   **Claim Frequency**: Estimating the number of fire-related claims.
-   **Average Claim Cost**: Calculating the expected cost per claim.

The ultimate goal is to compute the **CHARGE**, defined as:

```
CHARGE = Frequency × Average Cost × ANNEE_ASSURANCE
```

Where `ANNEE_ASSURANCE` represents the number of years since the insurance
contract was initiated.

## Data Description

Participants are provided with a comprehensive dataset that includes:

-   **Target Variables**: `FREQ` (frequency), `CM` (average cost), and `CHARGE`
    (total charge).
-   **Geographical Data**: Information such as department and weather
    conditions.
-   **Contract-Specific Data**: Details about the insured's activities (e.g.,
    farmer, polycultivator), number of buildings, employees, and claims reported
    at subscription.
-   **Surface Data**: Areas of various buildings, anonymized for
    confidentiality.
-   **Capital Data**: Insured capital for specific options, anonymized for
    confidentiality.
-   **Prevention Data**: Information on preventive measures, anonymized for
    confidentiality.

A supplementary file is available, providing detailed descriptions of all
variables.

## Benchmark Model

A baseline model utilizing **Generalized Linear Models (GLMs)** is provided for
reference:

1. **Claim Frequency Model**:

    - Distribution: Poisson
    - Link Function: Log

2. **Average Claim Cost Model**:
    - Distribution: Tweedie
    - Link Function: Log

Participants are encouraged to develop models that surpass this baseline in
terms of:

-   Prediction accuracy
-   Interpretability and efficiency
-   Alignment with business constraints

## Evaluation Metric

The primary evaluation metric for this challenge is the **Root Mean Square Error
(RMSE)**, calculated as:

$RMSE = \sqrt{\frac{1}{n}\sum_{i=1}^n (y_i - ŷ_i)^2}$

Where:

-   $y_i$ = Actual value
-   $ŷ_i$ = Predicted value
-   $n$ = Number of observations

The objective is to assess how well the proposed models improve upon the
baseline in terms of predictive performance.

---

_Note: This repository is intended for research and educational purposes as part
of the Data Challenge 2025._
