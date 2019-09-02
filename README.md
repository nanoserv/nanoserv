![](https://res.cloudinary.com/functorflow/image/upload/c_scale,w_1286/v1567428670/cover_aybzhh.png)


### install 

```bash
pip install nanoserv
```

### create a nanoservice

[![CREATE A REPL](https://res.cloudinary.com/functorflow/image/upload/v1567435934/new-repl.png)](https://repl.it/languages/python3) and expose any function using `@nanoserv.expose`:

```python
# https://repl.it/@username/math

import nanoserv

@nanoserv.expose
def add(a, b, **kwargs):
    return a + b

nanoserv.run(dev=True)
```

### use it everywhere

Connect to `username/math` repl and call it's function `add(8, 9)`

```python
from functorflow import ff

# Connect to repl at `username/math` 
math = ff.nanoserv.new(replit='username/math')

# use it
print(math.add(8, 9))
```

