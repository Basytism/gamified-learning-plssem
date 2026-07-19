# Data Dictionary

Survey-based study, synthetic dataset, N = 200 respondents. All items measured on a 5-point Likert scale (1 = Strongly Disagree, 5 = Strongly Agree) unless otherwise noted.

| Variable Name | Description | Measurement Type | Scale |
| --- | --- | --- | --- |
| IM1–IM4 | Intrinsic Motivation indicators (e.g., "I enjoy learning through this platform regardless of rewards") | Reflective | 5-point Likert |
| GE_Badges | Frequency/perceived presence of badge mechanics in the course | Formative | 5-point Likert |
| GE_Leaderboard | Perceived presence and visibility of leaderboard rankings | Formative | 5-point Likert |
| GE_FeedbackSpeed | Perceived speed of feedback after completing an activity | Formative | 5-point Likert |
| ENG1–ENG4 | Engagement indicators (e.g., time-on-task, voluntary re-engagement, attention) | Reflective | 5-point Likert |
| LO1–LO3 | Learning Outcomes indicators (self-reported mastery, quiz/assessment performance, retention) | Reflective | 5-point Likert / normalized 0-100 score |
| Demo_Age | Respondent age band | Formative (control variable) | Categorical (18-24, 25-34, 35-44, 45+) |
| Demo_Platform | Primary learning platform/device used | Formative (control variable) | Categorical (Desktop, Mobile, Tablet) |
| Demo_Experience | Months of prior experience with gamified ed-tech platforms | Formative (control variable) | Continuous (months) |

### Notes on Measurement Type

- **Reflective** indicators are interchangeable effects of their construct — dropping one indicator shouldn't change the construct's meaning. Used for Intrinsic Motivation, Engagement, and Learning Outcomes.
- **Formative** indicators are causes of their construct — each contributes distinct, non-interchangeable information. Used for Gamification Elements and the demographic/control variables.

All data in `/data` is synthetic and generated for structural/reproducibility purposes only; it does not represent real respondents.
