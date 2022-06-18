# Data_Analyitics

These are tips and records about studying basics of ML and trials in Dacon Competitions.
In these days, I especially focusing on EDA related libraries like pandas-profiling and pycaret.


### 1. Importing Libraries

```
import pandas as pd
from pandas_profiling import ProfileReport
from pycaret.datasets import get_data
from pycaret.classification import *
%matplotlib inline
```
### 2. Get sample data

> df = get_data('iris')
* if you want to see the lists of sample names, just try **get_data()**.<br>
  (eg. iris, diabetes, cancer, boston, etc.)


### 3. See pandas prifiling

>profile = ProfileReport(df, title="Pandas Profiling Report", explorative=True)

There are several ways to see the results.

>profile.to_widgets()

>profile.to_notebook_iframe()

>profile.to_file("your_report.html")


### 4. See Pycaret EDA

> exp_name = setup(data = df,  target = 'species')

> eda()

