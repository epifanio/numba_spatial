# numba_spatial

[![DOI](https://zenodo.org/badge/121392336.svg)](https://zenodo.org/badge/latestdoi/121392336)

Compile with:

```
python3.6 nbspatial_src.py
```

## Example:

```python
import nbspatial
import numpy as np
lenpoly = 10000
polygon = np.array([[np.sin(x)+0.5,np.cos(x)+0.5] for x in np.linspace(0,2*np.pi,lenpoly)[:-1]])
N = 1000000
points = zip(np.random.random(N),np.random.random(N))
result = [nbspatial.ray_tracing(point[0], point[1], polygon) for point in points]
# result=get_spatial_selection_cpu=get_spatial_selection_cpu(points,polygon)
```
