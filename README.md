# Map of Garibaldi Provincial Park Hike

The goal is to combine the hike route that was recorded using [mapmyride](http://www.mapmyride.com/my_home/#user_dashboard) and photos that were taken throughout the hike and display it onto an [Esri Leaflet](https://github.com/Esri/esri-leaflet) map.

Photos taken with an iPhone record latitude, longitude, and altitude (among other data points) that can be viewed through their EXIF data.


1. Export GPS points from mapmyride.
2. Convert to GPX.
3. Export latitude and longitude points from photos.
4. Join lat/long to photo JPEG.
5. Use [leaflet-omnivore](https://github.com/mapbox/leaflet-omnivore) to convert GPX to GeoJSON and add to [Esri Leaflet](https://github.com/Esri/esri-leaflet).
6. Add photos to exact point where they were taken on the hike.
7. View as pins and open pop-up with photo once clicked.

# Tools

### Route

1. [MapMyRide Route](http://www.mapmyride.com/workout/515362285): MapMyRide app was used to track GPS coordinates on the hike.
2. [MapMyRide GPX Converter](http://www.mikepalumbo.com/MMRConverter/index.php) - MapMyRide does not allow you to export the trail data so someone built a tool that allows you to grab the hike ID and download the info as a GPX file.
3. [Esri Leaflet](https://github.com/Esri/esri-leaflet) - Leaflet plugin for ArcGIS services that will render the map. Leaflet support the GeoJSON format, so the GPX data will need to be reformatted.
4. [leaflet-omnivore](https://github.com/mapbox/leaflet-omnivore) - Omnivore formats different file types into GeoJSON whicn can then be added to Leaflet.

### 2. Photos

1. [ExifTool](http://www.sno.phy.queensu.ca/~phil/exiftool/) - Powerful tool to extract EXIF data from photo files. This was used to extract Latitude and Longitude info.
