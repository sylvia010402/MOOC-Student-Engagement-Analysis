```python
# Load and examine the MOOC dataset
import pandas as pd
import numpy as np

# Load the dataset
df = pd.read_csv('/Users/le/Desktop/2025 Spring/S022 computing and data science/022 final project/S022_R_Project/data/MOOC_cleaned.csv')  # Replace with your file path


# Basic info about the dataset
print("Dataset shape:", df.shape)
print("\
Column names and types:")
print(df.dtypes)
print("\
First few rows:")
print(df.head())
```

    Dataset shape: (260838, 18)
    Column names and types:
    course_id             object
    userid_DI             object
    viewed                 int64
    explored               int64
    certified              int64
    final_cc_cname_DI     object
    LoE_DI                object
    YoB                    int64
    gender                object
    start_time_DI         object
    last_event_DI         object
    nforum_posts           int64
    nevents_log          float64
    nplay_video_log      float64
    ndays_act_log        float64
    grade_log            float64
    nchapters_log        float64
    nforum_posts_log     float64
    dtype: object
    First few rows:
                        course_id       userid_DI  viewed  explored  certified  \
    0  HarvardX/CB22x/2013_Spring  MHxPC130539455       1         0          0   
    1  HarvardX/CB22x/2013_Spring  MHxPC130088379       1         0          0   
    2  HarvardX/CB22x/2013_Spring  MHxPC130024894       1         0          0   
    3  HarvardX/CB22x/2013_Spring  MHxPC130340959       1         0          0   
    4  HarvardX/CB22x/2013_Spring  MHxPC130148402       0         0          0   
    
      final_cc_cname_DI      LoE_DI   YoB gender start_time_DI last_event_DI  \
    0            France   Secondary  1989      m    2013-01-01    2013-05-14   
    1     United States   Secondary  1993      m    2013-02-18    2013-03-17   
    2     United States    Master's  1987      f    2013-01-24    2013-08-03   
    3     United States  Bachelor's  1984      m    2013-02-11    2013-04-06   
    4     United States   Secondary  1982      f    2012-12-23    2013-11-17   
    
       nforum_posts  nevents_log  nplay_video_log  ndays_act_log  grade_log  \
    0             0     3.761200         2.564949       1.945910   0.000000   
    1             0     4.262680         2.397895       1.386294   0.000000   
    2             0     5.170484         2.890372       2.302585   0.067659   
    3             0     5.655992         5.700444       2.197225   0.048790   
    4             0     4.564348         2.639057       1.945910   0.000000   
    
       nchapters_log  nforum_posts_log  
    0       1.386294               0.0  
    1       1.386294               0.0  
    2       2.079442               0.0  
    3       1.609438               0.0  
    4       1.609438               0.0  


This code snippet loads a cleaned MOOC dataset and displays its shape, column names with types, and the first few rows.
- Load the dataset from a CSV file
- Print the shape of the dataset
- Print the data types of each column
- Display the first few rows of the dataset


