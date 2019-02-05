# ray-notes
Notes based on my exploration of the Ray distributed multiprocessing library

## General

Given:

```python
import ray
import numpy as np

@ray.remote
def func(arg_1, arg_2):
    do_stuff()
    arg_1[:] = 0
    
func.remote(np.ones(5), 5)
```

The above will error, because anything Ray passes to your function will be read-only (as is protocol per object store behavior).
