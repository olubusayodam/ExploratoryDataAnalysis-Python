
# Exploratory Data Analysis on StudentsPerformance Dataset

----
# Introduction:
In this analysis, I performed exploratory data analysis (EDA) on the "Students Performance" dataset. The purpose of the analysis is to gain insights into the dataset and understand the distribution and relationships among various features. The dataset contains information about students' scores in math, reading, and writing, as well as their demographic and educational background.
Dataset Availability:
The dataset file, "StudentsPerformance.csv," is included in this repository. It contains the raw data that was used for the analysis.

 Importing Libraries and Data:
To conduct the analysis, I imported the necessary Python libraries, including pandas, numpy, matplotlib, and seaborn. I then loaded the dataset into a pandas DataFrame named 'df' using `pd.read_csv()`.

 Understanding the Data:
To get a glimpse of the data, I displayed the first 10 rows of the DataFrame using `df.head(10)` and the last 10 rows using `df.tail(10)`. The dataset consists of 1000 rows and 8 columns.

I checked the data types of each column using `df.dtypes`, revealing that most columns are categorical ('object') while the scores are numerical ('int64'). Additionally, I used `df.info()` to obtain summary information about the DataFrame.




-----
# Data Cleaning:
I checked for missing values in the dataset using `df.isnull().sum()` and confirmed that there are no missing values.

To make the data more concise, I renamed the values in the 'race/ethnicity' column to shorter labels ('B', 'C', 'A', 'D', 'E') using `df['race/ethnicity'] = df['race/ethnicity'].replace()`. Similarly, I renamed the values in the 'parental level of education' column to shorter labels ('bsc', 'sc', 'msc', 'ad', 'hs', 'shs') using `df['parental level of education'] = df['parental level of education'].replace()`. I also renamed the column names to shorter ones using `df.columns = ['gender', 'race', 'p_edu', 'lunch', 'tprep_course', 'm_score', 'r_score', 'w_score']`.


----
# Relationship Analysis and Data Visualization:
To explore the relationships between numerical features, I calculated the correlation matrix using `df.corr()` and visualized it as a heatmap using `sns.heatmap()`.

I further explored the relationships between numerical features by creating a pairplot using `sns.pairplot()`.

I visualized the relationship between 'math score' and 'reading score' using a scatter plot, coloring the points by gender with `sns.relplot()`.

Histograms were plotted for the 'math score' and all numerical features using `sns.displot()` and `df.hist()` respectively.

A box plot was used to observe the distribution of the 'math score', detecting any outliers with `sns.catplot()`.

I also created a count plot to visualize the count of genders in the dataset using `sns.countplot()`.

---


# Conclusion
The exploratory data analysis (EDA) on the "StudentsPerformance.csv" dataset provided valuable insights into the data. I observed relationships between numerical features and explored the distributions of individual features. The dataset contains no missing values, ensuring the data's integrity for further analysis.