```python
# Get more detailed information about the dataset
print("Dataset summary statistics:")
print(df.describe())

print("\
Unique values in key categorical columns:")
print("Number of unique courses:", df['course_id'].nunique())
print("Number of unique users:", df['userid_DI'].nunique())
print("Countries:", df['final_cc_cname_DI'].value_counts().head(10))
print("\
Education levels:", df['LoE_DI'].value_counts())
print("\
Gender distribution:", df['gender'].value_counts())
```

    Dataset summary statistics:
                 viewed       explored      certified            YoB  \
    count  260838.00000  260838.000000  260838.000000  260838.000000   
    mean        0.49538       0.071297       0.025165    1983.876352   
    std         0.49998       0.257321       0.156626       9.654767   
    min         0.00000       0.000000       0.000000    1931.000000   
    25%         0.00000       0.000000       0.000000    1980.000000   
    50%         0.00000       0.000000       0.000000    1986.000000   
    75%         1.00000       0.000000       0.000000    1990.000000   
    max         1.00000       1.000000       1.000000    1997.000000   
    
            nforum_posts    nevents_log  nplay_video_log  ndays_act_log  \
    count  260838.000000  260838.000000    260838.000000  260838.000000   
    mean        0.014806       3.077671         1.834963       1.279803   
    std         0.170862       1.765387         1.459118       0.748111   
    min         0.000000       0.693147         0.693147       0.693147   
    25%         0.000000       1.386294         0.693147       0.693147   
    50%         0.000000       2.890372         1.098612       1.098612   
    75%         0.000000       4.564348         2.639057       1.609438   
    max         7.000000       5.976351         5.774552       5.075174   
    
               grade_log  nchapters_log  nforum_posts_log  
    count  260838.000000  260838.000000     260838.000000  
    mean        0.022743       1.248881          0.008663  
    std         0.107258       0.617578          0.090195  
    min         0.000000       0.693147          0.000000  
    25%         0.000000       0.693147          0.000000  
    50%         0.000000       1.098612          0.000000  
    75%         0.000000       1.386294          0.000000  
    max         0.693147       3.555348          2.079442  
    Unique values in key categorical columns:
    Number of unique courses: 5
    Number of unique users: 239052
    Countries: final_cc_cname_DI
    United States                     79953
    Unknown/Other                     42015
    India                             25277
    Other Europe                      16096
    Other Africa                      10497
    United Kingdom                     9571
    Brazil                             7356
    Canada                             6109
    Other Middle East/Central Asia     5957
    Other South Asia                   5589
    Name: count, dtype: int64
    Education levels: LoE_DI
    Bachelor's             105932
    Secondary               72480
    Master's                66949
    Doctorate                9095
    Less than Secondary      6382
    Name: count, dtype: int64
    Gender distribution: gender
    m    171764
    f     89066
    o         8
    Name: count, dtype: int64


This code snippet summarizes the dataset's statistics and counts unique values for key categorical columns.
- Print summary statistics of the dataset
- Count and print unique courses
- Count and print unique users
- Display the top 10 countries by count
- Display counts of education levels
- Display counts of gender distribution


```python
# Let's examine the engagement patterns and create some initial insights
print("Engagement funnel analysis:")
print("Viewed courses:", df['viewed'].sum())
print("Explored courses:", df['explored'].sum()) 
print("Certified completions:", df['certified'].sum())

print("\
Conversion rates:")
total_enrolled = len(df)
viewed_rate = df['viewed'].sum() / total_enrolled * 100
explored_rate = df['explored'].sum() / total_enrolled * 100
certified_rate = df['certified'].sum() / total_enrolled * 100

print(f"View rate: {viewed_rate:.1f}%")
print(f"Exploration rate: {explored_rate:.1f}%") 
print(f"Certification rate: {certified_rate:.1f}%")

# Check date ranges
df['start_time_DI'] = pd.to_datetime(df['start_time_DI'])
df['last_event_DI'] = pd.to_datetime(df['last_event_DI'])

print(f"\
Date range: {df['start_time_DI'].min()} to {df['last_event_DI'].max()}")
print("Courses offered:", df['course_id'].unique())
```

    Engagement funnel analysis:
    Viewed courses: 129214
    Explored courses: 18597
    Certified completions: 6564
    Conversion rates:
    View rate: 49.5%
    Exploration rate: 7.1%
    Certification rate: 2.5%
    Date range: 2012-07-23 00:00:00 to 2013-11-17 00:00:00
    Courses offered: ['HarvardX/CB22x/2013_Spring' 'HarvardX/CS50x/2012'
     'HarvardX/ER22x/2013_Spring' 'HarvardX/PH207x/2012_Fall'
     'HarvardX/PH278x/2013_Spring']


### Key Dataset Insights:
Engagement Funnel:

Viewed courses:
129214

Explored courses:
18597

Certified completions:
6564

Conversion rates:
View rate: 49.5%
Exploration rate: 7.1%
Certification rate: 2.5%
