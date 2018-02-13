# numba_spatial


Compile with:

```
python3.6 precomp.py
```

## Example:

```
import nbspatial
import numpy as np
lenpoly = 10000
polygon = np.array([[np.sin(x)+0.5,np.cos(x)+0.5] for x in np.linspace(0,2*np.pi,lenpoly)[:-1]])
N = 1000000
points = zip(np.random.random(N),np.random.random(N))
result = [nbspatial.ray_tracing(point[0], point[1], polygon) for point in points]
```
