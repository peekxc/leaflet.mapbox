
### What?

Add-on package for the Leaflet package to provide [Mapbox.js](https://www.mapbox.com/mapbox.js/api/v2.4.0/) v2.4.0 bindings.

### Why?

Mapbox.js provides several mapbox specific extensions which should be natively available in R, hence the package.

### How?

``` r
# For now you will need to build leaflet using a branch of mine
devtools::install_github('rstudio/leaflet')

devtools::install_github('bhaskarvk/leaflet.mapbox')

library(leaflet.mapbox)

leafletMapbox(access_token=<YOUR ACCESS TOKEN>) %>%
  addMapboxTileLayer(mapbox.classicStyleIds$dark)
```

### Progress

-   `leafletMapbox()` as an alternative to `leaflet::leaflet()` to initialize Mapbox specific [Map](https://www.mapbox.com/mapbox.js/api/v2.4.0/l-mapbox-map/).
-   `addMapboxTileLayer()` function to add [Mapbox TileLayer](https://www.mapbox.com/mapbox.js/api/v2.4.0/l-mapbox-tilelayer/).
-   `mapbox.classicStyleIds` list for a convenient list of mapbox classic style ids.
