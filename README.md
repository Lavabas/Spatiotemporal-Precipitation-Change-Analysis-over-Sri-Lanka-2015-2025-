# Spatiotemporal Precipitation Change Analysis over SriLanka (2015-2025)
## Overview
Understanding long-term precipitation variability is essential for water resource management, climate risk assessment, and disaster preparedness, particularly for island nations like Sri Lanka, which are highly sensitive to monsoonal dynamics and climate change.

This project analyzes annual precipitation patterns and interannual changes across Sri Lanka using GPM IMERG monthly rainfall data from 2015 to 2025. By integrating Google Earth Engine (GEE) with Python-based geospatial analysis, the workflow enables efficient large-scale data access, temporal aggregation, and spatial visualization of rainfall trends.

The analysis focuses on:
1. Annual precipitation accumulation
2. Year-to-year precipitation change using a temporal differencing technique
3. Mean spatial patterns of precipitation change over the study period

### Study Area
- Region: Sri Lanka
- Boundary Source: USDOS LSIB Simple International Boundaries (2017)
- Approach: Country boundary filtered and clipped dynamically using a user-defined ROI in GEE

## Data Sources
1. GPM IMERG Monthly Precipitation
- Dataset: NASA/GPM_L3/IMERG_MONTHLY_V07
- Temporal Coverage: 2015–2025
- Spatial Resolution: ~0.1° (~11 km)
- Variable Used: precipitation (mm/hr, converted to monthly totals)
- Provider: NASA / GPM Mission

2. Administrative Boundaries
- Dataset: USDOS/LSIB_SIMPLE/2017
- Purpose: National boundary clipping for Sri Lanka

## Tools & Libraries
1. Google Earth Engine (GEE)
2. Python
3. geemap
4. xee
5. xarray
6. NumPy
7. Matplotlib
8. NetCDF-based climate analysis

### Annual Precipitation (2015–2025) - Spatial distribution of annual accumulated precipitation over Sri Lanka derived from GPM IMERG monthly data. The maps highlight strong interannual variability associated with monsoon dynamics.
<img width="1463" height="590" alt="image" src="https://github.com/user-attachments/assets/f356b40e-b177-4742-8ae1-0f8eac5cab4b" />

### Year-to-Year Precipitation Change - Interannual precipitation change maps computed using temporal differencing. Positive values indicate wetter years, while negative values highlight drying trends.
<img width="1474" height="590" alt="image" src="https://github.com/user-attachments/assets/b0247bc4-5ffb-4dd2-a3a4-1dcc33add251" />

### Mean Annual Precipitation Change - Mean spatial pattern of precipitation change across Sri Lanka (2015–2025), revealing regions experiencing consistent increases or decreases in rainfall over the decade.
<img width="570" height="432" alt="image" src="https://github.com/user-attachments/assets/c80c7e08-8631-4fba-b204-bcb0d7cdeb53" />

## Notes & Considerations
- IMERG is a climate-scale dataset; minor coastal distortions are expected
- Spatial resolution (~11 km) limits fine-scale hydrological interpretation
- Boundary simplification was kept minimal to preserve island geometry
- Results are best interpreted as regional trends, not station-level estimates
- Suitable for climate diagnostics, not local flood modeling
