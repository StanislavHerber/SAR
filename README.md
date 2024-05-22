![image](https://github.com/StanislavHerber/SAR/assets/134272440/401e4413-11e2-4da9-80f3-ffd9cc8f0828)

Introduction

Pre-processing of Sentinel-1 imagery:

In SNAP:

1) open Sentinel-1 product in SNAP
2) raster -> subset to create clip of raster
3) radar -> radiometric -> calibrate (select polarisation and output band based on specific application) to make radiometric correction
4) radar -> radiometric -> radiometric terrain flatteing to radiometric terrain flatteing
5) radar -> radiometric -> S-1 Thermal Noise Removal to remove noise from image
6) geometric -> terrain correction -> Range-doppler terrain correction (vyberu SRTM 1sec) to make geometric corrections on the image

It is possible to do all of these steps at once using SNAP Graph builder
