# USGS

There is one dataset here so far:

- **Mt St Helens digital elevation model: before and after.** This is a fun dataset to introduce beginners to 2D arrays and visualization eg with Matplotlib's `plt.imshow()`. Most people know a bit about the 1980 eruption that redistributed the volcano's peak, and the contrast between these images shows the removed material (it was mostly deposited beyond the boundaries of this excerpt) [Read more](https://www.usgs.gov/media/images/digital-elevation-map-mount-st-helens-pre-and-post-1980) or [on Wikipedia](https://en.wikipedia.org/wiki/1980_eruption_of_Mount_St._Helens). Copyright free / Public domain.

## Example

```python
import matplotlib.pyplot as plt
import numpy as np
import requests
import io

# Load the 'before' data.
url = "https://raw.githubusercontent.com/scienxlab/datasets/refs/heads/main/usgs/st-helens-before.txt"
r = requests.get(url)
before = np.loadtxt(io.StringIO(r.text))
plt.imshow(before)
```

![image](https://github.com/user-attachments/assets/61e26626-8294-4384-9737-5ce5ebf5e443)
