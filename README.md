# GeoOptiCarbon-Spatial-Conservation-Planning
This spatial optimization system identifies optimal land parcels for conservation efforts by balancing three critical factors:  Carbon Storage Potential,  Implementation Costs and  Geospatial Constraints
GeoCarbon Optimizer
GeoCarbon Optimizer is a Python-based geospatial tool for selecting optimal land parcels to maximize carbon storage while adhering to budget and adjacency constraints.

Installation
Use Conda to install dependencies:

conda create -n geo_env python=3.9 geopandas pulp matplotlib jupyterlab -c conda-forge
conda activate geo_env
Usage
Prepare Data

Place your shapefile (land_parcels.shp + companion files) in the project directory.

Run Analysis

Launch Jupyter Lab and execute the workflow:

jupyter lab solution.ipynb
Example Code Snippet
# Load data
import geopandas as gpd
parcels = gpd.read_file("land_parcels.shp")

# Run optimization
prob.solve()
print("Optimal parcels:", [i for i in x if x[i].varValue == 1])
