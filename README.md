# nanoserv

### Create a nanoservice on Repl.it

```python
import nanoserv

@nanoserv.expose
def add(a, b, **kwargs):
    return a + b

nanoserv.run(dev=True)
```

### Call a function of nanoservice using FunctorFlow

```python
from functorflow import ff

# specify which repl.it nanoservice to connect
math = ff.nanoserv.new(replit='nanoserv/math')

# use it
print(math.add(8, 9))
```
