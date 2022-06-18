# Data_Analyitics

These are tips and records about studying basics of ML and trials in Dacon Competitions.</br>
In these days, I am especially focusing on EDA related libraries like pandas-profiling and pycaret.


<a href="https://pypi.org/project/pandas-profiling/" target="_blank" rel="noopener noreferrer"><img src="./img/pandas_profiling.png" width="40%" height="30%" title="pandas-profiling" alt="pandas-profiling"></img></a>
<a href ="https://pycaret.org/" target="_blank" rel="noopener noreferrer"><img src="./img/pycaret.png" width="40%" height="30%" title="pycaret" alt="pycaret"></img></a>

---


### 1. Importing Libraries

```python
import pandas as pd
from pycaret.datasets import get_data
from pandas_profiling import ProfileReport
from pycaret.classification import *
import matplotlib.pyplot as plt
%matplotlib inline
```
### 2. Get sample data

> df = get_data('iris')
* if you want to see the lists of sample names, just try **get_data()**.<br>
  (eg. iris, diabetes, cancer, boston, etc.)


### 3. See pandas prifiling

>profile = ProfileReport(df, title="Pandas Profiling Report", explorative=True)

* There are several ways to see the results.

>>>profile.to_widgets()

>>>profile.to_notebook_iframe()

>>>profile.to_file("your_report.html")


### 4. See Pycaret EDA

> exp_name = setup(data = df,  target = 'species')

> eda()

