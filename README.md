![](https://res.cloudinary.com/functorflow/image/upload/c_scale,w_1093/v1567428156/cover_ngfogb.png)

# nanoserv


### Install 

```bash
pip install nanoserv
```

### Create a nanoservice

> Create a Python repl and expose the `add` function using `@nanoserv.expose`:

```python
# https://repl.it/@username/math

import nanoserv

@nanoserv.expose
def add(a, b, **kwargs):
    return a + b

nanoserv.run(dev=True)
```

### Use it everywhere

> Connect to `username/math` repl and call it's function `add(8, 9)`

```python
from functorflow import ff

# Connect to repl at `username/math` 
math = ff.nanoserv.new(replit='username/math')

# use it
print(math.add(8, 9))
```
