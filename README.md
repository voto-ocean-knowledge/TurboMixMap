# SkaMixMap

This repo hosts code for near real time visualisation of diverse surface and subsurface platform locations, as well as earth observation data, for field co-ordination during the SkaMix project.

Check out the [startup TODO list](https://github.com/voto-ocean-knowledge/SkaMixMap/issues/1) for action items


### Envisaged dataflow

1. nrt locations from drifters, autonomous platforms and vessels are emailed to votodatain@gmail.com in a variety of formats
2. Every hour, a python script running as a cronjob checks the inbox for new emails
3. The python script reads the email and converts the locations to geojson
4. geojson locations and tracks are displayed on a leaflet map
5. The leaflet map uses wmts web tiles to display multiple layers: bathy, SST, SSH etc.
6. Additional static plots are made with more detailed and scaled SST raster data from satellite/reanalysis products
7. SST from platforms is overlain on these plots where available


