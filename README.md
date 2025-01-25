
# Superstore Sales Data Analysis using Python Libraries with Google Collabs

## Project Description
Explored and analyzed the Superstore sales dataset using Google Collabs. The analysis included data cleaning, statistical summary, and visualizations to derive actionable insights from sales, quantity, discount, and profit data.



## Steps and Code

### 1. Importing Libraries
```python
import pandas as pd
import seaborn as sbn
import numpy as np
```

### 2. Loading the Dataset
```python
df = pd.read_excel('/content/Sample - Superstore (1).xls')
df.head(10)
df.tail(10)
```

### 3. Statistical Summary of the Dataset
```python
df[['Sales', 'Quantity', 'Discount', 'Profit']].describe()
```

### 4. Data Imputation for Missing Values
#### Fill missing values with 0
```python
df['Sales_new'] = df['Sales'].fillna(0)
```

#### Fill missing values with the median of the column
```python
df['Sales_new1'] = df['Sales'].fillna(df['Sales'].median())
```

### 5. Data Visualization
#### Count plot for Category
```python
sbn.countplot(data=df, x='Category')
```

### 6. Grouping and Aggregation
#### Mean Sales by Category
```python
df.groupby(['Category'])['Sales'].mean()
```

## How to Use
1. **Clone the Repository**: Clone this repository to your local machine using `git clone <repository_url>`.
2. **Run the Jupyter Notebook**: Open the Jupyter Notebook file (`.ipynb`) and execute the cells to reproduce the analysis.
3. **Explore the Analysis**: Review the data cleaning, statistical summaries, and visualizations to gain insights from the Superstore sales dataset.

## Requirements
- **Google collab or Jupyter Notebook**: Ensure you have Jupyter Notebook or Google collab installed.
- **Pandas**: For data manipulation and analysis.
- **Seaborn**: For data visualization.
- **NumPy**: For numerical operations.


## Contact
For any questions or feedback, feel free to contact [Sharada S.] at [sharadasonaje25@gmail.com].





