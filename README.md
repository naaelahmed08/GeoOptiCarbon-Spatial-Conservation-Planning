# GeoCarbon Optimizer

GeoCarbon Optimizer is a Python-based geospatial tool for selecting optimal land parcels to maximize carbon storage while adhering to budget and adjacency constraints.

## Installation

Use [Conda](https://docs.conda.io/en/latest/) to install dependencies:

```bash
conda create -n geo_env python=3.9 geopandas pulp matplotlib jupyterlab -c conda-forge
conda activate geo_env
```
## Usage
1) Prepare Data

   Place your shapefile (land_parcels.shp + companion files) in the project directory.

2) Run Analysis 

   Launch Jupyter Lab and execute the workflow:

```bash
jupyter lab solution.ipynb
```

3) Example Code Snippet
```bash
# Load data
import geopandas as gpd
parcels = gpd.read_file("land_parcels.shp")

# Run optimization
prob.solve()
print("Optimal parcels:", [i for i in x if x[i].varValue == 1])
```
