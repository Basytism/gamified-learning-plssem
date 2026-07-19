# Analysis Summary: Gamified Learning PLS-SEM Model

This document explains the reasoning behind each modeling and validation decision — not just the mechanics of running SmartPLS, but why each threshold and test was chosen.

## 1. Measurement Model Assessment

### Reflective Constructs
Intrinsic Motivation, Engagement, and Learning Outcomes are modeled as **reflective** constructs — their indicators are interchangeable manifestations of the same underlying concept, so internal consistency matters.

- **Cronbach's Alpha & Composite Reliability (CR)**: both assessed against the conventional 0.70 threshold. CR is reported alongside Alpha because Alpha assumes equal indicator loadings, which is rarely realistic; CR relaxes that assumption and is treated as the primary reliability statistic here.
- **Average Variance Extracted (AVE)**: assessed against the 0.50 threshold to confirm each construct's indicators explain more variance than they leave as error — establishing convergent validity.

### Formative Construct
Gamification Elements (badges, leaderboards, feedback speed) is modeled as **formative** — the indicators are causes, not effects, of the construct, so internal consistency statistics don't apply. Instead, indicator weights, outer VIF (for collinearity), and significance via bootstrapping are used to assess the construct.

### Discriminant Validity
- **HTMT (Heterotrait-Monotrait Ratio)**: used as the primary criterion, with a conservative threshold of 0.85, since HTMT has been shown to detect discriminant validity issues that the older Fornell-Larcker criterion can miss.
- **Fornell-Larcker Criterion**: reported alongside HTMT for completeness and comparability with older PLS-SEM literature.

## 2. Structural Model Assessment

- **Path Coefficients**: standardized coefficients (range -1 to 1) interpreted for sign, size, and significance (via bootstrapped t-values / p-values, N = 5,000 subsamples, two-tailed at 0.05).
- **R² (Coefficient of Determination)**: reported for Engagement and Learning Outcomes to indicate the proportion of variance explained by their predictors, interpreted using Cohen's conventional bands (weak/moderate/substantial) rather than a single fixed cutoff.
- **f² (Effect Size)**: calculated for each path to show how much a given predictor contributes to a dependent construct's R², independent of sample-size-driven significance.
- **Q² (Predictive Relevance)**: obtained via the Blindfolding procedure; a Q² above zero confirms the model has predictive relevance for the dependent construct, not just explanatory fit.

## 3. Importance-Performance Matrix Analysis (IPMA)

IPMA was chosen as the advanced technique for this project because the research question is inherently prioritization-focused: which gamification elements deserve institutional investment? IPMA extends the standard PLS-SEM path model by plotting each antecedent construct's **total effect (importance)** against its **average latent variable score (performance)**, producing a four-quadrant map:

- High importance / low performance → priority for improvement (this project's key finding: Feedback Speed).
- High importance / high performance → maintain.
- Low importance / high performance → potential over-investment.
- Low importance / low performance → low priority.

## 4. Software & Parameters

- **Software**: SmartPLS 4.x
- **Estimation**: PLS Algorithm, path weighting scheme, standard settings (max 300 iterations, stop criterion 1.0e-7)
- **Bootstrapping**: 5,000 subsamples, no sign changes, two-tailed, 0.05 significance level
- **Blindfolding**: omission distance D = 7
