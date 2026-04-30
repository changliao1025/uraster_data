# Examples folder inputs

This folder contains example inputs for running **uraster** workflows.
Each example includes a source mesh, one or more raster files, and configuration details that defines how raster values are mapped or aggregated onto the mesh.

## Format used for each example

For consistency, every example entry uses the same structure.

* Source mesh, what mesh is used and its approximate resolution
* Input raster, what raster is used, key raster metadata, and data sources
* Configuration, what key settings it must contain

---

## Example 1

### Source mesh
* Description: Global rhealpix mesh, 116744 km² cell size
* Mesh type: rhealpix
* Mesh file or files `rhealpix_global_res3.geojson`
* Cell size: 116744 km²

### Input raster
* Raster file or files `EDGAR_CH4_emission_global_2015.tiff`
* Tiling: single
* Data type: continuous
* Spatial resolution: 0.1 x 0.1°
* CRS: EPSG 4326
* Spatial coverage: global
* Notes: EDGAR CH4 manure management inventory data in 2015, unit ton. The raw netCDF data has been pre-processed to tiff file.
* Data source:
  Data can be downloaded from [here](https://data.jrc.ec.europa.eu/dataset/b54d8149-2864-4fb9-96b9-5fd3a020c224)
* Reference:
    Crippa, M., et al. (2021). High resolution temporal profiles in the Emissions Database for Global Atmospheric Research (EDGAR).

### Configuration
* Resample method: Average

---

## Example 2

### Source mesh
* Description: isea3h mesh for Toronto and Buffalo, 3.55 km² cell size
* Mesh type: isea3h
* Mesh file or files `isea3h_bbox_res15.geojson`
* Cell size: 3.55 km²

### Input raster
* Raster file or files `WSF2015_v2_-80_42.tif`
* Tiling: single
* Data type: discrete
* Spatial resolution: 0.32 arcsec
* CRS: EPSG 4326
* Spatial coverage: one tile covering Toronto, Canada and Buffalo, US
* Notes: World settlement footprint data, 255/0 binary
* Data source:
  Data can be downloaded from [here](https://download.geoservice.dlr.de/WSF2015/)
* Reference:
    Marconcini, M., et al. (2020). Outlining where humans live, the World Settlement Footprint 2015. Scientific Data, 7(1), 242.

### Configuration
* Resample method: Dominant

---

## Example 3

### Source mesh
* Description: rhealpix mesh for mainland China, 116744 km² cell size
* Mesh type: rhealpix
* Mesh file or files `rhealpix_China_res3.geojson`
* Cell size: 116744 km²

### Input raster
* Raster file or files `China_CH4_emission_2020.tif`
* Tiling: single
* Data type: continuous
* Spatial resolution: 10 x 10 km
* CRS: EPSG 4024
* Spatial coverage: mainland China
* Notes: Coal Mine Methane Emissions in China in 2020, unit Mg km⁻² a⁻¹
* Data source:
  Data can be downloaded from [here](https://pubs.acs.org/doi/full/10.1021/acs.estlett.9b00294)
* Reference:
    Sheng, J., et al. (2019). Bottom-Up Estimates of Coal Mine Methane Emissions in China: A Gridded Inventory, Emission Factors, and Trends. Environmental Science & Technology Letters, 6(8), 473-478.

### Configuration
* Resample method: Average

---

## Example 4

### Source mesh
* Description: rhealpix mesh for mainland China, 160 km² cell size
* Mesh type: rhealpix
* Mesh file or files `rhealpix_China_res6.geojson`
* Cell size: 160 km²

### Input raster
* Raster file or files `China_CH4_emission_2020.tif` (same as example 3)
* Tiling: single
* Data type: continuous
* Spatial resolution: 10 x 10 km
* CRS: EPSG 4024
* Spatial coverage: mainland China
* Notes: Coal Mine Methane Emissions in China in 2020, unit Mg km⁻² a⁻¹
* Data source:
  Data can be downloaded from [here](https://pubs.acs.org/doi/full/10.1021/acs.estlett.9b00294)
* Reference:
    Sheng, J., et al. (2019). Bottom-Up Estimates of Coal Mine Methane Emissions in China: A Gridded Inventory, Emission Factors, and Trends. Environmental Science & Technology Letters, 6(8), 473-478.

### Configuration
* Resample method: Average

---

## Example 5

### Source mesh
* Description: isea7h mesh for the inland east US, 3034.84 km² cell size
* Mesh type: isea7h
* Mesh file or files `isea7h_bbox_res5.geojson`
* Cell size: 3034.84 km²

### Input raster
* Raster file or files
  `Hansen_GFC-2019-v1.7_treecover2000_40N_090W.tif`,
  `Hansen_GFC-2019-v1.7_treecover2000_40N_100W.tif`,
  `Hansen_GFC-2019-v1.7_treecover2000_50N_090W.tif`,
  `Hansen_GFC-2019-v1.7_treecover2000_50N_100W.tif`
* Tiling: multi-tile
* Data type: continuous
* Spatial resolution: 0.00025 x 0.00025°
* CRS: EPSG 4326
* Spatial coverage: four tiles covering the inland east US
* Notes: Tree cover in the year 2000, defined as canopy closure for all vegetation taller than 5m in height. Encoded as a percentage per output grid cell, in the range 0–100.
* Data source:
  Data can be downloaded from [here](https://earthenginepartners.appspot.com/science-2013-global-forest/download_v1.7.html)
* Reference:
    Hansen, M. C., et al. (2013). High-Resolution Global Maps of 21st-Century Forest Cover Change. Science, 342(6160), 850-853.

### Configuration
* Resample method: Average

---

## Example 6

### Source mesh
* Description: isea7h mesh for high-latitude area in Nunavut, 1.26 km² cell size
* Mesh type: isea7h
* Mesh file or files `isea7h_bbox_res8.geojson`
* Cell size: 1.26 km²

### Input raster
* Raster file or files
  `ArcticDEM_32_34_1_1_2m_v4.1_dem.tif`,
  `ArcticDEM_32_34_1_2_2m_v4.1_dem.tif`,
  `ArcticDEM_32_35_1_1_2m_v4.1_dem.tif`,
  `N79W078_FABDEM_V1-0.tif`,
  `N79W079_FABDEM_V1-0.tif`,
  `N79W080_FABDEM_V1-0.tif`,
  `N79W081_FABDEM_V1-0.tif`,
  `N79W082_FABDEM_V1-0.tif`,
  `N79W083_FABDEM_V1-0.tif`
* Tiling: multi-tile
* Data type: continuous
* Spatial resolution:
  ArcticDEM - 2 x 2 m
  FABDEM - 1 arcsec
* CRS:
  ArcticDEM - EPSG 3413
  FABDEM - EPSG 4326
* Spatial coverage: three ArcticDEM tiles + six FABDEM tiles, covering high-latitude area in Nunavut
* Notes:
  ArcticDEM is a high-resolution, high quality, digital surface model (DSM) of the Arctic. DSM can be viewed as DEM in the Arctic.
  FABDEM (Forest And Buildings removed Copernicus DEM) is a global elevation map that removes building and tree height biases from the Copernicus GLO 30 Digital Elevation Model (DEM).
* Data source:
  ArcticDEM data can be downloaded from [here](https://www.arcgis.com/apps/webappviewer/index.html?id=aff5fa8f5d5548c6bff44cc8be385f61)
  FABDEM data can be downloaded from [here](https://data.bris.ac.uk/data/dataset/25wfy0f9ukoge2gs7a5mqpq2j7)
* Reference:
    Hawker, L., Uhe, P., Paulo, L., Sosa, J., Savage, J., Sampson, C. and Neal, J., 2022. A 30 m global map of elevation with forests and buildings removed. Environmental Research Letters, 17(2), 024016.
    Porter, Claire; Howat, Ian; Noh, Myoung-Jon; Husby, Erik; Khuvis, Samuel; Danish, Evan; Tomko, Karen; Gardiner, Judith; Negrete, Adelaide; Yadav, Bidhyananda; Klassen, James; Kelleher, Cole; Cloutier, Michael; Bakker, Jesse; Enos, Jeremy; Arnold, Galen; Bauer, Greg; Morin, Paul, (2023): ArcticDEM - Mosaics, Version 4.1, Harvard Dataverse, V1 [Dataset] doi:10.7910/DVN/3VDC4W

### Configuration
* Resample method: Average

---

## Example 7

### Source mesh
* Description: isea3h mesh for the Rocky Mountains and surrounding areas, 95.98 km² cell size
* Mesh type: isea3h
* Mesh file or files `isea3h_bbox_res12.geojson`
* Cell size: 95.98 km²

### Input raster
* Raster file or files
  `11T_20240101-20241231.tif`,
  `11U_20240101-20241231.tif`,
  `12T_20240101-20241231.tif`,
  `12U_20240101-20241231.tif`
* Tiling: multi-tile
* Data type: discrete
* Spatial resolution: 10 x 10 m
* CRS: EPSG 32612, EPSG 32611
* Spatial coverage: four tiles covering part of the Rocky Mountains and the surrounding areas
* Notes: Esri land use/land cover derived from ESA Sentinel-2 imagery in 2024
* Data source:
  Data can be downloaded from [here](https://livingatlas.arcgis.com/landcoverexplorer/#mapCenter=-117.27100%2C33.94200%2C10.00&mode=step&timeExtent=2017%2C2022&year=2022)
* Reference:
    Karra, K., et al. (2021). Global land use/land cover with Sentinel-2 and deep learning. IGARSS 2021.

### Configuration
* Resample method: Dominant

---

## Example 8

### Source mesh
* Description: Tin mesh for the Susquehanna river basin, generated using JIGSAW
* Mesh type: tin
* Mesh file or files `tin.geojson`
* Cell size: NA

### Input raster
* Raster file or files `hyd_glo_dem_15s.tif`
* Tiling: single
* Data type: continuous
* Spatial resolution: 15 arc-second
* CRS: EPSG 4326
* Spatial coverage: Global
* Notes: HydroSHEDS global digital elevation model (DEM). Tin mesh for the Susquehanna river basin, generated using JIGSAW
* Data source:
  Data can be downloaded from [here](https://www.hydrosheds.org/)
* Reference:
    Lehner, B., et al. (2008). New global hydrography derived from spaceborne elevation data. Eos, Transactions American Geophysical Union, 89(10), 93-94.

### Configuration
* Resample method: Average

---

## Example 9

### Source mesh
* Description: Global mpas mesh
* Mesh type: mpas
* Mesh file or files `mpas.geojson`
* Cell size: NA

### Input raster
* Raster file or files `hyd_glo_dem_15s.tif` (same as example 8)
* Tiling: single
* Data type: continuous
* Spatial resolution: 15 arc-second
* CRS: EPSG 4326
* Spatial coverage: Global
* Notes: HydroSHEDS global digital elevation model (DEM). Global mpas mesh
* Data source:
  Data can be downloaded from [here](https://www.hydrosheds.org/)
* Reference:
    Lehner, B., et al. (2008). New global hydrography derived from spaceborne elevation data. Eos, Transactions American Geophysical Union, 89(10), 93-94.

### Configuration
* Resample method: Average

---

## Example 10

### Source mesh
* Description: same as example 3
* Mesh type: rhealpix
* Mesh file or files `rhealpix_China_res3.geojson` (same as example 3)
* Cell size: 116744 km²

### Input raster
* Raster file or files `China_CH4_emission_2020.tif` (same as example 3)
* Tiling: single
* Data type: continuous
* Spatial resolution: 10 x 10 km
* CRS: EPSG 4024
* Spatial coverage: mainland China
* Notes: Coal Mine Methane Emissions in China in 2020, unit Mg km⁻² a⁻¹
* Data source:
  Data can be downloaded from [here](https://pubs.acs.org/doi/full/10.1021/acs.estlett.9b00294)
* Reference:
    Sheng, J., et al. (2019). Bottom-Up Estimates of Coal Mine Methane Emissions in China: A Gridded Inventory, Emission Factors, and Trends. Environmental Science & Technology Letters, 6(8), 473-478.

### Configuration
* Resample method: Weighted average

---

