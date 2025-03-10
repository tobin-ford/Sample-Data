# Sample Weather/Irradiance Data For Geospatial Analysis

Goal: Provide simple test data for geospatial analysis using [`PVDeg`](https://github.com/NREL/PVDegradationTools)

Structure: Directories are named after data source. Each directory has two files. A netcdf containing geospatial weather/irradiance data, and a metadata csv containing corresponding metadata for locations in the netcdf.

# Loading Data

PVDeg uses pandas and xarray to load these types of files so we will use the same conventions here.

```
import pandas as pd
import xarray as xr

geo_weather = xr.open_dataset("<your_netcdf>.nc")
geo_meta = pd.read_csv("<your_csv>.csv", index_col=0)
```

# Sample Datasets
### NSRDB-Kestrel-TMY
79 CONUS data points taken directly from TMY data from the "current" directory on Kestrel. This data is in UTC/GMT 0 and uses a timezone naive pandas datetime index.

### NSRDB-Kestrel-5 Minute
coming soon...

### NSRDB-PVDeg Download
coming soon...

### NSRDB-PVGIS Download
coming soon...