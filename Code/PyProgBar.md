print progress bar in py:

```py
import time
from tqdm import tqdm
for i in tqdm(range(500)):
  time.sleep(0.05)
  
```
