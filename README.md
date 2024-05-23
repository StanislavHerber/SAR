![image](https://github.com/StanislavHerber/SAR/assets/134272440/db81e86d-30d4-4224-abe2-c2d75b8bbf5c)

# Introduction
This repository focuses on processing of Radar remote sensing data via SNAP or Google Earth Engine platform.

# Data archives

1. <a href="https://asf.alaska.edu/">Alaska Satellite Facility</a>
2. [Alaska](https://asf.alaska.edu/) - Alaska Satellite Facility</a>

3. <a href="https://scihub.copernicus.eu/">Sentinel Scientific Data Hub</a>
4. <a href="https://sso.eoc.dlr.de/eoc/auth/login?service=https://download.geoservice.dlr.de/supersites/files/">TerraSAR-X Geohazard Supersites EO Data Gateway</a>
5. <a href="https://sso.eoc.dlr.de/eoc/auth/login?service=https://download.geoservice.dlr.de/supersites/files/">Geohazard Supersites and Natural Laboratories Virtual Archive</a>
6. <a href="http://www.unavco.org/data/imaging/sar">WInSAR consortium and GeoEarthScope Data</a>
7. <a href="http://aria-products.jpl.nasa.gov/">Standard products of the Advanced Rapid Imaging and Analysis (ARIA) Project for Natural Hazards</a>



# Pre-processing of Sentinel-1 imagery:

In SNAP:

1) open Sentinel-1 product in SNAP
2) raster -> subset to create clip of raster
3) radar -> radiometric -> calibrate (select polarisation and output band based on specific application) to make radiometric correction
4) radar -> radiometric -> radiometric terrain flatteing to radiometric terrain flatteing
5) radar -> radiometric -> S-1 Thermal Noise Removal to remove noise from image
6) geometric -> terrain correction -> Range-doppler terrain correction (vyberu SRTM 1sec) to make geometric corrections on the image

It is possible to do all of these steps at once using SNAP Graph builder

```
This is how to make block for codes or text to copy 
```
