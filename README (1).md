# Gamified Learning and Student Engagement: A PLS-SEM Analysis

### Overview

This project investigates how game-based mechanics — badges, leaderboards, progress bars, and real-time feedback — influence student engagement and academic performance in asynchronous, ed-tech learning environments. Using Partial Least Squares Structural Equation Modeling (PLS-SEM) in SmartPLS, the study models the path from **Intrinsic Motivation** to **Learning Outcomes**, treating engagement as the key mediating construct.

### Project Motivation

With the rise of ed-tech, the effectiveness of gamified learning platforms is often debated. This research models the path from Intrinsic Motivation to Learning Outcomes, exploring how game mechanics act as catalysts for engagement in asynchronous learning environments — and, critically, where they fall short.

### Key Skills Demonstrated

- **Model Specification** — construction of reflective measurement models for Intrinsic Motivation, Engagement, and Learning Outcomes, and formative indicators for Gamification Elements (badges, leaderboards, feedback speed).
- **Measurement Model Assessment** — indicator reliability, convergent validity (AVE, Composite Reliability), and discriminant validity (HTMT, Fornell-Larcker criterion).
- **Structural Model Analysis** — path coefficient estimation, R² values, and f² effect sizes.
- **Advanced Technique: Importance-Performance Matrix Analysis (IPMA)** — used to identify which gamification elements matter most to learning outcomes versus which are actually delivering value.

### Methodology

1. **Data Cleaning** — pre-processing and normality checks performed in R (see `/notebooks`).
2. **Model Building** — reflective and formative constructs configured as a path diagram in SmartPLS.
3. **Validation** — Bootstrapping (N = 5,000 subsamples) for path significance; Blindfolding for predictive relevance (Q²).
4. **Post-hoc Analysis** — IPMA run on the structural model to map construct importance against performance.

### Repository Structure

```
/data          synthetic survey dataset (200 respondents)
/notebooks     R scripts for descriptive statistics and pre-processing
/docs          full PDF report (model validation + implications)
/images        SmartPLS path model and IPMA output screenshots
README.md
analysis_summary.md
data_dictionary.md
```

[Insert Image Here — Path Model / Inner Model diagram]

[Insert Image Here — IPMA Matrix output]

### Key Findings

- Intrinsic Motivation is a strong, significant predictor of Engagement (path coefficient reported in `analysis_summary.md`).
- Among gamification elements, **Leaderboards** are highly visible to students but show **low impact** on actual Learning Outcomes.
- **Feedback Speed** shows both **high importance** and currently **low performance** — the clearest opportunity for intervention.
- Engagement mediates the relationship between game mechanics and academic performance; mechanics with no engagement lift show negligible downstream effect.

### Managerial / Practical Implications

IPMA results indicate that while leaderboards are highly visible, they have low impact on actual learning outcomes. Conversely, feedback speed has both high importance and currently low performance. Institutions and ed-tech platforms should prioritize automated, real-time feedback systems over competitive leaderboard elements to improve student mastery — a reallocation of design effort rather than added spend.

### The Value of This Analysis

For an ed-tech product or academic institution, this type of analysis converts a vague debate ("does gamification work?") into a prioritized action list: which specific mechanics to invest in, which to deprioritize, and why — backed by validated measurement and structural model statistics rather than intuition.

### Data Ethics

The dataset in `/data` is synthetic, generated to resemble a 200-respondent survey structure. No real student data, PII, or institutional records are used or required to reproduce this analysis.
