# Python Basics for Statistical Analysis
```
import numpy as np
import pandas as pd
```

### import data from csv
`transactions = pd.read_csv("transactions.csv")`

### minimum
`min = np.amin(array)`

### maximum
`max = np.amax(array)`

### range
`range = max - min`

## find bin width
```
bins = # of bins u wanna have
bin_width = (range + 1) / bins
= (max-min + 1) / bins
```

### histogram function
`np.histogram(exercise_ages, range = (20, 70), bins = 5)`
* `exercise_ages` is the input array
* `range = (20, 70)` is the range of values we expect in our array.
* Range includes everything from 20, up until but not including 70.
* `bins = 5` is the number of bins.
* Python will automatically calculate equally-sized bins based on the range and number of bins.
* **Output:** First array is the counts for each bin. Second array includes the min & max for each bin

### to graph histograms...
```
from matplotlib import pyplot as plt

plt.hist(exercise_ages, range = (20, 70), bins = 5, edgecolor='black')
plt.title("Decade Frequency")
plt.xlabel("Ages")
plt.ylabel("Count")
plt.show()
```

