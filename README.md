# Ice Cover Analysis on Madison Lakes

## Project Overview
This project analyzes the freeze and thaw patterns of three lakes in Madison, Wisconsin: Monona, Mendota, and Wingra. The dataset contains historical records of ice cover duration, freeze-over dates, and thaw dates spanning over a century. The objective is to preprocess the data, visualize historical trends, and build predictive models to estimate the number of ice cover days based on various features.

## Dataset
The data consists of the following columns:
- `Winter`: The winter season (e.g., 1851-52)
- `Freeze-Over Date`: The date when the lake froze
- `Thaw Date`: The date when the lake thawed
- `Days of Ice Cover`: The number of days the lake remained frozen

After preprocessing, additional columns are created:
- `year`: The starting year of the winter season
- `freeze_month`, `freeze_day`: The month and day of freeze-over
- `thaw_month`, `thaw_day`: The month and day of thaw
- `decade`: The decade for trend analysis
- `no_freeze`: A binary column indicating whether there was no freeze
- `prev_year_ice_cover`: The number of ice cover days from the previous year

## Data Preprocessing
The preprocessing steps include:
1. Extracting numerical values from `Freeze-Over Date` and `Thaw Date`
2. Converting month names to numeric values
3. Handling missing values and replacing dashes (`–`) with `NaN`
4. Creating additional features for modeling
5. Encoding categorical variables (lake names) using one-hot encoding

## Exploratory Data Analysis (EDA)
Visualizations were created to explore trends and distributions:
- **Ice Cover Trends Over Time:** A line plot shows changes in the number of ice cover days over the years.
- **Freeze and Thaw Distributions:** Histograms display the distribution of freeze and thaw months.
- **Correlation Analysis:** A heatmap identifies relationships between variables.
- **Freeze Timing vs. Ice Cover Duration:** A scatter plot examines how early or late freezing affects ice cover duration.

## Machine Learning Models
Three regression models were implemented to predict ice cover days:
1. **Linear Regression**
2. **Random Forest Regressor**
3. **Support Vector Regression (SVR)**


### Predictions vs. Actual Values
A visualization compares the actual vs. predicted number of ice cover days, demonstrating the model's accuracy in capturing patterns.

## Technologies Used
- **Python** (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)
- **Machine Learning Models:** Linear Regression, Random Forest, SVR
- **Data Preprocessing & Feature Engineering**
- **Data Visualization**

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ice-cover-analysis.git
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
3. Run the Script:
  ```bash
  python ice_cover_analysis.py
