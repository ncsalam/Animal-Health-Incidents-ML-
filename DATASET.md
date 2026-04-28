The dataset used in this project is publicly available on Kaggle:

- [Global Animal Health Incident EDA & Insights (2005–Present)](https://www.kaggle.com/code/jasonrobinson1/global-animal-health-incident-eda-insights-2005)

This dataset provides historical records of global animal health incidents, including disease type, affected species, geographic location, and temporal information. Instructions for accessing and downloading the dataset can be found on the linked Kaggle page.

For reproducibility, the dataset can also be downloaded programmatically using the Kaggle API, as shown below:

```python
import kagglehub
import pandas as pd
import os

# Download latest version of the dataset
path = kagglehub.dataset_download("jasonrobinson1/animal-health-incident-reports")

# List all files in the dataset directory
files = os.listdir(path)

# Load the dataset (adjust filename if needed)
df = pd.read_csv(os.path.join(path, files[0]))