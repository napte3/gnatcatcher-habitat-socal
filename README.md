# Gnatcatcher Habitat Analysis - Southern California

## Overview
The coastal California Gnatcatcher is a tiny gray bird that is listed as federally threatened and is also designated as a Bird Species of Special Concern by the State of California. These birds live in or near coastal sage shrub, are highly territorial, and are non-migratory. They play a vital role in the ecosystem of coastal Southern California by keeping the population of pests in check. 
This project analyzes how coastal sage scrub habitat has changed across Southern California from 2001 to 2021, whether fragmentation has increased, and what the spatial distribution of gnatcatcher observations reveals about gnatcatcher vulnerability and resilience. 

## Key Findings
- **Net shrub change is deceptively stable**: +0.3% from 2001-2021, but this masks 179,506 hectares lost and 183,522 hectares gained. This indicates large-scale turnover likely driven by wildfires.

- **Gnatcatcher observations concentrated in post-fire recovery zones**: Spatial analysis shows observations clustered in San Diego County, coinciding with regrowth following the Cedar Fire (2003) and Witch Fire (2007). This indicates a fragile and fire-dependent habitat.

- **Increasing habitat fragmentation**: Distinct shrub patches increased 18.6% (114,330 -> 135,585). Median patch size is 0.18 hectares. This is well below the 1-4 hectares required for a breeding gnatcatcher pair. 

- **Observer bias, not habitat recovery**: Percent of pre-2010 gnatcatcher observations on scrub (17.3%) is lower than percent of post-2015 gnatcatcher observations on scrub (21.3%). This likely reflects iNaturalist's growth rather than genuine habitat improvement. The difference is statistically significant (bootstrap 95% CI: 20.10%–22.60%)

## Data Sources
- GBIF occurrence data for Polioptila californica
- NLCD Land Cover 2001 and 2021 (via Google Earth Engine)
- US Census county shapefiles

## Methods
- Raster differencing
- Connected component labeling
- Point sampling
- Bootstrap resampling

## Tools
- Python
- GeoPandas
- Rasterio
- Google Earth Engine
- SciPy
- Matplotlib

## How to run
1. Clone the repo
2. Install dependencies: pip install -r requirements.txt
3. Add raw data files to data/raw/
4. Run gnatcatcher_notebook.ipynb
Note: Raw data files are not included due to file size. GBIF data can be downloaded at gbif.org and NLCD rasters via Google Earth Engine.
