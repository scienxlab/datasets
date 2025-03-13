# USGS

There are two datasets here:

- **Mt St Helens digital elevation model: before and after.** This is a fun dataset to introduce beginners to 2D arrays and visualization eg with Matplotlib's `plt.imshow()`. Most people know a bit about the 1980 eruption that redistributed the volcano's peak, and the contrast between these images shows the removed material (it was mostly deposited beyond the boundaries of this excerpt) [Read more](https://www.usgs.gov/media/images/digital-elevation-map-mount-st-helens-pre-and-post-1980) or [on Wikipedia](https://en.wikipedia.org/wiki/1980_eruption_of_Mount_St._Helens). Copyright free / Public domain.
- **Sussex well data.** Some teaching data extracted from the following online publication: 3-D Reservoir Characterization of the House Creek Oil Field, Powder River Basin, Wyoming, V1.00. [U.S. GEOLOGICAL SURVEY DIGITAL DATA SERIES DDS-33](https://pubs.usgs.gov/dds/dds-033/USGS_3D/data_set/dreadme.htm). The conversion of the raw data into the files in `sussex.zip` is captured in the Jupyter Notebook [`Reorganize_Sussex_well_data.ipynb`](./Reorganize_Sussex_well_data.ipynb). Copyright free / Public domain.

## Example of use

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
