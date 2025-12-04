# Data Mining: NHANES Data Analysis & Preprocessing

This repository contains a comprehensive data mining project that demonstrates data preprocessing, exploratory data analysis (EDA), and basic hypothesis testing using the National Health and Nutrition Examination Survey (NHANES) 2017-2018 dataset.

##  Project Overview

The NHANES dataset provides rich health and nutritional data collected by the Centers for Disease Control and Prevention (CDC). This project showcases essential data mining techniques and statistical analysis methods applied to real-world health data.

### Learning Objectives
- Data preprocessing and cleaning techniques
- Exploratory data analysis (EDA) methodologies
- Basic hypothesis testing and statistical inference
- Feature engineering and data transformation
- Data visualization and pattern discovery

##  Dataset Description

The project utilizes three main components of the NHANES 2017-2018 dataset:

1. **Demographics (DEMO_J.XPT)**: Age, gender, race/ethnicity, education, income
2. **Body Measurements (BMX_J.XPT)**: Weight, height, BMI, waist circumference
3. **Blood Pressure (BPX_J.XPT)**: Multiple systolic and diastolic blood pressure readings

### Key Variables
- **Demographics**: Age, gender, race/ethnicity, education level, household income
- **Anthropometric**: Weight, height, BMI, waist circumference
- **Health Metrics**: Systolic and diastolic blood pressure measurements

##  Technologies & Libraries

```python
# Data Manipulation
import pandas as pd
import numpy as np

# Visualization
import matplotlib.pyplot as plt
import seaborn as sns

# Statistical Analysis
from scipy import stats

# Machine Learning
from sklearn.impute import SimpleImputer, KNNImputer
from sklearn.preprocessing import StandardScaler, MinMaxScaler, RobustScaler
from sklearn.decomposition import PCA
from sklearn.feature_selection import SelectKBest, f_classif
```

##  Project Structure

### Part 1: Data Loading and Initial Exploration
- **Data acquisition**: Downloading NHANES datasets from CDC website
- **Data integration**: Merging multiple datasets using respondent ID (SEQN)
- **Initial exploration**: Understanding data structure, dimensions, and variables

### Part 2: Data Preprocessing
- **Missing value analysis**: Identifying patterns and handling strategies
  - Mode imputation for categorical variables
  - Median imputation for numerical variables
- **Outlier detection**: Using IQR method with Tukey's rule
- **Outlier treatment**: Winsorization to cap extreme values
- **Feature engineering**: Creating meaningful derived variables
  - Age groups (Child/Teen, Young Adult, Middle-aged, Senior)
  - BMI categories (Underweight, Normal, Overweight, Obese)
  - Average blood pressure calculations
  - Hypertension indicators
  - Waist-to-height ratio
- **Data transformation**: Standardization, normalization, and log transformations
- **Categorical encoding**: One-hot encoding and label encoding

### Part 3: Exploratory Data Analysis (EDA)
- **Descriptive statistics**: Summary measures for numerical variables
- **Distribution analysis**: Histograms, box plots, and normality testing
- **Correlation analysis**: Identifying relationships between variables
- **Group comparisons**: Demographic and health metric analysis
- **Data visualization**: Comprehensive plotting for pattern discovery

### Part 4: Basic Hypothesis Testing
- **Two-sample t-tests**: Comparing systolic blood pressure between genders
- **Chi-square tests**: Association between BMI categories and hypertension
- **Effect size calculations**: Cohen's d and Cramer's V
- **Statistical interpretation**: P-values, confidence intervals, and practical significance

##  Key Findings & Insights

### Data Quality
- Comprehensive handling of missing values across multiple variables
- Effective outlier detection and treatment using statistical methods
- Successful feature engineering creating clinically relevant variables

### Health Patterns
- Blood pressure variations across demographic groups
- BMI distribution patterns by race/ethnicity and age
- Strong correlations between anthropometric measurements
- Significant associations between obesity and hypertension risk

### Statistical Results
- Gender differences in systolic blood pressure measurements
- Strong association between BMI categories and hypertension prevalence
- Effect sizes indicating practical significance of findings

##  Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn
```

### Running the Analysis
1. Clone this repository
2. Ensure you have the required Python libraries installed
3. Run the Jupyter notebook `nhanes-data-mining-analysis.ipynb`

### Data Files
The notebook automatically downloads the following files:
- `DEMO_J.xpt` - Demographics data
- `BMX_J.xpt` - Body measurements data
- `BPX_J.xpt` - Blood pressure data

##  Visualizations

The project includes comprehensive visualizations:
- **Missing value heatmaps** for data quality assessment
- **Distribution plots** (histograms, box plots, Q-Q plots)
- **Correlation matrices** showing variable relationships
- **Group comparison plots** across demographic categories
- **Transformation effects** before/after preprocessing

##  Statistical Methods

### Preprocessing Techniques
- **Missing value imputation**: Mode and median imputation strategies
- **Outlier detection**: Interquartile range (IQR) method
- **Data transformation**: Z-score standardization, min-max normalization, log transformation
- **Feature scaling**: Multiple scaling approaches for different use cases

### Statistical Tests
- **Normality testing**: Shapiro-Wilk test for distribution assessment
- **Two-sample t-tests**: Welch's t-test for unequal variances
- **Chi-square tests**: Independence testing for categorical associations
- **Effect size measures**: Cohen's d and Cramer's V for practical significance

##  Applications & Use Cases

This project demonstrates techniques applicable to:
- **Public health research**: Population health trend analysis
- **Clinical studies**: Biomedical data preprocessing and analysis
- **Epidemiological research**: Risk factor identification
- **Data science projects**: Real-world data preprocessing workflows
- **Statistical analysis**: Hypothesis testing and inference

##  Future Enhancements

Potential extensions to this project:
- **Machine learning models**: Predictive modeling for health outcomes
- **Advanced feature selection**: Automated feature engineering
- **Time series analysis**: Longitudinal health trend analysis
- **Causal inference**: Advanced statistical modeling
- **Interactive dashboards**: Web-based visualization tools

##  Learning Resources

- [NHANES Documentation](https://www.cdc.gov/nchs/nhanes/index.htm)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Scikit-learn User Guide](https://scikit-learn.org/stable/user_guide.html)
- [Scipy Statistical Functions](https://docs.scipy.org/doc/scipy/reference/stats.html)


##  License

This project is open source and available under the [MIT License](LICENSE).

##  Acknowledgments

- **CDC NHANES Program** for providing comprehensive health survey data
- **Python Data Science Community** for excellent tools and libraries
- **Statistical methods** adapted from standard epidemiological practices

---

**Note**: This project is for educational purposes and demonstrates data mining techniques using publicly available health data. Results should not be used for clinical decision-making without proper validation.
