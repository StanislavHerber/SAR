In SNAP:

1) open Sentinel-1 product in SNAP
2) raster -> subset to create clip of raster
3) radar -> radiometric -> calibrate (select polarisation and output band based on specific application) to make radiometric correction
4) radar -> radiometric -> radiometric terrain flatteing to radiometric terrain flatteing
5) radar -> radiometric -> S-1 Thermal Noise Removal to remove noise from image
6) geometric -> terrain correction -> Range-doppler terrain correction (vyberu SRTM 1sec) to make geometric corrections on the image

It is possible to do all of these steps at once using SNAP Graph builder
