# Student-AI-Socialmedia-EDA
EDA of how social media and AI usage relate to student health
# Student Health vs. Social Media and AI Usage: EDA

An exploratory data analysis of how daily social media and AI tool usage relate to sleep, physical activity, and the mental and physical health of students.

## Dataset
- **Size:** 16,000 students, 10 columns, with no missing values or duplicate rows
- **Columns:** Age, Gender, Education Level, Daily Social Media Hours, Daily AI Tool Usage Hours, Sleep Hours, Physical Activity Hours, Mental Health Score, Physical Health Score
- **Source:** - Kaggle

## Questions explored
- Is social media or AI tool usage more strongly related to student health?
- Do gender or education level make a difference to health scores?
- Do heavy social media users have lower mental health than light users?

## Key findings
- **Social media is associated with lower mental health** (correlation -0.40). Students using it more than 6 hours a day score about 9 points lower (67.7) than those using it less than 3 hours a day (76.8).
- **Social media also goes with less sleep (-0.30), less physical activity (-0.16) and lower physical health (-0.31).**
- **AI tool usage has a much weaker link to health** than social media (-0.11 with mental health, -0.02 with physical health).
- **Physical activity has the strongest link to physical health** (+0.42).
- **Gender and education level make almost no difference** to health scores (differences under 0.5 points).

## Limitations
- Correlation does not prove causation.
- `Physical_Health_Score` is capped near 100, so about 8% of students sit at the top of the scale.
- Age shows no relationship with any variable, so the data may be simulated.

## What I did
- Checked data quality (missing values, duplicates, data types)
- Explored distributions with histograms and countplots
- Detected outliers with boxplots and the IQR method
- Compared groups with `groupby`
- Measured relationships with a correlation heatmap
- Grouped social media use into Low, Medium and High with `pd.cut()`

## Tools
Python, pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

## Files
- `Student_Analysis.ipynb`: the full analysis
- `AI_SocialMedia_Student_Dataset.csv`: the dataset
