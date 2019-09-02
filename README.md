# nanoserv



### Create a nanoservice

> Create Python repl at: https://repl.it/@username/math

```python
import nanoserv

@nanoserv.expose
def add(a, b, **kwargs):
    return a + b

nanoserv.run(dev=True)
```

### Use it everywhere

```python
from functorflow import ff

# specify which repl.it nanoservice to connect
math = ff.nanoserv.new(replit='username/math')

# use it
print(math.add(8, 9))
```
