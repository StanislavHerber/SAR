![image](https://github.com/StanislavHerber/SAR/assets/134272440/db81e86d-30d4-4224-abe2-c2d75b8bbf5c)

# Introduction
This repository focuses on processing of Radar remote sensing data via SNAP or Google Earth Engine platform.

# Data archives

* [ASF](https://asf.alaska.edu/) - Alaska Satellite Facility</a>;
* [Sentinel](https://scihub.copernicus.eu/) - Sentinel Scientific Data Hub</a>;
* [TerraSAR-X](https://sso.eoc.dlr.de/eoc/auth/login?service=https://download.geoservice.dlr.de/supersites/files/) - TerraSAR-X Geohazard Supersites EO Data Gateway</a>;
* [TerraSAR-X](https://sso.eoc.dlr.de/eoc/auth/login?service=https://download.geoservice.dlr.de/supersites/files/) - Geohazard Supersites and Natural Laboratories Virtual Archive</a>;
* [WinSAR](https://sso.eoc.dlr.de/eoc/auth/login?service=https://download.geoservice.dlr.de/supersites/files/) - WInSAR consortium and GeoEarthScope Data</a>;
* [ARIA](http://aria-products.jpl.nasa.gov/) - Standard products of the Advanced Rapid Imaging and Analysis (ARIA) Project for Natural Hazards</a>;

# Websites
## Forums
* [Sentinel-1 material](https://custom-scripts.sentinel-hub.com/custom-scripts/sentinel/sentinel-1/) - Copernicus Sentinel data processing and use cases</a>;

## Training
* [ASF traning](https://asf.alaska.edu/training-resources/) - Alaska Satellite Facility training resources</a>;

# Basics of pre-processing of microwave imagery

Very useful free online material
[SAR Handbook](https://servirglobal.net/resources/sar-handbook) - The SAR Handbook: Comprehensive Methodologies for Forest Monitoring and Biomass Estimation</a>;

# Pre-processing of Sentinel-1 imagery:

Basic SAR data pre-processing steps consist of:
* Apply orbit files
   * Defines the relationship between ground and image coordinates,
improves accuracy of later orbit-based calibration steps.
* Radiometric corrections
   * Converts the image pixel values from digital number (DN) to a
standard geophysical measurement unit of radar backscatter.
* De-bursting
   * SAR scenes can be made up of multiple swaths or sections.
   * Instead you can do TOPS deburst
This step combines all swaths into a single image.
* Multilooking
   * Uses spatial averaging to reduce image speckle noise and converts to ground range,
producing an image with a standard pixel size. Reduces image resolution (optional).
* Speckle filtering
   * Removes noise, or speckle, in an image. Many types of speckle filters can be applied, and different applications
have specific filters that may work best. Unlike multilooking, this step does not reduce spatial resolution (optional).
* Terrain corrections: Radiometric Terrain Flattening (RTF) and geocoding
   * RTF: Uses a DEM to remove geometry-dependent radiometric distortions; normalizes measured backscatter with respect to terrain slope. Geocoding: Uses a DEM to remove geometric distortions such as foreshortening, layover, and shadow; connects the image to a geographic coordinate system.
* Convert to dB (optional)
   * Linearly-scaled data is converted into decibels (dB) (optional).

SLC images
- coregistration - top SAR splir and apply orbut files
- deburst
- mulitlookung
- terrain cor
- speckle filter
- terrain flattening
- subset need to be at the end

In SNAP:

1) open Sentinel-1 product in SNAP
2) raster -> subset to create clip of raster
3) radar -> radiometric -> calibrate (select polarisation and output band based on specific application) to make radiometric correction
4) radar -> radiometric -> radiometric terrain flatteing to radiometric terrain flatteing
5) radar -> radiometric -> S-1 Thermal Noise Removal to remove noise from image
6) geometric -> terrain correction -> Range-doppler terrain correction (vyberu SRTM 1sec) to make geometric corrections on the image

It is possible to do all of these steps at once using SNAP Graph builder

# Task: create a model of flood zones of the city Alessandria during flood event in November 2019
* Input data: Pair of Sentinel 1 Images captured 25.11.2019 (during the flood event) and 8.3.2021 (normal situation)


```
This is how to make block for codes or text to copy 
```
