# cabin-tileset

### Install gdal

https://gdal.org/download.html

### Install gdal2tiles

https://gdal.org/programs/gdal2tiles.html

### Convert png to tif

```sh
gdal_translate -of GTiff -gcp 4461.4 1584.9 -75.8 45.45 -gcp 1415.4 1218.3 -75.95 45.52 -gcp 2279.6 353.9 -75.88 45.53 -gcp 3755.7 104.89 -75.80 45.52 cabin.png cabin.tif
```

### Generate tiles

```sh
gdal2tiles.py -p raster --processes 12 --tilesize 128 -z 1-7 cabin.tif output/
```
