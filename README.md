# Air Quality in Dar es Salaam — Notebook

This repository contains a single Jupyter notebook, `035-assignment.ipynb`, exploring PM2.5 air quality readings for Dar es Salaam. The original distribution included proprietary WorldQuant University materials (and associated videos). Those proprietary materials have been removed from this copy.

**Story**
- Dar es Salaam is a bustling, growing city where air quality directly affects health and daily life. This notebook walks through a pragmatic time-series analysis pipeline: wrangling sensor readings, exploratory plots, baseline modeling, autoregression tuning, and walk-forward validation.

What I changed
- Removed WorldQuant University copyright and proprietary video references.
- Added this README with clear instructions and a brief narrative.

How to run
1. Create a Python environment and install dependencies:

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

2. Provide data — choose one:
- MongoDB: set the `host` variable in `035-assignment.ipynb` to your MongoDB address and ensure the `air-quality` database and `dar-es-salaam` collection are available.
- CSV: create `data/p2_readings.csv` with columns `timestamp` (ISO format) and `P2`, then adapt `wrangle()` to read from the CSV, or replace the MongoDB section with:

```python
import pandas as pd
df = pd.read_csv('data/p2_readings.csv', parse_dates=['timestamp']).set_index('timestamp')
# then follow the notebook's cleaning/resampling steps
```

3. Open the notebook and run the cells in order.

Notes & Next steps
- This copy intentionally omits proprietary datasets and videos. If you have access to similar sensor data, you can reuse the notebook pipeline.
- If you'd like, I can: (a) adapt the notebook to load a CSV automatically, (b) add a small example CSV with synthetic data, or (c) create a requirements-locked `requirements.txt` and a minimal GitHub-friendly `LICENSE`.

Enjoy exploring air quality in Dar es Salaam — and let me know how you'd like the notebook tailored to your data.