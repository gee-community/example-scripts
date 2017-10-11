# ee.Image.pixelLonLat
- Creates a new two-band image in which each pixel is set to the values of its longitude and latitude in degrees.

## Syntax

#### Javascript
```
newImage = ee.Image.pixelLonLat( )
```

- *newImage* is the new image.

## Example

#### Javascript
```javascript
var NewIMAGE = ee.Image.pixelLonLat( );
print( NewIMAGE.getInfo( ) );  
Map.addLayer( NewIMAGE, {bands:['longitude'],min:-180,max:180},'Longitude' );
Map.addLayer( NewIMAGE, {bands:['latitude'], min:- 60,max: 60},'Latitude'  );
Map.setCenter( 0, 0, 2 );
```
