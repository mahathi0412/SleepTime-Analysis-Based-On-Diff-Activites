# SleepTime-Analysis-Based-On-Diff-Activites

# Overview
This project analyzes the relationship between various activities (like workout time, phone usage, reading time, caffeine intake, and relaxation time) and their impact on sleep duration (SleepTime). Using Python, data preprocessing, clustering, and visualization techniques, we explore how different factors contribute to sleep patterns and extract actionable insights.

# Project Objectives
- **Understand Relationships:** Identify how individual activities correlate with sleep time.
- **Clustering:** Group individuals into distinct clusters based on behavioral patterns.
- **Visualizations:** Use 2D and 3D plots, heatmaps, and scatterplots to present the relationships between different variables and their combined effects.
- **Insights:** Extract actionable insights to improve sleep quality.

# Steps Performed

**1. Data Preprocessing**
- Checked for non-numeric columns and converted them to numeric if necessary.
- Removed invalid or missing values from the dataset to ensure accurate analysis.
- Standardized the features (WorkoutTime, ReadingTime, PhoneTime, etc.) using StandardScaler for clustering.

**2. Correlation Matrix**
- Generated a heatmap of the correlation matrix to identify the strength of relationships between features like:
    - WorkoutTime
    - ReadingTime
    - PhoneTime
    - CaffeineIntake
    - RelaxationTime
    - SleepTime
*Key Findings:*
- RelaxationTime had the strongest positive correlation with SleepTime.
- PhoneTime and CaffeineIntake negatively correlated with SleepTime.

**3. 3D Scatterplots**
*Combined Effects of Two Variables:*
- Visualized how two independent variables (e.g., WorkoutTime and RelaxationTime) influenced SleepTime.
*Key Findings:*
- Higher relaxation time combined with moderate workout time increased sleep.
- Low relaxation or reading time often resulted in poor sleep.

**4. Linear Regression Analysis**
- Created regression plots (e.g., sns.lmplot) to visualize:
    - Relationships between variables like PhoneTime, RelaxationTime, and SleepTime.
- Impact of each activity individually on sleep patterns.
- Added confidence intervals to assess the reliability of these relationships.

**5. Clustering Analysis (KMeans Clustering)**
*Used KMeans Clustering to group individuals into 3 distinct clusters based on their habits:*
  - Variables: WorkoutTime, ReadingTime, PhoneTime, WorkHours, CaffeineIntake, RelaxationTime.
*Key Insights:*
  - Cluster 0: Poor sleepers with high phone usage and caffeine intake.
  - Cluster 1: Moderate sleepers with balanced habits.
  - Cluster 2: Healthy sleepers with high relaxation and workout times.

**6. Relationship Scatterplots by Clusters**
*Visualized individual scatterplots to analyze the clustered data:*
- WorkoutTime vs. SleepTime
- ReadingTime vs. SleepTime
- PhoneTime vs. SleepTime
- RelaxationTime vs. SleepTime
- Differentiated clusters using distinct colors (hue='Cluster').
*Key Findings:*
- Clusters showed clear behavioral patterns (e.g., high WorkoutTime and RelaxationTime corresponded to better sleep).

**7. Categorical Sleep Analysis**
- Categorized SleepTime into 4 categories: Low, Moderate, Good, and Healthy using pd.cut.
- Created bar plots to visualize how individuals were distributed across sleep categories.
*Key Findings:*
- Most individuals fell into the Moderate or Low sleep categories.
- Very few achieved Healthy sleep levels.

**8. Combined Variable Heatmap**
- Created a heatmap for combinations of binned variables (e.g., PhoneTime and CaffeineIntake) to analyze their combined effects on SleepTime.
*Key Findings:*
- Low phone usage and low caffeine intake resulted in the best sleep outcomes.
- High caffeine intake combined with high phone usage significantly reduced sleep.

# Results
This project demonstrates the power of data analysis and visualization in understanding the combined and individual effects of activities on sleep. It provides actionable insights to improve sleep patterns, emphasizing the importance of balancing relaxation and reducing disruptive behaviors like excessive phone usage.
