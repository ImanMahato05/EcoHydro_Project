# EcoHydro_Project

## Uploading files from Google Colab

If you are working in Colab and want to upload files for this project:

```python
from google.colab import files

uploaded = files.upload()
```

This opens a file picker and uploads files to the current Colab runtime directory.

To move uploaded files into your project folder in Colab:

```python
import shutil
from pathlib import Path

project_dir = Path("/content/EcoHydro_Project")

for name in uploaded:
    shutil.move(name, project_dir / name)
```
