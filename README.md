# Metrics
Python implementation of some more uncommon metrics. Currently only longest common subsequence LCS metrics are implemented.

## Dependencies
This package requires the following python libraries:
 1. [numpy](http://www.numpy.org/) (automatically installed when package is installed via pip)
 
## Installation
The metrics package can be installed directly from `pip`.
```
pip3 install distance-metrics
```

## Metrics
The metrics library currently has support for the following modules.
 1. Longest common subsequence metrics `distance_metrics.lcs`
 
### Longest common subsequence metrics
The LCS module currently implements 2 distances:
 1. Length of longest common subsequence (`distance_metrics.lcs.llcs(u, v)`).
 2. [Bakkelund distance](http://hjem.ifi.uio.no/danielry/StringMetric.pdf) [1] (`metrics.lcs.bakkelund(u, v)`)
 
#### Usage
```python
# Imports
from distance_metrics import lcs
import numpy as np

# Create example input arrays
u = np.random.choice(list('ABCD'), size=20)
v = np.random.choice(list('BCDE'), size=20)

# Compute metrics
llcs      = lcs.llcs(u, v)
bakkelund = lcs.bakkelund(u, v)

# Print values
print("LLCS     : {}".format(llcs))
print("Bakkelund: {}".format(bakkelund))
```
 
| References |                                                                                     |
|------------|-------------------------------------------------------------------------------------|
| 1          | [Bakkelund, D. (2009). An LCS-based string metric. Olso, Norway: University of Oslo.](http://hjem.ifi.uio.no/danielry/StringMetric.pdf) |
